layout: default
title: Mahamed Abdullahi | My Portfolio
---
# Mahamed Abdullahi
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
- Assembly mips 
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
ISC2 Certified in Cybersecurity (CC)
Entry-level cybersecurity certification from ISC2 that demonstrates foundational knowledge in security principles, network security, access control, and risk management.
Skills Covered:
Security Principles and Concepts
Network Security Fundamentals
Access Control Concepts
Security Operations
Risk Management
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
![Basic scan](https://raw.githubusercontent.com/Mahamed88/port-scanner/main/Demo-screenshots/demo1.png)

**Features:**
* Concurrent scanning via a custom thread pool — scans 1024 ports in under 1 second
* Service detection using the OS `/etc/services` database
* Banner grabbing in verbose mode — identifies software and version on open ports
* JSON output for piping into other tools or a SIEM
* Top ports mode — scans the most commonly open ports (`--top-ports N`)
* Save output to file with `-oN`

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
