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
| Responder | LLMNR/NBT-NS poisioning, credential capture |
| Ipmacket-ntlmrelayx | SMB relay attacks |

