# LLMNR Poisioning attack

Local-link Multi-cast Name Resolution
LLMNR is used to recognize host incase DNS fails to do, used in legacy systems
For this attack to work user who tries to access the resources that they donot have permission. then dns will fail to recognize the user and llmnr comes to play. 

# crackmapexec
Lets use crackmapexec to map the smb

![Screenshot from 2025-05-05 11-42-31](https://github.com/user-attachments/assets/b2c32bc3-c70d-4894-8130-0dccdfbadfb4)

For poisioning the traffice we will be using the responder
open the responder and make some changes if required


![Screenshot from 2025-05-05 11-43-46](https://github.com/user-attachments/assets/af49d857-0d4d-4fd0-8be9-6d3b3bcd5470)

lets start the responder 

![Screenshot from 2025-05-05 11-53-25](https://github.com/user-attachments/assets/7d8d141d-197c-4169-813b-07fc2e3f15e3)


![Screenshot from 2025-05-05 11-53-38](https://github.com/user-attachments/assets/250e6828-45cf-4954-8482-fdb1cd262ce0)

We got the hashes from user1.
