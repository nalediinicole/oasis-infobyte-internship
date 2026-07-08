# Research Report: Social Engineering Attacks

**Internship:** Oasis Infobyte – Security Analyst Internship  
**Task:** Task 5 – Research Report on Social Engineering Attacks  
**Date:** July 2026  

---

## Introduction

When most people think about hacking, they imagine someone typing code and breaking through firewalls. But a lot of the time, attackers do not need to do any of that. Instead, they just trick people. This is what social engineering is — using psychological manipulation to get someone to give up information or do something that puts security at risk.

Social engineering is scary because it targets humans, not systems. And humans can be much easier to manipulate than a well-configured firewall. This report looks at three main types of social engineering attacks: phishing, pretexting, and baiting. For each one, I will explain how it works, share a real-world example, and talk about how to protect against it.

---

## 1. Phishing

### What is it?
Phishing is probably the most well-known social engineering attack. It is when an attacker sends a fake email (or message) pretending to be from a trusted source like a bank, a company, or even your workplace. The goal is to get you to click a link, download something, or hand over your login details.

### Types of Phishing

**Standard Phishing** – Mass emails sent to thousands of people at once, hoping some will fall for it.

**Spear Phishing** – A more targeted version where the attacker researches a specific person and personalises the message to make it more convincing.

**Whaling** – Spear phishing aimed at high-level executives like CEOs or CFOs, often involving large money transfers.

**Smishing and Vishing** – Phishing done through SMS texts (smishing) or phone calls (vishing).

### How does it work?
- You receive an email that looks like it is from your bank saying your account is about to be locked
- The email has a sense of urgency to make you panic and act quickly
- You click the link which takes you to a fake website that looks real
- You enter your username and password, which goes straight to the attacker
- The attacker now has access to your account

### Real-World Example
Between 2013 and 2015, a man named **Evaldas Rimasauskas** pulled off one of the biggest phishing scams ever. He created a fake company that looked like a real hardware supplier called Quanta Computer. He then sent fake invoices by email to both **Google and Facebook**. Both companies paid, and he ended up stealing over **$100 million** combined before he was caught. It is a good example of how even huge tech companies can be fooled.

### Impact
- Login credentials and personal data get stolen
- Companies can lose millions of dollars
- Customers of impersonated brands lose trust

### How to Prevent It
- Always check the sender's email address carefully before clicking anything
- Do not click links in emails — go directly to the website instead
- Enable Multi-Factor Authentication (MFA) on all important accounts
- Companies should run simulated phishing tests so employees learn to spot them

---

## 2. Pretexting

### What is it?
Pretexting is when an attacker makes up a fake story — a "pretext" — to gain someone's trust and get information out of them. The attacker usually pretends to be someone with a legitimate reason to ask questions, like an IT technician, a bank employee, or even a police officer.

Unlike phishing which happens mostly through emails, pretexting often happens over the phone or even in person.

### How does it work?
- The attacker does some research on the target or their organisation first
- They then contact the target pretending to be someone trustworthy
- They use the fake story to convince the target to give up passwords, account details, or system access
- Because the story sounds believable, the victim does not realise they are being manipulated

### Real-World Example 1: HP Pretexting Scandal (2006)
**Hewlett-Packard** hired private investigators to find out who was leaking information to journalists. The investigators used pretexting to call phone companies and pretend to be HP board members, getting access to their private call records. This caused a massive scandal and resulted in criminal charges and a large financial settlement for HP.

### Real-World Example 2: Twitter Hack (2020)
In July 2020, attackers called Twitter employees pretending to be from Twitter's own IT department. They convinced staff to hand over credentials to internal admin tools. Using those tools, they took over verified accounts belonging to **Barack Obama, Elon Musk, Apple, and Joe Biden** and used them to run a Bitcoin scam. They made over **$100,000 in Bitcoin** in just a few hours.

### Impact
- Attackers can get access to systems without needing any technical hacking skills
- Internal credentials and sensitive data can be compromised
- Even large, well-resourced organisations are vulnerable

### How to Prevent It
- Always verify someone's identity before giving out any information, even if they sound convincing
- Have a policy of calling back on known official numbers rather than numbers given by the caller
- Train employees to question unusual requests, even from people claiming to be from IT or management

---

## 3. Baiting

