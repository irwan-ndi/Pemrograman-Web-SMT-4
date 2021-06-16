# BAB 3
# STRUKTUR DASAR SKRIP PHP
- Untuk memberikan kemudahan bagi Anda dalam mempelajari bahasa pemrograman PHP, Saya akan mencoba memberikan tutorial secara step by step mengenai materi PHP mulai dari pemahaman dasar hingga implementasinya berupa studi kasus sederhana. 
- Sebelum Kita mulai belajar, pastikan Anda sudah menyiapkan aplikasi-aplikasi yang dibutuhkan, 
  - Jalankan Service Apache dan MySQL Server Anda melalui XAMPP Control Panel, 
  - buka aplikasi Text Editor Anda seperti 
    - Notepad++ atau 
    - SublimeText.
## Memahami Aturan Penulisan Skrip PHP
Aturan penulisan yang tidak boleh dilanggar adalah bahwa 
- format penulisan skrip PHP harus dibuka oleh tag `<?php` 
- dan ditutup dengan `?>`.
- 
  ```php
  <?php
  // Tulis Skrip PHP Disini
  ?>```
- Ekstensi file default untuk file PHP adalah **".php"**.
- Sebuah file PHP biasanya berisi tag HTML, dan beberapa kode Skrip PHP.
  - Skrip PHP memiliki kemampuan untuk mengintegrasikan format tampilan dengan database dalam membangun sebuah sistem.
  - Untuk menyisipkan file HMTL kedalam skrip PHP atau sebaliknya, Kita dapat menggunakan 2 cara, yaitu :
### 1. Embedded Script
```php
<!DOCTYPE html>
<html>
<body>
<h1>Halaman PHP Pertamaku</h1>
<?php
echo "Halo, Saya sedang belajar bahasa pemrograman PHP";
?>
</body>
</html>
```
### 2. Non-Embedded Script
```php
<?php
echo "<html>
<body>
    <h1>Halaman PHP Pertamaku</h1>
    <p>Halo, Saya sedang belajar bahasa pemrograman PHP</p>
    
</body>
</html>";

?>
```
- Adapun cara yang akan Anda gunakan, 
- silahkan pilih sesuai selera Anda, 
- karena baik menggunakan cara Embedded Script maupun Non-Embedded Script hasilnya sama saja.
## Memberikan Komentar pada Skrip PHP
Skrip komentar pada PHP digunakan untuk memberikan keterangan yang tidak terbaca pada saat dieksekusi oleh program. Hal ini sangatlah penting bagi seorang programmer untuk menandai atau memberikan keterangan pada masing-masing fungsi skrip.
Fungsi komentar pada skrip PHP digunakan untuk :
- Agar orang lain memahami apa yang Anda lakukan pada fungsi kode program tertentu.
- Mengingatkan pada diri Anda sendiri tentang bagian dari program yang sudah Anda kerjakan.
Ada dua cara memberikan komentar pada skrip PHP, yaitu :
- Komentar satu baris menggunakan tanda // atau #.
- Komentar lebih dari satu baris menggunakan tanda /* ... */.
Berikut adalah contoh latihan menggunakan komentar pada skrip PHP
- 
  ```php
  <?php
  /*
  Berikut adalah Program untuk menampilkan
  Tanggal saat ini menggunakan
  Fungsi date
  */
  
  // Membuat variabel berisi tanggal hari ini
  $tanggal = date("d-M-Y");
  
  # Menampilkan tanggal di browser menggunakan fungsi echo
  echo "Tanggal hari ini : $tanggal";
  ?>
  ```
## Memahami Variabel di PHP
Variabel adalah merupakan suatu tempat / wadah untuk menampung data atau konstanta di memori yang mempunyai nilai atau data yang dapat berubah–ubah selama proses program.

Ketentuan menulis nama variabel yang benar di PHP
- Variabel selalu diawali dengan tanda dollar ($), lalu diikuti nama variabel.
- Hanya ada tiga jenis karakter yang dapat digunakan untuk pemberian nama variabel, yaitu huruf, angka, dan garis bawah ( _ ).
- Karakter pertama setelah tanda $ harus berupa huruf atau garis bawah, tidak
boleh angka atau yang lain.
- Jika nama variabel lebih dari satu kata, tidak boleh memisahnya dengan spasi, alternatif lainnya dapat menggunakan garis bawah ( _ ).
- Nama variabel bersifat case sensitif, artinya PHP membedakan huruf besar dan huruf kecil.
Berikut adalah contoh latihan untuk memudahkan Anda dalam memahami cara menulis variabel di PHP
```php
<?php
$nama;
$nama_mahasiswa;
$alamat1;
$alamat1alamat2;
$_telpon;
echo "Jika teks ini tampil, <br>
maka semua pemberian nama variabel sudah benar";
?>
```
### Memberi Nilai pada Variabel
```php
<?php
// memberi nilai variabel
$nama_mahasiswa = "Novita Sari"; // String
$mata_kuliah = "Pemrograman Basis Data";
$jumsks = 3; // Integer
$nilai = 85.5; // Floating point

// Menampilkan nilai variabel
echo "Nama Mahasiswa : $nama_mahasiswa<br>
Mata Kuliah : $mata_kuliah<br>
Jumlah SKS : $jumsks<br>
Nilai : $nilai";
?>
```
Variabel dapat menyimpan berbagai jenis data, dan tipe data yang berbeda dapat melakukan hal-hal yang berbeda. PHP mendukung jenis data sebagai berikut:
#### String
String adalah sebuah tipe data yang terdiri dari kata, bisa berupa kata tunggal maupun kalimat. Penulisan string harus diapit oleh tanda petik, baik petik tunggal(‘ ‘) maupun petik ganda (” “).
#### Integer
Tipe data integer adalah tipe data yang berfungsi untuk menyimpan bilangan bulat, bukan desimal. Tipe data integer mempunyai range antara -2,147,483,648 sampai dengan 2,147,483,647.
#### Float
Tipe data floating point numbers biasa juga disebut dengan double, float atau real adalah tipe data yang berguna untuk menyimpan bilangan desimal.
#### Boolean
Tipe Data ini adalah tipe data yang paling sederhana. Hanya berupa true atau false. Penggunaan huruf besar atau kecil sama sekali tidak mempengaruhi dalam penulisan tipe data boolean.
#### Array
tipe data Array diguakan untuk menyimpan beberapa nilai dalam satu variabel tunggal.
#### Object
Objek adalah tipe data yang menyimpan data dan informasi tentang cara mengolah data tersebut.
#### NULL
Null adalah tipe data khusus yang hanya dapat memiliki satu nilai: NULL. Sebuah variabel tipe data NULL adalah variabel yang tidak memiliki nilai yang ditugaskan untuk itu. Jika variabel yang dibuat tanpa nilai, maka secara otomatis diberi nilai NULL.
#### Resource
Tipe Data resources ini di berfungsi untuk menyimpan resource, sumber atau alamat. Variabel tersebut hanya dapat dibuat oleh suatu fungsi khusus yang mengembalikan nilai berupa resource seperti penggunaan fungsi mysql_connect, mysql_query, fopen, opendir dan semacamnya.
