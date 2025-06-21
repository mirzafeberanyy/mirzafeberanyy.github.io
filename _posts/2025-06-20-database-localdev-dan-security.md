---
layout : post
tittle : "Data Base, Local Development dan Keamanan"
---

Penjelasan tentang Data Base, Local Development dan Keamanan.

### A. Database & ORM Tools

#### Apa itu Database, ORM, dan GUI Tools?

#### Database (Basis Data)

Tempat menyimpan dan mengelola data aplikasi secara terstruktur, agar dapat diakses, dimodifikasi, atau dihapus dengan mudah.

#### SQL Database (Relational Database)

SQL (Structured Query Language) adalah bahasa standar untuk mengelola dan mengakses data pada sistem basis data relasional (RDBMS). Database SQL menyimpan data dalam bentuk tabel-tabel yang saling terhubung melalui relasi, dan sangat cocok untuk aplikasi yang membutuhkan struktur data yang terorganisir dan konsisten.

Berikut ini adalah enam sistem manajemen basis data relasional (RDBMS) paling populer:

**1. MySQL**
- MySQL adalah database SQL open source yang paling banyak digunakan di seluruh dunia, terutama untuk pengembangan web.
- Digunakan oleh banyak platform besar seperti WordPress, Joomla, dan Drupal.
- Memiliki komunitas besar dan dokumentasi lengkap.
- Umumnya dipadukan dengan PHP dalam stack LAMP (Linux, Apache, MySQL, PHP).
- Cocok untuk aplikasi web, e-commerce, dan sistem akademik.
- Berikut gambar MySQL .![HTML Link dan Lists](/assets/images/mysql.webp)

**2. PostgreSQL**
- PostgreSQL adalah RDBMS open source yang terkenal karena kestabilan dan fitur canggihnya.
- Mendukung tipe data kompleks seperti array, JSON, dan juga GIS (spasial).
- Lebih strict terhadap standar SQL dan sangat disukai oleh developer backend profesional.
- Cocok untuk aplikasi yang membutuhkan validasi data kuat, indexing kompleks, dan transaksi berat.
- Berikut gambar PostgreSQL .![HTML Link dan Lists](/assets/images/postgresql.webp)

**3. SQLite**
- SQLite adalah database ringan yang disimpan sebagai satu file di sistem lokal.
- Tidak memerlukan server atau proses setup khusus.
- Sangat cocok untuk aplikasi mobile, embedded system (seperti IoT), dan prototipe.
- Banyak digunakan dalam aplikasi Android dan juga oleh browser seperti Chrome.
- Berikut gambar SQLite .![HTML Link dan Lists](/assets/images/sqllite.webp)

**4. Microsoft SQL Server**
- Merupakan RDBMS komersial yang dikembangkan oleh Microsoft.
- Terintegrasi erat dengan ekosistem .NET dan Microsoft Azure.
- Digunakan secara luas di lingkungan perusahaan dan instansi pemerintah berbasis Windows.
- Menyediakan fitur enterprise seperti integrasi reporting, analitik, dan keamanan data tinggi.
- Berikut gambar Microsoft SQL Server .![HTML Link dan Lists](/assets/images/mssqlserver.webp)

**5. MariaDB**
- MariaDB adalah "fork" dari MySQL, dikembangkan oleh pencipta MySQL sendiri setelah akuisisi MySQL oleh Oracle.
- Memiliki arsitektur yang mirip dengan MySQL, tetapi dengan tambahan fitur seperti engine penyimpanan baru dan performa lebih baik.
- 100% open source dan banyak digunakan oleh developer yang ingin lepas dari ketergantungan pada Oracle.
- Berikut gambar MariaDB .![HTML Link dan Lists](/assets/images/mariadb.webp)

**6. Oracle Database**
- Oracle adalah RDBMS komersial kelas enterprise yang sangat kuat dan kompleks.
- Memiliki fitur keamanan, skalabilitas, dan manajemen data yang sangat tinggi.
- Sering digunakan di perusahaan besar, perbankan, instansi pemerintahan, dan sistem ERP.
- Mendukung berbagai arsitektur seperti clustering, failover, dan data partitioning.
- Berikut gambar Oracle Database .![HTML Link dan Lists](/assets/images/oracledb.webp)

