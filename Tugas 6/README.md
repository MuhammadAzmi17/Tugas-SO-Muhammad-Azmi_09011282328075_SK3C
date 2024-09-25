By,Muhammad Azmi

09011282328075

SK3C

Praktikum Sistem Operasi

Tugas ke 6
---
1. Eksekusi seluruh profile yang ada :
   
   a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :

      echo “Profile dari /etc/profile”

   b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :

      /home/stD02001/.bash_profile

      /home/. stD02001/.bash_login

      /home/mahasiswa/.profile

      /home/mahasiswa/.bashrc

      Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap

      file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :

      echo “Profile dari .bash_profile”

      Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.

   c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

      $ su mahasiswa

      $ exit

      kemudian gunakan opsi – sebagai berikut :

      $ su – mahasiswa

      $ exit

      Jelaskan perbedaan kedua utilitas tersebut.

2. Prompt String (PS)
   
   a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell

      PS1=‟> „

      export PS1
  
   b. Eksperimen hasil PS1 :

      $ PS1=“\! > “

      69 > PS1=”\d > “

      Mon Sep 23 > PS1=”\t > “

      10:10:20 > PS1=”Saya=\u > “

      Saya=mahasiswa > PS1=”\w >”

      ~ > PS1=\h >”

3. Logout
   
   Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

   Echo “Terima kasih atas sesi yang diberikan”

   Sleep 5

   clear

4. Bash script
   
   a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

      p1.sh

      #! /bin/bash

      echo “Program p1”

      ls –l

      p2.sh

      #! /bin/bash

      echo “Program p2”

      who

      p3.sh

      #! /bin/bash

      echo “Program p3”

      ps x

   b. Jalankan script tersebut sebagai berikut :

      $ ./p1.sh ; ./p3.sh ; ./p2.sh

      $ ./p1.sh &
 
      $ ./p1.sh $ ./p2.sh & ./p3.sh &

      $ ( ./p1.sh ; ./p3.sh ) &

5. Jobs
    
   a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,

      setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

      #!/bin/bash

      while [ true ]

      do

      date >> hasil

      sleep 10

      done

   b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :

      $ jobs

      $ find / -print > files 2>/dev/null &

      $ jobs

   c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background

      $ fg %1

      $ bg

   d. Stop program background dengan utilitas kil

      $ ps x

      $ kill [Nomor PID]

6. History
   
   a. Ganti nilai HISTSIZE dari 1000 menjadi 20

      $ HISTSIZE=20

      $ h

   b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan

      $ !-5

   c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

      $ !!

   d. Ulangi instruksi pada history bufer nomor 150

      $ !150

   e. Ulangi instruksi dengan prefix “ls”

      $ !ls

Berikut Pemratekannya:
---
1. Pengeksekusian dari a,b, dan c.
   
   - su mahasiswa: Menjalankan shell baru sebagai mahasiswa tanpa menginisialisasi lingkungan penuh pengguna tersebut.
   - su - mahasiswa: Menjalankan shell baru sebagai mahasiswa dengan inisialisasi penuh, seperti login langsung dari awal.
<div align="center">
  <img src="./Gambar/H1.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
#

2. Pengeksekusian a dan b, beserta output.
   
   - Dengan berbagai format prompt PS1, kita dapat menampilkan informasi berbeda di prompt terminal sesuai kebutuhan, seperti nomor perintah, tanggal, waktu, nama pengguna, direktori kerja, dan hostname.
<div align="center">
  <img src="./Gambar/H2.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

#

3. Pengeksekusian dan mengedit .bash_logout.
   
   - setiap kali pengguna melakukan logout dari sesi terminal, pesan "Terima kasih atas sesi yang diberikan" akan muncul, menahan sesi selama 5 detik, lalu layar akan bersih (clear).
   <div align="center">
  <img src="./Gambar/H3.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H4.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

   #

4. Percobaan bash script p1, p2, dan p3 beserta outputnya.
   
   - Untuk mengeksekusi bash script diperlukan permission execute (+x)
   - Script p1.sh, p2.sh, dan p3.sh dibuat dan dijalankan dengan berbagai kombinasi foreground dan background execution.
   <div align="center">
  <img src="./Gambar/H5.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H6.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H7.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H8.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H9.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H10.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H11.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

#

5. Pembuatan shell script pwaktu.sh, pengoperasian secara background(bg), foreground(fg %1), killing background(kill [PID]).
   
   <div align="center">
  <img src="./Gambar/H12.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H13.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H14.png" alt="Deskripsi Gambar" width="1000"/>
   </div>

#

6. Pengubahan history buffer(HISTSIZE) dari 1000 menjadi 20, menampilkan histori, mengeksekusi ulang perintah ke-5 dari akhir, bernavigasi dalam history buffer, menjalankan ulang perintah yang berada di history dengan nomor 150, dan menjalankan ulang perintah terakhir yang dimulai dengan ls

   - Pada bagian mengeksekusi ulang perintah ke-5 dari akhir tidak ada perintah yang dapat di eksekusi dengan baik/tak terlihat melalui history
   - bernavigasi dalam history buffer menggunakan ^P (Ctrl + P): Melihat perintah sebelumnya, ^N (Ctrl + N): Melihat perintah selanjutnya.
   - saat menjalankan ulang perintah yang berada di history dengan nomor 150 tidak ada apa-apa di nomor 150, mengakibatkan tidak adanya yang di eksekusi.
   - menjalankan ulang perintah terakhir yang dimulai dengan ls tidak ada perintah history yang menggunakan ls, sehingga tidak ada yang di eksekusi.
   <div align="center">
  <img src="./Gambar/H15.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
   <div align="center">
  <img src="./Gambar/H16.png" alt="Deskripsi Gambar" width="1000"/>
   </div>
   
