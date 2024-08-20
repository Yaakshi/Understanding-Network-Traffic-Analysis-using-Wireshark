## 3. Based upon their activities, auditing team has started investigation against them and found that the insider passed some sensitive information via call to someone. The traffic has been captured.

Calls via the Internet uses RTP and SIP protocol.

RTP stands for real-time transport protocol. It is used to deliver audio and video streams over the Internet enabling the VoIP – Voice over internet protocol.

## a. Analyze the traffic and find those conversations and extract the sensitive information in it.

![image](https://github.com/user-attachments/assets/a15c952a-96a9-45b1-89ee-8d6470df7b69)

First, we filter the packets based on the rtp protocol. To find the conversations, we do:

Telephony → RTP → RTP Streams

![image](https://github.com/user-attachments/assets/d4e01653-b245-43dc-bc86-3d381a1a5344)

We can identify two conversations.

![image](https://github.com/user-attachments/assets/9982bd32-7f93-465f-a7f6-4f853bc1cf72)

Listening to the conversation, we can listen to the password that was shared.

### ```The sensitive information: limbo```

## b. Find the call-ID when the status of the call is ringing.

SIP stands for Session Initiation Protocol. It is a signalling protocol. This is used to set up the connection across the network.

To identify the ringing call, we use SIP protocol as the display filter.

![image](https://github.com/user-attachments/assets/ca10aac1-f508-4e06-b3f5-135ef81d88aa)

![image](https://github.com/user-attachments/assets/5074e989-5430-41f6-a7e6-6dea041286b5)

Under the SIP header, we can find the call ID.

### ```Call-ID: 01caab9b53b12efe00d3493a67ff695d@192.168.31.8:5060```

