# In this attack we will try to get a shell in our target and perform some data exfiltration

# Create a file in the user2
![Screenshot from 2025-05-05 14-48-32](https://github.com/user-attachments/assets/eeb3798a-1ccf-47dd-b696-cea92819ab72)


# we will fire the responder

![Screenshot from 2025-05-05 14-53-22](https://github.com/user-attachments/assets/29db717e-5e8b-4978-9b2d-23043861a726)

![Screenshot from 2025-05-05 14-53-31](https://github.com/user-attachments/assets/157a9ea9-1e6f-43fd-8475-52268d61df69)

Once the responder starts poisioning the network we can start our impacket

# impacket-ntlmrelayx

![Screenshot from 2025-05-05 14-53-42](https://github.com/user-attachments/assets/877a0033-02ef-48a3-9ee1-9c405746a162)

![Screenshot from 2025-05-05 14-53-53](https://github.com/user-attachments/assets/cd34fe4e-8cbf-4cd9-a36c-82bda22697dc)

You can see a  interactive shell has started you can use netcat to connect to it and we get access into our
target.

# netcat

![Screenshot from 2025-05-05 14-54-14](https://github.com/user-attachments/assets/856e7c23-0c06-4235-a032-321fdbdee076)

![Screenshot from 2025-05-05 14-54-23](https://github.com/user-attachments/assets/8119b3d3-5067-4567-99dd-979e5ed3c751)

![Screenshot from 2025-05-05 14-54-32](https://github.com/user-attachments/assets/f191b237-af8c-4df4-b81a-89bdd63c5ab9)

![Screenshot from 2025-05-05 14-54-37](https://github.com/user-attachments/assets/8bc080ec-fa3a-4e83-be29-1d11e52e6392)

