Contoh Penggunaan Operator Aritmatika dengan Form
Nama file : form_jumlah.php
```php
<form method="POST" action="hasil.php">
	Nilai a : <input type="text" name="a"><br><br>
	Nilai b : <input type="text" name="b"><br><br>
<input type="submit" value="Jumlahkan">
</form>
```

Nama file : hasil.php
```php
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