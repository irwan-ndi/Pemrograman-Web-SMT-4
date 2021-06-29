# Bab 4 OPERATOR ARITMATIKA DENGAN PHP

Dalam mempelajari bahasa pemrograman dasar, Kita selalu dihadapkan dengan istilah operator aritmatika. Operator Aritmatika adalah operator matematis yang terdiri dari operator penambahan, pengurangan, perkalian, pembagian, modulus, plus, dan minus. Dan pada tutorial kali ini, saya akan memberikan contoh latihan operator aritmatika dengan menggunakan bahasa pemrograman PHP.
$a + $b | Penambahan | Total dari $a dan $b
| ------------- | :-------------: | ------------- |
$a - $b | Pengurangan | Selisih dari $a dan $b
$a * $b | Perkalian | Hasil kali dari $a dan $b
$a / $b | Pembagian | Hasil bagi dari $a dan $b
$a % $b | Mod / Sisa hasil bagi | Sisa dari pembagian $a/$b

# Contoh Penggunaan Operator Aritmatika di dalam PHP
- Nama file : `aritmatika.php`
- ```php
	<?php
	$a = 35;
	$b = 10;
	$hasil1 = $a + $b; // Penjumlahan
	$hasil2 = $a - $b; // Pengurangan
	$hasil3 = $a * $b; // Perkalian
	$hasil4 = $a / $b; // Pembagian
	$hasil5 = $a % $b; // Modulus
	echo "Nilai a : $a<br>
	Nilai b : $b <br>
	Hasil penjumlahan $a + $b = $hasil1<br>
	Hasil pengurangan $a - $b = $hasil2<br>
	Hasil perkalian $a x $b = $hasil3<br>
	Hasil pembagian $a / $b = $hasil4<br>
	Sisa dari pembagian $a / $b = $hasil5";
	?>
	```

# Contoh Penggunaan Operator Aritmatika dengan Form
- Nama file : `form_jumlah.php`
- ```php
	<form method="POST" action="hasil.php">
		Nilai a : <input type="text" name="a"><br><br>
		Nilai b : <input type="text" name="b"><br><br>
	<input type="submit" value="Jumlahkan">
	</form>
	```

- Nama file : `hasil.php`
- ```php
	<?php
	// Ambil variabel dari form
	$a = $_POST['a'];
	$b = $_POST['b'];
	$hasil = $a + $b;
	echo "Nilai a : $a<br>
	Nilai b : $b<br>
	Hasil Penjumlahan $a + $b = $hasil";
	?>
	```

# Tingkat Presedensi
Dalam menggunakan operator aritmatik, kita harus berhati-hati terutama ketika menggunakan lebih dari satu operator yang berbeda dalam satu statement
perhitungan. Sebagai contoh skrip berikut ini:
```php
<?php
$a = 3 + 4 * 5 – 6;
echo $a;
?>
```

Apabila skrip di atas dijalankan, maka hasil yang muncul bukan 29, tapi 17. Mengapa demikian? itu dikarenakan operasi aritmatik yang dikerjakan terlebih dahulu adalah perkalian `(*)`. Mengapa demikian? Karena perkalian memiliki tingkat presedensi yang lebih tinggi daripada `+` dan `-`. Setelah perkalian`(*)` dikerjakan, baru dikerjakan operasi penjumlahan`(+)` atau pengurangan`(-)`. Operasi penjumlahan`(+)` dan pengurangan`(-)` memiliki tingkat presedensi yang sama. Oleh karenanya, maka yang dikerjakan lebih dahulu adalah yang terletak di bagian yang lebih kiri, yaitu penjumlahan `(+)`.

Bagaimana dengan operator pembagian `(/)`? Operator ini memiliki tingkat presedensi yang sama dengan perkalian`(*)`. Keduanya memiliki tingkat presedensi yang lebih
tinggi daripada penjumlahan `(+)` dan pengurangan `(-)`. Sedangkan operator modulus `(%)` levelnya juga sama dengan perkalian `(*)` dan pembagian `(/)`.
Jika kita ingin yang mengerjakan penjumlahan terlebih dulu, caranya adalah dengan memberikan tanda kurung seperti contoh di bawah ini.

```php
<?php
$a = (3 + 4) * 5 – 6;
echo $a;
?>
```

# Kombinasi Operator Aritmatik dan Assignment
Selain bentuk operator aritmatik yang dibahas sebelumnya, ada juga operator yang merupakan kombinasi antara operator aritmatik dengan assignment. Dalam pemrograman seringkali dijumpai proses yang melibatkan proses increment (kenaikan nilai). Misalkan kita menginginkan proses increment dengan tingkat kenaikan 1, maka perintah yang dituliskan dapat berupa 
``$counter = $counter + 1;``
Maksud dari perintah di atas adalah, nilai variabel $counter yang baru diperoleh dari nilai $counter yang lama ditambah 1. dalam PHP, perintah di atas dapat ditulis dalam satu perintah singkat sebagai
``$counter += 1;``
Dari contoh di atas tampak bahwa operator yang digunakan (+=) merupakan gabungan dari operator aritmatik dan assignment. Berikut ini adalah bentuk-bentuk operator lain jenis ini.
| Operator | Contoh | Operasi yang Ekuivalen |
| :---         |     :---:      |          ---: |
| `+=`   | `$x += 2;`     | `$x = $x + 2;`   |
| `-=`    | `$x -= 4;`       | `$x = $x - 4;`      |
| `*=`     | `$x *= 3;`       | `$x = $x * 3;`      |
| `/=`    | `$x /= 2;`       | `$x = $x / 2;`      |
| `%=`    | `$x %= 5;`       | $x = $x % 5;      |
| `.=`    | `$var_str.="hello";`       | `$var_str = $var_str . "hello";`      |

# Operator Pre/Post Increment dan Decrement
Operator jenis ini merupakan pengembangan dari operator jenis sebelumnya.
Operator ini hanya digunakan pada proses increment maupun decrement dengan
tingkat 1.
Berikut ini adalah operator yang termasuk jenis ini :
```
$x++;
ekuivalen dengan $x += 1; atau $x = $x + 1;
$x--;
ekuivalen dengan $x -= 1; atau $x = $x – 1;
```

Contoh :
```php
<?php
$x = 4;
$x++;
echo "Nilai x yang baru : ". $x;
$x = 4;
$x--;
echo "Nilai x yang baru : ". $x;
?>
```
