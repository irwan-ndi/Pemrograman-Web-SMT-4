Tingkat Presedensi
Dalam menggunakan operator aritmatik, kita harus berhati-hati terutama ketika
menggunakan lebih dari satu operator yang berbeda dalam satu statement
perhitungan.
Sebagai contoh skrip berikut ini:
```php
<?php
$a = 3 + 4 * 5 – 6;
echo $a;
?>
```

Apabila skrip di atas dijalankan, maka hasil yang muncul bukan 29, tapi 17. Mengapa
demikian? itu dikarenakan operasi aritmatik yang dikerjakan terlebih dahulu adalah
perkalian (*). Mengapa demikian? Karena perkalian memiliki tingkat presedensi yang
lebih tinggi daripada + dan -. Setelah perkalian(*) dikerjakan, baru dikerjakan operasi
penjumlahan(+) atau pengurangan(-).
Operasi penjumlahan(+) dan pengurangan(-) memiliki tingkat presedensi yang sama.
Oleh karenanya, maka yang dikerjakan lebih dahulu adalah yang terletak di bagian
yang lebih kiri, yaitu penjumlahan (+).

Bagaimana dengan operator pembagian (/)? Operator ini memiliki tingkat presedensi
yang sama dengan perkalian(*). Keduanya memiliki tingkat presedensi yang lebih
tinggi daripada penjumlahan (+) dan pengurangan (-). Sedangkan operator modulus
(%) levelnya juga sama dengan perkalian (*) dan pembagian (/).
Jika kita ingin yang mengerjakan penjumlahan terlebih dulu, caranya adalah dengan
memberikan tanda kurung seperti contoh di bawah ini.

```php
<?php
$a = (3 + 4) * 5 – 6;
echo $a;
?>
```