# Kali Linux and Medusa Attack Simulation Project

<p align="center">
<img 
    src="./images/kali-medusa (1).png"
    width="300"
/>
</p>

## 📌 Objective

This project aims to implement, document, and share a practical security testing environment using the Kali Linux operating system and the Medusa tool, together with vulnerable environments such as Metasploitable 2 and DVWA (Damn Vulnerable Web Application).

The main focus is to simulate real-world brute-force attack scenarios and demonstrate basic prevention and mitigation measures.

> Project developed based on the Santander Cybersecurity Bootcamp 2025, in partnership with DIO.

---

# 🛠️ Technologies Used

* Kali Linux
* Medusa
* Metasploitable 2
* DVWA
* VirtualBox
* SMB
* FTP
* Linux
* Host-Only Networks

---

# 🧪 Simulated Scenarios

## 1. FTP Brute-Force Attack

Use of the Medusa tool to perform automated login attempts against a vulnerable FTP service.

### Objectives

* Validate weak credentials
* Demonstrate the risks of simple passwords
* Understand how brute-force attacks work against FTP services

---

## 2. Automated Attempts on a Web Form (DVWA)

Simulation of automated attacks against vulnerable web forms using the DVWA environment.

### Objectives

* Understand authentication vulnerabilities
* Simulate automated login attacks
* Identify protection measures against brute-force attacks

---

## 3. SMB Password Spraying

User enumeration and password spraying against SMB services.

### Objectives

* Identify valid accounts
* Demonstrate the risks of password reuse
* Understand the differences between traditional brute-force attacks and password spraying

---

# 🖥️ Environment Structure

The environment was configured using two virtual machines in VirtualBox:

| Virtual Machine  | Role               |
| ---------------- | ------------------ |
| Kali Linux       | Attacker machine   |
| Metasploitable 2 | Vulnerable machine |

### Network Configuration

* Network type: **Host-Only**
* Communication restricted to the local laboratory environment
* Isolated environment for educational purposes

---

# ⚙️ Lab Configuration

## Requirements

* VirtualBox installed
* Kali Linux ISO
* Metasploitable 2 VM
* Minimum resources:

  * 4 GB RAM
  * 20 GB storage
  * Configured Host-Only adapter

---

# 🚀 Test Execution

## Host Discovery

```bash
netdiscover
```

or

```bash
nmap -sn 192.168.X.0/24
```

---

# 🔓 FTP Brute-Force Test

## Medusa Command Example

```bash
medusa -h 192.168.X.X -u msfadmin -P wordlist.txt -M ftp
```

### Parameters Used

| Parameter | Description       |
| --------- | ----------------- |
| -h        | Target host       |
| -u        | Username          |
| -P        | Password wordlist |
| -M        | Target service    |

---

# 🌐 Web Form Test (DVWA)

## Automation Example

```bash
medusa -h 192.168.X.X -u admin -P wordlist.txt -M http
```

---

# 🧩 SMB Enumeration

## User Enumeration

```bash
enum4linux 192.168.X.X
```

## Password Spraying with Medusa

```bash
medusa -h 192.168.X.X -U usuarios.txt -p Senha123 -M smbnt
```

---

# 📚 Wordlists Used

Example of a simple wordlist:

```txt
123456
admin
password
msfadmin
toor
123123
```

---

# ✅ Results Validation

Successful access was validated through:

* FTP login
* Web login in DVWA
* SMB authentication
* Positive responses from Medusa

---

# 🛡️ Mitigation Recommendations

## Recommended Measures

* Use strong passwords
* Implement MFA (Multi-Factor Authentication)
* Block consecutive failed login attempts
* Implement rate limiting
* Monitor logs
* Disable unnecessary services
* Establish appropriate password management policies

---

# ⚠️ Legal Disclaimer

This project was developed exclusively for educational and laboratory purposes.

All tests were performed in controlled and authorized environments. Misuse of the techniques presented against systems without authorization is illegal.

---

# 📖 Key Learnings

During the development of this laboratory, I gained an understanding of:

* How brute-force attacks work
* The difference between brute force and password spraying
* The importance of password policies
* Common vulnerabilities in exposed services
* Basic mitigation techniques

---

# 👩‍💻 Author

[FSS](https://github.com/FS-MyCodePath) -
Junior Systems Analysis and Development.

Focus on Cybersecurity, Networking, and Infrastructure.

---

