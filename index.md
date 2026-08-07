---
layout: default
title: Mahamed Abdullahi
---
 
### Computer Science Student
 
Welcome to my professional portfolio. This website highlights my academic background, technical skills, and software development projects as I progress through my Computer Science studies.
 
---
 
## About Me
 
I am a Computer Science student with interests in **cybersecurity, networking, and software development**. I enjoy learning how computer systems work at both the software and systems level, and I am particularly interested in how secure and efficient systems are designed.
 
Through my coursework and personal projects, I am developing strong foundations in programming, operating systems, and computer networks. I am continuously working to improve my technical skills and build projects that demonstrate practical problem-solving and software engineering principles.
 
---
 
## Technical Interests
 
- Cybersecurity
- Computer Networking
- Software Development
- Systems Programming
- Robotics
---
 
## Skills
 
### Programming Languages
 
- Java
- C
- HTML
- C++
- Assembly MIPS
### Tools & Technologies
 
- Git
- GitHub
- Linux
### Computer Science Concepts
 
- Data Structures
- Object-Oriented Programming
- Operating Systems
- Networking Fundamentals
---
 
## Certifications
 
**ISC2 Certified in Cybersecurity (CC)**
 
Entry-level cybersecurity certification from ISC2 that demonstrates foundational knowledge in security principles, network security, access control, and risk management.
 
Skills Covered:
- Security Principles and Concepts
- Network Security Fundamentals
- Access Control Concepts
- Security Operations
- Risk Management
Issuing Organization: ISC2
 
---
 
## Projects
 
Below are selected projects demonstrating my skills in systems programming and software development.
 
---
 
### TCP Port Scanner (C++, macOS/Linux)
 
A fast multithreaded TCP connect port scanner built from scratch in C++. Developed as a cybersecurity portfolio project to understand how network reconnaissance tools work at the socket level — and how defenders can detect and respond to them.
 
