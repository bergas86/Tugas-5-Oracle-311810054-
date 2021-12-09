# 1. Membuat Koneksi Oracle Menggunakan PHP
Hal yang pertama dilakukan untuk membuat program Oracle menggunakan PHP adalah dengan mengkoneksikan Oracle ke PHP.

  1. Menginstal Oci8 (Di pertemuan ke-9)
  2. Menentukan versi PHP masing-masing
  3. Copy oci8.ddl dan oci8_11g dll, copy ke /Xampp/php/ext
  4. Edit php.ini di xampp/php
  5. Restar Apache/Xampp

Kemudian koneksi database dan menggunakan fungsi pada extension.

  `<?php $user="bergas_054"; $pass="054"; $database="LOCALHOST/XE"; $con = oci_connect($user, $pass, $database); if($con){    echo "Koneksi Sukses";  } else{    $err = oci_error();    echo "Gagal Koneksi". $err['text'];   } ?>`

    - Tentukan variable $username, $password, dan $db untuk database Oracle
    - Tentukan variable $db sebagai SID database
 
Jika Koneksi Berhasil, silahkan buka Browser web kalian dengan memasukkan link 'Localhost/Oracle/koneksi.php'. Catatan : Link Sesuai dengan folder dan Nama file yang sudah kalian simpah
![oracle3](https://user-images.githubusercontent.com/46914608/145457170-60b423d7-098b-4d1f-be2f-ba8b2ddca996.png)

# 2. Membuat View
View adalah salah satu object database di Oracle yang berfungsi sebagai virtual tabel. Bedanya Tabel dengan View adalah kalau View, Anda tidak bisa memodifikasi nilai atau data yang ada di View tersebut.

View biasanya digunakan untuk men-generate sebuah report untuk keperluan tertentu, misalkan report transaksi harian, bulanan, dan lain sebagainya.

View dibuat dengan menggunakan query SELECT statement dari satu atau lebih tabel.

Selanjutnya saya akan mencontohkan dan menampilkan beberapa saja membuat view.

`CREATE OR REPLACE view fak_transaksi as SELECT * FROM transaksi WHERE kd_faktur = 'barang xxx'; `

`CREATE OR REPLACE view stok_barang as SELECT * FROM barang WHERE stok = '99 pcs';`

Jika sudah dibuat maka akan coba kita tampilkan Hasil dari view yang sudah kita buat dengan Query View tersebut
![oracle1](https://user-images.githubusercontent.com/46914608/145457849-0895e5a7-7feb-4fe0-b40b-0035c7f9920a.png)
![oracle2](https://user-images.githubusercontent.com/46914608/145457885-5c9d7bea-4d7d-4d61-8e46-a438bc649452.png)

# 3. Membuat Halaman Home/Beranda
Halaman web yang bersifat dinamis dapat sangat berguna dan menghemat segala keperluan. contohnya untuk mengedit suatu halaman, kita hanya perlu mengeditnya di halaman itu saja. tanpa harus mengubah di semua halaman.

Untuk memulai pembuatan web dinamis, kita buat sebuah project di localhost (htdocs), misalnya sebuah project (folder). Disini fordel saya dengan nama “oracle“ (C:\xampp\htdocs\oracle). Kemudian buat sebuah file dengan nama index.php.

![oracle4](https://user-images.githubusercontent.com/46914608/145458353-a184fa8c-2e50-4aea-80ce-03c990ba154f.png)

# 4. Membuat Tabel Master
Setelah sukses koneksi, membuat view dan menjalankan di PHP maka kali ini kita akan membuat Tabel Master / Data Tabel dari Database yang sudah kita buat di Oracle.
![oracle5](https://user-images.githubusercontent.com/46914608/145458902-11a1802e-16e7-4ae6-8e13-c4cb1b7ade4d.png)
![oracle6](https://user-images.githubusercontent.com/46914608/145458920-2c1b1f56-4298-4005-b5e4-c35d0ee7f2d2.png)
![oracle7](https://user-images.githubusercontent.com/46914608/145458952-08d46e53-ca19-4967-b52c-6e4631a67ce4.png)
![oracle8](https://user-images.githubusercontent.com/46914608/145458971-3070042c-29f8-461c-bea2-21b0d18bc703.png)
