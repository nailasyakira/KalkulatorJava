# Kalkulator Java

### Deskripsi

Kalkulator Java adalah aplikasi kalkulator sederhana berbasis Graphical User Interface (GUI) yang dibuat menggunakan bahasa pemrograman Java. Aplikasi ini memiliki tampilan seperti kalkulator pada umumnya dengan tombol angka, operator, dan beberapa fungsi tambahan.

Program dibuat menggunakan komponen GUI dari Java Swing dan AWT. Swing digunakan untuk membuat komponen seperti jendela, tombol, label, dan panel, sedangkan AWT digunakan untuk pengaturan warna, font, layout, serta event pada aplikasi.


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

### Cara Menjalankan

Pastikan Java Development Kit (JDK) sudah terpasang pada komputer.
Buka terminal pada folder project, kemudian lakukan,
*Compile:*
```
javac Kalkulator.java 
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

## Tim Pengembang

| Nama | NPM |
| :--- | :--- |
| **Keisya Zahira** | 250810701100038 |
| **Naila Syakira Bahri** | 250810701100042 |
| **Abrar Muda** | 250810701100080 |
