📘 Modul Praktikum Basis Data

Ringkasan Bab 1 & Bab 2


---

📌 Pendahuluan

Repository ini berisi rangkuman dua bab awal praktikum Basis Data, yaitu:

1. Bab 1 – Konversi ERD ke Skema Relasi


2. Bab 2 – Pengantar Basis Data & DDL



Rangkuman dibuat agar mudah dipahami oleh pemula yang baru belajar database.


---

🧩 BAB 1 – Konversi ER Diagram ke Skema Relasi

Bab ini menjelaskan bagaimana sebuah ERD menggambarkan struktur data dan bagaimana diagram tersebut diubah menjadi tabel relasional di MySQL.


---

🔍 Apa itu Basis Data?

Basis data adalah kumpulan data terorganisasi yang disimpan dalam tabel berisi kolom (field) dan baris (record).

Contoh pada sistem apotek:

tabel pasien

tabel obat

tabel pembayaran


Tujuan: data mudah dicari, diolah, dan dipertahankan konsistensinya.


---

🔍 Apa itu ERD?

ERD (Entity Relationship Diagram) adalah diagram yang menggambarkan struktur data, berisi:

Entitas (objek)

Atribut (informasi)

Relasi antar entitas



---

🔍 Komponen ERD (Singkat)

Entitas → objek seperti Pasien, Pegawai, Obat

Atribut → informasi entitas (Nama, Alamat, dll)

Primary Key (PK) → pembeda unik (NIM, KodeObat, IDPegawai)

Relasi → hubungan antar entitas (Pasien–Resep, Pegawai–Pembayaran)

Kardinalitas → bentuk hubungan (1:1, 1:N, N:M)



---

🔄 Konversi ERD → Tabel

1. Strong Entity → Tabel


2. Composite Attribute → Dipecah (Alamat → Jalan, Kota, Provinsi)


3. Multivalue Attribute → Tabel Baru (Pasien punya banyak nomor telepon)


4. Weak Entity → PK Gabungan


5. Relasi 1:1 → Tambah FK


6. Relasi 1:N → FK di sisi N


7. Relasi N:M → Tabel Relasi Baru
Contoh: Resep — DetailObat — Obat




---

🧩 BAB 2 – Pengantar Basis Data & DDL

Bab ini mengenalkan dasar-dasar database, DBMS, MySQL, dan perintah dasar kategori DDL.


---

🔍 Apa itu DBMS?

DBMS (Database Management System) adalah software untuk mengelola basis data.

Contoh DBMS:

MySQL / MariaDB

PostgreSQL

SQL Server

Oracle


Fungsi DBMS: menyimpan data, mengakses data, menghubungkan tabel, dan mencegah duplikasi.


---

🔍 Apa itu MySQL?

MySQL adalah DBMS open-source yang:

cepat

stabil

gratis

mudah digunakan

banyak dipakai dalam aplikasi web


Di XAMPP modern, MySQL digantikan MariaDB, namun perintah SQL tetap sama.


---

🔍 Mengakses MySQL via Command Line

Masuk MySQL:

mysql -u root -p

Keluar MySQL:

\q

Lokasi penyimpanan database:

Windows → C:\xampp\mysql\data\

Linux → /opt/lampp/var/mysql/



---

🔍 Apa itu DDL?

DDL (Data Definition Language) adalah perintah SQL untuk mengatur struktur database, seperti:

membuat database

menghapus database

memilih database



---

🧱 Perintah DDL Dasar

1️⃣ Membuat database

CREATE DATABASE nama_database;

2️⃣ Melihat semua database

SHOW DATABASES;

3️⃣ Mengaktifkan database

USE nama_database;

4️⃣ Menghapus database

DROP DATABASE nama_database;


---

📅 Rangkuman Pertemuan

Berikut tabel markdown yang rapi untuk README:

| Pertemuan | Materi                 | Penjelasan Singkat                              |
|-----------|-------------------------|--------------------------------------------------|
| 1         | Pengenalan Basis Data   | Apa itu database, tabel, record, dan DBMS       |
| 2         | ERD & Komponen          | Entitas, atribut, PK, relasi, dan kardinalitas  |
| 3         | Konversi ERD → Tabel    | Aturan strong entity, weak entity, 1:N, N:M     |
| 4         | DDL MySQL               | CREATE, SHOW, USE, DROP untuk manajemen database|
