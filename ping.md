## **1. You, as a SOC analyst noted that someone tried to send information (PING) to unknown IP address, and you are suspecting some malicious information might transferred in it. Analyze the traffic file.**


## **a. Find the data transferred.**

To find the data transferred, we enter icmp in the display filter field because ping uses ICMP packets.
![image](https://github.com/user-attachments/assets/6e65c901-0d5e-41de-9084-c76b9e71e972)
We can identify two ICMP packets – request and reply.

![image](https://github.com/user-attachments/assets/4a5d7108-bdc5-4e1d-8632-2a030562aa3a)
Analysing the layers of the request packet, we can identify the data that has been sent.

### ``` Data: 7061737321402324```

## **b. Find the source and destination IP of that log.**

From the columns of the request packet, we can identify the source and destination IP
addresses.
![image](https://github.com/user-attachments/assets/ae181d9f-b981-4215-b43d-bf399fe85bed)

### ```Source IP address: 192.168.31.89```
### ```Destination IP address: 192.168.31.16```

## **c. Find the Data length (Bytes) and verify the checksum status on destination.**

![image](https://github.com/user-attachments/assets/5655055f-0899-42cb-ad67-1eb5142ec8eb)

### ```Length of the data = 8 bytes```

Request packet:
![image](https://github.com/user-attachments/assets/11676423-63a9-44b1-9395-9e422c7f02cb)

Response packet:
![image](https://github.com/user-attachments/assets/18a1c887-dd62-4b3e-9344-cf150dd26ce0)

### ```The checksum of request packet = 0xcfc6```
### ```The checksum of reply packet = 0xd7c6```

XOR operation of 0xcfc6 and 0xd7c6 gives 0x1800. For the checksum to be valid, the XOR operation must return 0.

We can see that both the checksums differ. Hence there has been some transmission error or the data has been tampered.


