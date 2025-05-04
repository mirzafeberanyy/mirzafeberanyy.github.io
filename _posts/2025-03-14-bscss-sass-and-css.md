---
layout : post
tittle : "SCSS, SASS and CSS"
---

Penjelasan tentang SCSS, SASS dan CSS.

### A. CSS (Cascading Style Sheets)

>**1. Apa itu CSS**

>CSS adalah bahasa untuk mengatur tampilan (style) halaman HTML. Dengan CSS, kamu bisa mengatur warna, font, layout, animasi, dan banyak lagi.

>**2. Ciri-ciri CSS**

>| Aspek          | Penjelasan                    |
| :-------------- | :----------------------------- |
| Sintaks        | Sederhana dan langsung        |
| File eksternal | **.css**                        |
| Ditulis manual | Ya                            |
| Komponen dasar...... | Selektor, properti, dan nilai |


### B. SASS (Syntactically Awesome Stylesheets)

SASS adalah preprocessor CSS – artinya, kamu menulis dalam format SASS dan dikompilasi menjadi CSS biasa. Tujuan utamanya adalah mempermudah penulisan CSS yang kompleks.

SASS hadir dalam dua format penulisan:

- SASS (indentasi-based) ➜ Tanpa tanda kurung {} dan titik koma ;
- SCSS (Sassy CSS) ➜ Format mirip CSS tapi dengan fitur SASS

### C. SCSS (Sassy CSS)

SCSS adalah varian dari SASS yang menggunakan sintaks seperti CSS, tapi mendukung fitur SASS. Ini adalah format yang paling umum digunakan oleh developer saat ini.

### D. Fitur-Fitur SASS / SCSS yang tidak ada di CSS Biasa

>| Fitur                              | Penjelasan  | Contoh           |
| :--------------------------------- | :---------------------------------- | :---------------------------------------------- |
| *Variabel*                      | Simpan nilai untuk digunakan ulang..... | `$warna-utama: #3498db;`                     |
| *Nesting (penulisan bersarang)*.... | Tulis selector di dalam selector   | `.menu { ul { li { color: red; }}}`     |
| *Partial & Import*              | Bagi file besar jadi kecil         | `_header.scss` lalu `@import 'header';`     |
| *Mixins*                        | Seperti fungsi untuk CSS    | `@mixin border-radius($radius) { border-radius: $radius; }` |
| *Inheritance*                   | Warisi gaya dari selector lain     | `@extend .button `                    |
| *Operators*                     | Gunakan operasi matematika         | `width: 100% / 3;`             |


### E. Kelebihan SASS / SCSS

- DRY (Don't Repeat Yourself)
- Lebih mudah dikelola saat proyek besar
- Bisa pakai fungsi, variabel, dan logic
- Modular dengan partial & import

### F. Kekurangan

- Perlu compiler tambahan
- Ada kurva belajar dibandingkan CSS biasa

### H. Kesimpulan

>| Aspek                                                | CSS   | SASS   | SCSS         |
| :---------------------------------------------------- | :-----: | :------: | :------------: |
| Standar browser                                      | Ya    | Tidak  | Tidak        |
| Butuh compiler                                       | Tidak | Ya     | Ya           |
| Sintaks ringkas                                      | Cukup.... | Ya     | Ya           |
| Mendukung fitur lanjutan (variabel, fungsi, nesting)..... | Tidak | Ya     | Ya           |
| Digunakan luas                                       | Ya    | Kurang | Ya (populer) |


*gambar scss, sass dan css*

![HTML Link dan Lists](/assets/images/gambar7.jpg)