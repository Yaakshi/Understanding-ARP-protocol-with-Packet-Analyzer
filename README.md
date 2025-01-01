Use the provided pcap file (Arp) to answer the following questions.

## 1. Answer the following questions based on the contents of the Ethernet frame containing the HTTP GET message.

### _a. What is the 48-bit Ethernet address of your computer?_

![image](https://github.com/user-attachments/assets/edc2a13a-f9ce-4b6e-9fd2-a1ab8aaa104d)
The 48-bit Ethernet address of my computer is 00:d0:59:3d:68

### _b. What is the 48-bit destination address in the Ethernet frame? Is this the Ethernet address of gaia.cs.umass.edu? What device has this as its Ethernet address?_

![image](https://github.com/user-attachments/assets/619ae36c-c67b-4e1d-b1ba-90ef69296256)
The 48-bit destination address in the Ethernet frame is 00:06:25:da:af:73

To verify the address with IP address, we use ARP protocol.
![image](https://github.com/user-attachments/assets/297a993e-1a11-4bab-96f0-a3c2e7e9f4ce)
The Ethernet address 00:06:25:da:af:73 is associated with the IP address 192.168.1.1 which is the IP address of my router (gateway to the Internet).

Hence, this address is not the Ethernet address of gaia.cs.umass.edu. The address is associated to my TP link router.

### _c. Give the hexadecimal value for the two-byte Frame type field. What upper layer protocol does this correspond to?_

![image](https://github.com/user-attachments/assets/b187ad6d-dd57-409e-b804-8fb3bf135b90)
The hexadecimal value for two-byte frame type field is 0x0800. It corresponds to IPv4.

## 2. Answer the following questions based on the contents of the Ethernet frame containing the first byte of the HTTP response message.

### _a. What is the value of the Ethernet source address?_

![image](https://github.com/user-attachments/assets/5b9e9b14-6483-4804-9f86-e893e11d86b0)
The Ethernet source address is 00:06:25:da:af:73

### _b. What is the destination address in the Ethernet frame? Is this the Ethernet address of your computer?_

![image](https://github.com/user-attachments/assets/4091fce5-17ab-4b41-9e09-c8e060f13219)
The Ethernet destination address is 00:d0:59:a9:3d:68 Yes, this is the Ethernet address of my computer.

### _c. Give the hexadecimal value for the two-byte Frame type field. What upper layer protocol does this correspond to?_

![image](https://github.com/user-attachments/assets/6e42d45a-c252-478e-8794-29d0adb2316a)
The hexadecimal value for the two-byte frame type field is 0x0800. It corresponds to IPv4.

## 3. Answer the following questions based on the contents of the ARP Request packets.

### _a. What are the hexadecimal values for the source and destination addresses in the Ethernet frame containing the ARP request message?_

![image](https://github.com/user-attachments/assets/0a6612e3-c395-4071-b197-202f9118756c)
The hexadecimal value of source Ethernet address is 00d059a93d68. The hexadecimal value of destination Ethernet address is ffffffffffff.

### _b. Give the hexadecimal value for the two-byte Ethernet Frame type field._

![image](https://github.com/user-attachments/assets/89fb3481-b3fe-45dd-8c2c-349af8359bc5)
The hexadecimal value for the two-byte Ethernet frame type field is 0x0806.

### _c. How many bytes from the very beginning of the Ethernet frame does the ARP opcode field begin?_

![image](https://github.com/user-attachments/assets/07863f8d-d2e6-4547-8eb1-f25842eaea74)
The ARP opcode field begins after 20 bytes from the beginning of the Ethernet frame.

### _d. What is the value of the opcode field within the ARP-payload part of the Ethernet frame in which an ARP request is made?_

![image](https://github.com/user-attachments/assets/5fe808b2-9fa9-494d-9e40-9127d963e4ad)
The value of ARP opcode is request (1).

### _e. Does the ARP message contain the IP address of the sender?_

![image](https://github.com/user-attachments/assets/5bc3e51d-8ce5-4086-bfa8-77b7560f0b7e)
The ARP message contains the IP address of the sender 192.168.1.105

### _f. Where in the ARP request does the “question” appear – the Ethernet address of the machine whose corresponding IP address is being queried?_

![image](https://github.com/user-attachments/assets/eca752c4-078f-4d1c-928f-31ebe7ef8ba6)
The Target MAC address field questions the Ethernet address of the machine whose corresponding IP address is queried.

## 4. Answer the following questions based on the contents of the ARP Reply packets.

### _a. How many bytes from the very beginning of the Ethernet frame does the ARP opcode field begin?_

![image](https://github.com/user-attachments/assets/403a0b25-85f7-44b9-a527-deb18b246257)
The ARP opcode field begins after 20 bytes from the beginning of the Ethernet frame.

### _b. What is the value of the opcode field within the ARP-payload part of the Ethernet frame in which an ARP response is made?_

![image](https://github.com/user-attachments/assets/eda961e6-be05-43af-bc00-9d1f174c2a09)
The value of ARP opcode is reply (2).

### _c. Where in the ARP message does the “answer” to the earlier ARP request appear – the IP address of the machine having the Ethernet address whose corresponding IP address is being queried?_

![image](https://github.com/user-attachments/assets/747bed75-4777-44f0-afd0-85614075fbf3)
The Target MAC address field now contains the Ethernet address 00:d0:59:a9:af:73 for corresponding IP address 192.168.1.105 (my computer).

### _d. What are the hexadecimal values for the source and destination addresses in the Ethernet frame containing the ARP reply message?_

![image](https://github.com/user-attachments/assets/c20a7ae1-6f96-4fd6-a299-e00f26747e51)
The hexadecimal value of source Ethernet address is 000625daaf73. The hexadecimal value of destination Ethernet address is 00d059a93d68.

### _e. There is yet another computer on this network, as indicated by packet 6 – another ARP request. Why is there no ARP reply (sent in response to the ARP request in packet 6) in the packet trace?_

![image](https://github.com/user-attachments/assets/fbde2b0c-9476-40ca-a3c5-ffb49a96b22d)
The Target IP address is 192.168.1.117. It must be 192.168.1.1 which is the IP address of my router (gateway to the Internet). Since the target IP address is incorrect, the request does not reach the destination.













