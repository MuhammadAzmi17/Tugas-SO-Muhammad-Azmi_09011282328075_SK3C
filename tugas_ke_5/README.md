Tugas 5 Sistem Operasi(Parktikum)
----
By,Muhammad Azmi

Kelas SK3C

NIM: 09011282328075

Berikut soal yang saya kerjakan:
----
1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.
2. Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
3. Urutkan file baru dengan cara membelokkan standard input.
4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.
5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.
6. Urutkan kalimat berikut :
   - Jakarta
   - Bandung
   - Surabaya
   - Padang
   - Palembang
   - Lampung
     
   Dengan menggunakan notasi here document (<@@@ …@@@)
7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
8. Gunakan perintah di bawah ini dan perhatikan hasilnya.
$ cat /etc/passwd | sort | pr –n | grep tty03
$ find /etc –print | head
$ head /etc/passwd | tail –5 | sort
9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.


Penjelasan dari saya(Penyelesaian):
----

<div align=center>
   <img src= Gambar/P1.png alt= gambar 1 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P2.png alt= gambar 2 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P3.png alt= gambar 3 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P4.png alt= gambar 4 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P5.png alt= gambar 5 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P6.png alt= gambar 6 width= 1000>
</div>

##

<div align=center>
   <img src= Gambar/P7.png alt= gambar 7 width= 1000>
</div>

****
Pada nomor 8 dibawah memiliki 3 penjelasan berdasarkan gambar:
****

<div align=center>
   <img src= Gambar/P81.png alt= gambar 8 width= 1000>
</div>

Pada gambar di atas Menampilkan isi dari /etc/passwd menggunakan cat /etc/passwd, mengurutkannya secara alfabetis menggunakan sort, menambahkan nomor pada setiap baris menggunakan pr -n, dan menyaring (mencari) hanya baris yang mengandung "tty03" menggunakan grep.
##
<div align=center>
   <img src= Gambar/P82.png alt= gambar 8 width= 1000>
</div>
Perintah di atas mencari dan mencetak daftar semua file dan direktori di dalam direktori /etc tetapi hanya menampilkan 10 hasil pertama(menggunakan head) dari pencarian tersebut.

##
<div align=center>
   <img src= Gambar/P83.png alt= gambar 8 width= 1000>
</div>
Terjadi 3 even di atas yaitu:

- head /etc/passwd – Menampilkan 10 baris pertama dari /etc/passwd.

- tail -5 – Mengambil 5 baris terakhir dari hasil di atas.

- sort – Mengurutkan 5 baris tersebut secara alfabetis.


****
Nomor 9 ada di bawah sini V
****

<div align=center>
   <img src= Gambar/P9.png alt= gambar 9 width= 1000>
</div>
Berikut yang terjadi di atas:

- Menampilkan pengguna aktif dengan perintah who.

- Mengurutkan daftar pengguna tersebut dengan perintah sort.

- Memformatnya menggunakan pr untuk pagination.

- Menampilkan 10 baris pertama dari hasil tersebut dengan head.

Untuk command cat di sini tidak menambah fungsi apa pun selain meneruskan input ke perintah berikutnya. Jadi untuk perulangan ini bisa dihilangkan sebenarnya tanpa merubah hasil output.
