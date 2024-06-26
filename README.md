UAS
Basis Data Lanjutan
Putu Aris Surya Kusuma - 2201010075



ERD (Entity Relationship Diagram)



Deskripsi Proyek
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

