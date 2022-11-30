### __KELOMPOK 10 :__
- Khoyrur Roykhan
- Delphia Aryana
- Naila Hasanah

<br>

<h1 align="center"> Low-Pass Filtering</h1>

<p align="justify">Low-pass filtering adalah proses filter yang melewatkan komponen citra dengan nilai intensitas yang rendah dan meredam komponen citra dengan nilai intensitas yang tinggi. Low pass filter akan menyebabkan citra menjadi lebih halus dan lebih blur.</p>

### __Aturan Kernel untuk Low-Pass Filter__

1. Semua koefisien kernel harus positif
2. Jumlah semua koefisien kernel harus sama dengan 1

Contoh kernel  yang dapat digunakan pada low-pass filtering adalah :

<p align="center"><img width="700" src="img/kernel low pass.jpg"></p>

Low-pass filtering menggunakan kernel (iii) disebut juga __neighborhood averaging.__ 

<h3 align="center">Kode LPF Manual</h3>

<p align="center"><img width="550" src="img/lpf_manual.jpg"></p>

<p align="center">Output :

<p align="center"><img width="650" src="img/hasil_lpf_manual.jpg"></p>

<h3 align="center">Kode Menggunakan Fungsi pada Octave</h3>

<p align="center"><img width="700" src="img/kode.png"></p>

<p align="center">Output :

- Citra Asli
<p align="center"><img width="400" src="img/figure1.png"></p>

- Citra Menggunakan Kernel 1
<p align="center"><img width="400" src="img/figure2.png"></p>

- Citra Menggunakan Kernel 2
<p align="center"><img width="400" src="img/figure3.png"></p>

- Citra Menggunakan Kernel 3
<p align="center"><img width="400" src="img/figure4.png"></p>

<br>

<h1 align="center">High-Pass Filtering</h1>

<p align="justify"><i>High Pass Filter</i> (HPF) adalah proses filter yang mengambil citra dengan gradiasi intensitas yang tinggi dan perbedaan intensitas yang rendah akan dikurangi atau dibuang. <i>High Pass Filtering</i> adalah salah satu dari metode penajaman <i>(sharpening).</i> 

<p align="justify"> Tujuan utama dari proses penajaman ini adalah untuk menyoroti detail-detail halus dalam gambar atau untuk meningkatkan detail yang telah dikaburkan baik dalam kesalahan atau efek alami dari proses akuisisi citra tertentu.

### __Kegunaan__

- __High-Pass Filter__ sering disebut juga sebagai filter penajaman tepi __(edge sharpening)__ karena HPF digunakan dalam proses penajaman citra. 
- Operasi penajaman citra bertujuan untuk memperjelas tepi pada objek di dalam citra atau menghilangkan bagian citra yang lembut.
- Karena penajaman citra lebih berpengaruh pada tepi __(edge)__ objek, maka penajaman citra sering disebut juga penajaman tepi __(edge sharpening)__ atau peningkatan kualitas tepi __(edge enhancement)__.

### __Aturan-Aturan Dalam High-Pass Filter__

1. Koefisien penapis boleh negatif, nol, ataupun bernillai positif.
2. Total keseluruhan koefisiennya ialah bernilai 0 ataupun 1.
3. Apabila jumlah koefisiennya berjumlah = 0, maka setiap elemen yang rendah frekuensinya nilainya akan menurun. 
4. Namun, apabila total dari koefisien adalah = 1, maka elemen yang memiliki frekuensi rendah nilainya tetap sama dengan nilai semula.

### __Kode HPF Manual__

<p align="center"><img width="550" src="img/hpf_manual.jpeg"></p>

Output :

<p align="center"><img width="650" src="img/hasil_hpf_manual.jpeg"></p>

### __High Pass Filtering Menggunakan Octave__

<p align="center"><img width="500" src="img/kode_highpass.png"></p>

Output :

<p align="center"><img width="900" src="img/output_highpass.png"></p>

<br>

<h1 align="center">Median Filtering</h1>

<p align="justify"><i>Median Filtering</i> merupakan teknik penyaringan digital nonlinear, sering digunakan untuk menghilangkan noise. Penyaringan median sangat banyak digunakan dalam pemrosesan gambar digital karena mempertahankan tepi sambil menghilangkan <i>noise. Median Filtering</i> dilakukan pada matriks citra dengan cara mencari median dari piksel tetanggaan dengan menggunakan jendela yang menggeser piksel demi piksel.

### __Bentuk Penerapan__

<p align="justify">Penerapan dari <i>median filtering</i> dapat berupa untuk peningkatan kualitas citra gambar yang mengalami penurunan mutu citra, misalnya karena mengandung cacat atau derau <i>(noise)</i>. Contohnya adalah bintik hitam atau putih yang muncul secara acak yang tidak diinginkan di dalam citra. bintik acak ini disebut dengan derau <i>(noise) salt & pepper.</i>

### Kode Median Filtering Manual

<p align="center"><img width="550" src="img/median_manual.png"></p>

Output :

<p align="center"><img width="650" src="img/hasil_median_manual.jpeg"></p>

### Kode Menggunakan Function pada Octave</h3>

<p align="center"><img width="550" src="img/median_fungsi.png"></p>

Output :

<p align="center"><img width="650" src="img/hasil_median_fungsi.jpeg"></p>

