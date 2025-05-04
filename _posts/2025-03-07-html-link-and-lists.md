---
layout : post
tittle : "HTML Link and Lists"
---

Penjelasan tentang link dan lists pada HTML.

### A. Apa itu Link

Link (tautan) digunakan untuk menghubungkan antar halaman web, baik dalam satu situs maupun ke luar situs. Dalam HTML, tag yang digunakan adalah `<a>` (anchor).

### B. Sintaks Dasar Link

> `<a href="https://www.example.com">Klik di sini</a>`  
- `<a>` = tag pembuka anchor
- `href` = atribut untuk menetapkan alamat tujuan
- Teks antara `<a>` dan `</a>` adalah yang akan tampil di halaman
- Contoh hasil: **Klik di sini**

### C. Jenis-jenis Link

>| Jenis                      | Contoh                                               | Keterangan                             |
| :-------------------------- | :---------------------------------------------------- | :-------------------------------------- |
| *Link eksternal*         | `<a href="https://google.com">Google</a>`            | Menuju situs lain                      |
| *Link internal*          | `<a href="about.html">Tentang Kami</a>`              | Menuju halaman dalam situs             |
| *Link ke bagian halaman*..... | `<a href="#kontak">Hubungi</a>`                      | Menuju bagian dalam halaman yang sama  |
| *Link email*             | `<a href="mailto:email@example.com">Kirim Email</a>`..... | Membuka email client                   |
| *Link telpon*            | `<a href="tel:+628123456789">Hubungi</a>`            | Menjalankan panggilan telepon (mobile) |

### D. Apa itu List

List adalah elemen HTML untuk menampilkan informasi dalam bentuk daftar terurut (ordered) atau tidak terurut (unordered).

### E. Jenis-Jenis List
>**1. Unordered List (Daftar Tidak Terurut):**
- Menggunakan tag `<ul>` (unordered list)
- Item menggunakan `<li>` (list item)
- Ditampilkan dengan simbol (•, ○)

>**2. Ordered List (Daftar Terurut):**
- Menggunakan tag `<ol>` (ordered list)
- Item dengan `<li>`, tapi diberi nomor (1, 2, 3...)

>**3. Description List (Daftar Penjelasan):**
- Gunakan `<dl>` (description list)
- `<dt>` untuk judul daftar, `<dd>` untuk deskripsi

### F. Atribut Tambahan pada Ordered List

>| Atribut     | Fungsi                                 |
| :----------- | :-------------------------------------- |
| `type="A"`  | Urutan dengan huruf besar (A, B, C...) |
| `type="a"`  | Huruf kecil (a, b, c...)               |
| `type="I"`  | Angka Romawi besar (I, II, III...)     |
| `start="5"`......... | Mulai dari angka tertentu              |

### G. Kesimpulan

>| Elemen      | Kegunaan                          |
| :----------- |:--------------------------------- |
| `<a>`       | Membuat tautan ke halaman lain    |
| `<ul>`      | Daftar tanpa urutan               |
| `<ol>`      | Daftar terurut (bernomor)         |
| `<dl>`      | Daftar penjelasan/kamus           |
| `<li>`      | Item dalam daftar                 |
| `<dt>/<dd>` ..........| Judul dan penjelasan dalam `<dl>` |

*gambar Link dan List pada HTML*

![HTML Link dan Lists](/assets/images/gambar5.jpg)