#### NoSQL (Non-relational Database)

NoSQL adalah jenis sistem basis data yang tidak menggunakan struktur tabel relasional seperti SQL. NoSQL dirancang untuk:
- Menangani data besar (Big Data)
- Menyimpan data tidak terstruktur (seperti JSON, dokumen, key-value)
- Skalabilitas tinggi dan performa cepat
- Cocok untuk aplikasi real-time, sosial media, IoT, hingga sistem terdistribusi

Berikut penjelasan masing-masing:

**1. MongoDB**
- MongoDB adalah NoSQL database berbasis dokumen, di mana data disimpan dalam format BSON (versi binary dari JSON).
- Struktur data sangat fleksibel — kamu tidak perlu skema tetap seperti SQL.
- Mendukung query kompleks, indexing, agregasi, dan replikasi.
- Sangat populer dalam aplikasi Node.js dan digunakan oleh banyak startup serta perusahaan besar.
- Cocok untuk aplikasi real-time, dashboard, sistem user-profile, hingga e-commerce modern.
- Berikut gambar MongoDB .![HTML Link dan Lists](/assets/images/mongodb.webp)


**2. Firebase Realtime Database**
- Merupakan layanan database berbasis cloud dari Google yang menyimpan data dalam format JSON.
- Data disimpan dan disinkronkan secara real-time ke semua client yang terhubung.
- Cocok untuk aplikasi kolaboratif seperti chat, whiteboard, notulensi bersama, game multiplayer ringan.
- Satu kelemahannya: struktur datanya kurang cocok untuk query yang kompleks.
- Berikut gambar Firebase Realtime Database .![HTML Link dan Lists](/assets/images/firebasedb.webp)

**3. Firestore**
- Penerus dari Firebase Realtime Database, juga dikembangkan oleh Google.
- Memiliki struktur data berupa koleksi dan dokumen yang lebih rapi dan scalable.
- Mendukung query kompleks, indexing otomatis, dan keamanan berbasis role (Firestore Rules).
- Sangat cocok untuk aplikasi web & mobile modern, terutama yang dibangun dengan Flutter atau React Native.
- Berikut gambar Firestore .![HTML Link dan Lists](/assets/images/firestore.webp)

**4. CouchDB**
- Database dokumen seperti MongoDB, tetapi menonjol dalam fitur replikasi dan offline sync.
- Menggunakan format JSON dan mendukung query melalui HTTP REST API.
- Cocok untuk aplikasi offline-first, yang bisa digunakan tanpa koneksi internet dan disinkronkan kembali nanti.
- Berikut gambar CouchDB .![HTML Link dan Lists](/assets/images/couchdb.webp)

**5. Cassandra**
- Merupakan column-family NoSQL database yang sangat kuat dan highly scalable.
- Dirancang untuk menangani data dalam skala terdistribusi di banyak server, cocok untuk skenario Big Data.
- Banyak digunakan oleh perusahaan besar seperti Netflix, Facebook, dan Instagram.
- Ideal untuk aplikasi dengan jutaan pengguna dan permintaan tinggi yang tersebar global.
- Berikut gambar Cassandra .![HTML Link dan Lists](/assets/images/cassandra.webp)

**6. Redis**
- Redis adalah in-memory key-value store. Artinya, semua data disimpan di RAM, menjadikannya sangat cepat.
- Cocok digunakan untuk caching, session storage, pub-sub system, leaderboard game, dan antrian pesan
- Bisa juga digunakan sebagai temporary database atau pelengkap sistem utama
- Berikut gambar Redis .![HTML Link dan Lists](/assets/images/redisdb.webp)

#### Singkatnya:

