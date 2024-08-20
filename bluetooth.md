## 4. On further investigation, you have a suspect on some wireless device communications. List out the Bluetooth devices communications from this traffic and find the details about native Bluetooth adapter.

We type ‘bluetooth’ in display filter.
![image](https://github.com/user-attachments/assets/ae52b133-947c-435a-8585-e424777f6c8d)

![image](https://github.com/user-attachments/assets/fee66335-28c1-4f32-996b-ea67c472863f)

To identify all the Bluetooth devices, we go to:

Wireless → Bluetooth devices

It also details the local Bluetooth adapter.

![image](https://github.com/user-attachments/assets/94be468f-3167-4656-af8f-e77d54df7ffd)

### ```ChiconyElect is the native virtual bluetooth adapter```
### ```MAC address of the adapter: 4c:bb:58:43:35:be```

## a. Analyze the captured WPA handshake from this traffic and report in detail about it to your administrator.

WPA handshake uses keys derived from the EAPOL handshake.

EAPoL stands for Extensible Authentication Protocol over LAN. It is an authentication protocol to access resources on a network.

![image](https://github.com/user-attachments/assets/af8c01f3-0f93-4186-bc65-52d11379ac62)

![image](https://github.com/user-attachments/assets/b5f6f417-463b-496e-8bb6-d1b8b2be240e)

### ```WPA is a four-way handshake. But here, there are only three messages under the eapol protocol. The third message from the access point to the client is missing.```

## b. Geo locate all the endpoint of wireless devices.

First, we need to download the GeoIP databases from MaxMind.
![image](https://github.com/user-attachments/assets/48935914-24f8-4c4f-a972-756049fce061)

We will get three files in. mmdb extension.

Save them in a single folder and add the directory to Wireshark.
![image](https://github.com/user-attachments/assets/e81b45f4-4ea4-4216-836a-b299380f2879)

![image](https://github.com/user-attachments/assets/06885bb0-4a98-4e06-8ca4-b983ef3df88c)

To add the directory to wireshark, we go to:

Edit → Preferences

![image](https://github.com/user-attachments/assets/4e36dcbd-844c-4766-8a7d-a6155815478e)
Under ‘name resolution’ tab, enable the IP geolocation. Add the MaxMind database directory containing the .mmdb files.

![image](https://github.com/user-attachments/assets/de22484f-5356-48d1-b7bf-9199ba5795fa)

To view the map, go to:

Statistics → Endpoints

![image](https://github.com/user-attachments/assets/bee16fbe-57ea-4f69-9cac-bfd9de061620)

Under the IPv4 tab we can find the country, city, latitude and longitude columns denoting the geolocation of the all the devices on the network.

To view the geolocation on the world map, click on:

Map → Open in browser

![image](https://github.com/user-attachments/assets/9b08a127-85e8-4229-8b02-89276cdab9ed)

![image](https://github.com/user-attachments/assets/559e7f7e-1a9a-445e-a5d1-d866271c5fa4)

## c. Analyze the protocol level information transfer between wireless devices.

To analyse the packet transfers based on several protocols, we can use the following:

Statistics → Protocol hierarchy

![image](https://github.com/user-attachments/assets/8bacd4e3-18f2-47ca-a5c1-63042e971777)

![image](https://github.com/user-attachments/assets/2c0afe44-10ae-45e4-b4f9-b1bd9897e7d4)

This hierarchy gives details about number of packets, number of bytes transferred and their corresponding percentage with respect to all the packets in the capture file.

