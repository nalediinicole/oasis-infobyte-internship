Research Report: Common Network Security Threats

Internship: Oasis Infobyte – Security Analyst Internship
Task: Task 4 – Research Report on Common Network Security Threats
Date: July 2026


Introduction

Network security is something that affects everyone who uses the internet, whether it is a big company or just an individual at home. As more people and businesses move online, attackers have more opportunities to cause damage. This report looks at three of the most common network security threats: Denial of Service (DoS) attacks, Man-in-the-Middle (MITM) attacks, and Spoofing. I will explain what each one is, how it works, give a real-world example, and talk about how to prevent it.


1. Denial of Service (DoS) Attacks

What is it?

A Denial of Service attack is when an attacker tries to make a website or server unavailable by flooding it with so much traffic that it cannot cope anymore. Think of it like a shop doorway being blocked by a crowd of people so that real customers cannot get in.

When the attack comes from many different computers at the same time, it is called a Distributed Denial of Service (DDoS) attack. Attackers usually use a network of infected computers called a botnet to do this.

How does it work?


The attacker sends thousands or millions of fake requests to a server
The server gets overwhelmed trying to respond to all of them
Real users cannot access the service because the server is too busy or has crashed
A common method is called a SYN Flood, where the attacker starts connections but never completes them, using up all the server's resources


Real-World Example

In 2016, a huge DDoS attack hit a company called Dyn, which is a DNS provider. The attack used thousands of hacked IoT devices like cameras and routers running malware called Mirai. Because of this, popular websites like Twitter, Netflix, and Reddit went down for hours. Many people could not access these sites at all.

Impact


Websites and services go offline, causing businesses to lose money
Customers lose trust in the affected company
In serious cases, critical services like hospitals or emergency services could be disrupted


How to Prevent It


Use firewalls to block suspicious traffic
Set up rate limiting so one IP address cannot send too many requests
Use DDoS protection services like Cloudflare
Spread traffic across multiple servers so no single one gets overwhelmed



2. Man-in-the-Middle (MITM) Attacks

What is it?

A Man-in-the-Middle attack is when an attacker secretly gets in between two people or systems that are communicating with each other. Both sides think they are talking directly to each other, but the attacker is actually reading or even changing the messages being sent.

A simple way to think about it is like someone intercepting letters between two people and reading them before resealing and sending them on.

How does it work?


The attacker intercepts traffic between a user and a website or server
They can use a technique called ARP Spoofing to trick devices on a network into sending their traffic through the attacker's machine
Another method called SSL Stripping downgrades a secure HTTPS connection to an insecure HTTP one so the attacker can read the data
The attacker can then steal passwords, credit card details, or other sensitive information


Real-World Example

In 2011, a company called DigiNotar, which was a certificate authority in the Netherlands, was hacked. The attackers created fake SSL certificates and used them to intercept the Gmail communications of around 300,000 users in Iran. The users thought they were connecting securely to Gmail but their data was being read by the attackers. DigiNotar ended up going bankrupt because of the breach.

Impact


Login credentials and personal data can be stolen
Financial information like banking details can be captured
Victims usually have no idea the attack is happening


How to Prevent It


Always use websites that have HTTPS, not just HTTP
Avoid using public Wi-Fi for anything sensitive like banking
Use a VPN to encrypt your internet traffic
Enable Multi-Factor Authentication (MFA) on important accounts



3. Spoofing Attacks

What is it?

Spoofing is when an attacker pretends to be something or someone they are not. They fake their identity to trick a target into trusting them. This can happen with email addresses, IP addresses, websites, and more.

Types of Spoofing

IP Spoofing – The attacker sends packets with a fake source IP address to make it look like the traffic is coming from a trusted computer.

Email Spoofing – The attacker fakes the "From" address in an email to make it look like it came from someone the victim trusts, like their bank or boss.

Website Spoofing – The attacker creates a fake website that looks exactly like a real one to trick users into entering their login details.

DNS Spoofing – The attacker tampers with DNS records so that when a user types in a real website address, they get redirected to a fake malicious site instead.

How does it work? (Email Spoofing Example)


The attacker sends an email that looks like it is from a trusted company like a bank
The email asks the victim to click a link or confirm their details
The link goes to a fake website that captures whatever the victim types in
The attacker then uses that information for fraud or to access accounts


Real-World Example

In 2019, Toyota Boshoku Corporation, a supplier for Toyota, lost about $37 million because of an email spoofing attack. Attackers sent emails pretending to be trusted business partners and convinced an employee to change bank account details for a large wire transfer. By the time the company realised what had happened, the money was gone.

Impact


Huge financial losses for businesses
Identity theft for individuals
Damage to the reputation of organisations whose identities were faked


How to Prevent It


Use email security protocols like SPF, DKIM, and DMARC
Train employees to double check sender addresses before responding
Use DNSSEC to protect against DNS spoofing
Always verify unusual requests, especially ones involving money transfers



Comparison Table

ThreatMain GoalWho it TargetsKey PreventionDoS/DDoSTake a service offlineServers and websitesFirewalls, DDoS protectionMITMIntercept communicationsUsers and their dataHTTPS, VPN, MFASpoofingFake a trusted identityUsers and systemsEmail protocols, staff training


Conclusion

After researching these three threats, it is clear that network security is not just about protecting systems — it is also about protecting people. DoS attacks can shut down entire services, MITM attacks can silently steal your data, and spoofing can trick even careful people into making costly mistakes.

What stood out to me the most is that all three of these attacks can be reduced significantly with the right combination of tools and awareness. No single solution is enough on its own. Businesses and individuals need to use technical controls like firewalls and encryption together with good habits like verifying emails and avoiding public Wi-Fi.

As someone studying network systems and interested in cybersecurity, understanding these threats is an important foundation for everything else I will learn going forward.


References


Cloudflare. (2023). What is a DDoS attack? https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/
CISA. (2022). Understanding and Responding to Distributed Denial-of-Service Attacks. https://www.cisa.gov
OWASP. (2021). Man-in-the-Middle Attack. https://owasp.org/www-community/attacks/Manipulator-in-the-middle_attack
Imperva. (2023). What is Spoofing? https://www.imperva.com/learn/application-security/spoofing-attack/
BBC News. (2019). Toyota supplier loses $37m in email scam. https://www.bbc.com/news/technology-47903496
NIST. (2020). Guidelines for Network Security. https://www.nist.gov