- MongoDB → *serbaguna, skema fleksibel, cocok untuk web modern*
- Firebase / Firestore → *real-time, cocok untuk aplikasi mobile/chat*
- CouchDB → *sync offline-online, cocok untuk aplikasi tanpa koneksi stabil*
- Cassandra → *big data dan sistem terdistribus*
- Redis → *performa supercepat, cache, antrian, session data*

#### ORM & ODM (Object-Relational / Object-Document Mapping)

ORM (Object Relational Mapping) dan ODM (Object Document Mapping) adalah alat bantu bagi developer untuk berinteraksi dengan database menggunakan kode pemrograman, tanpa harus menulis query SQL (atau MongoDB query) secara langsung.
- Dengan ORM/ODM:
    - Objek dalam kode (class/model) akan mewakili tabel atau dokumen di database.
    - Developer bisa menggunakan metode pemrograman biasa untuk insert, update, delete, dan query, tanpa harus menulis SQL secara manual.

**1. Sequelize (Node.js)**
- ORM untuk Node.js yang mendukung berbagai RDBMS seperti MySQL, PostgreSQL, SQLite, dan SQL Server.
- Menggunakan pendekatan berbasis model (definisi skema), relasi antar model (one-to-many, many-to-many), dan fitur migrasi database.
- Banyak digunakan dalam proyek Node.js berbasis Express.
- Cocok untuk developer yang ingin menghindari SQL mentah dan tetap punya kendali atas relasi antar tabel.
- Berikut gambar Sequelize (Node.js) .![HTML Link dan Lists](/assets/images/sequelizejs.webp)

**2. Prisma (Node.js)**
- ORM modern untuk Node.js yang sangat cepat, efisien, dan type-safe.
- Menggunakan pendekatan skema deklaratif (schema.prisma) untuk mendefinisikan struktur database, lalu Prisma akan menghasilkan client khusus untuk mengakses database dengan mudah.
- Mendukung MySQL, PostgreSQL, SQLite, SQL Server, dan MongoDB.
- Terintegrasi erat dengan TypeScript, menjadikannya favorit di kalangan developer modern.
- Cocok untuk tim profesional yang mengutamakan performa, konsistensi, dan pengalaman developer (DX).
- Berikut gambar Prisma (Node.js) .![HTML Link dan Lists](/assets/images/prismajs.webp)

**3. Mongoose (MongoDB)**
- ODM (Object Document Mapper) untuk MongoDB di lingkungan Node.js.
- Membantu developer mengelola dokumen MongoDB dengan skema yang jelas, validasi, middleware, dan fitur relasi sederhana (referensi atau embedded).
- Merupakan salah satu library paling populer untuk menghubungkan Node.js dan MongoDB.
- Cocok untuk aplikasi full-stack JavaScript dengan backend MongoDB.
- Berikut gambar Mongoose (MongoDB) .![HTML Link dan Lists](/assets/images/mongosedb.webp)

**4. TypeORM (Node.js)**
- ORM untuk Node.js yang mendukung TypeScript secara native.
- Mendukung database seperti MySQL, PostgreSQL, SQLite, dan lainnya.
- Menawarkan fitur deklarasi entitas, relasi, migrasi, dan lazy loading.
- Cocok untuk developer yang menggunakan arsitektur OOP (Object-Oriented Programming) dengan bahasa JavaScript atau TypeScript.
- Berikut gambar TypeORM (Node.js) .![HTML Link dan Lists](/assets/images/typeorm.webp)

**5. Eloquent (Laravel)**
- ORM bawaan framework Laravel (PHP).
- Mengusung sintaks yang elegan dan expressive — cukup dengan memanggil User::all() atau Post::where(...), kamu sudah bisa melakukan query database tanpa SQL.
- Mendukung relasi yang kompleks seperti one-to-many, many-to-many, polymorphic, serta fitur eager/lazy loading.
- Sangat cocok untuk web app berbasis Laravel yang ingin efisien dan readable dalam mengelola database.
- Berikut gambar Eloquent (Laravel) .![HTML Link dan Lists](/assets/images/lraveleloq.webp)

