# Nmap Cheatsheet 🕵️‍♂️

A **complete A-to-Z guide** for beginners to advanced penetration testers using **Nmap (Network Mapper)**.

---

## 👨‍💻 Author Introduction  

Hello! I am **Muhammad Saqlain Shoukat** also known as **Dark Wolf** founder and developer of **Coding Chat Room**, a passionate learner and creator in the field of **Cybersecurity, Programming, and DevSecOps**.  

🔹 My mission is to make **complex technical concepts simple and easy** so that students and professionals can learn without confusion.  
🔹 On my platforms, I share tutorials, study notes, and practical tips about **Linux, Ethical Hacking, Development, Programming and Cybersecurity**.  
🔹 I believe in **learning by sharing** — the more we teach, the more we grow.  

---

## 📌 Table of Contents
1. [Introduction](#introduction)
2. [Basic Scanning](#basic-scanning)
3. [Target Specification](#target-specification)
4. [Scan Techniques](#scan-techniques)
5. [Port Scanning Options](#port-scanning-options)
6. [Service and Version Detection](#service-and-version-detection)
7. [OS Detection](#os-detection)
8. [Timing and Performance](#timing-and-performance)
9. [Firewall / IDS Evasion](#firewall--ids-evasion)
10. [Output Formats](#output-formats)
11. [Nmap Scripting Engine (NSE)](#nmap-scripting-engine-nse)
12. [Advanced Scans](#advanced-scans)
13. [Examples](#examples)
14. [References](#references)

---

> **Watch Demo**: You can also watch demo for its learning from here 👉: [HYDRA in 1 Video](https://youtu.be/LdSuTnqLRdk?si=WfalotoJSfucJkGX)

## 📖 Introduction
**Nmap** (Network Mapper) is an open-source tool for:
- Network discovery
- Security auditing
- Penetration testing
- Vulnerability scanning

---

## 🔹 Basic Scanning
```bash
nmap <target>
nmap 192.168.1.1
nmap example.com
```
- Scans the most common 1000 ports.

---

## 🎯 Target Specification
```bash
nmap 192.168.1.1              # Single target
nmap 192.168.1.1 192.168.1.2  # Multiple targets
nmap 192.168.1.0/24           # Subnet scan
nmap -iL targets.txt          # List of targets from file
nmap -iR 10                   # Scan 10 random hosts
```

---

## 🔍 Scan Techniques
```bash
nmap -sS <target>   # TCP SYN scan (stealthy)
nmap -sT <target>   # TCP connect scan
nmap -sU <target>   # UDP scan
nmap -sA <target>   # ACK scan (firewall rules)
nmap -sW <target>   # Window scan
nmap -sM <target>   # Maimon scan
nmap -sN <target>   # Null scan
nmap -sF <target>   # FIN scan
nmap -sX <target>   # Xmas scan
```

---

## ⚡ Port Scanning Options
```bash
nmap -p 80 <target>          # Scan specific port
nmap -p 1-65535 <target>     # Scan all ports
nmap -F <target>             # Fast scan (100 ports)
nmap --top-ports 100 <target> # Scan top 100 ports
```

---

## 🛠 Service and Version Detection
```bash
nmap -sV <target>           # Detect service versions
nmap --version-intensity 9  # Aggressive detection
```

---

## 🖥 OS Detection
```bash
nmap -O <target>        # Enable OS detection
nmap -A <target>        # Aggressive scan (OS + services + traceroute + scripts)
```

---

## ⏱ Timing and Performance
```bash
nmap -T0 <target>  # Paranoid (slow, evasion)
nmap -T1 <target>  # Sneaky
nmap -T2 <target>  # Polite
nmap -T3 <target>  # Normal
nmap -T4 <target>  # Aggressive
nmap -T5 <target>  # Insane (very fast, noisy)
```

---

## 🛡 Firewall / IDS Evasion
```bash
nmap -f <target>                # Fragment packets
nmap -D RND:10 <target>         # Decoy scan
nmap -S <spoofed_IP> <target>   # Spoof source IP
nmap --source-port 53 <target>  # Specify source port
nmap --data-length 50 <target>  # Append random data
```

---

## 📤 Output Formats
```bash
nmap -oN output.txt <target>   # Normal output
nmap -oX output.xml <target>   # XML output
nmap -oG output.gnmap <target> # Grepable output
nmap -oA fullscan <target>     # All formats
```

---

## 📜 Nmap Scripting Engine (NSE)
- NSE allows automation with Lua scripts.

```bash
nmap --script <script-name> <target>
nmap --script=vuln <target>    # Run all vuln scripts
nmap --script=default <target> # Default scripts
nmap --script=discovery <target>
nmap --script=auth <target>
```

**Script Examples:**
```bash
nmap --script=http-title <target>
nmap --script=ftp-anon <target>
nmap --script=smb-os-discovery <target>
```

---

## 🚀 Advanced Scans
```bash
nmap -A <target>              # Aggressive scan
nmap --traceroute <target>    # Trace route
nmap --script=vuln <target>   # Vulnerability scan
nmap --script=exploit <target># Exploit scripts
```

---

## 🧑‍💻 Examples
```bash
nmap -sS -sV -O -p 1-1000 192.168.1.1
nmap -A example.com
nmap -T4 -F 192.168.0.0/24
nmap -Pn 192.168.1.1
```

---

## 📚 References
- [Official Nmap Docs](https://nmap.org/book/man.html)
- [Nmap Scripts Database](https://nmap.org/nsedoc/)
- [Nmap Cheat Sheet (SANS)](https://www.sans.org/security-resources/nmap/)

---

## 📚 More Learning & Connect with Me

If you found this helpful and want to learn more about **search tricks, cybersecurity, and coding**, follow me here and **Star this Resporatory**:

- 🎥 **YouTube**: [Coding Chat Room](https://www.youtube.com/@CodingChatRoom)  
- 📸 **Instagram**: [@codingchatroom](https://www.instagram.com/codingchatroom/?igsh=czBrcjAyYmxma2du)
- 💻 GitHub: [Coding Chat Room](https://github.com/CodingChatRoom)

💡 I share tutorials, tips, and resources to make learning **cybersecurity and coding easier**.  
Don’t forget to **subscribe & follow** for more updates and **Star this Resporatory** 🚀  
