# Rencana Pembelajaran Semester (RPS) Praktikum:

# Cyber Security

| **Mata Pembelajaran** | Cyber Security |
|----------------------|----------------|
| **Kode** | CYB-P01C |
| **Fokus** | Pengembangan Keterampilan Keamanan Siber Menggunakan Kali Linux, Virtual Machine, dan Tools Penetration Testing |
| **Prasyarat** | Pemahaman dasar jaringan komputer dan sistem operasi Linux (direkomendasikan) |

**Deskripsi Mata Pembelajaran:**

Praktikum ini memberikan keterampilan praktis dalam keamanan siber mulai dari tingkat dasar hingga mahir. Mahasiswa akan mempelajari cara mengidentifikasi, menganalisis, dan mengatasi berbagai ancaman keamanan menggunakan Kali Linux sebagai platform utama dalam lingkungan virtual machine. Pembelajaran mencakup konsep fundamental keamanan informasi, teknik reconnaissance, vulnerability assessment, exploitation, post-exploitation, hingga defensive security. Mahasiswa akan menggunakan tools industri standar seperti Nmap, Metasploit, Burp Suite, Wireshark, dan berbagai tools spesialisasi lainnya dalam environment yang aman dan terkontrol.

**Capaian Pembelajaran / Course Learning Outcomes (CLO):**

Setelah menyelesaikan praktikum ini, Anda diharapkan mampu:

- **CLO 1:** Menyiapkan dan mengkonfigurasi lingkungan penetration testing menggunakan Virtual Machine dengan Kali Linux dan memahami fundamental keamanan siber.

- **CLO 2:** Melakukan information gathering dan reconnaissance menggunakan berbagai teknik OSINT dan network scanning untuk mengidentifikasi target dan vulnerability.

- **CLO 3:** Menganalisis dan mengeksploitasi kerentanan sistem menggunakan tools seperti Metasploit, SQLMap, dan exploitation frameworks lainnya secara etis.

- **CLO 4:** Melakukan web application security testing, wireless security assessment, dan social engineering dengan metodologi yang terstruktur.

- **CLO 5:** Mengimplementasikan defensive security measures, incident response, dan mampu membuat laporan penetration testing profesional.

**Rencana Pembelajaran Mingguan**

**Fokus: Kali Linux, Virtual Machine, dan Penetration Testing Tools**

