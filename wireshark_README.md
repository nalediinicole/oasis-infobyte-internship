# Task 8: Capture Network Traffic with Wireshark

**Internship:** Oasis Infobyte – Security Analyst Internship  
**Task:** Task 8 – Capture and Analyse Network Traffic with Wireshark  
**Date:** July 2026  

---

## Objective
The goal of this task was to install Wireshark, capture live network traffic on my local machine, filter for HTTP traffic, and analyse the packets to understand what kind of data is being transmitted.

---

## What is Wireshark?
Wireshark is a free, open-source network protocol analyser. It allows you to capture and inspect packets of data travelling across a network in real time. It is widely used by network administrators, security analysts, and penetration testers to troubleshoot network issues and investigate suspicious activity.

---

## Tools Used
- **Wireshark** (with Npcap for packet capture)
- **Operating System:** Windows 11
- **Interface Used:** Wi-Fi (local network)
- **Filter Applied:** HTTP

---

## Steps Taken

1. Downloaded and installed Wireshark from wireshark.org
2. Opened Wireshark and selected the active Wi-Fi network interface
3. Started a live packet capture
4. Browsed to several websites to generate network traffic
5. Stopped the capture after enough packets were collected
6. Applied an **HTTP filter** to display only HTTP traffic
7. Analysed the filtered packets and documented the findings
8. Saved the capture as `wireshark_capture.pcap`

---

## Findings and Analysis

After filtering for HTTP traffic, the following types of packets were observed:

### HTTP GET Requests
- The most common packet type captured
- These are requests sent from my computer to a web server asking for a resource (like a webpage or file)
- Example seen: `GET /browsernetworktime/time/1/current` — my computer requesting the current time from a Microsoft server
- Example seen: `GET /json/?lang=en` — a request for JSON data

### HTTP 200 OK
- These are responses from the server confirming that the request was successful
- The server found what was requested and sent it back
- Example seen: `HTTP/1.1 200 OK, JSON (application/json)` — server successfully returned JSON data

### HTTP 304 Not Modified
- This response means the content the browser requested has not changed since the last time it was loaded
- Instead of sending the full content again, the server just tells the browser to use its cached version
- This is normal browser behaviour and helps save bandwidth

### HTTP 301 Moved Permanently
- This is a redirect response
- It means the resource the browser requested has permanently moved to a new URL
- The browser will automatically follow the redirect to the new location

### OCSP (Online Certificate Status Protocol)
- These packets were checking whether SSL certificates used by websites are still valid and have not been revoked
- This is part of normal HTTPS security checks happening in the background

### Observations
- Most of the HTTP traffic captured was from **Microsoft servers** in the background — Windows was checking for updates and syncing time while the capture was running
- Source and destination **IPv6 addresses** were visible, showing modern network addressing in use
- **TCP Port 80** was used for HTTP traffic, which is the standard port for unencrypted web communication
- The packet details panel showed full **Ethernet, IP, TCP, and HTTP layer information**, demonstrating how data is structured in layers as it travels across a network

---

## What I Learned
This task gave me a practical understanding of how network traffic actually looks at the packet level. Before doing this, I knew that browsers send requests and get responses, but seeing it happen in real time with all the details — the IP addresses, ports, protocols, and response codes — made it much clearer. I also found it interesting that even when I was not actively browsing, my computer was generating HTTP traffic in the background from Windows services.

---

## Security Implications
- HTTP traffic (port 80) is **unencrypted**, meaning anyone capturing packets on the same network could potentially read the data being sent
- This is why **HTTPS** (port 443) should always be used instead — it encrypts the data so it cannot be read even if captured
- Tools like Wireshark are powerful for defenders to monitor network traffic, but they can also be misused by attackers on the same network to intercept sensitive data
- This highlights the importance of always using encrypted connections, especially on public Wi-Fi networks

---

## Files in This Repository
| File | Description |
|------|-------------|
| `wireshark_capture.pcap` | Raw packet capture file from Wireshark |
| `wireshark_README.md` | Explanation of the capture and findings |
| `wireshark_screenshot.jpeg` | Screenshot of Wireshark showing filtered HTTP traffic |

---

## References
- Wireshark Official Documentation: https://www.wireshark.org/docs/
- Wireshark Display Filters: https://wiki.wireshark.org/DisplayFilters
- OWASP: https://owasp.org
- Cloudflare. (2023). *What is HTTP?* https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/