**6. SQLAlchemy (Python)**
- ORM untuk bahasa Python, mendukung berbagai database SQL seperti PostgreSQL, MySQL, SQLite, Oracle, dan lainnya.
- Sangat fleksibel: bisa digunakan dalam mode deklaratif (OOP) atau langsung (core SQL expression).
- Banyak digunakan di web framework Python seperti Flask dan FastAPI, bahkan juga di bidang data science.
- Cocok untuk developer Python yang ingin struktur kode rapi, query fleksibel, dan pengendalian penuh atas model.
- Berikut gambar SQLAlchemy (Python) .![HTML Link dan Lists](/assets/images/sqlalchemy.webp)

#### Singkatnya:

- Sequelize → *Kuat, populer di Node.js, cocok untuk SQL dengan pendekatan klasik*
- Prisma → *Modern, cepat, mendukung TypeScript, cocok untuk proyek baru*
- Mongoose → *Andalan MongoDB di Node.js, mudah digunakan*
- TypeORM → *ORM Node.js berbasis TypeScript yang powerful*
- Eloquent → *Elegan dan expressive, terbaik di Laravel*
- SQLAlchemy → *Fleksibel dan lengkap untuk Python developer*

#### GUI Tools (Graphical User Interface for Databases)

GUI Tools adalah aplikasi dengan tampilan visual (grafis) yang digunakan untuk mengelola database tanpa harus menulis perintah manual (SQL/command line). Alat ini sangat membantu bagi:
- Mahasiswa atau pemula yang belum terbiasa dengan query manual
- Admin database yang ingin bekerja lebih cepat dan efisien
- Developer yang ingin melakukan eksplorasi data secara visual

#### Penjelasan alat-alat GUI database paling umum dan populer:

**1. phpMyAdmin**
- Merupakan alat GUI berbasis web untuk mengelola MySQL dan MariaDB.
- Sering disediakan secara default pada hosting bersama (shared hosting).
- Memungkinkan pengguna untuk:
    - Membuat database dan tabel
    - Menjalankan query SQL
    - Mengimpor dan mengekspor data
    - Mengatur user dan hak akses
- Kelebihan utamanya: gratis, ringan, dan mudah digunakan langsung dari browser.
- Berikut gambar phpMyAdmin  .![HTML Link dan Lists](/assets/images/phpmyadmin.webp)

**2. DBeaver**
- Merupakan GUI multi-database yang mendukung banyak jenis DB seperti MySQL, PostgreSQL, SQLite, Oracle, MongoDB, SQL Server, dan lainnya.
- Bersifat open source dan tersedia lintas platform (Windows, Mac, Linux).
- Cocok untuk developer atau DBA (Database Administrator) yang bekerja dengan lebih dari satu jenis database.
- Memiliki fitur tambahan seperti ER Diagram, query visual builder, dan plugin analitik.
- Berikut gambar DBeaver  .![HTML Link dan Lists](/assets/images/dbeaver.webp)

**3. pgAdmin**
- Merupakan GUI resmi untuk PostgreSQL, tersedia dalam versi desktop dan web.
- Memungkinkan kamu untuk:
    - Membuat skema dan tabel
    - Mengelola user, role, dan permission
    - Menjalankan query dan melihat hasilnya secara real-time
    - Dilengkapi juga dengan visualisasi data, editor function/procedure, dan debugger untuk SQL dan PL/pgSQL.
    - Ideal untuk pengguna PostgreSQL dari tingkat pemula hingga profesional.
- Berikut gambar pgAdmin  .![HTML Link dan Lists](/assets/images/pgadmin.webp)

**4. MongoDB Compass**
- Merupakan GUI resmi dari MongoDB, dirancang khusus untuk eksplorasi data berbasis dokumen (NoSQL).
- Fitur utama meliputi:
    - Visualisasi koleksi dokumen
    - Query builder tanpa kode
    - Analisis performa indeks
    - Validasi skema otomatis
    - Sangat berguna untuk melihat isi data MongoDB secara langsung dan memodifikasi dokumen dengan lebih nyaman dibandingkan command line.
