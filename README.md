# rangkuman_pertemuan1-2
📘 Modul Praktikum Basis Data

Ringkasan Penjelasan Bab 1 & Bab 2


---

📌 Pendahuluan

Repository ini berisi rangkuman dua bab awal modul praktikum Basis Data, yaitu:

1. Bab 1 – Konversi ERD ke Skema Relasi


2. Bab 2 – Pengantar Basis Data & DDL



Penjelasan disusun agar mudah dipahami mahasiswa yang baru pertama kali belajar database.


---

🧩 BAB 1 – Review Konversi ER Diagram ke Skema Relasi

Bab ini membahas bagaimana sebuah sistem digambarkan dalam bentuk diagram (ERD), lalu diubah menjadi tabel yang dapat dibuat di MySQL.


---

🔍 Apa itu Basis Data?

Basis data adalah kumpulan data yang terorganisasi.
Data disimpan dalam tabel yang berisi baris (record) dan kolom (field).

Contoh basis data apotek:

tabel pasien

tabel obat

tabel pembayaran


Tujuan basis data → menyimpan data agar mudah dicari, diolah, dan dipelihara.


---

🔍 Apa itu ERD (Entity Relationship Diagram)?

ERD adalah diagram yang menggambarkan struktur data dalam suatu sistem.
Diagram ini menunjukkan:

objek apa saja yang ada (entitas)

data apa saja yang dimiliki (atribut)

dan saling berhubungan atau tidak (relasi)



---

🔍 Komponen-Komponen ERD

1️⃣ Entitas

Entitas adalah objek di dunia nyata yang ingin disimpan datanya.

Contoh entitas pada sistem apotek:

Pasien

Pegawai

Obat

Resep

Pembayaran


2️⃣ Atribut

Atribut adalah informasi yang dimiliki entitas.

Contoh:
Entitas Pasien punya atribut:

Nama Pasien

Alamat

Tanggal Lahir

No Rekam Medis (sekaligus PK)


3️⃣ Primary Key (PK)

Atribut unik yang membedakan setiap data.

Contoh:

KodeObat

NoResep

NIM

IDPegawai


4️⃣ Relationship (Relasi)

Relasi adalah hubungan antar entitas.

Contoh relasi:

Pasien memiliki Resep

Pegawai melayani Pembayaran

Resep berisi Obat


5️⃣ Kardinalitas

Menjelaskan berapa banyak hubungan terjadi.

Jenis kardinalitas:

1 : 1 → satu data berhubungan dengan satu data lain

1 : N → satu data berhubungan dengan banyak data

N : M → banyak ke banyak



---

🔄 Konversi ERD → Tabel Relasi

Bagian terpenting bab 1 adalah aturan konversi.
Berikut penjelasan lengkapnya:

1. Strong Entity → Tabel

Entitas biasa langsung menjadi tabel.

Contoh entitas Pegawai → tabel pegawai.

2. Composite Attribute → Dipecah

Atribut majemuk dipecah jadi beberapa kolom.

Contoh:
Alamat → Jalan, Kota, Provinsi

3. Multivalue Attribute → Tabel Baru

Atribut yang bisa punya banyak nilai tidak boleh disimpan dalam 1 kolom.

Contoh:
Pasien memiliki banyak nomor telepon → buat tabel telp_pasien.

4. Weak Entity → Mengikuti Induk

Entitas ini tidak bisa berdiri sendiri → PK-nya gabungan.

5. Relasi 1 : 1 → Tambah FK

Salah satu tabel menerima FK dari tabel pasangannya.

6. Relasi 1 : N → FK di sisi N

Sisi “banyak” menyimpan foreign key.

7. Relasi N : M → TABEL BARU

Pasti menjadi tabel baru yang menyimpan:

id entitas pertama

id entitas kedua

atribut relasi (jika ada)


Contoh: Resep —< DetailObat >— Obat


---

🧩 BAB 2 – Pengantar Basis Data & DDL

Bab ini mengenalkan konsep dasar database serta perintah dasar SQL untuk mengelola struktur database.


---

🔍 Apa itu DBMS?

DBMS (Database Management System) adalah software pengelola basis data.
Fungsinya:

menyimpan data

mengakses data

menjaga keamanan data

mencegah data ganda

menghubungkan tabel


Contoh DBMS:

MySQL / MariaDB

PostgreSQL

SQL Server

Oracle



---

🔍 Apa itu MySQL?

MySQL adalah DBMS open source yang populer karena:

cepat

gratis

digunakan banyak aplikasi web

mudah dipelajari


Di XAMPP versi baru, MySQL digantikan MariaDB, tapi perintah SQL tetap sama.


---

🔍 Mengakses MySQL di Command Line

Masuk:

mysql -u root -p

Keluar:

\q

Lokasi penyimpanan database:

Windows: C:\xampp\mysql\data\

Linux: /opt/lampp/var/mysql/



---

🔍 Apa itu DDL?

DDL (Data Definition Language) adalah perintah SQL untuk membuat dan mengatur struktur database.

Contoh operasi DDL:

Membuat database

Menghapus database

Menggunakan database



---

🧱 Perintah DDL Dasar

1️⃣ Membuat Database

CREATE DATABASE nama_database;

2️⃣ Melihat Semua Database

SHOW DATABASES;

3️⃣ Mengaktifkan Database

USE nama_database;

4️⃣ Menghapus Database

DROP DATABASE nama_database;


---

📅 Rangkuman Pertemuan

Pertemuan	Materi	Penjelasan

1	Pengenalan Basis Data	Apa itu database, tabel, record, DBMS
2	ERD & Komponen	Penjelasan entitas, atribut, PK, relasi, kardinalitas
3	Konversi ERD → Tabel	Aturan strong entity, weak entity, 1:N, N:M
4	DDL MySQL	Perintah membuat database, memilih, dan menghapus

