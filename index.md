## Projects

Below are selected projects demonstrating my skills in systems programming and software development.

---

### TCP Port Scanner (C++, macOS/Linux)

A fast multithreaded TCP connect port scanner built from scratch in C++. Developed as a cybersecurity portfolio project to understand how network reconnaissance tools work at the socket level — and how defenders can detect and respond to them.

**GitHub Repository:**
[View Project Code](https://github.com/Mahamed88/port-scanner)

**Verbose scan — banner grabbing on open ports:**

![Verbose scan](Demo-screenshots/demo3.png)

**Basic scan — filtered ports with service detection:**

![Basic scan](Demo-screenshots/demo1.png)

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
