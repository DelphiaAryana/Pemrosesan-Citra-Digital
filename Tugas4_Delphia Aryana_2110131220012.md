### Tugas 4 Pemrosesan Citra Digital
### Nama : Delphia Aryana
### NIM : 2110131220012
<br>

<h1 align="center">Pseudocode Algoritma Patterning, Dithering, Bit Plane Slicing, dan Histogram Equalization</h1>

### 1) Patterning 

Banyak pola :

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

<p> &nbsp &nbspfor x (x = 1; x < gambar.length; x++){
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp for (y = 1; y < gambar.length; y++){
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp if (gambar[x,y] >=0 and gambar[x,y] <= 25):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola0
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=26 and gambar[x,y] <= 51):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola1
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=52 and gambar[x,y] <= 77):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola2
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=78 and gambar[x,y] <= 103):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola3
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=104 and gambar[x,y] <= 129):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola4
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=130 and gambar[x,y] <= 155):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola5
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=156 and gambar[x,y] <= 181):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola6
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=182 and gambar[x,y] <= 207):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola7
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=208 and gambar[x,y] <= 233):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola8
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp elif (gambar[x,y] >=234 and gambar[x,y] <= 259):
<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp gambar[x,y] = pola9

<p> &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp}
<p> &nbsp &nbsp }

<br>

Penjelasan :

- Menggunakan perulangan for di dalam for untuk mengakses baris dari 1 hingga kurang dari panjang gambar, dan update +1
- Lalu, terdapat percabangan untuk menentukan pola matriks
- Jika nilai matriks gambar pada posisi [x, y] >= 0 dan <= 25, maka posisi tersebut akan diisi dengan pola 0
- Jika nilai matriks gambar pada posisi [x, y] >= 26 dan <= 51, maka posisi tersebut akan diisi dengan pola 1
- Dan seterusnya.