### What is it?
Baiting works by offering something tempting to lure a victim into taking an action that compromises security. The attacker uses curiosity or greed as the weapon. It can happen physically or online.

### How does it work?

**Physical Baiting (USB Drop Attack)**
- The attacker loads malware onto a USB drive
- They label it something interesting like "Salary List 2026" or "Confidential"
- They leave it somewhere it will be found, like a company car park or reception area
- A curious employee picks it up and plugs it into their work computer
- The malware runs automatically and the attacker now has access to the network

**Online Baiting**
- The attacker sets up a fake website offering free movies, music, or software
- The victim downloads the file thinking it is something they want
- The file is actually malware that installs on their device

### Real-World Example
The **US Department of Homeland Security** ran an experiment in 2011 where they dropped USB drives in government car parks. They found that **60% of employees picked them up and plugged them in**. When the drives had an official-looking logo on them, that number went up to **90%**. This shows how powerful simple curiosity can be, and why physical baiting is such an effective attack.

### Impact
- Malware and ransomware can be installed on corporate systems
- Sensitive data can be stolen or encrypted for ransom
- One infected device can spread the infection to the whole network

### How to Prevent It
- Never plug in a USB drive you found or that came from an unknown source
- Disable auto-run on USB ports so malware cannot execute automatically
- Train employees about the risks of unknown devices
- Use endpoint security software that can detect malware on removable media

---

## Other Social Engineering Techniques Worth Knowing

**Tailgating** – Following an authorised person through a secure door without having access yourself, relying on politeness to not get challenged.

**Quid Pro Quo** – Offering help in exchange for information. For example, someone calls pretending to be IT support and offers to fix your computer problem if you give them your password.

**Watering Hole** – The attacker infects a website that the target regularly visits. When the target visits the site, their device gets infected with malware.

---

## Comparison Table

| Attack | Method | Psychological Trick Used | Technical Skill Needed |
|--------|--------|--------------------------|------------------------|
| Phishing | Email, SMS, Phone | Fear and urgency | Low |
| Pretexting | Phone, In-person | Trust and authority | Low to Medium |
| Baiting | Physical or Online | Curiosity and greed | Low |
| Tailgating | Physical | Social politeness | None |
| Quid Pro Quo | Phone | Helpfulness | Low |

---

## Recommendations for Prevention

Based on what I have researched, here are the most important steps organisations and individuals can take:

1. **Security awareness training** – Regular training that teaches employees how to spot social engineering attempts is the single most effective defence.
2. **Simulated attacks** – Running fake phishing campaigns internally helps test whether training is working.
3. **Multi-Factor Authentication** – Even if credentials are stolen, MFA makes it much harder for attackers to get in.
4. **Verify before you trust** – Always confirm the identity of anyone asking for sensitive information, especially over the phone.
5. **Clear policies on sensitive requests** – Have strict rules around things like wire transfers or password resets that require multiple approvals.
6. **Report without fear** – Create a culture where employees feel comfortable reporting mistakes. If someone realises they fell for an attack, they need to report it immediately without being afraid of getting in trouble.

---

## Conclusion

Social engineering attacks are a reminder that cybersecurity is not just a technical problem — it is a human one. Phishing, pretexting, and baiting all exploit basic human behaviour like trust, curiosity, and fear of consequences. The real-world examples in this report, from the $100 million Google and Facebook scam to the Twitter hack that targeted some of the most famous accounts in the world, show that no one is immune.

What I found most interesting while researching this topic is that the solution is not just about having better technology. It is about building a security-aware mindset in every person who uses a system. Training, verification habits, and open communication are just as important as firewalls and antivirus software.

---

## References

- Hadnagy, C. (2011). *Social Engineering: The Art of Human Hacking.* Wiley.
- Verizon. (2023). *Data Breach Investigations Report.* https://www.verizon.com/business/resources/reports/dbir/
- FBI. (2022). *Business Email Compromise: The $43 Billion Scam.* https://www.ic3.gov
- KrebsOnSecurity. (2020). *Twitter Got Hacked.* https://krebsonsecurity.com
- CISA. (2023). *Avoiding Social Engineering and Phishing Attacks.* https://www.cisa.gov/tips/st04-014
- SANS Institute. (2022). *Social Engineering: Understanding the Threat.* https://www.sans.org
