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


Membuat dan memasukkan data pada tabel
Saya membuat 4 tabel, diantaranya:


1. Tabel Customer (tb_customer)
Berisi customer_id, nama, alamat, dan no_telp
![DB DAN TB CUSTOMER - Copy](https://github.com/suryaaris/UAS-BDL/assets/173940200/5f3870ca-040c-48d9-91a7-616292a147e3)
Pengisian data
![TB CUSTOMER INSERT](https://github.com/suryaaris/UAS-BDL/assets/173940200/0205ff89-405b-4227-9bcc-eae9dc0f9b27)


2. Tabel produk (produk)
Berisi produk_id, nama_produk, harga, stok
![TB PRODUK](https://github.com/suryaaris/UAS-BDL/assets/173940200/27cd20f3-b281-48af-86e8-6651804ce948)
Pengisian data
![TB PRODUK INSERT](https://github.com/suryaaris/UAS-BDL/assets/173940200/192f47f0-480f-4bf1-b95c-83fa470f5a12)


3. Tabel Order (tb_order)
Berisi order_id, customer_id, tanggal
![TB ORDER](https://github.com/suryaaris/UAS-BDL/assets/173940200/f86915b4-cb60-48a4-9346-ae609c1a5cec)
Pengisian data
![TB ORDER INSERT](https://github.com/suryaaris/UAS-BDL/assets/173940200/80078a5f-0b91-4bbd-bf06-536e93932739)

4. Tabel detail (tb_detail)
Berisi detail_id, order_id, produk_id, kuantitas
[TB DETAIL](https://github.com/suryaaris/UAS-BDL/assets/173940200/9d217266-759c-4995-aacc-3d7afac55ace)
Pengisian data
![TB DETAIL INSERT](https://github.com/suryaaris/UAS-BDL/assets/173940200/11fe89c4-7f89-4494-8ff6-6b77e789a28a)

Trigger
Memiliki fungsi untuk mengurangi stok produk secara otomatis setiap kali ada pesanan baru yang dimasukkan ke dalam tb_detail
![Screenshot 2024-06-26 181219](https://github.com/suryaaris/UAS-BDL/assets/173940200/a1dab674-16fc-4fed-acc4-677a8fa86574)


View
- Untuk menampilkan informasi pesanan lengkap dengan detailnya dalam bentuk yang lebih mudah dipahami
- View menggabungkan data dari beberapa tabel untuk memberikan gambaran lengkap setiap pesanan yang dilakukan
![Screenshot 2024-06-26 182043](https://github.com/suryaaris/UAS-BDL/assets/173940200/850afc59-9ca9-4ea9-9d07-660fbe62beb7)


Agregat

- Agregat tersebut menggunakan operator SUM dan digunakan untuk melihat total penjualan per produk
  ![Screenshot 2024-06-26 182806](https://github.com/suryaaris/UAS-BDL/assets/173940200/a0dbbb37-03ad-40c6-bb85-f55a941af821)

- Agregat ini menggunakan operator COUNT yang digunakan untuk melihat jumlah pesanan per pelanggan
  ![Screenshot 2024-06-26 183121](https://github.com/suryaaris/UAS-BDL/assets/173940200/662902b5-1f58-4f1b-9007-855de223ae8b)

- Agregat ini menggunakan operator AVARAGE yang digunakan untuk melihat rata-rata jumlah produk yang dipesan
  ![Screenshot 2024-06-26 183324](https://github.com/suryaaris/UAS-BDL/assets/173940200/4dd225f4-493c-4459-86a6-de97f3971cc2)

- Agregat ini menggunakan operator SIM yang digunakan untuk melihat total penjualan per hari
  ![Screenshot 2024-06-26 183540](https://github.com/suryaaris/UAS-BDL/assets/173940200/d5349854-ed86-4b21-b3e2-0498601a8103)

Index
Index membantu mempercepat operasi query dengan membuat struktur data yang memungkinkan pencarian lebih cepat.

- Index pada kolom customer_id di tb_order
  ![tborder](https://github.com/suryaaris/UAS-BDL/assets/173940200/c9364ef7-299f-4fab-a83f-453889ef04a0)

- Index pada kolom order_id di tb_detail
  ![rbdetail](https://github.com/suryaaris/UAS-BDL/assets/173940200/6d315569-06ba-4611-830e-6c7a1552a856)

- Index pada kolom produk_id di tb_detail
  ![tbdetail2](https://github.com/suryaaris/UAS-BDL/assets/173940200/c8fcfc30-83d3-4574-81e6-39792c4813dd)

- Index pada kolom nama_produk di tb_produk
  ![produk](https://github.com/suryaaris/UAS-BDL/assets/173940200/3c806d43-70da-4cf2-b44a-10b323f0a834)


Left Join
Menggabungkan dua tabel dan mengembalikan semua baris dari tabel kiri, serta baris yang cocok dari tabel kanan
![inner left](https://github.com/suryaaris/UAS-BDL/assets/173940200/b88f2446-dfcc-4af8-8294-effb787e97ce)

Inner Join
Menggabungkan dua tabel dan hanya mengembalikan baris yang memiliki kecocokan di kedua tabel
![inner join](https://github.com/suryaaris/UAS-BDL/assets/173940200/0eff7eeb-0fe1-460a-87b1-213f8339afa3)

Subquery
Membantu memecah query yang rumit menjadi bagian-bagian yang lebih mudah dipahami dan dikelola serta digunakan dalam klausa WHERE, HAVING, FROM, dan SELECT untuk membandingkan dan menyaring data.
![inner join](https://github.com/suryaaris/UAS-BDL/assets/173940200/0eff7eeb-0fe1-460a-87b1-213f8339afa3)

Having
Untuk menyaring hasil agregat setelah menggunakan group by
![having](https://github.com/suryaaris/UAS-BDL/assets/173940200/662b5070-12df-437c-9925-b55e83dab775)

Wildcard
Digunakan dalam klausa LIKE untuk mencari pola dalam teks. % digunakan untuk mencocokkan nol atau karakter, dan _ digunakan untuk mencocokkan satu karakter
![wildcard](https://github.com/suryaaris/UAS-BDL/assets/173940200/225b65cd-0985-4c19-8fcd-af3a7e53c46e)

Dump
Proses ekspor data dari sebuah database ke dalam format yang dapat disimpan, dipisahkan, atau diimpor kembali. 
![Screenshot 2024-06-26 172817](https://github.com/suryaaris/UAS-BDL/assets/173940200/61e6fe86-96b9-4c8d-978f-a2a632594602)

![Screenshot 2024-06-26 172850](https://github.com/suryaaris/UAS-BDL/assets/173940200/3d3c5f3d-4a6a-44f2-8958-c65b2ea2cf6b)















