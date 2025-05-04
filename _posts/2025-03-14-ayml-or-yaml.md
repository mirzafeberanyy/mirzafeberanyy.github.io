---
layout : post
tittle : "YML or YAML"
---

Penjelasan tentang YAML (YML).

### A. Apa Itu YAML

YAML (singkatan dari: YAML Ain’t Markup Language) adalah format file berbasis teks yang digunakan untuk menyimpan data konfigurasi secara ringkas, mudah dibaca manusia, dan sering digunakan dalam DevOps dan pengembangan aplikasi.

File YAML biasanya berekstensi:  `.yaml` atau `.yml `(keduanya sama saja)

### B. Kegunaan YAML

>| Digunakan di       | Contoh Penggunaan                         |
| :------------------ | :----------------------------------------- |
| *Jekyll*         | Konfigurasi situs di `_config.yml`        |
| *GitHub Actions*........ | Workflow otomatis di `.github/workflows/` |
| *Docker Compose* | Menjalankan banyak container Docker       |
| *Kubernetes*     | Deskripsi pod, service, deployment        |
| *CI/CD Tools*    | CircleCI, Travis CI, GitLab CI            |
| *Ansible*        | Manajemen otomatisasi server              |

### C. Aturan Penulisan YAML

>| Aturan                                     | Penjelasan                                 |
| ------------------------------------------ | ------------------------------------------ |
| **Indentasi pakai spasi (bukan tab)**      | Wajib menggunakan *2 spasi atau 4 spasi* |
| **Sensitif terhadap spasi**                | Salah indentasi = error                    |
| **Tidak ada tanda kurung atau titik koma**..... | Lebih ringkas daripada JSON                |
| **Komentar diawali `#`**                   | Bisa beri catatan                          |

### D. Keuntungan Pakai YAML

- Mudah dibaca dan ditulis
- Cocok untuk konfigurasi
- Populer di tools modern (Jekyll, GitHub, Docker, dll)
- Bisa menangani struktur data kompleks (list, nested)

### E. Kelemahan YAML

- Rentan error jika indentasi salah
- Tidak cocok untuk menyimpan data jumlah besar (lebih cocok pakai JSON/Database)

### F. Kesimpulan

- YAML/YML adalah format konfigurasi teks populer, simpel, dan sangat terbaca manusia.
- Digunakan dalam berbagai tools modern seperti Jekyll, GitHub Actions, Docker, dan Kubernetes.
- Memiliki sintaks yang mudah, tapi harus sangat hati-hati pada spasi dan indentasi.

*gambar YAML or YML*

![HTML Link dan Lists](/assets/images/gambar6.png)