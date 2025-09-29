
# Cyber Security Internship - Task 5

## Task: Capture and Analyze Network Traffic Using Wireshark

### Objective
The objective of this task was to capture live network packets using Wireshark, analyze them, and identify different network protocols.

### Tools Used
- Wireshark (Free and open-source packet analyzer)
- Active Internet Connection

### Procedure
1. Installed and opened Wireshark.
2. Selected the active network interface for packet capture.
3. Initiated browsing and ping requests to generate traffic.
4. Stopped the capture after ~1 minute.
5. Applied filters to analyze traffic by protocol (e.g., HTTP, DNS, TCP).
6. Identified at least 3 different protocols in the capture.
7. Exported the capture as a `.pcap` file.
8. Documented findings and packet details.

### Findings
The following protocols were observed during analysis:
- **DNS Packets:** Used for hostname resolution (queries & responses).
- **TCP Packets:** Reliable, connection-oriented packets showing the 3-way handshake.
- **HTTP Packets:** Representing web traffic with GET/POST requests and server responses.

### Screenshots
Screenshots included in this repository:
- DNS Packet Analysis
- TCP Packet Analysis
- HTTP Packet Analysis

### Outcome
- Successfully captured and analyzed live packets.
- Identified multiple protocols (DNS, TCP, HTTP).
- Gained hands-on experience in packet analysis and network troubleshooting.

### Key Concepts Learned
- Packet Capture
- Protocol Analysis
- TCP/IP Layers
- Filtering in Wireshark
- Network Troubleshooting

### Interview Questions & Answers
1. **What is Wireshark used for?**
   A packet analyzer for capturing and inspecting network traffic.

2. **What is a packet?**
   A small unit of data transmitted over a network.

3. **How to filter packets in Wireshark?**
   By using filters such as `tcp`, `http`, `dns`.

4. **Difference between TCP and UDP?**
   TCP is reliable and connection-oriented, UDP is faster but connectionless.

5. **What is a DNS query packet?**
   A request sent by a client to resolve a domain name to an IP address.

6. **How can packet capture help in troubleshooting?**
   By identifying issues such as dropped packets or misconfigurations.

7. **What is a protocol?**
   A set of rules governing communication between devices.

8. **Can Wireshark decrypt encrypted traffic?**
   Not directly, unless encryption keys are provided.

---

