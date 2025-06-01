
# 🛡️ Vulnerability Assessment Exercise

## 📌 Objective

Gain hands-on experience in identifying, categorizing, and reporting vulnerabilities in a simulated or real-world environment. This exercise demonstrates essential skills for penetration testing and risk management.

---

## ⚙️ Tools Used

- **Nmap** – Network discovery and port scanning
- **Nikto** – Web server scanner
- **OpenVAS** or **Nessus** – Vulnerability scanners (optional)
- **Whois / nslookup / dig** – OSINT
- **Metasploit Framework** – For validation and exploitation (optional and legal only)

---

## 🧪 Target

**Simulated Environment**:  
Use [Metasploitable2](https://sourceforge.net/projects/metasploitable/) or [DVWA (Damn Vulnerable Web App)](http://www.dvwa.co.uk/).

> ⚠️ Do **not** scan systems you do not own or have explicit permission to test.

---

## 📝 Assessment Workflow

### 1. **Information Gathering**

```bash
whois <target-ip>
nslookup <target-ip>
nmap -sS -sV -O -Pn <target-ip>
```

- Identify open ports
- Determine services and versions
- OS fingerprinting

---

### 2. **Vulnerability Scanning**

#### 🔍 Using Nikto (Web Servers)

```bash
nikto -h http://<target-ip>
```

#### 🔍 Using Nmap Scripts

```bash
nmap -sV --script vuln <target-ip>
```

#### 🔍 Optional: OpenVAS/Nessus

- Launch a scan against the target
- Export and review findings

---

### 3. **Analysis and Risk Classification**

Use the **CVSS (Common Vulnerability Scoring System)** to classify risks:

| Vulnerability | CVSS Score | Risk Level | Description |
|---------------|------------|------------|-------------|
| Apache 2.2.8 | 7.5 | High | Remote Code Execution |
| MySQL 5.0 | 5.0 | Medium | Version Disclosure |
| XSS on Login | 4.3 | Medium | Reflected XSS via login field |

---

### 4. **Reporting**

Create a structured report with these sections:

- **Executive Summary**
- **Scope of Engagement**
- **Findings and Risk Levels**
- **Screenshots / Evidence**
- **Recommendations**

Example:

```
Vulnerability: Apache Remote Code Execution
Port: 80
Tool: Nikto
CVSS: 7.5 (High)
Remediation: Update Apache to latest version or migrate to supported release.
```

---

## 📸 Screenshots to Include

- Nmap scan results
- Nikto scan showing web vulnerabilities
- Screenshots from vulnerability reports
- (Optional) Exploitation result using Metasploit in a legal sandbox

---

## 🛡️ Best Practices

- Always scan with permission
- Prioritize critical vulnerabilities first
- Provide actionable remediation advice

---

## 📂 License

This assessment is part of a personal cybersecurity learning portfolio. Educational use only. Do not perform unauthorized scans.

---

