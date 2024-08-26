# 👁️ NMap-Basic-Port-Scans

In this project, I am exploring the fundamentals of port scanning using Nmap, focusing on identifying which ports are open, listening, or closed on a target system. This is a crucial step in network reconnaissance and penetration testing. Through the TryHackMe **Nmap Basic Port Scans** module, I will be learning and applying different types of port scans such as TCP Connect, TCP SYN, and UDP port scans. These scans allow us to gather important information about the services running on a system and help identify potential vulnerabilities. My documentation will cover the usage of these scans, analysis of results, and insights into the effectiveness of each method.

## **Task 2 Module - TCP & UDP Ports**

A TCP or UDP port identifies a specific network service running on host, similar to how an IP address identifies the host itself. Common services bind to sepcific ports, for example, HTTP on TCP port 80, HTTPS on TCP port 443. Only one service can listen on a particular port at any time for a given IP address.

Ports can be in one of two basic states:
-**Open**: A service is actively listening on the port.
**Closed**: No service listening, port is accessible.

Nmap, however, may detect six possible port states:
-**Open**
**Closed**
**Filtered**: Nmap can not determine the port's status due to firewall interference.
**Unfiltered**: The port is accessible, but it's status (open or closed) is unclear.
**Open|Filtered**: Nmap can not distinguish between open and filtered.
**Closed|Filtered**: Nmap can not determine if the port is closed or filtered.

## **Task 3 Module - TCP Flags** 🏁

![TCPFlags_Nmap_Task3](https://github.com/user-attachments/assets/70447113-a800-433b-bc23-761917795d20)

The TCP header is 24 bytes long, consisting of six rows of data. Key fields within include source and destination port numbers (16 bits each) and sequence and acknowledgement numbers (32 bits each).

Nmap can manipulate the TCP flags in the header, which are important for scanning. Flags area:

- **URG (Urgent)**: Marks urgent data that needs immediate processing.
- **ACK (Acknowledgement)**: Acknowledges the receipt of a TCP segment.
- **PSH (Push)**: Requests that TCP deliver the data to the application immediately.
- **RST (Reset)**: Resets a connections, often sent by firewalls or when no service responds on the target.
- **SYN (Synchronize)**: Initiates a TCP connection with a 3-way handshake.
- **FIN (Finish)**: Indicated the sender has finished sending data.

## **Task 4 Module - TCP Connect Scan**

![TCPConnectScanTask4](https://github.com/user-attachments/assets/ebfa472c-4519-4831-b58a-e6143be5e17f)

- In this example, we use **-sT** (TCP connect scan) to obtain a detailed list of open ports.
- Note, we can use **-F** to enable fast mode and decrease the number of scanned ports from 1000 to 100 most common ports.

## **Task 6 Module - UDP Scan**

UDP is a connectionless protcol, meaning it doesn't require a handshake to establish a connection. Because of this, a service listening on a UDP port may not respond to sent packets. However, if a UDP packet is sent to a closed port, an ICMP port unreachable error will be returned. Nmap can perform a UDP scan using the **-sU** option, and this can be combined with a TCP scan. When sending a UDP packet to an open port, you might not receive any response, making it difficult to determine the port's status nased on the lack of replies.


![UDP Scan](https://github.com/user-attachments/assets/affa2c84-b42b-4a7f-91ea-fd008d60a0cc)

- Ran the command: **nmap -sU -F -v 10.10.127.44** to answer the below questions:

![Task6Q A](https://github.com/user-attachments/assets/627dbff5-a2fc-4484-9311-2bc931b5ae00)