- Berikut gambar MongoDB Compass  .![HTML Link dan Lists](/assets/images/mongodbcompass.webp)

**5. Oracle SQL Developer**
- GUI resmi dari Oracle untuk mengelola Oracle Database.
- Memungkinkan pengguna untuk:
    - Membuat dan menjalankan query SQL atau PL/SQL
    - Membuat dan mengelola tabel, trigger, dan prosedur
    - Membuat laporan analisis dan ekspor data
    - Biasanya digunakan dalam lingkungan enterprise atau instansi besar yang menggunakan Oracle sebagai sistem utamanya.
- Berikut gambar Oracle SQL Developer  .![HTML Link dan Lists](/assets/images/oraclesqldev.webp)

#### Ringkasan Fungsi :

- phpMyAdmin →*web GUI untuk MySQL/MariaDB, ringan dan umum di hosting*
- DBeaver → *GUI universal untuk banyak DB sekaligus, open source*
- pgAdmin → *GUI resmi PostgreSQL, lengkap dan fleksibel*
- MongoDB Compass → *GUI MongoDB untuk eksplorasi data dokumen*
- Oracle SQL Developer → *GUI untuk Oracle Database, banyak digunakan di perusahaan besar*


### B. Local Development & Virtualization Tools

Alat-alat dalam kategori ini digunakan untuk menyediakan lingkungan pengembangan lokal (local server) dan virtualisasi (meniru lingkungan server sebenarnya di komputer pengembang). Tujuannya adalah agar developer bisa menjalankan aplikasi tanpa perlu langsung mengunggah ke internet, lebih aman, cepat, dan fleksibel saat proses coding.

**1. XAMPP**
- Merupakan paket aplikasi lokal yang berisi:   
    - Apache (web server)
    - MySQL/MariaDB (database)
    - PHP dan Perl (bahasa pemrograman)
    - Cocok untuk membangun aplikasi PHP dan MySQL secara lokal.
    - Tersedia di Windows, macOS, dan Linux.
    - Sangat populer di kalangan pemula dan mahasiswa karena mudah diinstal dan digunakan.
- Berikut gambar XAMPP  .![HTML Link dan Lists](/assets/images/xampp.webp)

**2. WAMP**
- Singkatan dari Windows + Apache + MySQL + PHP.
- Mirip seperti XAMPP, tetapi hanya tersedia untuk Windows.
- Memiliki interface GUI yang lebih sederhana dan stabil di Windows.
- Cocok untuk pengembang PHP yang hanya menggunakan Windows sebagai platform pengembangan.
- Berikut gambar WAMP  .![HTML Link dan Lists](/assets/images/wamp.webp)

**3. MAMP**
- Singkatan dari Mac + Apache + MySQL + PHP.
- Versi lokal server khusus untuk pengguna macOS, meskipun kini ada versi untuk Windows juga.
- Banyak digunakan oleh developer web yang memakai Mac untuk membuat dan menguji aplikasi PHP.
- Berikut gambar MAMP  .![HTML Link dan Lists](/assets/images/mamp.webp)

**4. Laragon**
- Merupakan local development environment untuk Windows, ringan dan modern.
- Lebih fleksibel dibanding XAMPP/WAMP, bisa digunakan untuk PHP, Node.js, Python, Ruby, Go, dll.
- Mendukung instalasi satu-klik untuk WordPress, Laravel, dan framework lain.
- Fitur auto-hosting lokal (.test domain) sangat mempermudah preview proyek.
- Cocok untuk developer yang ingin local stack yang cepat, modular, dan bisa diatur sendiri.
- Berikut gambar Laragon  .![HTML Link dan Lists](/assets/images/laragon.webp)

**5. Docker**
- Docker adalah platform containerisasi: memungkinkan kamu menjalankan aplikasi dan semua dependensinya dalam satu unit yang disebut container.
- Dengan Docker, kamu bisa memastikan bahwa aplikasi berjalan sama di semua tempat — baik di laptop, server, atau cloud.
- Sangat cocok untuk tim besar, proyek skala menengah-besar, atau aplikasi yang kompleks dan membutuhkan konsistensi lingkungan.
- Berikut gambar Docker  .![HTML Link dan Lists](/assets/images/docker.webp)

