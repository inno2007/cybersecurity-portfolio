# 🧠 Traffic Analysis, Password Cracking, and SQL Injection Lab

This repository showcases a cybersecurity lab covering three fundamental topics:
- **Network traffic analysis** using Wireshark
- **Password cracking** using John the Ripper
- **SQL Injection** to bypass vulnerable login pages

---

## 📚 Lab Summary

### 🔍 1. Network Traffic Analysis with Wireshark

- Captured HTTP login traffic to observe credential leaks.
- Used display filters like `http`, `ftp`, `tcp.port==80` to isolate sensitive data.
- Identified usernames and passwords transmitted in cleartext.

**Key Takeaways**:
- Importance of HTTPS for protecting credentials.
- How attackers use packet sniffing for data extraction.

---

### 🔓 2. Password Cracking with John the Ripper

- Simulated a compromised Linux system by collecting `/etc/passwd` and `/etc/shadow`.
- Combined both using the `unshadow` command.
- Used `john` to crack weak passwords using a wordlist attack.

**Commands Used**:
```bash
unshadow passwd shadow > combined.txt
john --wordlist=/usr/share/wordlists/rockyou.txt combined.txt
