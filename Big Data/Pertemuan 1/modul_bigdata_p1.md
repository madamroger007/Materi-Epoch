# Modul Praktikum 1

# Setup Environment Big Data dengan Virtual Machine dan Ubuntu Linux

| | |
|------------------|------------------------------------------------------|
| **Topik** | Instalasi dan Konfigurasi Virtual Machine dengan Ubuntu Linux untuk Environment Big Data |
| **Mata Kuliah** | Praktikum Pengantar Big Data |
| **Estimasi Waktu** | 120 Menit |

---

## A. Capaian Pembelajaran (Sub-CPMK)

Setelah menyelesaikan modul praktikum ini, mahasiswa diharapkan mampu:

1. Menjelaskan pentingnya penggunaan Virtual Machine untuk environment Big Data.
2. Menginstal dan mengonfigurasi VirtualBox di Windows.
3. Membuat Virtual Machine baru dengan spesifikasi yang sesuai untuk Big Data tools.
4. Menginstal Ubuntu 22.04/24.04 LTS Desktop di Virtual Machine.
5. Melakukan konfigurasi dasar sistem Ubuntu (update, network, user permissions).
6. Memverifikasi bahwa environment siap digunakan untuk instalasi Big Data tools.

---

## B. Alat dan Bahan

- **Laptop/PC** dengan spesifikasi minimum:
  - Processor: Intel Core i5/AMD Ryzen 5 atau lebih tinggi
  - RAM: Minimum 8 GB (Recommended 16 GB)
  - Storage: Minimum 50 GB free space (SSD recommended)
  - OS: Windows 10/11 64-bit
- **Software yang dibutuhkan**:
  - VirtualBox 7.x (akan diunduh)
  - Ubuntu 22.04 LTS atau 24.04 LTS ISO file (akan diunduh)
- **Koneksi internet** yang stabil untuk download ISO dan update sistem

---

## C. Dasar Teori

### Konsep Virtual Machine (VM)

Virtual Machine adalah emulasi sistem komputer yang berjalan di atas sistem operasi host. VM memungkinkan kita menjalankan sistem operasi guest (Ubuntu) di dalam sistem operasi host (Windows) tanpa perlu dual boot atau instalasi langsung ke hardware.

**Keuntungan menggunakan VM untuk Big Data:**
- **Isolasi**: Environment Big Data terpisah dari sistem host
- **Portability**: VM dapat di-backup dan dipindahkan ke komputer lain
- **Snapshot**: Dapat membuat checkpoint sebelum instalasi/konfigurasi baru
- **Resource Management**: Dapat mengatur alokasi RAM, CPU, dan storage sesuai kebutuhan

### VirtualBox

VirtualBox adalah software virtualisasi open-source yang dikembangkan oleh Oracle. VirtualBox mendukung berbagai sistem operasi guest termasuk Linux, Windows, dan macOS.

**Komponen utama VirtualBox:**
- **Virtual Machine Manager**: Interface untuk mengelola VM
- **Virtual Hard Disk (VDI)**: File yang menyimpan data sistem guest
- **Network Adapter**: Mengatur koneksi jaringan VM (NAT, Bridge, Host-only)
- **Guest Additions**: Driver tambahan untuk meningkatkan performa dan integrasi

### Ubuntu Linux untuk Big Data

Ubuntu adalah distribusi Linux berbasis Debian yang paling populer untuk server dan development. Ubuntu LTS (Long Term Support) mendapat dukungan update selama 5 tahun.

**Mengapa Ubuntu untuk Big Data?**
- **Industry Standard**: Mayoritas perusahaan menggunakan Ubuntu untuk Big Data infrastructure
- **Package Management**: APT (Advanced Package Tool) memudahkan instalasi software
- **Documentation**: Tutorial dan troubleshooting Hadoop/Spark kebanyakan menggunakan Ubuntu
- **Compatibility**: Semua Big Data tools (Hadoop, Spark, Kafka, Hive) fully supported di Ubuntu

### Struktur Environment Big Data

```
Windows 10/11 (Host OS)
    └── VirtualBox
        └── Ubuntu 22.04/24.04 LTS (Guest OS)
            ├── Java JDK (prerequisite)
            ├── Apache Hadoop
            ├── Apache Spark
            ├── Apache Hive
            ├── Apache Kafka
            └── Python & Jupyter Notebook
```

