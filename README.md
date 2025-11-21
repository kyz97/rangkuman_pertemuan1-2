h📘 Modul Praktikum Basis Data

Ringkasan Bab 1 & Bab 2


---

📌 Pendahuluan

Repository ini berisi rangkuman dua bab awal praktikum Basis Data, yaitu:

1. Bab 1 – Konversi ERD ke Skema Relasi


2. Bab 2 – Pengantar Basis Data & DDL



Rangkuman dibuat agar mudah dipahami bagi pemula yang baru belajar database.


---

🧩 BAB 1 – Konversi ER Diagram ke Skema Relasi

Bab ini menjelaskan bagaimana sebuah ERD menggambarkan struktur data dan bagaimana diagram tersebut diubah menjadi tabel relasional di MySQL.


---

🔍 Apa itu Basis Data?

Basis data adalah kumpulan data terorganisasi yang disimpan dalam tabel berisi kolom (field) dan baris (record).
Contoh pada sistem apotek: tabel pasien, obat, pembayaran.

Tujuan: data mudah dicari, diolah, dan dijaga konsistensinya.


---

🔍 Apa itu ERD?

ERD (Entity Relationship Diagram) adalah diagram struktur data yang menunjukkan:

entitas (objek),

atribut (informasi),

dan relasi antar entitas.



---

🔍 Komponen ERD (Singkat)

Entitas → objek seperti Pasien, Pegawai, Obat

Atribut → informasi entitas (Nama, Alamat, dll)

Primary Key → pembeda unik (NIM, KodeObat, IDPegawai)

Relasi → hubungan antar entitas (Pasien–Resep, Pegawai–Pembayaran)

Kardinalitas → jenis hubungan (1:1, 1:N, N:M)



---

🔄 Konversi ERD → Tabel

1. Strong Entity → Tabel


2. Composite Attribute → Dipecah (Alamat → Jalan, Kota, Provinsi)


3. Multivalue Attribute → Tabel Baru (Pasien punya banyak nomor telepon)


4. Weak Entity → PK Gabungan


5. Relasi 1:1 → Tambah FK


6. Relasi 1:N → FK di sisi N


7. Relasi N:M → Tabel Relasi Baru (contoh: Resep–DetailObat–Obat)




---

🧩 BAB 2 – Pengantar Basis Data & DDL

Bab ini mengenalkan konsep dasar database, DBMS, MySQL, serta perintah dasar DDL.


---

🔍 Apa itu DBMS?

DBMS (Database Management System) adalah software untuk mengelola basis data.

Contoh: MySQL, MariaDB, PostgreSQL, SQL Server, Oracle.

Fungsi: menyimpan data, mengakses data, menghubungkan tabel, mencegah duplikasi.


---

🔍 Apa itu MySQL?

MySQL adalah DBMS open-source yang:

cepat, gratis, stabil,

mudah digunakan,

umum dipakai di aplikasi web.


Di XAMPP modern, MySQL digantikan MariaDB, tetapi perintah SQL tetap sama.


---

🔍 Mengakses MySQL via Command Line

Masuk:

mysql -u root -p

Keluar:

\q

Lokasi penyimpanan database:

Windows → C:\xampp\mysql\data\

Linux → /opt/lampp/var/mysql/



---

🔍 Apa itu DDL?

DDL (Data Definition Language) adalah perintah SQL untuk mengatur struktur database seperti membuat atau menghapus database dan tabel.


---

🧱 Perintah DDL Dasar

Membuat database

CREATE DATABASE nama_database;

Melihat semua database

SHOW DATABASES;

Mengaktifkan database

USE nama_database;

Menghapus database

DROP DATABASE nama_database;



---

## 📅 Rangkuman Pertemuan

| Pertemuan | Materi                   | Penjelasan Singkat                                     |
|-----------|--------------------------|---------------------------------------------------------|
| 1         | Pengenalan Basis Data    | Dasar database, tabel, record, serta fungsi DBMS       |
| 2         | ERD & Komponen           | Entitas, atribut, PK, relasi, dan kardinalitas         |
| 3         | Konversi ERD → Tabel     | Aturan strong/weak entity, 1:N, 1:1, dan N:M           |
| 4         | DDL MySQL                | Perintah dasar CREATE, SHOW, USE, DROP untuk database  |
