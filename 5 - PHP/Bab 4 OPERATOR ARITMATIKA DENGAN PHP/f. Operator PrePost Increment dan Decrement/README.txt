Operator Pre/Post Increment dan Decrement
---
Operator jenis ini merupakan pengembangan dari operator jenis sebelumnya.
Operator ini hanya digunakan pada proses increment maupun decrement dengan
tingkat 1.
Berikut ini adalah operator yang termasuk jenis ini :
$x++;
ekuivalen dengan $x += 1; atau $x = $x + 1;
$x--;
ekuivalen dengan $x -= 1; atau $x = $x – 1;
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