---

## D. Langkah-Langkah Praktikum

### Tugas 1: Download dan Instalasi VirtualBox

#### Langkah 1.1: Download VirtualBox

1. Buka browser dan akses website resmi VirtualBox: **https://www.virtualbox.org**
2. Klik menu **Downloads**
3. Pilih **Windows hosts** untuk download VirtualBox installer
4. Tunggu hingga file installer (sekitar 100-150 MB) selesai diunduh
5. File yang diunduh: `VirtualBox-7.x.x-xxxxxx-Win.exe`

#### Langkah 1.2: Instalasi VirtualBox di Windows

1. Double-click file installer VirtualBox yang telah diunduh
2. Klik **Next** pada welcome screen
3. Pada **Custom Setup**, biarkan default (install semua komponen), klik **Next**
4. Pada **Warning: Network Interfaces**, klik **Yes** (koneksi internet akan terputus sementara)
5. Klik **Install** untuk memulai instalasi
6. Jika muncul prompt instalasi driver, klik **Install** dan pilih **Trust Oracle Corporation**
7. Setelah selesai, centang **Start Oracle VM VirtualBox after installation**
8. Klik **Finish**

#### Langkah 1.3: Verifikasi Instalasi VirtualBox

1. VirtualBox Manager akan terbuka otomatis
2. Pastikan tampilan menunjukkan interface VirtualBox dengan menu: File, Machine, Tools
3. Periksa versi VirtualBox di menu **Help → About VirtualBox**
4. Screenshot tampilan VirtualBox Manager sebagai dokumentasi

**Expected Output:**
```
VirtualBox Manager window dengan toolbar dan empty VM list
Version: 7.x.x (or latest)
```

---

### Tugas 2: Download Ubuntu ISO

#### Langkah 2.1: Download Ubuntu LTS

1. Buka browser dan akses: **https://ubuntu.com/download/desktop**
2. Pilih versi **Ubuntu 22.04.x LTS** atau **Ubuntu 24.04.x LTS**
   - **Rekomendasi**: Gunakan Ubuntu 22.04 LTS (lebih stable)
