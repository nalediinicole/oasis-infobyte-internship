# Research Report: Common Network Security Threats

**Internship:** Oasis Infobyte – Security Analyst Internship  
**Task:** Task 4 – Research Report on Common Network Security Threats  
**Date:** July 2026  

---

## Table of Contents
1. [Introduction](#introduction)
2. [Denial of Service (DoS) Attacks](#1-denial-of-service-dos-attacks)
3. [Man-in-the-Middle (MITM) Attacks](#2-man-in-the-middle-mitm-attacks)
4. [Spoofing Attacks](#3-spoofing-attacks)
5. [Comparison of Threats](#comparison-of-threats)
6. [Conclusion](#conclusion)
7. [References](#references)

---

## Introduction

As organisations continue to rely heavily on networked systems and the internet for daily operations, the threat landscape in cybersecurity has grown significantly. Network security threats are malicious activities that target the integrity, availability, and confidentiality of networked systems and the data they carry. Understanding these threats is a critical first step in building effective defences against them.

This report examines three of the most common and impactful network security threats: Denial of Service (DoS) attacks, Man-in-the-Middle (MITM) attacks, and Spoofing attacks. For each threat, this report explains how it works, its real-world impact, and the preventive measures that can be taken to mitigate it.

---

## 1. Denial of Service (DoS) Attacks

### What is a DoS Attack?
A Denial of Service (DoS) attack is a cyberattack in which an attacker attempts to make a machine, network, or service unavailable to its intended users by overwhelming it with a flood of illegitimate requests or traffic. When the target system is flooded beyond its capacity, it becomes slow or completely unresponsive, denying access to legitimate users.

A more powerful variant is the **Distributed Denial of Service (DDoS)** attack, where the attacker uses multiple compromised computers — often called a **botnet** — to launch the attack simultaneously from many different locations, making it much harder to block.

### How it Works
1. The attacker identifies a target system such as a web server or network device.
2. The attacker sends an overwhelming volume of traffic or requests to the target.
3. The target's resources (bandwidth, processing power, memory) become exhausted.
4. Legitimate users can no longer access the service.

Common DoS techniques include:
- **SYN Flood:** The attacker sends a large number of TCP SYN requests to a server without completing the handshake, consuming server resources.
- **UDP Flood:** The attacker sends large amounts of UDP packets to random ports, forcing the target to process and respond to each one.
- **HTTP Flood:** The attacker sends a large number of HTTP GET or POST requests to a web server, overwhelming it.

### Real-World Example
In **2016**, a massive DDoS attack targeted **Dyn**, a major DNS provider. The attack used a botnet of compromised IoT devices (cameras, routers) running the **Mirai malware**. The result was that major websites including Twitter, Netflix, Reddit, and CNN became unavailable for millions of users across the United States and Europe for several hours.

### Impact
- Loss of revenue for businesses during downtime
- Damage to brand reputation and customer trust
- Disruption of critical services such as healthcare and emergency services
- Costs associated with incident response and recovery

### Prevention and Mitigation
- **Rate limiting:** Restrict the number of requests a server accepts from a single IP address.
- **Firewalls and intrusion prevention systems (IPS):** Configure rules to detect and block suspicious traffic patterns.
- **Content Delivery Networks (CDNs):** Distribute traffic across multiple servers to absorb large volumes of requests.
- **DDoS protection services:** Use cloud-based services such as Cloudflare or AWS Shield to filter malicious traffic before it reaches the target.
- **Blackholing:** Route malicious traffic to a null interface, effectively discarding it.

---

## 2. Man-in-the-Middle (MITM) Attacks

### What is a MITM Attack?
A Man-in-the-Middle (MITM) attack occurs when an attacker secretly intercepts and potentially alters the communication between two parties who believe they are communicating directly with each other. The attacker positions themselves between the sender and receiver, allowing them to eavesdrop, steal data, or inject malicious content into the communication.

### How it Works
1. The attacker intercepts communication between a client (e.g., a user's browser) and a server (e.g., a banking website).
2. The attacker may use techniques such as **ARP spoofing** or **DNS spoofing** to redirect traffic through their machine.
3. The attacker reads, captures, or modifies the data in transit.
4. The altered data is forwarded to the intended recipient, with neither party aware of the interception.

Common MITM techniques include:
- **ARP Spoofing:** The attacker sends fake ARP (Address Resolution Protocol) messages on a local network, linking their MAC address with the IP address of a legitimate host.
- **SSL Stripping:** The attacker downgrades an HTTPS connection to HTTP, allowing them to read unencrypted traffic.
- **Evil Twin Attack:** The attacker sets up a rogue Wi-Fi access point that mimics a legitimate one, tricking users into connecting to it.
- **DNS Spoofing:** The attacker corrupts DNS cache entries to redirect users to malicious websites.

### Real-World Example
In **2011**, **DigiNotar**, a Dutch certificate authority, was compromised by attackers who issued fraudulent SSL certificates. These certificates were used to perform MITM attacks on Gmail users in Iran, allowing the attackers to intercept encrypted communications of approximately **300,000 users**. The attack ultimately led to DigiNotar declaring bankruptcy.

### Impact
- Theft of sensitive data including login credentials, credit card numbers, and personal information
- Financial fraud and identity theft
- Unauthorised access to corporate systems
- Compromise of confidential business communications

### Prevention and Mitigation
- **Use HTTPS:** Always ensure websites use HTTPS with valid SSL/TLS certificates to encrypt communications.
- **Certificate pinning:** Applications can be configured to only trust specific certificates, preventing fake certificate attacks.
- **VPNs (Virtual Private Networks):** Encrypt all network traffic, making it unreadable to potential interceptors.
- **Multi-factor authentication (MFA):** Even if credentials are stolen, MFA adds an additional layer of protection.
- **Avoid public Wi-Fi:** Refrain from accessing sensitive accounts on unsecured public networks.
- **HSTS (HTTP Strict Transport Security):** Forces browsers to only connect to websites over HTTPS.

---

## 3. Spoofing Attacks

### What is a Spoofing Attack?
Spoofing is a type of cyberattack in which an attacker disguises themselves as a trusted entity by falsifying data such as an IP address, email address, MAC address, or website URL. The goal is to deceive the target into trusting the attacker, allowing them to gain unauthorised access, steal information, or deliver malware.

### Types of Spoofing Attacks

#### a) IP Spoofing
The attacker sends IP packets with a forged source IP address to make it appear as though the traffic is coming from a trusted source. This is commonly used in DoS attacks and to bypass IP-based access controls.

#### b) Email Spoofing
The attacker forges the "From" field in an email to make it appear as though it was sent by a trusted sender such as a bank, employer, or colleague. This is one of the most common techniques used in **phishing attacks**.

#### c) DNS Spoofing (DNS Cache Poisoning)
The attacker corrupts the DNS cache of a resolver, causing it to return incorrect IP addresses. Users who try to visit a legitimate website are redirected to a malicious one instead.

#### d) MAC Spoofing
The attacker changes their device's MAC address to impersonate another device on the network, bypassing MAC address filtering controls.

#### e) Website Spoofing
The attacker creates a fake website that looks identical to a legitimate one (e.g., a bank's login page) to trick users into entering their credentials.

### How it Works (Email Spoofing Example)
1. The attacker composes an email using a legitimate-looking "From" address (e.g., support@mybank.com).
2. The email is sent to a victim, appearing to come from their bank.
3. The victim, trusting the sender, clicks a malicious link or provides sensitive information.
4. The attacker uses this information for fraud or further attacks.

### Real-World Example
In **2019**, **Toyota Boshoku Corporation**, a Toyota supplier, lost approximately **$37 million** in a business email compromise (BEC) attack. Attackers spoofed email addresses of trusted business partners and convinced an employee to change bank account details for a wire transfer. The funds were transferred to an account controlled by the attackers before the fraud was discovered.

### Impact
- Financial losses through fraudulent transactions
- Data breaches and identity theft
- Reputational damage to organisations whose identities are spoofed
- Legal and regulatory consequences for affected organisations

### Prevention and Mitigation
- **Email authentication protocols:** Implement SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication) to verify the authenticity of email senders.
- **Packet filtering:** Configure firewalls to reject packets with suspicious or forged source IP addresses.
- **DNS Security Extensions (DNSSEC):** Adds cryptographic signatures to DNS records to prevent DNS spoofing.
- **User awareness training:** Educate employees to verify sender identities before clicking links or transferring funds.
- **Two-factor authentication:** Reduces the impact of credential theft through spoofed websites.

---

## Comparison of Threats

| Threat | Primary Goal | Target | Common Tools Used |
|--------|-------------|--------|-------------------|
| DoS/DDoS | Disrupt availability | Servers, networks | Botnets, traffic floods |
| MITM | Intercept/alter data | Communications | ARP spoofing, SSL stripping |
| Spoofing | Impersonate trusted entity | Users, systems | Fake IPs, forged emails |

---

## Conclusion

Network security threats such as DoS attacks, Man-in-the-Middle attacks, and Spoofing attacks pose serious risks to organisations and individuals alike. Each threat operates differently but shares a common goal: to exploit weaknesses in network systems for malicious purposes.

DoS attacks disrupt the availability of services, MITM attacks compromise the confidentiality and integrity of communications, and spoofing attacks undermine trust by impersonating legitimate entities. Real-world incidents such as the Mirai botnet DDoS attack, the DigiNotar SSL compromise, and the Toyota email fraud demonstrate that these are not theoretical threats — they cause real and significant harm.

Effective defence against these threats requires a layered security approach that combines technical controls such as firewalls, encryption, and authentication protocols with human factors such as security awareness training. Staying informed about evolving attack methods and regularly updating security practices is essential for maintaining a strong security posture in today's networked world.

---

## References

- Cloudflare. (2023). *What is a DDoS attack?* https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/
- CISA. (2022). *Understanding and Responding to Distributed Denial-of-Service Attacks.* https://www.cisa.gov
- OWASP. (2021). *Man-in-the-Middle Attack.* https://owasp.org/www-community/attacks/Manipulator-in-the-middle_attack
- Imperva. (2023). *What is Spoofing?* https://www.imperva.com/learn/application-security/spoofing-attack/
- Krebs, B. (2016). *Hacker Lexicon: What Is the Mirai Botnet?* Wired. https://www.wired.com
- BBC News. (2019). *Toyota supplier loses $37m in email scam.* https://www.bbc.com/news/technology-47903496
- NIST. (2020). *Guidelines for Network Security.* National Institute of Standards and Technology. https://www.nist.gov
