### Tugas 4 Pemrosesan Citra Digital
### Nama : Delphia Aryana
### NIM : 2110131220012
<br>

<h2 align="center">Algoritma Patterning, Dithering, Bit Plane Slicing, dan Histogram Equalization</h2>

### 1) Patterning 

<p> &nbsp pola0 = [

    [0 0 0],
    [0 0 0],
    [0 0 0]
<p> &nbsp ];

<p> &nbsp pola1 = [

    [0 0 0],
    [0 0 0],
    [0 0 1]
<p> &nbsp ];

<p> &nbsp pola2 = [

    [1 0 0],
    [0 0 0],
    [0 0 1]
<p> &nbsp ];

<p> &nbsp pola3 = [

    [1 0 1],
    [0 0 0],
    [0 0 1]
<p> &nbsp ];

<p> &nbsp pola4 = [

    [1 0 1],
    [0 0 0],
    [1 0 1]
<p> &nbsp ];

<p> &nbsp pola5 = [

    [1 0 1],
    [0 0 0],
    [1 1 1]
<p> &nbsp ];

<p> &nbsp pola6 = [

    [1 0 1],
    [1 0 0],
    [1 1 1]
<p> &nbsp ];

<p> &nbsp pola7 = [

    [1 0 1],
    [1 0 1],
    [1 1 1]
<p> &nbsp ];

<p> &nbsp pola8 = [

    [1 1 1],
    [1 0 1],
    [1 1 1]
<p> &nbsp ];

<p> &nbsp pola9 = [

    [1 1 1],
    [1 1 1],
    [1 1 1]
<p> &nbsp ];

<p> &nbsp &nbsp gambar = [ ]

Pseudocode :

<p> &nbsp &nbspfor x (x = 1; x < gambar.length; x++){
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp for (y = 1; y < gambar.length; y++){
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp if (gambar [x, y] >= 0 and gambar [x, y] <= 25):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x, y] = pola0
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 26 and gambar [x,y] <= 51):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola1
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 52 and gambar [x, y] <= 77):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x, y] = pola2
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 78 and gambar [x, y] <= 103):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola3
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 104 and gambar [x, y] <= 129):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola4
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 130 and gambar [x, y] <= 155):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola5
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 156 and gambar [x, y] <= 181):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola6
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 182 and gambar [x, y] <= 207):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola7
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 208 and gambar [x, y] <= 233):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola8
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar [x, y] >= 234 and gambar [x, y] <= 259):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar [x, y] = pola9

<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp}
<p> &nbsp &nbsp }

Penjelasan :

- Menggunakan perulangan for di dalam for untuk mengakses baris dari 1 hingga kurang dari panjang gambar, dan update +1
- Selanjutnya, terdapat percabangan untuk menentukan pola matriks
- Jika nilai matriks gambar pada posisi [x, y] >= 0 dan <= 25, maka posisi tersebut akan diisi dengan pola 0
- Jika nilai matriks gambar pada posisi [x, y] >= 26 dan <= 51, maka posisi tersebut akan diisi dengan pola 1
- Dan seterusnya.

<br>

### 2) Dithering

Treshold :

<p> &nbsp T = [

    [50 120],
    [150 10]
<p> &nbsp ];

Kemudian terdapat matriks M yang akan kita bandingkan dengan batas/treshold.

Pseudocode :

<p> &nbsp &nbspfor (all x & y) do
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp if M (x,y) > T (x, y) then
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp g (x, y) = 255
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp else 
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp g (x, y) = 0
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp endif
<p> &nbsp &nbspendfor

Penjelasan :
- Untuk setiap bagian blok matriks M dibandingkan dengan batas/treshold
- Jika matriks lebih besar dari batas, maka matriks bernilai 255 atau putih
- Jika matriks lebih kecil dari batas, maka matriks bernilai 0 atau hitam

<br>

### 3) Bit Plane Slicing

- Misal, diketahui :

<p> &nbsp A = [

    [100 210],
    [215 112]
<p> &nbsp ];

- Ubah setiap nilai pada matriks menjadi biner, sehingga memberikan hasil :

<p> &nbsp Biner = [

    [01100100 11010010],
    [11010111 01110000]
<p> &nbsp ];

- Simpan masing-masing nilai angka biner.
- Setiap 1 angka dari masing-masing hasil bilangan biner, dimasukkan ke dalam matriks baru sesuai urutan, sehingga terbentuk 8 buah matriks baru :

<p> &nbsp A1 = [

    [0 0],
    [1 0]
<p> &nbsp ];

<p> &nbsp A2 = [

    [0 1],
    [1 0]
<p> &nbsp ];

<p> &nbsp A3 = [

    [1 0],
    [1 0]
<p> &nbsp ];

<p> &nbsp A4 = [

    [0 0],
    [0 0]
<p> &nbsp ];

<p> &nbsp A5 = [

    [0 1],
    [1 1]
<p> &nbsp ];

<p> &nbsp A6 = [

    [1 0],
    [0 1]
<p> &nbsp ];

<p> &nbsp A7 = [

    [1 1],
    [1 1]
<p> &nbsp ];

<p> &nbsp A8 = [

    [0 1],
    [1 0]
<p> &nbsp ];

- Untuk matriks pada kanal pertama adalah Least Significant Bit (LSB)
- Sedangkan matriks pada kanal terakhir adalah Most Significant Bit (MSB)

<br>

### 4) Histogram Equalization

Misal :

Gray level = [0 1 2 3 4 5 6  7]

Non of pixel = [8 7 10 9 5 3 6 12]

- Hitung seluruh nilai histogram yaitu dengan cara menjumlahkan nilai histogram dengan nilai histogram sebelumnya.
- Normalisasi jumlah histogram. Bagi jumlah histogram dengan jumlah seluruh nilai histogram.
- Kalikan hasil normalisasi tersebut dengan maximum dari gray level.
- Tentukan jumlah masing-masing gray levelnya dengan menjumlahkan number of pixel dengan gray level yang sama.


