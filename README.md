# Task 1: Basic Network Scanning with Nmap

## Objective
Perform a network scan to identify open ports and services running on a local machine using Nmap.

---

## What is Nmap?
Nmap (Network Mapper) is a free, open-source tool used by cybersecurity professionals to discover hosts and services on a network. It works by sending packets to a target and analysing the responses to determine what ports are open and what services are running.

---

## Tools Used
- **Nmap 7.99** with Zenmap GUI
- **Target:** 127.0.0.1 (localhost — my own machine)
- **Scan Type:** Intense Scan
- **Operating System:** Windows 11

---

## Scan Results

```
Host is up (0.00040s latency).
Not shown: 998 closed tcp ports (reset)
PORT    STATE SERVICE       VERSION
135/tcp open  msrpc         Microsoft Windows RPC
445/tcp open  microsoft-ds?

Device type: general purpose
Running: Microsoft Windows 11
OS details: Microsoft Windows 11 24H2 - 25H2
```

---

## Findings and Analysis

### Port 135 — Microsoft Windows RPC (Remote Procedure Call)
- **State:** Open
- **What it does:** RPC allows programs to communicate with each other across a network. Windows uses this port for internal service communication.
- **Security significance:** If exposed to the internet, this port can be targeted by attackers to exploit RPC vulnerabilities. On a local machine it is expected to be open, but should be blocked at the firewall level from external access.

### Port 445 — Microsoft DS (SMB — Server Message Block)
- **State:** Open
- **What it does:** SMB is used for file sharing, printer sharing, and network communication between Windows machines.
- **Security significance:** This is one of the most well-known vulnerable ports in cybersecurity. The **WannaCry ransomware attack (2017)** exploited an SMB vulnerability (EternalBlue) to infect hundreds of thousands of machines worldwide. It is critical to keep Windows updated to patch SMB vulnerabilities.

---

## SMB Security Mode
The scan revealed:
```
smb2-security-mode: Message signing enabled and required
```
This is a **positive security indicator**. SMB message signing protects against relay attacks where an attacker intercepts and modifies SMB traffic. Having it enabled and required means the system is well configured in this regard.

---

## OS Detection
Nmap successfully identified the operating system as **Windows 11 24H2 - 25H2**. This demonstrates how powerful network scanning can be — an attacker can determine your exact OS version without ever logging in, which helps them identify known vulnerabilities to target.

---

## Recommendations
1. Ensure **Windows Firewall** blocks ports 135 and 445 from external/internet access.
2. Keep Windows updated regularly to patch any SMB-related vulnerabilities.
3. Disable SMB v1 if it is enabled — it is outdated and highly vulnerable.
4. Use network monitoring tools like Wireshark to detect any unusual traffic on these ports.

---

## Demo Video
Watch the Nmap scan demo here: https://drive.google.com/file/d/1GydIHM1egdmYOaFUoECFI1gLxzQDrgB_/view?usp=sharing

---

## Files in This Repository
| File | Description |
|------|-------------|
| `nmap_scan_results.txt` | Raw output from the Nmap scan |
| `README.md` | Explanation of scan results and findings |
| `screenshot.png` | Screenshot of Zenmap showing scan output |

---

## References
- Nmap Official Documentation: https://nmap.org/docs.html
- CVE Details - SMB Vulnerabilities: https://www.cvedetails.com
- WannaCry Ransomware Analysis: https://www.malwarebytes.com/wannacry
