# For the user we will be using windows 10 enterprise and connect it to our domain
# Start the virtual box and install the iso image
During the installation and configuring process assign more ram to the machine for easier process, which 
can be toned down after completion.

![Screenshot from 2025-05-03 18-34-42](https://github.com/user-attachments/assets/8d5654e7-a023-48a9-b81b-58430b4b6ef4)

![Screenshot from 2025-05-03 18-35-33](https://github.com/user-attachments/assets/e6babdf2-cf31-44a5-acc8-8e2c4cbdf2cb)

![Screenshot from 2025-05-03 18-35-47](https://github.com/user-attachments/assets/0fd87584-205d-4ced-a7b0-826ff0f1756f)

![Screenshot from 2025-05-03 18-35-55](https://github.com/user-attachments/assets/5b36a297-0319-40c7-949c-577970c9a1ec)

# Rename the PC
![Screenshot from 2025-05-03 18-48-46](https://github.com/user-attachments/assets/72b7bdb3-eb5f-407d-8603-a0d932ddbbd4)

# Join the Domain
First of all we need to connect to set up the ip for the dns server and set up dns suffix for the domain we are going to be part of 
go to your network settings; adapter; properties and select ip4; properties

![Screenshot from 2025-05-05 08-13-47](https://github.com/user-attachments/assets/39f98de8-51b2-4404-9959-fd516e195804)

![Screenshot from 2025-05-05 08-15-19](https://github.com/user-attachments/assets/4c9e6753-40b2-49f4-9aa5-a62220110367)

![Screenshot from 2025-05-05 08-16-24](https://github.com/user-attachments/assets/4c4f03d4-539a-42d9-a149-6ab15234e49e)

Now go to settings; system; about; advanced settings 

![Screenshot from 2025-05-05 08-32-12](https://github.com/user-attachments/assets/27e68274-1e1d-4acf-839e-420a48c08ab3)

![Screenshot from 2025-05-05 08-32-53](https://github.com/user-attachments/assets/48822133-1747-4c2c-99d8-940599e1758d)

![Screenshot from 2025-05-05 08-33-01](https://github.com/user-attachments/assets/4a338c75-528f-4e79-b83c-591a41be65fe)

# Confirm that you joined the domain

![Screenshot from 2025-05-05 08-36-13](https://github.com/user-attachments/assets/41c66160-c18b-40cd-a31c-4f884c108e47)

Check users in the server

![Screenshot from 2025-05-05 08-38-12](https://github.com/user-attachments/assets/b612af0c-5d7a-4d76-881d-ea58e0e420a8)

go to user1
![Screenshot from 2025-05-05 08-39-47](https://github.com/user-attachments/assets/04d64a0d-90ce-4bf6-85d1-53336fe0d249)

You can see the user is user1.NOOB which confirms connecting to domain and we ping the both domain controller and dns to see 
we have connections and they can communicate

# Log in using admin account

![Screenshot from 2025-05-05 09-02-38](https://github.com/user-attachments/assets/aacff812-0b0f-4159-9037-5e28a958cecc)

enable local administrator account

![Screenshot from 2025-05-05 09-08-06](https://github.com/user-attachments/assets/45f3bc89-4fbc-430c-8464-58fef4f07059)

![Screenshot from 2025-05-05 09-39-45](https://github.com/user-attachments/assets/7480bbb0-e929-435f-a408-c53bd7fb5019)

![Screenshot from 2025-05-05 09-40-38](https://github.com/user-attachments/assets/662103c2-51bd-4c9b-ba90-2a1b06efde2b)

![Screenshot from 2025-05-05 09-40-56](https://github.com/user-attachments/assets/82fee53c-d2ce-44e1-9bf7-5a3015b53c01)

![Screenshot from 2025-05-05 09-41-13](https://github.com/user-attachments/assets/3970387b-db75-439b-85b6-baeca6e562d5)

![Screenshot from 2025-05-05 09-47-15](https://github.com/user-attachments/assets/b246062e-1dea-408b-b9f8-e883cf8c6535)

![Screenshot from 2025-05-05 09-47-32](https://github.com/user-attachments/assets/3ad5f7ce-c726-402a-8ffb-063ab8cfc602)

![Screenshot from 2025-05-05 09-47-56](https://github.com/user-attachments/assets/c2e009c9-d0f1-4d97-9ab2-31d4437898e2)

# sign in locally and map network drives

![Screenshot from 2025-05-05 09-51-08](https://github.com/user-attachments/assets/efd92ecc-7d85-490c-8330-55c66f32d171)

Go to network discovery and turn it on

![Screenshot from 2025-05-05 09-52-07](https://github.com/user-attachments/assets/57b3a496-23f3-48af-b7bb-6917b72f4364)

![Screenshot from 2025-05-05 09-52-17](https://github.com/user-attachments/assets/ddbedfe5-0c68-4321-b6e5-28c45f6d4705)

![Screenshot from 2025-05-05 09-52-38](https://github.com/user-attachments/assets/d370918e-c054-4e31-aaa5-e86a4e95bd60)

![Screenshot from 2025-05-05 09-52-57](https://github.com/user-attachments/assets/c173ede1-e172-470e-90ce-6dfaa5f518c3)

![Screenshot from 2025-05-05 09-53-49](https://github.com/user-attachments/assets/36e12419-312d-48ed-965d-dbe9582f8636)

We have successfully set up our user, we will add another user and set it up replicate the entire procedure.