| Mg Ke- | Sub-CPMK (Kemampuan Akhir yang Direncanakan) | Bahan Kajian (Materi Pembelajaran) | Bentuk & Metode Pembelajaran | Estimasi Waktu | Pengalaman Belajar Mahasiswa | Kriteria & Bentuk Penilaian (Indikator) | Bobot Penilaian (%) |
|--------|----------------------------------------------|-------------------------------------|------------------------------|----------------|------------------------------|----------------------------------------|-------------------|
| **1** | Mampu menyiapkan lingkungan penetration testing dengan Virtual Machine dan Kali Linux. | Pengenalan Cyber Security, Konsep CIA Triad, Instalasi VirtualBox/VMware, Download dan Setup Kali Linux VM, Navigasi Dasar Linux Terminal. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Instalasi VirtualBox/VMware, import Kali Linux VM, konfigurasi network (NAT/Bridged), eksplorasi interface Kali Linux dan basic terminal commands. | Kriteria: Berhasil instalasi dan booting Kali Linux. Bentuk: Checklist instalasi dan screenshot. | 2% |
| **2** | Mampu menggunakan Linux command line dan melakukan basic system administration. | Linux Command Line Essentials (ls, cd, pwd, cat, grep, find), File Permissions, User Management, Package Management (apt), Basic Shell Scripting. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Praktik navigasi filesystem, manipulasi file, mengubah permissions, membuat user baru, install/update package, membuat bash script sederhana. | Kriteria: Menyelesaikan command line challenges. Bentuk: Laporan Praktikum (Command History & Screenshot). | 2% |
| **3** | Mampu memahami fundamental networking dan TCP/IP protocol. | OSI Model & TCP/IP Stack, IP Addressing & Subnetting, Common Ports & Protocols (HTTP, HTTPS, FTP, SSH, DNS), Wireshark Basics untuk packet analysis. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Menggunakan Wireshark untuk capture dan analyze traffic, identifikasi protocols, membaca packet headers, melakukan ping/traceroute analysis. | Kriteria: Mampu membaca dan menginterpretasi packet capture. Bentuk: Laporan Praktikum (Wireshark Analysis). | 3% |
| **4** | Mampu melakukan passive dan active reconnaissance. | Information Gathering Methodology, OSINT Techniques (Google Dorking, Shodan, theHarvester), DNS Enumeration (dig, nslookup, dnsenum), WHOIS Lookup, Social Media Intelligence. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Melakukan OSINT pada target dummy, menggunakan Google Dorks, theHarvester untuk email gathering, DNS enumeration, dokumentasi findings. | Kriteria: Mengumpulkan informasi target secara komprehensif. Bentuk: Reconnaissance Report. | 3% |
| **5** | Mampu melakukan network scanning dan enumeration. | Network Scanning dengan Nmap (port scanning, service detection, OS fingerprinting), Nmap Scripting Engine (NSE), Network Enumeration dengan NetBIOS, SMB, SNMP. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Scanning target network dengan berbagai teknik Nmap, menggunakan NSE scripts, enumeration services, membuat network map. | Kriteria: Mengidentifikasi open ports dan services. Bentuk: Laporan Praktikum (Nmap Scan Results). | 3% |
| **6** | Mampu melakukan vulnerability assessment dan analysis. | Vulnerability Assessment Concepts, OpenVAS/Nessus Setup & Usage, Vulnerability Scoring (CVSS), Common Vulnerabilities (CVE Database), Manual Vulnerability Verification. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Setup OpenVAS, melakukan vulnerability scan pada target, analisis hasil scan, prioritize vulnerabilities berdasarkan severity, verifikasi false positive. | Kriteria: Menghasilkan vulnerability assessment report. Bentuk: Laporan Praktikum (Vulnerability Report). | 4% |
| **7** | Mampu mengeksploitasi vulnerabilities menggunakan Metasploit Framework. | Metasploit Framework Architecture, Exploit Development Basics, Meterpreter Sessions, Payload Generation dengan msfvenom, Post-Exploitation dengan Meterpreter. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Menggunakan Metasploit untuk exploit vulnerable services (misal: vsftpd, tomcat), generate payloads, establish meterpreter session, basic post-exploitation. | Kriteria: Berhasil mendapatkan shell access. Bentuk: Laporan Praktikum (Exploitation Log). | 4% |
| **8** | Mampu melakukan post-exploitation dan maintaining access. | Post-Exploitation Techniques, Pivoting & Lateral Movement, Persistence Mechanisms (Backdoors, Scheduled Tasks), Data Exfiltration, Covering Tracks (Log Cleaning), Living Off The Land (LOLBins). | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Melakukan post-exploitation pada compromised system, pivot ke internal network, establish persistence, extract sensitive data, clean logs untuk avoid detection. | Kriteria: Berhasil maintain access dan pivot. Bentuk: Laporan Praktikum (Post-Exploitation Report). | 4% |
| **9** | Mampu melakukan password cracking dan privilege escalation. | Password Attack Techniques (Dictionary, Brute Force, Rainbow Tables), John the Ripper & Hashcat, Linux Privilege Escalation (SUID, sudo misconfig, kernel exploits), Windows Privilege Escalation Basics. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Cracking password hashes dengan John/Hashcat, identifikasi privilege escalation vectors, eksploitasi misconfiguration untuk root/SYSTEM access. | Kriteria: Berhasil escalate privileges. Bentuk: Laporan Praktikum (Privilege Escalation Path). | 4% |
| **10** | Mampu melakukan web application security testing. | OWASP Top 10, SQL Injection (SQLMap), Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), Burp Suite Professional Tools, Directory Traversal, File Upload Vulnerabilities. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Testing vulnerable web apps (misal: DVWA, bWAPP), melakukan SQL injection dengan SQLMap, manual XSS testing, menggunakan Burp Suite untuk intercept dan modify requests. | Kriteria: Mengidentifikasi dan exploit web vulnerabilities. Bentuk: Web Application Assessment Report. | 4% |
| **11** | Mampu melakukan wireless security assessment. | Wireless Security Protocols (WEP, WPA, WPA2, WPA3), Monitor Mode & Packet Injection, Aircrack-ng Suite, Handshake Capture & Cracking, Evil Twin & Rogue AP Attacks, Wireless Deauthentication Attacks. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Setup wireless adapter dalam monitor mode, capture WPA/WPA2 handshake dengan airodump-ng, cracking dengan aircrack-ng, membuat rogue access point. | Kriteria: Berhasil capture dan crack wireless password. Bentuk: Laporan Praktikum (Wireless Assessment). | 4% |
| **12** | Mampu melakukan social engineering dan phishing campaigns. | Social Engineering Principles, Phishing Email Creation, Social Engineering Toolkit (SET), Credential Harvesting, USB Drop Attacks, Pretexting & Baiting Techniques, Awareness dan Defense. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Membuat phishing campaign dengan SET, credential harvesting page, membuat malicious payload untuk USB attacks, awareness training simulation. | Kriteria: Memahami social engineering vectors dan countermeasures. Bentuk: Social Engineering Campaign Report. | 4% |
| **13** | Mampu mengimplementasikan defensive security dan incident response. | Defensive Security Concepts, Firewall Configuration (iptables), Intrusion Detection Systems (Snort), Log Analysis, Incident Response Methodology, Digital Forensics Basics, Malware Analysis Introduction. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Konfigurasi iptables firewall rules, setup Snort IDS, analisis log files untuk detect intrusions, basic incident response scenarios, memory forensics dengan Volatility. | Kriteria: Mampu detect dan respond terhadap security incidents. Bentuk: Incident Response Report. | 4% |
| **14** | Mampu membuat professional penetration testing report dan remediation recommendations. | Penetration Testing Methodology (PTES, OSSTMM), Professional Report Writing, Executive Summary Creation, Technical Findings Documentation, Remediation Recommendations, Best Practices Compliance. | **Bentuk:** Praktikum **Metode:** Studi Kasus, Praktik Berkelompok | 100' | Review penetration testing methodology, membuat report template, dokumentasi findings dengan severity scoring, membuat remediation recommendations, peer review reports. | Kriteria: Report yang profesional dan actionable. Bentuk: Draft Final Project Report. | 4% |
| **15** | Mampu mendemonstrasikan dan mempresentasikan hasil proyek akhir penetration testing. | Demo & Presentasi Proyek Akhir | **Bentuk:** Proyek **Metode:** Presentasi Kelompok | 100' | Setiap kelompok mendemonstrasikan complete penetration testing yang dilakukan pada target environment, menjelaskan metodologi, findings, dan remediation recommendations. | Kriteria: Metodologi yang benar, dokumentasi lengkap, presentasi profesional. Bentuk: Presentasi & Demo Live. | **20%** |
| **16** | (UAS) Mampu menyajikan dokumentasi penetration testing secara komprehensif dan profesional. | Pengumpulan Final Report | **Bentuk:** Proyek **Metode:** Submission Individual/Kelompok | - | Mahasiswa menyelesaikan dan mengumpulkan comprehensive penetration testing report yang mencakup executive summary, methodology, detailed findings, evidence (screenshots/logs), dan remediation plan. | Kriteria: Kelengkapan, kualitas teknis, dan profesionalisme report. Bentuk: Final Penetration Testing Report. | **20%** |

