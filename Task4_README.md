# Task 4: Firewall Configuration and Testing

## 📌 Objective
The objective of this task is to configure and test basic firewall rules using **Windows Firewall** and **UFW (Uncomplicated Firewall)** on Linux.  
The goal is to block insecure services (like Telnet), allow secure connections (like SSH), and verify how firewall rules filter network traffic.

## 🛠 Tools Used
- Windows Firewall (Windows 10)  
- Linux UFW (Ubuntu 20.04)  
- Target Ports: 23 (Telnet), 22 (SSH), 80 (HTTP)  

## 🔍 Steps Performed

### Windows Firewall
1. Opened **Windows Firewall with Advanced Security**.  
2. Listed current inbound and outbound firewall rules.  
3. Created a new inbound rule to **block Telnet (port 23)**.  
4. Tested connectivity on port 23 → connection blocked.  
5. Allowed HTTP traffic (port 80).  
6. Removed Telnet rule to restore defaults.  

### Linux UFW
1. Checked firewall status: `sudo ufw status verbose`.  
2. Blocked Telnet: `sudo ufw deny 23`.  
3. Tested with `telnet localhost 23` → connection refused.  
4. Allowed SSH: `sudo ufw allow 22`.  
5. Removed Telnet rule: `sudo ufw delete deny 23`.  

## 📊 Firewall Rules & Results (Sample)
| Rule Name     | Action | Port | Protocol | Result                          |
|---------------|--------|------|----------|---------------------------------|
| Block Telnet  | Deny   | 23   | TCP      | Connection blocked successfully |
| Allow SSH     | Allow  | 22   | TCP      | SSH connection permitted        |
| Allow HTTP    | Allow  | 80   | TCP      | Web traffic allowed             |

## 📑 Analysis
- **Blocking Telnet (port 23):** prevents plaintext transmission of credentials.  
- **Allowing SSH (port 22):** secure encrypted remote access.  
- **HTTP (port 80):** allowed for normal web browsing.  
- Firewalls filter based on **ports, protocols, and direction** (inbound/outbound).  

## 🛡 Best Practices
- Disable insecure services like Telnet/FTP.  
- Use SSH for secure remote login.  
- Apply **least privilege** principle when defining rules.  
- Regularly review and clean up unused rules.  
- Enable logging for suspicious activity.  

## 🎯 Key Concepts Learned
- Firewalls monitor and control network traffic.  
- **Stateful vs Stateless:** Stateful tracks sessions; Stateless filters per packet.  
- **Inbound vs Outbound:** inbound = entering traffic, outbound = leaving traffic.  
- **UFW simplifies Linux firewall management**.  
- Blocking insecure ports reduces exploitation risks.  

## ❓ Interview Questions & Answers
**Q1: What is a firewall?**  
A: A firewall monitors and filters network traffic based on predefined security rules.  

**Q2: Difference between stateful and stateless firewall?**  
A: Stateful firewalls track sessions, stateless check packets individually.  

**Q3: What are inbound and outbound rules?**  
A: Inbound = controls traffic entering; Outbound = controls traffic leaving.  

**Q4: How does UFW simplify firewall management?**  
A: UFW uses simple commands to configure rules easily.  

**Q5: Why block port 23 (Telnet)?**  
A: Telnet is insecure and transmits data in plaintext.  

**Q6: What are common firewall mistakes?**  
A: Leaving ports open, misconfigured rules, not enabling logging.  

**Q7: How does a firewall improve network security?**  
A: By blocking unauthorized access and filtering malicious traffic.  

**Q8: What is NAT in firewalls?**  
A: Network Address Translation maps private IPs to public ones, hiding internal systems.  

## ✅ Conclusion
This task provided hands-on experience with **Windows Firewall** and **Linux UFW**.  
I learned how to configure rules, block insecure services, allow secure connections, and verify results.  
Firewalls are a critical defense layer for protecting systems from unauthorized access.  