**6. Docker Compose**
- Alat tambahan dari Docker untuk menjalankan beberapa container sekaligus menggunakan satu file konfigurasi (docker-compose.yml).
- Contohnya: kamu bisa jalankan aplikasi web + database + cache server hanya dengan satu perintah.
- Memudahkan manajemen lingkungan pengembangan yang terdiri dari banyak layanan (multi-service).
- Berikut gambar Docker Compose  .![HTML Link dan Lists](/assets/images/dockercmps.webp)

**7. Vagrant**
- Alat virtualisasi yang menggunakan VirtualBox atau provider lain untuk menjalankan mesin virtual lengkap (VM).
- Vagrant memungkinkan kamu mengotomatiskan pembuatan, konfigurasi, dan distribusi VM untuk pengembangan.
- Lebih berat daripada Docker karena berbasis virtual machine, tetapi memberikan isolasi dan kontrol penuh atas sistem operasi.
- Cocok untuk proyek yang butuh environment sangat spesifik atau mirip server produksi.
- Berikut gambar Vagrant  .![HTML Link dan Lists](/assets/images/vagrant.webp)

#### Singkatnya :

- XAMPP/WAMP/MAMP → *solusi instan dan mudah untuk local server*
- Laragon → *lebih ringan dan fleksibel, ideal untuk Windows*
- Docker → *standar modern untuk environment portabel dan konsisten*
- Docker Compose → *untuk mengelola banyak container sekaligus*
- Vagrant → *solusi virtualisasi berat, tapi sangat powerful untuk simulasi server penuh*

### C. Keamanan

#### Keamanan (Security Tools & Practices)

Keamanan dalam pengembangan web mencakup perlindungan data, otentikasi pengguna, pencegahan eksploitasi, dan pengamanan komunikasi. Alat-alat berikut ini membantu developer dalam mengamankan aplikasi mereka baik saat proses development maupun saat live/produksi.

**1. OWASP ZAP (Zed Attack Proxy)**
- Merupakan alat open source untuk melakukan pengujian keamanan aplikasi web (penetration testing).
- Dikembangkan oleh OWASP (Open Web Application Security Project).
- Digunakan untuk mendeteksi kerentanan seperti SQL Injection, XSS (Cross Site Scripting), dan lainnya.
- Cocok untuk melakukan audit keamanan aplikasi web baik secara manual maupun otomatis.
- Berikut gambar OWASP ZAP (Zed Attack Proxy)  .![HTML Link dan Lists](/assets/images/owqsp.webp)

**2. Burp Suite**
- Alat profesional untuk pengujian keamanan aplikasi web, mirip dengan OWASP ZAP namun lebih lengkap dan banyak digunakan oleh penetration tester.
- Memungkinkan kamu menganalisis dan memodifikasi permintaan HTTP/S yang dikirim dari dan ke aplikasi.
- Tersedia versi Community (gratis) dan versi Professional (berbayar).
- Berikut gambar Burp Suite  .![HTML Link dan Lists](/assets/images/burp.webp)

**3. Helmet.js**
- Middleware untuk framework Express.js yang membantu mengatur HTTP headers keamanan secara otomatis.
- Melindungi aplikasi Node.js dari berbagai serangan umum seperti:
    - Clickjacking
    - MIME sniffing
    - XSS
- Mudah diimplementasikan cukup dengan app.use(helmet()) dalam aplikasi Express.
- Berikut gambar Helmet.js  .![HTML Link dan Lists](/assets/images/helmet.webp)

**4. CORS (Cross-Origin Resource Sharing)**
- Merupakan mekanisme keamanan browser untuk mengatur akses lintas domain.
- Tanpa konfigurasi CORS yang tepat, browser akan memblokir permintaan dari domain yang berbeda demi mencegah serangan seperti data theft.
- Developer harus mengatur header CORS dengan benar agar API hanya bisa diakses dari frontend yang sah.
- Berikut gambar ORS (Cross-Origin Resource Sharing)  .![HTML Link dan Lists](/assets/images/cors.webp)

