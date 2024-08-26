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

## **Task 3 Module - TCP Flags**

![TCPFlags_Nmap_Task3](https://github.com/user-attachments/assets/70447113-a800-433b-bc23-761917795d20)
