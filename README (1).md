# Task 3: Basic Vulnerability Scan Report

## 📌 Objective

The objective of this task is to perform a basic vulnerability scan on
my PC using free tools such as **OpenVAS** or **Nessus Essentials**.\
The goal is to identify common vulnerabilities, understand their
severity, and document possible mitigations.

## 🛠 Tools Used

-   Nessus Essentials (Free Vulnerability Scanner)\
-   Operating System: Windows 10\
-   Target: Localhost (127.0.0.1)

## 🔍 Steps Performed

1.  Installed Nessus Essentials and registered with an activation code.\
2.  Configured localhost (127.0.0.1) as the scan target.\
3.  Launched a full vulnerability scan.\
4.  Waited for the scan to complete (\~45 minutes).\
5.  Reviewed the report for vulnerabilities and severity levels.

## 📊 Scan Results & Findings (Sample)

  -------------------------------------------------------------------------
  Vulnerability                     Severity    CVSS Score   Description
  --------------------------------- ----------- ------------ --------------
  Outdated Windows SMB Service      Critical    9.3          SMBv1 enabled,
                                                             vulnerable to
                                                             EternalBlue
                                                             exploit.

  Weak TLS Configuration            High        8.0          TLS 1.0
                                                             supported,
                                                             insecure.

  Unpatched Browser                 Medium      6.5          Chrome
                                                             outdated,
                                                             missing
                                                             security
                                                             patches.

  Open Port (3389 - RDP)            Medium      5.8          RDP service
                                                             running and
                                                             exposed.

  Missing Windows Updates           Low         4.0          Several
                                                             non-critical
                                                             patches not
                                                             installed.
  -------------------------------------------------------------------------

## 📑 Analysis

-   **Critical Issue:** SMBv1 service, linked to ransomware like
    WannaCry.\
-   Weak TLS and outdated browsers increase MITM attack risks.\
-   Open RDP port could allow brute-force attacks.

## 🛡 Mitigation / Fixes

-   Disable SMBv1 and upgrade to SMBv2/3.\
-   Enforce TLS 1.2 or higher.\
-   Keep browsers and apps updated.\
-   Restrict RDP access or disable if not needed.\
-   Regularly apply Windows Updates.

## 🎯 Key Concepts Learned

-   Vulnerability scanning basics.\
-   CVSS scoring system.\
-   Remediation techniques.\
-   Importance of continuous scanning.

## ❓ Interview Questions & Answers

**Q1: What is vulnerability scanning?**\
A: Identifying security weaknesses in systems using automated tools.

**Q2: Difference between vulnerability scanning and penetration
testing?**\
A: Scanning detects issues; penetration testing exploits them to assess
impact.

**Q3: What are some common vulnerabilities in PCs?**\
A: Unpatched software, weak passwords, outdated services, open ports.

**Q4: How do scanners detect vulnerabilities?**\
A: By comparing system configs/software versions with known
vulnerability databases.

**Q5: What is CVSS?**\
A: Common Vulnerability Scoring System (0--10 scale for severity).

**Q6: How often should vulnerability scans be performed?**\
A: Monthly or after major updates/changes.

**Q7: What is a false positive in scanning?**\
A: When a scanner flags a non-existent vulnerability.

**Q8: How do you prioritize vulnerabilities?**\
A: Based on severity (CVSS), exploitability, and impact on critical
systems.

## ✅ Conclusion

This task provided hands-on experience in vulnerability scanning.\
I learned how to detect critical vulnerabilities, interpret CVSS scores,
and suggest mitigations.\
Regular scanning is essential for maintaining strong system security.
