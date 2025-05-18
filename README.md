🛡️ Network Penetration Testing with Real-World Exploits and Security Remediation
This project simulates real-world network attacks and defense strategies using Kali Linux as the attacker machine and Metasploitable as the target.

🎯 Objectives
Understand and simulate real-world network attacks
Perform scanning, enumeration, and exploitation using tools like Nmap and Metasploit
Crack Linux password hashes using John the Ripper
Identify outdated services and recommend security remediations

💻 Lab Setup

🖥️ Operating Systems
Kali Linux – Attacker Machine
Metasploitable 2 – Target Machine
🛠️ Tools Used
nmap – Port, OS, and service version scanning
Metasploit – Exploitation
John the Ripper – Password hash cracking
Linux built-in commands – user management and enumeration

🚀 Tasks Performed

🔍 Network Scanning
nmap -v IP – Basic scan
nmap -v -p- IP – Full port scan
nmap -sV IP – Service version detection
nmap -O IP – OS detection

🔐 Hidden Ports Discovered
21/tcp   open  ftp
22/tcp   open  ssh
23/tcp   open  telnet
25/tcp   open  smtp
53/tcp   open  domain
80/tcp   open  http
111/tcp  open  rpcbind
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
512/tcp  open  exec
513/tcp  open  login
514/tcp  open  shell
1524/tcp open  ingreslock
2049/tcp open  nfs
2121/tcp open  ccproxy-ftp
3306/tcp open  mysql
5900/tcp open  vnc
6000/tcp open  X11
6667/tcp open  irc

📡 Enumeration
OS: Linux 2.6.x (Metasploitable)
Open services: vsftpd, OpenSSH, Apache, MySQL, Samba, etc.
Vulnerable ports: 21 (FTP), 22 (ssh), 5900 (VNC Server)

💥 Exploitation
vsftpd 2.3.4 backdoor
ssh root login through brute force 
vnc window based root access

👤 Privilege Escalation
Created user aryan and kali with root permissions
Extracted and cracked password hash using John the Ripper

📚 Major Learning
When exploiting the Metasploitable vulnerable machine using Kali Linux, we step into the shoes of a real-world attacker, not to cause harm, but to understand the anatomy of vulnerability, the fragility of misconfigured services, and the power of information in the wrong hands. Through vsftpd, we learn how backdoored services can silently provide attackers with root shells—highlighting the importance of keeping software up-to-date and scanning for malicious code even in "official" packages. SSH login attacks teach us the value of weak or reused credentials, where brute force and default passwords can crack entry wide open—underscoring why security policies must enforce strong password hygiene and monitoring. When breaking into the VNC window, we see how remote desktop services, when left open without authentication or with default credentials, become gateways for total GUI-based control—making it painfully obvious how dangerous exposed ports are.
Diving deeper, tools like John the Ripper show us the raw reality of password cracking. We learn how hashes are not enough if the underlying passwords are weak or commonly used. John teaches us that passwords are only as strong as the user’s imagination, and that security doesn’t end at encryption—it begins with behavior.
In the grand scheme, this entire exercise isn’t just about exploiting a machine—it’s a brutal mirror reflecting the laziness, ignorance, and misconfigurations that plague real-world systems. 

⚠️ Disclaimer
This project is for educational purposes only. All activities were performed in a safe, offline lab environment. 

