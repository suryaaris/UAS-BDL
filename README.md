UAS
Basis Data Lanjutan
Putu Aris Surya Kusuma - 2201010075



1. ERD (Entity Relationship Diagram)

![image](https://github.com/suryaaris/UAS-BDL/assets/173940200/5ef715ba-f129-45a8-8112-d2a6328a690f)


2. Deskripsi Proyek
Projek basis data yang saya buat yakni membangun sistem basis data yang efisien dan terstruktur untuk mengelola data toko sayur, yang mencakup pelanggan, produk, pesanan, dan detail pesanan. Komponen yang digunakan yakni:

Basis data
Tabel Customer: Menyimpan informasi pelanggan seperti ID, nama, alamat, dan nomor telepon.
Tabel Produk: Menyimpan informasi produk seperti ID, nama produk, harga, dan stok.
Tabel Order: Menyimpan informasi pesanan seperti ID pesanan, ID pelanggan, dan tanggal pesanan.
Tabel Detail: Menyimpan detail setiap pesanan seperti ID detail pesanan, ID pesanan, ID produk, dan jumlah produk.

Fungsi Agregat
SUM: Menghitung total penjualan.
COUNT: Menghitung jumlah total pesanan.
AVG: Menghitung rata-rata jumlah barang yang dipesan.

Trigger dan View
Trigger: Mengurangi stok produk secara otomatis setiap kali ada pesanan baru.
View: Menyediakan ringkasan pesanan.

Index
Dibuat untuk meningkatkan kinerja query pada kolom-kolom yang sering digunakan dalam pencarian dan join

3. Penjelasan


Membuat database
Database yang saya buat, saya namai dengan db_uas
![DB](https://github.com/suryaaris/UAS-BDL/assets/173940200/a2b376fb-5c2a-40cc-9124-335eb66891e0)



