### Tugas 6 Pemrosesan Citra Digital

Nama : Delphia Aryana

NIM : 2110131220012

<h1 align="center">Spatial Frequency Domain </h1>

<p align="justify">Metode untuk perbaikan kualitas citra <i>(image enhancement)</i> dapat dikelompokkan menjadi 2 kategori :

1. _Image Enhancement_ dalam ranah spasial (spatial)
2. _Image Enhancement_ dalam ranah frekuensi (frequency)

<br>

### 1) Domain Spasial 

<p align="justify">Metode-metode <i>Image Enhancement</i> dalam ranah spasial dilakukan dengan memanipulasi secara langsung <i>pixel-pixel</i> di dalam citra. Domain spasial melibatkan operasi konvolusi, sehingga komputasinya lebih tinggi dan prosesnya lebih kompleks.

<p align="justify">Metode pemrosesan citra dalam ranah ini dinyatakan sebagai :

<p>&nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp g(x, y) = T[f(x, y)]

Keterangan :
- f(x, y) = Citra original/citra input
- g(x, y) = Citra baru yang dimodifikasi/citra output
- T       = Sebuah transformasi yang diterapkan untuk mendapatkan citra baru (g(x,y))

<p align="justify">Untuk citra 8-bit, f dapat mengambil nilai dari 0-255 yang dimana 0 adalah hitam dan 255 adalah putih. T bisa beroperasi pada satu <i>pixel</i>, sekelompok <i>pixel</i> bertetangga, atau keseluruhan <i>pixel</i> di dalam citra. Jadi, metode dalam ranah spasial dapat dilakukan pada aras titik<i>(pixel)</i>, aras lokal, dan aras global. Untuk lebih jelas, lihat ilustrasi berikut.

<p align="center"><img src="img/photo7.png" width="620px">

<br>

### 2) Domain Frekuensi

<p align="justify">Metode-metode <i>Image Enhancement</i> dalam ranah frekuensi dilakukan dengan mengubah citra terlebih dahulu dari ranah spasial ke ranah frekuensi, baru kemudian memanipulasi nilai-nilai frekuensi tersebut. Domain frekuensi hanya dapat dilakukan pada aras global dan tidak melibatkan operasi konvolusi, sehingga komputasinya rendah cepat dan prosesnya relatif simple.

<p align="justify">Prose perubahan fungsi dari ranah spasial ke dalam ranah frekuensi dilakukan melalui <b>Transformasi Fourier</b>. Sedangkan perubahan fungsi dari ranah frekuensi ke ranah spasial dilakukan melalui <b>Transformasi Fourier Balikan (invers)</b>.

<p align="center"><img src="img/photo8.png" width="520px">

<br>

## Metode Domain Spasial

 Terdapat 2 metode untuk perbaikan kualitas citra <i>(image enhancement)</i> pada domain spasial, yaitu :

 1. _Point Processing_
 2. _Mask Processing_

 <br>

 ### a. _Point Processing_ (Operasi titik)

 <p align="justify">Untuk melakukan pengolahan titik pada metode ini tidak memiliki ketergantungan dengan titik-titik yang ada di sebelahnya. Titik yang ada langsung saja di ubah tanpa mempengaruhi atau dipengaruhi oleh titik yang berada di sebelahnya.

1. __Citra Negatif__

Rumus :

<img src="img/photo9.png" width="280px">

<p align="center">Contoh Hasil 

<p align="center"><img src="img/photo10.png" width="550px">

<br>

2. __Contrast Stretching__
<p align="justify">Untuk mengubah kontras dari suatu image dengan cara mengubah graylevel piksel-piksel pada citra menurut fungsi s = T(r) tertentu. 

<img src="img/photo12.png" width="420px">

<p align="center">Contoh Hasil 

<p align="center"><img src="img/photo11.png" width="550px">

<br>

3. __Histogram Equalization__

<p align="justify">Histogram merupakan diagram yang menunjukkan jumlah kemunculan grey level (0-255) pada suatu citra. 

- Gambar gelap : histogram cenderung ke sebelah kiri.
- Gambar terang : histogram cenderung ke sebelah kanan.
- Gambar low contrast : histogram mengumpul di suatu tempat.
- Gambar high contrast : histogram merata di semua tempat.

<p align="center"><img src="img/photo13.png" width="400px">

<p align="center">Contoh Hasil :

<p align="center"><img src="img/photo14.png" width="500px">

<br>

4. __Image Substraction__

<p align="justify">Image Substaction dilakukan jika kita ingin mengambil bagian tertentu saja dari citra.

Contoh Hasil :

<img src="img/photo15.png" width="400px">

<br>

5. __Image Averaging__

<p align="justify">Dilakukan jika kita memiliki beberapa citra yang bergambar sama, namun semua citra memiliki noise (gangguan). Noise satu citra berbeda dengan noise citra lainnya (tidak berkolerasi). Cara memperbaikinya adalah dengan melakukan operasi rata-rata terhadap semua citra tersebut.

<img src="img/photo16.png" width="280px">

<br>

### b. _Mask Processing_ 

<p align="justify">Jika pada <i>point processing</i> kita hanya melakukan operasi terhadap masing-masing piksel, maka pada <i>mask processing</i> kita melakukan operasi terhadap suatu jendela ketetanggaan pada citra. Kemudian kita menerapkan (mengkonvolusikan) suatu <i>mask</i> terhadap jendela tersebut. <i>Mask</i> sering juga disebut <i>filter</i>.

Contoh 1 :

<img src="img/photo17.png" width="180px">

<p align="justify">Jendela ketetanggaan 3x3. Nilai pixel pada posisi x dipengaruhi oleh nilai 8 tetangganya. Perbedaan dengan <i>point processing</i>, nilai pada suatu piksel tidak dipengaruhi oleh nilai tetangga-tetangganya.

Contoh 2 :

<img src="img/photo18.png" width="180px">

Sebuah mask berukuran 3x3. Filter ini akan diterapkan/dikonvolusikan pada setiap jendela ketetanggaan 3x3 pada citra (anggap filter sudah dalam bentuk terbalik).

<img src="img/photo19.png" width="500px">





