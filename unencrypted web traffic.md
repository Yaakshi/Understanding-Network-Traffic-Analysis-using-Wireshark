## 2. Now you have found that some kind of file has been downloaded by insider in unencrypted web traffic. Your task is to:

## a. Find the name and type of file.

Data can be downloaded using HTTP from the web. Hence, use the display filter to filter based on http packets.
![image](https://github.com/user-attachments/assets/0ce01362-cfdd-44f1-89d0-f6e9e741ead2)

The first packet is a GET request.
The second packet is a HTTP response from the destination IP address.
![image](https://github.com/user-attachments/assets/73e50e67-f375-495e-ab18-fa925282f443)

We select the HTTP response packet. To identify what file has been downloaded, we go to:

File → Export object → HTTP

![image](https://github.com/user-attachments/assets/98b44d03-5e2f-444e-b5cd-3f24f1a6c174)

### ```Name of the file: 1.jpeg```
### ```Type of the file: image/jpeg```

## b. Export that file from that web traffic, then analyze the file for any secret information.

![image](https://github.com/user-attachments/assets/eb9f7f24-855c-417a-a290-00cb99498619)
This is the file downloaded by the insider.

If we zoom in the image, we can find the secret information.
![image](https://github.com/user-attachments/assets/5c25c0a1-7a38-4ed8-abe8-6d4c52b4ee0c)

### ```The secret information: anthem```

## c. Find the hostname in which the file is stored.

![image](https://github.com/user-attachments/assets/09f5a4d4-9089-47b3-8071-65d92e51d0fd)

### ```The host name on which the file is stored is: 192.168.31.67```

