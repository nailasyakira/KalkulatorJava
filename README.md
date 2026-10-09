# Kalkulator Java

### Deskripsi

Kalkulator Java adalah aplikasi kalkulator sederhana berbasis Graphical User Interface (GUI) yang dibuat menggunakan bahasa pemrograman Java. Aplikasi ini memiliki tampilan seperti kalkulator pada umumnya dengan tombol angka, operator, dan beberapa fungsi tambahan.

Program dibuat menggunakan komponen GUI dari Java Swing dan AWT. Swing digunakan untuk membuat komponen seperti jendela, tombol, label, dan panel, sedangkan AWT digunakan untuk pengaturan warna, font, layout, serta event pada aplikasi.

### Tujuan

Aplikasi Kalkulator Java dibuat untuk membantu pengguna melakukan perhitungan matematika dasar melalui antarmuka grafis yang sederhana dan mudah digunakan. Proyek ini juga bertujuan untuk menerapkan pemrograman Java, penggunaan komponen GUI dengan Swing dan AWT, serta pengelolaan event pada aplikasi desktop.

### Fitur

- Penjumlahan (+)
- Pengurangan (-)
- Perkalian (×)
- Pembagian (÷)
- Persentase (%)
- Positif/Negatif (+/-)
- Bilangan desimal (.)
- Reset (AC)

### Struktur 

- App.java → file utama untuk menjalankan program.
- Kalkulator.java → berisi tampilan dan fungsi kalkulator.

### Teknologi

- **Java** sebagai bahasa pemrograman.
- **Java Swing** untuk membuat komponen GUI seperti JFrame, JButton, JLabel, dan JPanel.
- **AWT (Abstract Window Toolkit)** untuk mendukung pengaturan warna, font, layout, dan event pada GUI.

### Cara Menjalankan/Instalasi

Pastikan Java Development Kit (JDK) sudah terpasang pada komputer.

1. Unduh atau clone repositori GitHub ke komputer.
2. Buka folder proyek melalui terminal atau Visual Studio Code.
3. Pastikan file App.java dan Kalkulator.java berada di lokasi yang sesuai.
4. Buka terminal pada folder project, kemudian lakukan,
   
*Compile:*
```
javac App.java 
```
*Jalankan*
```
java App
```

### Tampilan Program

Kalkulator memiliki ukuran layar 360 × 540 pixel. Tombol disusun menggunakan GridLayout dengan 5 baris dan 4 kolom.
Semua tombol kalkulator disimpan dalam array nilaiTombol, yaitu:

```
AC  +/-  %  ÷
7   8    9  ×
4   5    6  -
1   2    3  +
0   .    √  =
```

### Cara Penggunaan

Masukkan angka, pilih operator, masukkan angka kedua, kemudian tekan = untuk mendapatkan hasil perhitungan.

### Contoh I/O

Contoh 1: Penjumlahan

Input: 10 + 5
Output: 15

Contoh 2: Pengurangan

Input: 10 - 4
Output: 6

Contoh 3: Perkalian

Input: 6 × 3
Output: 18

Contoh 4: Pembagian

Input: 20 ÷ 4
Output: 5

Contoh 5: Persentase

Input: 50%
Output: Sesuai dengan implementasi fungsi persentase pada aplikasi.

### Catatan Penggunaan

- Tekan tombol AC untuk menghapus input dan mengatur ulang kalkulator.
- Gunakan tombol +/− untuk mengubah tanda bilangan jika didukung oleh input yang sedang ditampilkan.
- Gunakan tombol titik untuk memasukkan bilangan desimal.
- Tekan tombol = untuk menampilkan hasil perhitungan.

## Tim Pengembang

| Nama | NPM |
| :--- | :--- |
| **Keisya Zahira** | 250810701100038 |
| **Naila Syakira Bahri** | 250810701100042 |
| **Abrar Muda** | 250810701100080 |
