# 1. Membuat Koneksi Oracle Menggunakan PHP
Hal yang pertama dilakukan untuk membuat program Oracle menggunakan PHP adalah dengan mengkoneksikan Oracle ke PHP.

`<?php $user="bergas_054"; $pass="054"; $database="LOCALHOST/XE"; $con = oci_connect($user, $pass, $database); if($con){    echo "Koneksi Sukses";  } else{    $err = oci_error();    echo "Gagal Koneksi". $err['text'];   } ?>`

<h3>Jika Koneksi Berhasil, silahkan buka Browser web kalian dengan memasukkan link 'Localhost/Oracle/koneksi.php'. Catatan : Link Sesuai dengan folder dan Nama file yang sudah kalian simpah</h3>

