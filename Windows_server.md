# For the server we are using windows server 2022

setup the virtual machine select the iso image, i am keeping the adpater in brideged
start the machine and press install

![Screenshot from 2025-05-02 11-06-25](https://github.com/user-attachments/assets/2dd01966-984e-4037-94d7-25a4e355e5f1)
choose the second one

# select password for administrator account

![Screenshot from 2025-05-02 11-11-56](https://github.com/user-attachments/assets/5dd0884c-10d9-4c92-9162-4980bfc8f66d)

# rename the Pc
it is going to be the name of our domain controller in my case i put noobbiee-DC
![Screenshot from 2025-05-03 14-56-40](https://github.com/user-attachments/assets/d6b55f8e-6e2d-4691-b078-779d33c57362)

# Promote the server to domain controller
go to server manager

![Screenshot from 2025-05-03 15-00-36](https://github.com/user-attachments/assets/89562964-82f4-40a1-be81-d45db5790f90)

Keep default settings until you get to the server roles and select Active Directory Domain services Services
and add features
![Screenshot from 2025-05-03 15-04-34](https://github.com/user-attachments/assets/3fb794b9-bc42-41ed-9b60-c738b377284d)

Then press next

![Screenshot from 2025-05-03 15-05-31](https://github.com/user-attachments/assets/b950ba50-25bc-4b8d-9d16-018b3cdf38d6)

![Screenshot from 2025-05-03 15-05-41](https://github.com/user-attachments/assets/096e1a85-b148-4230-b8d0-577046edac3d)

Select promtoe this server to a domain controller
select add new forest and give a domain name : NOOB.local

![Screenshot from 2025-05-03 15-07-53](https://github.com/user-attachments/assets/fc050831-a557-4530-a403-848e0b8380b1)

select the password and keep everything as default
![Screenshot from 2025-05-03 15-09-25](https://github.com/user-attachments/assets/cab0aabe-50a4-4dd3-95a3-e8f3611d92e0)

the domain name will appear here
leave everything as default and perform prerequisite test

![Screenshot from 2025-05-03 15-11-32](https://github.com/user-attachments/assets/66172314-9255-4024-b7a6-cce9eafa6b3f)

![Screenshot from 2025-05-03 15-11-43](https://github.com/user-attachments/assets/bfb71f8d-2215-43fe-8064-52402055e548)

once the installation is completed you will be signed out

# Active Directory Certificate services
go to manage, add roles and feauters and select default until server roles
select Active Directory Certififcate Service

![Screenshot from 2025-05-03 15-33-04](https://github.com/user-attachments/assets/3c530c7b-c1bc-4f03-b0c8-097ddbbcba38)

![Screenshot from 2025-05-03 15-33-28](https://github.com/user-attachments/assets/7812256d-b46c-402c-9e21-89560f0bf192)

press Configure Active Directory Certificate Services on the destination server

![Screenshot from 2025-05-03 15-35-51](https://github.com/user-attachments/assets/2a2a5257-6d2b-41db-a236-24fe45acadf6)

![Screenshot from 2025-05-03 15-36-02](https://github.com/user-attachments/assets/af383fb8-1bcc-4234-98e1-4b23453e9a87)

![Screenshot from 2025-05-03 15-36-22](https://github.com/user-attachments/assets/263aa43c-c60d-4b1b-8e58-db07adf7fac0)

![Screenshot from 2025-05-03 15-36-41](https://github.com/user-attachments/assets/7efb0860-7d13-408c-8c36-5338112380b7)

![Screenshot from 2025-05-03 15-36-48](https://github.com/user-attachments/assets/3e524a46-e2ee-4b22-94b0-154526d0b2e3)

Then restart the server

# Create new admin user
Go to server manager; active directory users and computers
go to NOOB.local and create a new organizational unit and move all the security group and users into that folder
except administrator and guest

![Screenshot from 2025-05-03 15-40-20](https://github.com/user-attachments/assets/087ebba7-1fd2-45fb-b91c-7ad494c7f4ee)

![Screenshot from 2025-05-03 15-44-23](https://github.com/user-attachments/assets/de5fdbd2-6aa0-43c4-8906-b4a65b453432)

![Screenshot from 2025-05-03 15-44-57](https://github.com/user-attachments/assets/9abee765-9f4b-49de-9caf-46d9aacb27e1)

for all account we create leave the password never expires

# Mariadb service
We will copy the adminstrator account and try to simulate the maria db services

![Screenshot from 2025-05-03 15-48-29](https://github.com/user-attachments/assets/88d59553-9725-488c-8b0c-630a85eb979c)

Go to cmd prompt

![Screenshot from 2025-05-03 16-00-07](https://github.com/user-attachments/assets/e3f3a43f-3a6e-4d5f-bfb1-4a54bd79ac96)

![Screenshot from 2025-05-03 16-00-20](https://github.com/user-attachments/assets/0614a53b-c272-44a4-8284-02b1de098a26)

# Create Users account

![Screenshot from 2025-05-03 15-50-45](https://github.com/user-attachments/assets/a183c339-7284-415e-b9e5-79ff81873865)

![Screenshot from 2025-05-03 15-51-12](https://github.com/user-attachments/assets/fbe04585-403c-409a-a405-c4c7727c5c7d)

# Create shared folders

Go to serrver manager; files and storage services

![Screenshot from 2025-05-03 16-03-25](https://github.com/user-attachments/assets/bb1e6cd2-4fa8-46c4-bfda-25db85751235)

![Screenshot from 2025-05-03 16-03-36](https://github.com/user-attachments/assets/1312e171-a18d-41cd-aded-927ed0133b31)

![Screenshot from 2025-05-03 16-03-53](https://github.com/user-attachments/assets/f24f121b-7400-4ae3-b21b-25965cc57fe2)

![Screenshot from 2025-05-03 16-04-09](https://github.com/user-attachments/assets/ba8aa89f-13b2-4b80-b0fa-9f308316d8d6)