## Referensi Praktikum

Berikut adalah buku dan resource yang relevan untuk mendukung praktikum ini:

1. **The Web Application Hacker's Handbook: Finding and Exploiting Security Flaws** - Dafydd Stuttard & Marcus Pinto
   - Referensi utama untuk web application security testing (Pertemuan 10).

2. **Metasploit: The Penetration Tester's Guide** - David Kennedy et al.
   - Panduan lengkap Metasploit Framework (Pertemuan 7).

3. **Kali Linux Revealed: Mastering the Penetration Testing Distribution** - Raphaël Hertzog et al.
   - Official Kali Linux documentation dan best practices (Pertemuan 1-16).

4. **The Hacker Playbook 3: Practical Guide To Penetration Testing** - Peter Kim
   - Metodologi praktis penetration testing end-to-end (Pertemuan 8-16).

5. **OWASP Testing Guide** (https://owasp.org/www-project-web-security-testing-guide/)
   - Framework standar untuk web application security testing (Pertemuan 10).

6. **NIST Cybersecurity Framework** (https://www.nist.gov/cyberframework)
   - Framework untuk defensive security dan incident response (Pertemuan 13).

7. **Offensive Security Training Materials** (https://www.offensive-security.com/)
   - Resource dari creator Kali Linux untuk advanced techniques.

## Catatan Penting Etika dan Legalitas

**PENTING:** Semua praktikum harus dilakukan dalam lingkungan yang legal dan terkontrol:

- Gunakan HANYA vulnerable machines yang disediakan (Metasploitable, DVWA, Vulnhub VMs)
- TIDAK DIPERBOLEHKAN melakukan testing pada sistem tanpa izin tertulis
- Pahami dan patuhi Computer Fraud and Abuse Act dan regulasi lokal
- Praktik hanya untuk tujuan pembelajaran dan defensive security
- Tandatangani ethical hacking agreement sebelum memulai praktikum

**Target Praktikum Legal:**
- Metasploitable 2/3
- DVWA (Damn Vulnerable Web Application)
- bWAPP (Buggy Web Application)
- HackTheBox (dengan akun student)
- TryHackMe (learning platform)
- Vulnhub VMs

RPS ini dirancang untuk memberikan pembelajaran cyber security yang komprehensif, etis, dan praktis dengan progression dari basic hingga advanced topics.