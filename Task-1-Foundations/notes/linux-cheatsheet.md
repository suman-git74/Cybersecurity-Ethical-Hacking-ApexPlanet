# Linux & Security Tools Command Cheat-Sheet

**Author:** Sumanth Uppala  
**Environment:** Kali Linux  

---

## 1. Directory & File Operations

| Command | Syntax / Example | Description |
| :--- | :--- | :--- |
| `pwd` | `pwd` | Prints the current working directory path |
| `ls` | `ls -la` | Lists all files and hidden files with detailed metadata |
| `cd` | `cd /home/kali/Projects` | Changes current working directory |
| `mkdir` | `mkdir cyber_practice` | Creates a new folder |
| `touch` | `touch notes.txt` | Creates an empty file |
| `cat` | `cat notes.txt` | Displays full contents of a file in terminal |
| `rm` | `rm -rf cyber_practice` | Deletes files or directories recursively |

---

## 2. File Permissions (`chmod` & `chown`)

| Command | Syntax / Example | Description |
| :--- | :--- | :--- |
| `chmod +x` | `chmod +x hlo.py` | Makes a script executable |
| `chmod 600` | `chmod 600 secret.txt` | Read/Write permission for owner only |
| `chmod 755` | `chmod 755 script.sh` | Full access for owner; Read/Execute for others |
| `chown` | `chown kali:kali hlo.py` | Changes file owner and group |

---

## 3. System & Package Management

| Command | Syntax / Example | Description |
| :--- | :--- | :--- |
| `apt update` | `sudo apt update` | Refresh package repository indexes |
| `apt upgrade` | `sudo apt upgrade` | Upgrade installed software packages |
| `dpkg` | `dpkg -i package.deb` | Direct Debian package installation manager |

---

## 4. Networking & Interface Diagnostics

| Command | Syntax / Example | Description |
| :--- | :--- | :--- |
| `ifconfig` / `ip a` | `ifconfig` | Displays IP addresses, subnets, and active interfaces |
| `ping` | `ping -c 4 192.168.56.3` | Sends ICMP echo requests to test network reachability |
| `netstat` | `netstat -tuln` | Shows active listening ports and network connections |
| `traceroute` | `traceroute google.com` | Traces network hops taken by packets to target host |

---

## 5. Cryptography Hands-On (`OpenSSL`)

### AES-256 Symmetric Encryption
```bash
# Encrypt a file using AES-256 CBC cipher
openssl enc -aes-256-cbc -salt -in hlo.py -out encrypted_hlo.py
