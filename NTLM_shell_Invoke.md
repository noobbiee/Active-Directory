# In this attack we are going to use the nishang script
i have taken the script form '
```
https://github.com/samratashok/nishang/blob/master/Shells/Invoke-PowerShellTcp.ps1
```

i am going execute this script in the windows from my attacking machine to get a powershell

# Invoke-PowerShellTcp.ps1
![Screenshot from 2025-05-05 18-32-03](https://github.com/user-attachments/assets/6ed40443-3471-4a92-b0d6-b8c8620cdadf)

This will give us reverse shell access into the windows machine

# Netcat
Since the script is going to connect to us in port 4646
i will use netcat to bind the port 4646 so we can connect to the windows
![Screenshot from 2025-05-05 18-36-44](https://github.com/user-attachments/assets/578f0f29-c106-45ea-b535-0333782874f3)


# Python-server
lets setup a python-server through which we will inject the script into our victim machine
![Screenshot from 2025-05-05 18-36-05](https://github.com/user-attachments/assets/76e1ab59-d32e-40a6-aed6-25ef7c4d25a4)


# responder
![Screenshot from 2025-05-05 18-30-19](https://github.com/user-attachments/assets/81beba38-3fc0-4359-a1ca-441e84037090)

# Impacket-ntlmrelayx

![Screenshot from 2025-05-05 18-37-26](https://github.com/user-attachments/assets/61b59a32-4bac-4440-8d73-016230401a75)

![Screenshot from 2025-05-05 18-37-36](https://github.com/user-attachments/assets/00ea98da-46db-47cf-a2ec-be335d57e8bc)

# Reverse powershell

![Screenshot from 2025-05-05 18-38-44](https://github.com/user-attachments/assets/528560bd-b407-405f-ba38-e03a759efd4d)

As you can see i have reverse-powershell 

#Local-users 

![Screenshot from 2025-05-05 18-39-12](https://github.com/user-attachments/assets/6a77025d-d318-4b9a-96af-6aadeff4fea2)

We can see all the local user in the machine

# Services 

![Screenshot from 2025-05-05 18-39-23](https://github.com/user-attachments/assets/8b7c3cdc-8b0b-4c87-b516-4272878c43e4)

We can see all the services in windows machine which are running and stopped

# smb-shares

![Screenshot from 2025-05-05 18-39-42](https://github.com/user-attachments/assets/3e85f82e-5d75-4f70-90a1-877a08334e57)

We can see the smb-shares

# View the logs

![Screenshot from 2025-05-05 18-39-53](https://github.com/user-attachments/assets/10861aac-6260-415f-b139-d716d167c0fd)

We can view the logs

# hot-fixes

![Screenshot from 2025-05-05 18-40-11](https://github.com/user-attachments/assets/19c6b037-4f7f-4f80-8d66-5f80860f1014)

See the hotfixes and plan our further attacks






