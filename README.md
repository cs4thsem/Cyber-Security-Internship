# Cyber Security Internship - Task 1

## Task: Scan Your Local Network for Open Ports

### Objective
The objective of this task is to perform network reconnaissance using **Nmap** to identify open ports on devices within the local network and understand potential security risks.

### Tools Used
- **Nmap** (Network Mapper)
- **Wireshark** (Optional, for packet analysis)

### Procedure
1. Installed Nmap from the official website.
2. Identified local IP range using `ipconfig` (Windows) or `ifconfig/ip a` (Linux).
3. Performed TCP SYN scan using:
   ```bash
   nmap -sS 192.168.1.0/24
   ```
4. Recorded results of detected devices and open ports.
5. Analyzed risks associated with these ports.
6. (Optional) Used Wireshark to analyze captured traffic.

### Sample Results
- **Nmap Scan Output:** Open ports detected on hosts (22 - SSH, 80 - HTTP, 443 - HTTPS, 3389 - RDP)
- **Wireshark Capture:** Displayed TCP SYN and ACK packets during scanning.

### Observations
- Multiple devices in the subnet were identified.
- Critical ports such as **22 (SSH), 80 (HTTP), 443 (HTTPS), 3389 (RDP)** were open.
- Open ports indicate potential entry points for attackers.

### Analysis
- Open ports expose services that may be vulnerable to exploitation.
- For example:
  - **SSH (22)** may face brute-force attacks.
  - **HTTP (80)** could expose web vulnerabilities.
  - **RDP (3389)** is often exploited for unauthorized remote access.
- Security measures include firewall rules, patching, and restricting access.

### Interview Questions & Answers
**Q1:** What is an open port?  
**A1:** A communication endpoint that accepts incoming connections.

**Q2:** How does Nmap perform a TCP SYN scan?  
**A2:** It sends SYN packets and listens for SYN-ACK responses to identify open ports.

**Q3:** What risks are associated with open ports?  
**A3:** They can allow unauthorized access or exploitation of vulnerable services.

**Q4:** Difference between TCP and UDP scanning?  
**A4:** TCP is connection-based; UDP is connectionless and harder to detect.

**Q5:** How can open ports be secured?  
**A5:** Close unnecessary ports, use firewalls, and apply strong authentication.

**Q6:** What is the firewall’s role regarding ports?  
**A6:** It filters and controls traffic flow, blocking unauthorized access.

**Q7:** Why do attackers perform port scans?  
**A7:** To discover active services that can be exploited.

**Q8:** How does Wireshark complement port scanning?  
**A8:** It analyzes network traffic at a packet level for deeper insights.

### Conclusion
This task improved my understanding of **network reconnaissance**, **open ports**, and **security risks**. Using Nmap and Wireshark provided valuable practical experience in identifying vulnerabilities and securing networks.

---

📌 **Submission:**  
Upload this repository with the PDF report, screenshots, and README.md file.

