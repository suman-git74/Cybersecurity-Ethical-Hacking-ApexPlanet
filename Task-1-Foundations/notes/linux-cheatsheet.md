# Task 1: Foundations & Environment Setup

**Intern Name:** Sumanth Uppala  
**Program:** Cybersecurity & Ethical Hacking Internship, ApexPlanet Software Pvt. Ltd.  
**Timeline:** Days 1–12  
**Report Date:** 29-10-2026  

---

## 1. Objective
The objective of this task is to build strong core fundamentals in cybersecurity, networking, and cryptography, and to configure an isolated, professional penetration-testing lab for ethical hacking practice throughout the internship.

---

## 2. Cybersecurity Basics

### CIA Triad
* **Confidentiality:** Ensuring that sensitive data is accessible only to authorized users and protected against unauthorized disclosure.
* **Integrity:** Safeguarding data accuracy and completeness by preventing unauthorized modification or tampering.
* **Availability:** Ensuring systems, networks, and data remain operational and accessible to authorized users when needed.

### Threat Types & Attack Vectors Studied
* **Threat Types:** Phishing, Malware, DDoS, SQL Injection, Brute Force, Ransomware.
* **Attack Vectors:** Social Engineering, Wireless Attacks, Insider Threats.

---

## 3. Lab Environment Setup & Architecture

An isolated virtual testing environment was created using Oracle VirtualBox with a private **Host-Only Adapter** network to ensure all pentesting traffic remains completely confined to the host machine.

| Virtual Machine | Role | IP Address (Host-Only) |
| :--- | :--- | :--- |
| **Kali Linux** | Attacker Machine | `192.168.56.3` / `192.168.56.4` |
| **Metasploitable2** | Vulnerable Target | `192.168.56.3` |

### Key Setup Verification
* **Network Mode:** VirtualBox Host-Only Adapter (`VirtualBox Host-Only Ethernet Adapter`).
* **Connectivity Test:** Ping testing was conducted from Metasploitable2 to Kali (`ping 192.168.56.4`) confirming 0% packet loss, while external pings (`ping 8.8.8.8`) failed as expected due to host isolation.

### Lab Setup Visuals
* **VirtualBox Manager:**
  ![VirtualBox Manager showing VMs running](screenshots/01_virtualbox_vms_running.png)
* **Host-Only Network Configuration:**
  ![Host-Only Network Adapter settings](screenshots/02_host_only_network_settings.png)
* **Ping Connectivity Test:**
  ![Ping test between VMs](screenshots/03_ping_connectivity_test.png)

---

## 4. Networking & Cryptography Overview

### Networking Fundamentals
* **OSI Model (7 Layers):** Physical → Data Link → Network → Transport → Session → Presentation → Application.
* **TCP/IP Protocol Suite:** Practical 4-layer protocol stack; compared connection-oriented TCP (3-way handshake) vs. connectionless UDP.
* **Core Protocols:** DNS (port 53), HTTP (port 80 plaintext) vs. HTTPS (port 443 encrypted via TLS/SSL).
* **IP Addressing & NAT:** CIDR subnetting and Network Address Translation for private/public mapping.

### Cryptography Basics
* **Symmetric vs. Asymmetric:** Single shared-key encryption (AES-256) versus public/private key-pair encryption (RSA).
* **Hashing:** One-way integrity fingerprints (MD5, SHA-256).
* **SSL/TLS & Certificates:** Establishing identity trust via Certificate Authorities (CAs).
* **Hands-on Practice:** Encrypted and decrypted text scripts (`hlo.py`) using `openssl aes-256-cbc`.

---

## 5. Tool Familiarization Summary

| Tool | Purpose | Verified Working |
| :--- | :--- | :---: |
| **Wireshark** | Packet capture and network traffic analysis | ✅ |
| **Nmap** | Host discovery and port scanning | ✅ |
| **Burp Suite** | Web proxy and HTTP request interceptor | ✅ |
| **Netcat (`nc`)** | Banner grabbing and network debugging | ✅ |

---

## 6. Screenshots & Proof of Work

* **Linux Networking & Diagnostics (`ifconfig`, `ping`, `traceroute`):**  
  ![Linux Network Commands](Task-1-Foundations/screenshots/Kali_terminal-ifconfig_ping.png)

* **File Permissions & Python Script Execution (`chmod`, `chown`):**  
  ![File Permissions and Script Execution](screenshots/05_chmod_chown_permissions.png)

* **System Updates & Package Management (`apt update`):**  
  ![Apt Package Management](screenshots/06_apt_package_management.png)

* **OpenSSL Symmetric Encryption & Decryption (AES-256):**  
  ![OpenSSL Commands and Output](screenshots/07_openssl_encryption_decryption.png)

* **Wireshark Packet Capture & Analysis:**  
  ![Wireshark Capture Window](screenshots/08_wireshark_packet_capture.png)

* **Nmap Scanning, Burp Suite Proxy, and Netcat Testing:**  
  ![Tool Familiarization Screenshots](screenshots/09_nmap_burpsuite_netcat.png)

---

## 7. Project Links
* **Lab Setup Report (PDF):** `Task 1 Lab Report – Foundations & Environment Setup.pdf`
* **GitHub Repository:** [suman-git74/Cybersecurity-Ethical-Hacking-ApexPlanet](https://github.com/suman-git74/Cybersecurity-Ethical-Hacking-ApexPlanet)
