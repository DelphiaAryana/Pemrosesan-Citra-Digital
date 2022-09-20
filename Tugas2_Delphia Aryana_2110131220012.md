### Tugas 2 Pemrosesan Citra Digital

Nama : Delphia Aryana

NIM : 2110131220012

<h2 align="center">Eksplorasi <i>Octave</i> dengan <i>Package Image</i></h2>
<hr>

<p align="justify">Langkah pertama adalah memulai <i>package image</i> terlebih dahulu. Ketik <b>pkg load image</b> pada <i>command window</i>. Dilanjutkan dengan <b>pkg list</b> yang berguna untuk mengecek apakah <i>package image</i> pada <i>octave</i> sudah dapat digunakan atau belum. Jika pada bagian <i>package</i> <b>image</b> sudah bertanda bintang (*), maka <i>package</i> sudah siap untuk untuk diakses. 

<p><img src="img/photo1.png" width="700px"></p>

<p align="justify">Foto yang saya gunakan untuk mengeksplorasi memiliki dimensi 32x32x3, keterangan ini akan muncul saat kita menggunakan fungsi <b>imread</b> yang dimana fungsi tersebut berguna untuk membaca gambar (Penjelasan mengenai fungsi-fungsi yang akan saya pakai terdapat di bagian akhir). 

Seperti yang kita ketahui, sebuah gambar memiliki 3 layer warna, yaitu merah _(red)_, hijau _(green)_ dan biru _(blue)_. Perhatikan gambar di bawah ini :

1. __Gambar dan Histogram Dasar__

<p><img src="img/photo2.png" width="500px"></p>

<br>

2. __Gambar dan Histogram Merah _(Red)___

<p><img src="img/photo3.png" width="500px"></p>

<br>

3. __Gambar dan Histogram Hijau _(Green)___

<p><img src="img/photo4.png" width="500px"></p>

<br>

4. __Gambar dan Histogram Biru _(Blue)___

<p><img src="img/photo2.png" width="500px"></p>

<br><br>

### Fungsi-fungsi yang dipakai :

<p><img src="img/photo6.png" width="500px"></p>

- __imread__ : berfungsi untuk membaca sebuah <i>file</i> gambar berada.
- __imshow__ : berfungsi untuk menampilkan objek gambar.
- __imhist__ : berfungsi untuk menampilkan <i>image</i> dalam bentuk histogram.