3. Klik tombol **Download** untuk Ubuntu Desktop
4. Tunggu hingga ISO file (sekitar 4-5 GB) selesai diunduh
5. File yang diunduh: `ubuntu-22.04.x-desktop-amd64.iso` atau `ubuntu-24.04.x-desktop-amd64.iso`
6. Simpan di lokasi yang mudah diakses (misalnya: `C:\Users\[Username]\Downloads\`)

**Catatan:** Proses download membutuhkan waktu tergantung kecepatan internet (15-60 menit untuk koneksi 10-50 Mbps).

---

### Tugas 3: Membuat Virtual Machine Baru

#### Langkah 3.1: Inisialisasi VM Baru

1. Buka **VirtualBox Manager**
2. Klik tombol **New** (ikon monitor biru dengan bintang) atau menu **Machine → New**
3. Pada wizard **Create Virtual Machine**:

   **Name and Operating System:**
   - **Name**: `BigData-Ubuntu` (atau nama sesuai preferensi)
   - **Folder**: Biarkan default atau pilih lokasi dengan space cukup
   - **ISO Image**: Klik dropdown, pilih **Other**, browse ke lokasi Ubuntu ISO yang telah diunduh
   - **Type**: Linux
   - **Version**: Ubuntu (64-bit)
   - Centang **Skip Unattended Installation** (agar kita install manual)
   - Klik **Next**

#### Langkah 3.2: Konfigurasi Hardware

**Memory (RAM):**
- Atur slider ke **4096 MB (4 GB)** minimum
- **Rekomendasi**: 6144 MB (6 GB) atau 8192 MB (8 GB) jika RAM host 16 GB
- Jangan alokasikan lebih dari 50% total RAM host
- Klik **Next**

**Processors:**
- Atur **CPU cores** ke **2** minimum
- **Rekomendasi**: 4 cores jika host memiliki 6+ cores
- Klik **Next**

#### Langkah 3.3: Konfigurasi Virtual Hard Disk

**Create Virtual Hard Disk:**
- Pilih **Create a Virtual Hard Disk Now**
- **Disk Size**: Atur ke **40 GB** minimum
  - **Rekomendasi**: 50 GB untuk space yang cukup
- **Hard Disk File Type**: Pilih **VDI (VirtualBox Disk Image)**
- **Storage on Physical Hard Disk**: Pilih **Dynamically allocated**
  - Dynamically allocated = file VDI akan membesar sesuai penggunaan (lebih efisien)
- Klik **Next**

#### Langkah 3.4: Summary dan Finish

1. Review konfigurasi VM:
   - Name: BigData-Ubuntu
   - RAM: 4-8 GB
   - CPU: 2-4 cores
   - Storage: 40-50 GB
2. Klik **Finish** untuk membuat VM

**Expected Output:**
```
VM "BigData-Ubuntu" muncul di VirtualBox Manager dengan status "Powered Off"
```

---

### Tugas 4: Konfigurasi Advanced VM Settings

#### Langkah 4.1: Network Configuration

1. Pilih VM **BigData-Ubuntu** di VirtualBox Manager
2. Klik **Settings** (ikon gear) atau klik kanan → Settings
3. Buka tab **Network**
4. Pastikan **Adapter 1** enabled dengan pengaturan:
   - **Attached to**: NAT (default)
   - NAT memungkinkan VM akses internet melalui host
5. **(Optional)** Untuk akses VM dari host, enable **Adapter 2**:
   - Centang **Enable Network Adapter**
   - **Attached to**: Host-only Adapter
6. Klik **OK**

#### Langkah 4.2: Display Configuration

1. Di **Settings**, buka tab **Display**
2. **Screen**:
   - **Video Memory**: Atur ke **128 MB**
   - **Graphics Controller**: VMSVGA (default)
3. Klik **OK**

#### Langkah 4.3: System Configuration (Optional Optimization)

1. Di **Settings**, buka tab **System**
2. Tab **Motherboard**:
   - **Boot Order**: Pastikan Hard Disk di urutan pertama (setelah instalasi)
   - Uncheck **Floppy**
   - **Chipset**: ICH9
3. Tab **Processor**:
   - **Enable PAE/NX**: Centang (jika tersedia)
4. Tab **Acceleration**:
   - **Paravirtualization Interface**: Default atau KVM
   - **Hardware Virtualization**: Centang Enable VT-x/AMD-V
5. Klik **OK**

---

### Tugas 5: Instalasi Ubuntu di Virtual Machine

#### Langkah 5.1: Boot VM dari ISO

1. Pilih VM **BigData-Ubuntu** di VirtualBox Manager
2. Klik **Start** (panah hijau) atau double-click VM
3. VM akan boot dari Ubuntu ISO
4. Tunggu hingga muncul **GNU GRUB menu**
5. Pilih **Try or Install Ubuntu** (tekan Enter)
6. Tunggu Ubuntu live environment loading (2-5 menit)

#### Langkah 5.2: Mulai Instalasi

1. Setelah desktop Ubuntu muncul, double-click icon **Install Ubuntu 24.04 LTS** (atau versi sesuai ISO)
2. Pada **Welcome screen**:
   - **Language**: Pilih **English** atau **Bahasa Indonesia**
   - Klik **Continue**

#### Langkah 5.3: Keyboard Layout

1. **Keyboard layout**: Pilih **English (US)** (recommended) atau sesuai preferensi
2. Klik **Continue**

#### Langkah 5.4: Updates and Other Software

1. **What apps would you like to install?**
   - Pilih **Normal installation** (include web browser, utilities, office software, games, media players)
2. **Other options**:
   - Centang **Download updates while installing Ubuntu**
   - Centang **Install third-party software for graphics and Wi-Fi hardware**
3. Klik **Continue**

#### Langkah 5.5: Installation Type

1. **Installation type**:
   - Pilih **Erase disk and install Ubuntu** (jangan khawatir, ini hanya virtual disk)
   - VM menggunakan virtual hard disk terpisah dari host Windows
2. Klik **Install Now**
3. Muncul dialog **Write changes to disks?**, klik **Continue**

#### Langkah 5.6: Time Zone

1. **Where are you?**
   - Map akan auto-detect atau manual select
   - Pilih **Jakarta** atau timezone Indonesia lainnya
2. Klik **Continue**

#### Langkah 5.7: User Account Setup

1. **Who are you?**
   - **Your name**: Masukkan nama lengkap (misal: `Student BigData`)
   - **Your computer's name**: `bigdata-vm` (hostname)
   - **Pick a username**: `bigdata` (username untuk login)
   - **Choose a password**: Buat password yang mudah diingat (misal: `bigdata123`)
   - **Confirm password**: Ketik ulang password
   - Pilih **Log in automatically** (untuk kemudahan, karena ini VM lokal)
2. Klik **Continue**

#### Langkah 5.8: Proses Instalasi

1. Instalasi Ubuntu dimulai (sekitar 10-20 menit tergantung performa PC)
2. Progress ditampilkan dengan slideshow fitur Ubuntu
3. **Jangan tutup VM atau restart selama proses instalasi!**
4. Setelah selesai, muncul dialog **Installation Complete**
5. Klik **Restart Now**

#### Langkah 5.9: Post-Installation Reboot

1. Setelah restart, jika muncul pesan **Please remove the installation medium, then press ENTER**:
   - VirtualBox biasanya auto-remove ISO
   - Tekan **Enter**
2. VM akan reboot dan boot ke Ubuntu yang telah terinstal
3. Login otomatis (jika pilih log in automatically) atau masukkan password

**Expected Output:**
```
Ubuntu desktop dengan wallpaper default
Taskbar di bagian bawah dengan aplikasi favorites
Terminal dan Files icon visible
```

---

### Tugas 6: Konfigurasi Dasar Ubuntu

#### Langkah 6.1: Update Ubuntu System

1. Setelah login ke Ubuntu, tekan `Ctrl + Alt + T` untuk membuka **Terminal**
2. Jalankan perintah update repository:
   ```bash
   sudo apt update
   ```
3. Masukkan password jika diminta
4. Tunggu hingga proses update package list selesai
5. Jalankan perintah upgrade sistem:
   ```bash
   sudo apt upgrade -y
   ```
6. Proses upgrade akan download dan install package updates (5-15 menit)
7. Jika muncul prompt konfigurasi, pilih **Keep current version** atau default
8. Setelah selesai, restart sistem:
   ```bash
   sudo reboot
   ```

**Expected Output Terminal:**
```
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
All packages are up to date.
```

#### Langkah 6.2: Install Guest Additions (Optional but Recommended)

Guest Additions meningkatkan performa VM dan fitur integrasi dengan host.

1. Login kembali ke Ubuntu setelah restart
2. Di VirtualBox menu bar (window VM), klik **Devices → Insert Guest Additions CD image**
3. Ubuntu akan auto-mount CD, muncul notifikasi
4. Buka **Files** (file manager)
5. Klik **VBox_GAs_x.x.x** di sidebar kiri
6. Klik kanan di area kosong, pilih **Open in Terminal**
7. Di terminal, jalankan:
   ```bash
   sudo ./VBoxLinuxAdditions.run
   ```
8. Masukkan password, tunggu instalasi selesai (2-5 menit)
9. Restart VM:
   ```bash
   sudo reboot
   ```

**Keuntungan Guest Additions:**
- Shared clipboard antara host dan guest
- Drag and drop files
- Auto-resize screen resolution
- Shared folders
- Better graphics performance

#### Langkah 6.3: Verifikasi Koneksi Internet

1. Buka Terminal (`Ctrl + Alt + T`)
2. Test koneksi internet dengan ping:
   ```bash
   ping -c 4 google.com
   ```
3. Expected output:
   ```
   PING google.com (xxx.xxx.xxx.xxx) 56(84) bytes of data.
   64 bytes from xxx.xxx.xxx.xxx: icmp_seq=1 ttl=xxx time=xx.x ms
   64 bytes from xxx.xxx.xxx.xxx: icmp_seq=2 ttl=xxx time=xx.x ms
   ...
   4 packets transmitted, 4 received, 0% packet loss
   ```
4. Jika koneksi berhasil, internet siap digunakan

**Troubleshooting jika tidak bisa ping:**
- Pastikan host Windows terhubung internet
- Check VM Network Settings: NAT adapter enabled
- Restart VM networking:
  ```bash
  sudo systemctl restart NetworkManager
  ```

#### Langkah 6.4: Install Build Essential dan Tools Dasar

Install package yang diperlukan untuk kompilasi dan development:

```bash
sudo apt install -y build-essential curl wget git vim nano net-tools
```

**Penjelasan package:**
- `build-essential`: Compiler GCC, make, dan library untuk compile software
- `curl`, `wget`: Download file dari command line
- `git`: Version control system
- `vim`, `nano`: Text editor di terminal
- `net-tools`: Network utilities (ifconfig, netstat, dll)

#### Langkah 6.5: Check System Information

Verifikasi spesifikasi sistem:

1. Check OS version:
   ```bash
   lsb_release -a
   ```
   Expected output:
   ```
   Distributor ID: Ubuntu
   Description:    Ubuntu 22.04.x LTS atau 24.04.x LTS
   Release:        22.04 atau 24.04
   Codename:       jammy atau noble
   ```

2. Check memory (RAM):
   ```bash
   free -h
   ```
   Expected: Total memory sesuai alokasi VM (4-8 GB)

3. Check disk space:
   ```bash
   df -h
   ```
   Expected: Filesystem `/` dengan size sesuai alokasi (40-50 GB)

4. Check CPU:
   ```bash
   lscpu
   ```
   Expected: CPU(s) sesuai alokasi (2-4 cores)

5. Check IP address:
   ```bash
   ip addr show
   ```
   atau
   ```bash
   ifconfig
   ```
   Expected: Interface `enp0s3` atau `eth0` dengan IP address

---

### Tugas 7: Snapshot VM (Backup State)

Membuat snapshot sebagai checkpoint sebelum instalasi Big Data tools.

#### Langkah 7.1: Create Snapshot

1. **Shutdown VM** terlebih dahulu:
   - Di Ubuntu, klik **Power → Power Off**
2. Di VirtualBox Manager, pilih VM **BigData-Ubuntu**
3. Klik menu **Machine → Tools → Snapshots** (atau icon hamburger menu kanan atas)
4. Klik **Take** (icon camera) atau klik kanan → **Take Snapshot**
5. **Snapshot Name**: `Fresh Ubuntu Installation`
6. **Snapshot Description**: `Ubuntu 22.04 LTS with updates and Guest Additions`
7. Klik **OK**

**Keuntungan Snapshot:**
- Bisa restore ke state ini jika terjadi error di langkah berikutnya
- Eksperimen tanpa takut merusak sistem
- Rollback cepat jika instalasi Big Data tools gagal

---

### Tugas 8: Dokumentasi dan Testing Akhir

#### Langkah 8.1: Create Testing Document

Buat file dokumentasi untuk verifikasi instalasi:

1. Start VM **BigData-Ubuntu**
2. Buka Terminal
3. Buat file testing:
   ```bash
   nano ~/system_check.txt
   ```
4. Copy-paste hasil command berikut ke file:
   ```bash
   echo "=== SYSTEM INFORMATION ===" >> ~/system_check.txt
   lsb_release -a >> ~/system_check.txt
   echo "" >> ~/system_check.txt
   echo "=== MEMORY ===" >> ~/system_check.txt
   free -h >> ~/system_check.txt
   echo "" >> ~/system_check.txt
   echo "=== DISK SPACE ===" >> ~/system_check.txt
   df -h >> ~/system_check.txt
   echo "" >> ~/system_check.txt
   echo "=== CPU INFO ===" >> ~/system_check.txt
   lscpu | head -15 >> ~/system_check.txt
   echo "" >> ~/system_check.txt
   echo "=== NETWORK ===" >> ~/system_check.txt
   ip addr show >> ~/system_check.txt
   ```
5. View file:
   ```bash
   cat ~/system_check.txt
   ```

#### Langkah 8.2: Checklist Verifikasi

Pastikan semua indikator berikut terpenuhi:

- [ ] VirtualBox terinstal di Windows dan berjalan normal
- [ ] VM "BigData-Ubuntu" telah dibuat dengan spesifikasi:
  - RAM: 4-8 GB
  - CPU: 2-4 cores
  - Storage: 40-50 GB
  - Network: NAT enabled
- [ ] Ubuntu 22.04/24.04 LTS terinstal di VM
- [ ] Sistem Ubuntu ter-update (`sudo apt update && sudo apt upgrade` berhasil)
- [ ] Guest Additions terinstal (optional)
- [ ] Koneksi internet berfungsi (ping google.com berhasil)
- [ ] Build tools terinstal (gcc, make, curl, wget, git)
- [ ] Snapshot "Fresh Ubuntu Installation" telah dibuat
- [ ] File system_check.txt berisi informasi sistem lengkap

**Jika semua checklist terpenuhi, environment Big Data siap untuk pertemuan berikutnya!**

---

## E. Troubleshooting Common Issues

### Issue 1: VirtualBox Gagal Install di Windows

**Gejala:** Error saat instalasi VirtualBox, message "Installation failed"

**Solusi:**
1. Disable antivirus sementara
2. Run installer as Administrator (klik kanan → Run as administrator)
3. Pastikan Windows Hyper-V disabled:
   - Buka PowerShell as Administrator
   - Jalankan: `bcdedit /set hypervisorlaunchtype off`
   - Restart Windows
4. Install ulang VirtualBox

### Issue 2: VM Tidak Bisa Start / Error "VT-x is not available"

**Gejala:** VM tidak bisa start, muncul error "VT-x/AMD-V hardware acceleration is not available"

**Solusi:**
1. Enable Virtualization di BIOS:
   - Restart PC, masuk BIOS (tekan F2/F10/Del saat boot)
   - Cari menu **Virtualization Technology** atau **Intel VT-x** / **AMD-V**
   - Set ke **Enabled**
   - Save & Exit BIOS
2. Disable Hyper-V di Windows (jika langkah 1 tidak berhasil):
   - Control Panel → Programs → Turn Windows features on or off
   - Uncheck **Hyper-V** dan **Virtual Machine Platform**
   - Restart Windows

### Issue 3: Ubuntu Instalasi Lambat atau Freeze

**Gejala:** Instalasi Ubuntu stuck atau sangat lambat

**Solusi:**
1. Pastikan alokasi RAM cukup (minimum 4 GB)
2. Pastikan host tidak menjalankan aplikasi berat saat instalasi
3. Gunakan SSD untuk storage VirtualBox jika memungkinkan
4. Increase video memory VM ke 128 MB (Settings → Display)
5. Disable 3D acceleration (Settings → Display → uncheck 3D Acceleration)

### Issue 4: Tidak Bisa Koneksi Internet di Ubuntu VM

**Gejala:** Ping google.com failed, "Network is unreachable"

**Solusi:**
1. Check VM Network Settings:
   - Power off VM
   - Settings → Network → Adapter 1
   - Attached to: **NAT**
   - Cable Connected: **Checked**
2. Restart NetworkManager di Ubuntu:
   ```bash
   sudo systemctl restart NetworkManager
   ```
3. Reboot VM:
   ```bash
   sudo reboot
   ```
4. Jika masih gagal, coba switch ke **Bridged Adapter**:
   - Settings → Network → Adapter 1
   - Attached to: **Bridged Adapter**
   - Name: Pilih network adapter host yang aktif

### Issue 5: Screen Resolution Tidak Pas / Tidak Bisa Auto-Resize

**Gejala:** Desktop Ubuntu terpotong atau tidak mengikuti ukuran window VM

**Solusi:**
1. Install Guest Additions (lihat Tugas 6.2)
2. Setelah install Guest Additions, restart VM
3. Menu View → Auto-resize Guest Display
4. Atau manual set resolution:
   - Settings → Displays
   - Resolution: Pilih resolusi yang sesuai
   - Apply

---

## F. Penutup & Preview Pertemuan Berikutnya

Pada akhir praktikum ini, mahasiswa telah berhasil:
- Menginstal VirtualBox di Windows sebagai platform virtualisasi
- Membuat Virtual Machine dengan spesifikasi yang sesuai untuk Big Data
- Menginstal Ubuntu 22.04/24.04 LTS sebagai sistem operasi guest
- Melakukan update sistem dan konfigurasi dasar
- Memverifikasi koneksi internet dan system readiness

**Environment Big Data kini telah siap!** VM Ubuntu yang telah dikonfigurasi akan menjadi foundation untuk instalasi Big Data tools di pertemuan-pertemuan selanjutnya.

**Preview Pertemuan Berikutnya:**
Pertemuan 2 akan membahas **Linux Fundamentals & Java Setup**, termasuk:
- Navigasi dan operasi file melalui command line (cd, ls, mkdir, rm, cp, mv)
- File permissions dan ownership (chmod, chown)
- Text editors (nano, vim)
- Package management dengan APT
- Instalasi dan konfigurasi Java Development Kit (JDK)
- Environment variables (JAVA_HOME, PATH)

**Persiapan untuk Pertemuan 2:**
- Pastikan VM dapat dijalankan dan login berhasil
- Pastikan koneksi internet stabil
- Backup/snapshot VM sudah dibuat
- Familiar dengan Terminal (Ctrl + Alt + T)

---

## G. Sumber Buku Referensi

1. **White, T. (2015). *Hadoop: The Definitive Guide*, 4th Edition. O'Reilly Media.**
   - Chapter 2: MapReduce (foundation concepts)
   - Appendix A: Installing Apache Hadoop

2. **Chambers, B., & Zaharia, M. (2018). *Spark: The Definitive Guide*. O'Reilly Media.**
   - Chapter 1: What is Apache Spark?
   - Chapter 2: A Gentle Introduction to Spark

3. **VirtualBox User Manual (Oracle)**
   - Available at: https://www.virtualbox.org/manual/
   - Chapter 1: First Steps
   - Chapter 3: Configuring Virtual Machines

4. **Ubuntu Server Guide (Canonical)**
   - Available at: https://ubuntu.com/server/docs
   - Installation Guide
   - Package Management

5. **Linux Command Line and Shell Scripting Bible, 4th Edition**
   - Richard Blum & Christine Bresnahan
   - Fundamental Linux commands and system administration

---

## H. Lampiran

### Lampiran A: Spesifikasi Rekomendasi VM

| Komponen | Minimum | Recommended | Optimal |
|----------|---------|-------------|---------|
| **RAM** | 4 GB | 6 GB | 8 GB |
| **CPU Cores** | 2 | 4 | 6 |
| **Storage** | 40 GB | 50 GB | 80 GB |
| **Video Memory** | 64 MB | 128 MB | 128 MB |
| **Network** | NAT | NAT + Host-only | Bridged |

### Lampiran B: Ubuntu Keyboard Shortcuts

| Shortcut | Fungsi |
|----------|--------|
| `Ctrl + Alt + T` | Open Terminal |
| `Ctrl + C` | Cancel/Stop command |
| `Ctrl + D` | Exit Terminal |
| `Ctrl + L` | Clear Terminal screen |
| `Ctrl + R` | Search command history |
| `Ctrl + Alt + F1-F6` | Switch to TTY console |
| `Ctrl + Alt + F7` | Switch back to GUI |
| `Super (Windows key)` | Open Activities (search apps) |

### Lampiran C: Basic Linux Commands Cheat Sheet

```bash
# Navigation
pwd                 # Print working directory
ls                  # List files
ls -la              # List all files with details
cd /path/to/dir     # Change directory
cd ~                # Go to home directory
cd ..               # Go up one directory

# File Operations
mkdir dirname       # Create directory
touch filename      # Create empty file
cp source dest      # Copy file
mv source dest      # Move/rename file
rm filename         # Remove file
rm -rf dirname      # Remove directory recursively

# System Information
uname -a            # System information
df -h               # Disk space usage
free -h             # Memory usage
top                 # Process monitor (press q to quit)
htop                # Better process monitor (if installed)

# Package Management
sudo apt update     # Update package list
sudo apt upgrade    # Upgrade installed packages
sudo apt install pkg # Install package
sudo apt remove pkg  # Remove package
sudo apt search pkg  # Search package

# Network
ping host           # Test connectivity
ifconfig            # Network interfaces (if net-tools installed)
ip addr             # Network interfaces (modern)
curl url            # Download/test URL
wget url            # Download file
```

---

**Selamat! Anda telah menyelesaikan Modul Praktikum 1 - Setup Environment Big Data.**

**Next:** Modul Praktikum 2 - Linux Fundamentals & Java Setup