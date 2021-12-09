# 1. Membuat Koneksi Oracle Menggunakan PHP
Hal yang pertama dilakukan untuk membuat program Oracle menggunakan PHP adalah dengan mengkoneksikan Oracle ke PHP.

`<?php $user="bergas_054"; $pass="054"; $database="LOCALHOST/XE"; $con = oci_connect($user, $pass, $database); if($con){    echo "Koneksi Sukses";  } else{    $err = oci_error();    echo "Gagal Koneksi". $err['text'];   } ?>`

Jika Koneksi Berhasil, silahkan buka Browser web kalian dengan memasukkan link 'Localhost/Oracle/koneksi.php'. Catatan : Link Sesuai dengan folder dan Nama file yang sudah kalian simpah
![oracle3](https://user-images.githubusercontent.com/46914608/145457170-60b423d7-098b-4d1f-be2f-ba8b2ddca996.png)

# 2. Membuat View
Selanjutnya adalah untuk membuat view. Sebenarnya saya membuat view lebih dari 5, Namun agar lebih mudah disini hanya saya tampilkan 2 dari view yang sudah saya buat

`CREATE OR REPLACE view fak_transaksi as SELECT * FROM transaksi WHERE kd_faktur = 'barang xxx'; `

`CREATE OR REPLACE view stok_barang as SELECT * FROM barang WHERE stok = '99 pcs';`

Jika sudah dibuat maka akan coba kita tampilkan Hasil dari view yang sudah kita buat dengan Query View tersebut
![oracle1](https://user-images.githubusercontent.com/46914608/145457849-0895e5a7-7feb-4fe0-b40b-0035c7f9920a.png)
![oracle2](https://user-images.githubusercontent.com/46914608/145457885-5c9d7bea-4d7d-4d61-8e46-a438bc649452.png)

# 3. Membuat Halaman Home/Beranda
Selanjutnya kita akan coba menampilkan view yang sudah dibuat kedalam project PHP menggunakan sublime Text 3. Berikut tampilannya!
![oracle4](https://user-images.githubusercontent.com/46914608/145458353-a184fa8c-2e50-4aea-80ce-03c990ba154f.png)

# 4. Membuat Tabel Master
Setelah sukses koneksi, membuat view dan menjalankan di PHP maka kali ini kita akan membuat Tabel Master / Data Tabel dari Database yang sudah kita buat di Oracle.
![oracle5](https://user-images.githubusercontent.com/46914608/145458902-11a1802e-16e7-4ae6-8e13-c4cb1b7ade4d.png)
![oracle6](https://user-images.githubusercontent.com/46914608/145458920-2c1b1f56-4298-4005-b5e4-c35d0ee7f2d2.png)
![oracle7](https://user-images.githubusercontent.com/46914608/145458952-08d46e53-ca19-4967-b52c-6e4631a67ce4.png)
![oracle8](https://user-images.githubusercontent.com/46914608/145458971-3070042c-29f8-461c-bea2-21b0d18bc703.png)
