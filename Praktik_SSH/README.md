Prakti menyambungkan antar dua perangkat yang berbeda.
---

By,Muhammad Azmi

09011282328075

SK3C

Praktikum Sistem Operasi

Untuk praktik kali ini saya akan menghubungkan dua mesin virtual di dua device berbeda(Laptop dan PC) yang menggunakan OS Linux Ubuntu dan Mint. Saya menggunakan metode penyambungan ssh secara kabel(LAN) dan nirkabel(WLAN).
Berikut adalah langkah yang saya lakukan:

1. Menggunakan Kabel LAN

 <div align="center">
  <img src="./Image/G2.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
<div align="center">
  <img src="./Image/G3.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
<div align="center">
  <img src="./Image/G5.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

Pertama-tama saya menyeting jaringan di virtualbox menggunakan Bridge adapter,setelah itu pilih port LAN pada Virtualbox kedua device.

Berikut spek singkat dari Laptop dan PC yang saya gunakan untuk validasi kalau saya menggunakan 2 perangkat berbeda:

Untuk Laptop:

<div align="center">
  <img src="./Image/G10.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

OS: Windows 11 Enterprise LTSC 24h2

OS Virtual: Linux Mint Cinnamon

CPU: i5 3210m 2.5Ghz

Memory: DDR3 8GB 1600mhz Dualchanel

Seri Mobo: k55vm Rev 2.2

Chipset: HM71

LAN: Realtek PCIe GbE Family controller

WiFi Card: Atheros Wifi Card

---
Untuk PC:

<div align="center">
  <img src="./Image/G11.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

OS: Windows 11 Enterprise LTSC 24h2

OS Virtual: Linux Ubuntu 24

CPU: i7 4770k 3.5Ghz

Memory: DDR3 12GB 1333mhz Dualchanel (4.2.4.2)

Seri Mobo: ASRock fatal1ty killer Z87

Chipset: Z87

LAN: Killer E2200 Gigabit Ethernet

WiFi: USB WiFi dogle

---
Setelah LAN sudah terpilih, maka selanjutnya tinggal masuk ke Linux di kedua laptop.

<div align="center">
  <img src="./Image/G1.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
<div align="center">
  <img src="./Image/G4.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

Pada kedua laptop saya menyeting Ip address secara manual,hal ini diperlukan supaya LAN terhubung.

Ip Address Laptop: 192.168.1.3

Ip Address PC: 192.168.1.2

---

Kemudian pasang Openssh dan jalankan ssh dengan command "sudo apt istall openssh-server" "sudo systemctl enable ssh" dan "sudo systemctl start ssh"

---
<div align="center">
  <img src="./Image/G6.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

Disini saya menyambungkan Laptop ke PC saya supaya bisa di kontrol melalui PC saya, untuk menyambungkannya gunakan command "ssh altmimi@192.168.1.3" altmimi = user dan 192.168.1.3 adalah ip address yang sudah saya set di laptop.

Kemudian gunakan "neofetch" untuk melihat informasi perangkat laptop yang sudah di remote.

---
2. Menggunakan WLAN(WiFi)

Sebenarnya metodenya hampir sama,tetapi untuk WLAN tidak perlu set Ip manual lagi, ip sudah automatis dan tinggal di lihat saja menggunakan command "ip addr show".

<div align="center">
  <img src="./Image/G12.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

Dan untuk di atas set ke WiFi card,bukan LAN port lagi.

Di sini saya meremote PC saya menggunakan Laptop(Kebalikan dari sebelumnya).
<div align="center">
  <img src="./Image/G8.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

Saya juga sempat menginstall "neofetch" di Ubuntu melalui remote dari laptop dikarenakan Ubuntu tidak memilikinya secara default seperti yang saya lakukan di bawah ini
<div align="center">
  <img src="./Image/G9.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
---

Mungkin itu saja dari saya, jikalau ada salah ketik dan peng-istilahan mohon maaf.
