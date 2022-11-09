### Tugas 5 Pemrosesan Citra Digital

Nama : Delphia Aryana

NIM : 2110131220012

<h1 align="center">Bit Plane Slicing</h1>

Gambar yang dipakai :

<img src="img/pohon.jpeg" width="300px">



<p align="justify"> Di sini saya mengaplikasikan teknik <i>bit plane slicing</i> terhadap citra <i>grayscale</i> dengan menggunakan Octave.

Kode Program :

<img src="img/photo20.png" width="750px">

Penjelasan :

- Membuat variabel gambar untuk membaca citra dengan menggunakan fungsi <b>imread</b>.
- Mengubah citra berwarna menjadi citra grayscale atau abu-abu
menggunakan fungsi <b>>rgb2gray</b> yang disimpan ke dalam variabel <b>gambar_gray</b>.
- Menyimpan nilai di variabel <b>row</b> dan <b>col</b> sesuai dengan ukuran/size dari gambar grayscale.
- Terdapat <b>subplot(3, 3, 1)</b> dan <b>imshow(gambar_gray)</b> untuk menampilkan gambar grayscale dan meletakkan plot fungsinya pada bidang plot ukuran 3 baris dan 3 kolom di area ke-1.
- Membuat keterangan gambar dengan menggunakan <b>tittle</b>.
- Selanjutnya, membuat 8 matriks yang semua datanya bernilai 0 dengan kode <b>zeros(row, col, 8)</b>. Matriks memiliki jumlah baris dan kolom sesuai dengan nilai dari variabel <b>row</b> dan <b>col</b>. 8 matriks tersebut nantinya akan mewakili tiap-tiap lapisan.
- Menggunakan perulangan untuk menampilkan semua lapisan.
- Terdapat for i dengan kondisi loop 1-8, for j dengan kondisi loop 1-row (mewakili baris matriks), dan for k dengan kondisi loop 1-col (mewakili kolom matriks). 
- Lalu terdapat kode <b>matriks(j, k, i) = bitget(gambar_gray(j, k), i)</b> untuk mengubah nilai dari setiap matriks 0 yang baru dibuat. Nilai matriks baris ke-j, kolom ke-k, dan lapisan ke-i akan diubah sama seperti nilai bitget dari gambar grayscale baris ke-j, kolom ke-k, dan lapisan ke-i.
- Menggunakan <b>subplot(3, 3, i+1)</b> dan <b>imshow(:, :, i)</b> untuk menampilkan hasil tiap lapisan dan meletakkan plot fungsinya pada bidang plot ukuran 3 baris dan 3 kolom di area ke-i+1.
- Membuat keterangan gambar dengan menggunakan <b>tittle</b>. Ubah angka (numbers) i ke dalam format string untuk memberikan keterangan urutan tiap lapisan.

<p align="center">Hasil Bit Plane Slicing

<p align="center"><img src="img/photo21.png" width="750px">

<br>

### Menggabungkan dengan Gambar Teman

- Gambar Saya :

<img src="img/gambar_delphia.png" width="300px">

- Gambar Maysarah

<img src="img/gambar_maysarah.png" width="300px">

Kode Program :

<img src="img/photo23.png" width="700px">

<img src="img/photo22.png" width="700px">

<p align="center"><i>Bit Plane Slicing</i> Gambar yang Telah Digabung

<p align="center"><img src="img/photo24.png" width="700px">

<br>

<h1 align="center">Steganografi</h1>

<p align="justify">Steganografi adalah sebuah metode dalam pemrosesan citra digital untuk menyembunyikan suatu data rahasia ke dalam sebuah citra. Data yang dapat disembunyikan berupa :

- Gambar
- Teks
- Suara
- dll.

<p align="justify">Disini saya akan mengaplikasikan metode ini steganografi terhadap citra gray_scale dengan menggunakan Octave.

Kode Program :

<img src="img/photo26.png" width="700px">


<img src="img/photo27.png" width="700px">

<p align="center">Hasil

<p align="center"><img src="img/photo25.png">