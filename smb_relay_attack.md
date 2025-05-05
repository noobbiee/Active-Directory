# SMB Relay Attack

In this attack we will capture the hashes and try to relay it to the smb server and get the credentials.
For this attack to work we need to have local administrator priviliges which we already enabled during our setup.

# responder

 lets make some changes in our responder conf files

turn off the smb and http 

![Screenshot from 2025-05-05 13-49-20](https://github.com/user-attachments/assets/3975e0fe-a730-46b0-a801-0969f8b02f76)

lets start the responder and poision the traffic

![Screenshot from 2025-05-05 13-49-41](https://github.com/user-attachments/assets/25b60821-766f-4e94-a020-64d525861c1e)

![Screenshot from 2025-05-05 13-49-50](https://github.com/user-attachments/assets/d49476f6-b612-480b-ad1d-ea0ca5db5fa5)

# lets get the hashes
# impacket-relayx

Lets create a file where we have the ip of our targets and we will feed it to impacket

![Screenshot from 2025-05-05 13-53-48](https://github.com/user-attachments/assets/348595c6-3870-4c63-a241-52d7f83af276)

![Screenshot from 2025-05-05 13-50-00](https://github.com/user-attachments/assets/bff943de-c32b-450a-ba01-d8f3d62431d4)

![Screenshot from 2025-05-05 13-50-10](https://github.com/user-attachments/assets/23424c66-b20b-4467-9496-d05d926ee677)

We got our hashes. Save the hashes in the file.