**5. CSRF (Cross-Site Request Forgery)**
- Jenis serangan yang memanfaatkan sesi login pengguna untuk menjalankan perintah tidak sah.
- Pencegahan dilakukan dengan menggunakan token CSRF yang unik untuk setiap sesi/form
- Framework modern seperti Laravel, Django, dan Express biasanya sudah menyediakan middleware atau plugin untuk melindungi dari CSRF.
- Berikut gambar CSRF (Cross-Site Request Forgery)  .![HTML Link dan Lists](/assets/images/csrf.webp)

**6. HTTPS / SSL (Let’s Encrypt)**
- HTTPS mengenkripsi komunikasi antara client dan server menggunakan SSL/TLS certificate.
- Let’s Encrypt adalah layanan penyedia sertifikat SSL gratis untuk domain publik.
- Mengaktifkan HTTPS sangat penting untuk melindungi data pengguna (terutama form login, transaksi, dan data sensitif).
- Saat ini, browser modern akan menandai situs tidak aman jika hanya menggunakan HTTP.
- Berikut gambar HTTPS / SSL (Let’s Encrypt)  .![HTML Link dan Lists](/assets/images/lestencript.webp)

**7. Auth0**
- Platform as-a-service (PaaS) untuk otentikasi dan otorisasi pengguna.
- Mendukung login sosial (Google, Facebook, GitHub), SSO (Single Sign-On), serta integrasi dengan OAuth dan OpenID Connect.
- Cocok untuk aplikasi skala menengah hingga besar yang ingin keamanan login profesional tanpa membuat sistem dari nol.
- Berikut gambar Auth0  .![HTML Link dan Lists](/assets/images/autho.webp)

**8. Firebase Auth**
- Layanan otentikasi milik Google Firebase.
- Mendukung login dengan email/password, nomor telepon, Google, Facebook, GitHub, Apple, dan lain-lain.
- Sangat mudah diintegrasikan ke aplikasi web maupun mobile, khususnya bila menggunakan stack Firebase atau React Native.
- Berikut gambar Firebase Auth  .![HTML Link dan Lists](/assets/images/firebaseautho.webp)

**9. OAuth 2.0 / OpenID Connect**
- OAuth 2.0 adalah protokol untuk delegated authorization, memungkinkan pengguna memberikan akses terbatas ke aplikasimu melalui akun lain (misalnya login via Google).
- OpenID Connect (OIDC) dibangun di atas OAuth 2.0 untuk autentikasi, bukan hanya otorisasi.
- Keduanya adalah standar penting untuk integrasi login pihak ketiga (SSO) secara aman.
- Berikut gambar OAuth 2.0 / OpenID Connect  .![HTML Link dan Lists](/assets/images/outhopenid.webp)

**10. JWT (JSON Web Token)**
- Format token yang digunakan untuk menyimpan dan mengirim informasi secara aman antar pihak sebagai JSON ter-enkripsi.
- Umumnya digunakan dalam sistem autentikasi token-based, menggantikan sesi tradisional.
- JWT dapat menyimpan informasi pengguna seperti ID, role, dan waktu kadaluarsa.
- Mudah digunakan di frontend (sebagai token) dan backend (untuk verifikasi).
- Berikut gambar JWT (JSON Web Token)  .![HTML Link dan Lists](/assets/images/jwt.webp)

#### Singkatnya :

- Gunakan OWASP ZAP / Burp Suite untuk mengecek celah keamanan.
- Gunakan Helmet.js, CORS, CSRF agar server kamu lebih aman dari serangan umum.
- Pastikan aplikasi sudah menggunakan HTTPS (bisa pakai Let’s Encrypt).
- Gunakan Auth0, Firebase Auth, OAuth, dan JWT untuk sistem login yang aman dan modern.