**GitHub Repository:**
[View Project Code](https://github.com/Mahamed88/port-scanner)
 
**Verbose scan — banner grabbing on open ports:**
![Verbose scan](https://raw.githubusercontent.com/Mahamed88/port-scanner/main/Demo-screenshots/demo3.png)
 
**Basic scan — filtered ports with service detection:**
![Basic scan](https://raw.githubusercontent.com/Mahamed88/port-scanner/main/Demo-screenshots/demo6.png)
 
**Features:**
* Concurrent scanning via a custom thread pool — scans 1024 ports in under 1 second
* Service detection using the OS `/etc/services` database — no hardcoding, reads directly from the system
* Banner grabbing in verbose mode (`-v`) — identifies software name and version on open ports
* Nmap-inspired `--top-ports N` — scans the N most commonly open ports in the real world, same frequency ordering Nmap uses
* JSON output (`--json`) — machine-readable output that can be piped into a SIEM, parsed by a script, or fed into other security tools
* Save output to file (`-oN output.txt`) — same flag convention as Nmap for saving scan results
* Three port states — OPEN, CLOSED, FILTERED — with color coded terminal output
* Configurable thread count (`-t`) — tune concurrency for your network
**Technologies Used:**
* C++ (C++17)
* POSIX Sockets
* pthreads
* Makefile
**Key Concepts:**
* TCP three-way handshake and socket programming
* Non-blocking I/O with `select()` and timeout handling
* Custom thread pool implementation with mutex and condition variables
* Network protocol parsing and service fingerprinting
**What I Learned:**
* How port scanners work at the byte level — SYN, RST, and timeout behavior
* Why threading matters — sequential scanning at 2s timeout takes 34 minutes, threaded takes under 1 second
* How offensive tools inform defensive thinking — built the scanner then used it to understand what detection rules would catch it
---
 
### Active Directory Attack & Defense Homelab (Proxmox, Kali, Wazuh SIEM)
 
A fully virtualized enterprise network built on Proxmox to practice offensive security and detection engineering end-to-end. I stood up a Windows domain, attacked it as a penetration tester, and monitored the attack in a SIEM as a SOC analyst — mapping every technique to MITRE ATT&CK.
 
**GitHub Repository:**
[View Project Code](https://github.com/Mahamed88/AD-Lab)
 
**Domain enumeration — netexec pulling all domain users from the DC:**
![Domain Enumeration](https://raw.githubusercontent.com/Mahamed88/AD-Lab/main/screenshots/domain-enumeration.png)
 
**Kerberoasting — extracting a crackable TGS hash for the svc-sql service account:**
![Kerberoasting](https://raw.githubusercontent.com/Mahamed88/AD-Lab/main/screenshots/kerberoasting.png)
 
**Lateral movement — Evil-WinRM shell confirming domain admin access:**
![Lateral Movement](https://raw.githubusercontent.com/Mahamed88/AD-Lab/main/screenshots/evil-winrm.png)
 
**Wazuh detection — 1,690 alerts generated and mapped to MITRE ATT&CK:**
![Wazuh Dashboard](https://raw.githubusercontent.com/Mahamed88/AD-Lab/main/screenshots/wazuh-dashboard.png)
 
**Attack Chain:**
Kali (attacker) → recon on WS01 (low-privilege helpdesk account) → lateral movement to WS02 (cached IT admin credentials) → full domain compromise on DC01
 
**Offensive Techniques:**
* Network and service reconnaissance with nmap
* Domain enumeration with netexec (users, groups, SPNs)
* Kerberoasting against a service account using impacket, cracked offline with John the Ripper
* Lateral movement via Evil-WinRM using harvested credentials
* Full domain credential dump with impacket-secretsdump, including the krbtgt hash
**Detection Engineering:**
* Deployed Wazuh 4.7 as a SIEM with agents on every domain-joined host
* Correlated 1,690 security alerts against the live attack chain
* Mapped detections to MITRE ATT&CK: Valid Accounts (T1078), Kerberoasting (T1558.003), Pass the Hash (T1550.002), Lateral Movement (T1021), Credential Dumping (T1003), Privilege Escalation (T1068)
* Analyzed authentication success/failure patterns (761 successes, 31 failures) to distinguish attacker activity from normal traffic
**Supporting IT Administration:**
* Built the Windows Server 2022 domain (`corp.local`) attackers would target — OUs, GPOs, service accounts, SPNs
* Intentionally misconfigured a GPO (unrestricted PowerShell execution) to model a real-world weak baseline
**Technologies Used:**
* Proxmox VE, Windows Server 2022, Windows 11, Kali Linux, Ubuntu Server
* Wazuh, nmap, netexec, impacket, Evil-WinRM, John the Ripper
**What I Learned:**
* How a full attack chain looks from initial recon to domain compromise, not just isolated exploits
* How Kerberoasting and credential dumping actually work against real AD infrastructure
* How to tune a SIEM to catch specific attacker behaviors and map raw alerts to a recognized threat framework
* Why weak GPOs and credential hygiene matter — I built the misconfiguration, then exploited it, then watched it get flagged
---
 
### Prac-Shell (C, Linux/macOS)
 
A Unix-like shell written in C that supports command execution, built-in commands, pipelines, I/O redirection, signal handling, and both interactive and batch execution modes. This project demonstrates my understanding of systems programming concepts, POSIX process management, and shell architecture.
 
**GitHub Repository:**
[View Project Code](https://github.com/Mahamed88/Prac-shell)
 
**PATH management and shell environment handling:**
![PATH Management Demo](https://raw.githubusercontent.com/Mahamed88/Prac-shell/main/prac-screenshots/path-management.png)
 
**Input and output redirection demonstration:**
![Redirection Demo](https://raw.githubusercontent.com/Mahamed88/Prac-shell/main/prac-screenshots/redirection-demo.png)
 
**Alias support and command history tracking:**
![Alias and History Demo](https://raw.githubusercontent.com/Mahamed88/Prac-shell/main/prac-screenshots/history-alias-demo.png)
 
**Features:**
* Interactive shell mode
* Batch file execution mode
* Built-in commands (`cd`, `exit`, `path`, `alias`, `myhistory`)
* Multiple commands separated with semicolons (`;`)
* Input and output redirection (`<`, `>`)
* Command pipelines (`|`)
* PATH environment variable management
* Signal handling for `Ctrl-C` and `Ctrl-Z`
* Command history tracking
* Alias creation and execution
**Technologies Used:**
* C Programming
* POSIX System Calls
* Linux/macOS Terminal Environment
* GCC Compiler
* Makefile
**Key Concepts:**
* Process creation using `fork()`
* Program execution using `execvp()`
* Inter-process communication with `pipe()`
* File descriptor manipulation using `dup2()`
* Signal handling with `signal()`
* Shell parsing and command execution
* UNIX process synchronization with `waitpid()`
**What I Learned:**
* How Unix shells execute and manage processes internally
* Implementing pipelines and I/O redirection at the file descriptor level
* Managing PATH variables and built-in shell commands
* Designing modular systems-level software across multiple C source files
* Defensive programming and robust shell error handling
---
 
### Bitwise Operations Tool (C, Linux)
 
A command-line application written in C that performs low-level bitwise operations on 32-bit integers. This project demonstrates my understanding of systems programming, binary data manipulation, and modular software design.
 
**GitHub Repository:**
[View Project Code](https://github.com/Mahamed88/c-bitwise-tool.git)
 
**Features:**
* Count Leading Zeroes (CLZ)
* Endian Byte Swapping
* Rotate Right (bit rotation)
* Parity Calculation (even/odd number of bits)
**Technologies Used:**
* C Programming
* GCC Compiler
* Linux
* Makefile
**Key Concepts:**
* Bitwise operators (`&`, `|`, `^`, `<<`, `>>`)
* Endianness and memory representation
* Multi-file program structure
* Input validation and error handling
**What I Learned:**
* How data is represented and manipulated at the bit level
* Writing efficient bitwise algorithms
* Organizing large C programs across multiple files
* Using Makefiles for compiling projects
---
 
## Contact
 
**GitHub Profile**
[github.com/Mahamed88](https://github.com/Mahamed88)
 
**LinkedIn Profile**
[linkedin.com/in/mahamed-abdullahi-6b653523a](https://www.linkedin.com/in/mahamed-abdullahi-6b653523a/)
 
**Email**
Mahamed518279@gmail.com
