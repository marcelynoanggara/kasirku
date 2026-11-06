# KasirKu

**Sistem Kasir QR Ringan untuk UMKM Lokal**

KasirKu adalah produk dari startup **Kasir Jaya Abadi**, dibuat untuk tugas kelompok mata kuliah Keprofesian (Keprof) IT-08-02. Produk ini ditujukan untuk pemilik warung, toko kelontong, kedai makanan, dan UMKM kecil lain yang selama ini mencatat penjualan secara manual atau hanya mengandalkan stiker QRIS tempel tanpa pencatatan.

Inti produknya adalah **Starter Pack**: satu box berisi aplikasi kasir dan perangkat pendukung yang siap pakai. Pemilik usaha tidak perlu merakit apa pun sendiri. Buka box, pasang stand, nyalakan printer, langsung jualan.

Repository ini berisi web demo interaktifnya. Seluruh alur kasir bisa dicoba langsung di halaman web, tanpa install dan tanpa server.

## Bagaimana produk ini bekerja

### 1. Alur pemilik usaha, dari pesan sampai jualan

1. **Pesan dan box sampai.** Pemilik usaha mengisi formulir pemesanan di web. Tim KasirKu mengonfirmasi lewat WhatsApp, lalu Starter Pack dikirim dalam 2 sampai 4 hari kerja. Di dalam box, akun toko sudah aktif dan menu contoh sudah terisi.
2. **Unboxing sekitar 15 menit.** Pasang stand QRIS di meja kasir, nyalakan printer, buka aplikasi. Ada buku panduan bergambar di dalam box, plus kartu QR untuk video setup. Kalau mau dibantu, tersedia pelatihan online 1 jam untuk input menu.
3. **Jualan dan pantau omzet.** Semua pembayaran, QRIS maupun tunai, tercatat dari satu layar kasir. Setiap malam, rekap penjualan otomatis terkirim ke WhatsApp pemilik. Tidak ada lagi rekap manual di buku tulis.

### 2. Alur transaksi di kasir

Ini alur yang berjalan di demo POS pada halaman web, meniru cara aplikasi kasirnya dipakai sehari-hari:

1. Kasir memilih menu yang dipesan pelanggan. Ada 12 menu contoh yang bisa difilter per kategori (Makanan, Minuman, Camilan) atau dicari lewat kotak pencarian, dan setiap item langsung masuk ke keranjang.
2. Total belanja dihitung otomatis mengikuti isi keranjang. Item bisa ditambah, dikurangi, atau dibatalkan sebelum bayar, dan ada kolom diskon persen untuk potongan harga.
3. Pelanggan memilih cara bayar:
   - **QRIS.** Layar menampilkan kode QR sesuai nominal belanja, lengkap dengan timer 5 menit. Kode yang kedaluwarsa bisa dibuat ulang. Setelah pembayaran terkonfirmasi, transaksi tercatat sebagai lunas.
   - **Tunai.** Kasir memasukkan jumlah uang yang diterima atau menekan tombol uang pas dan nominal cepat, lalu sistem menghitung kembaliannya. Tombol terima pembayaran tidak aktif selama uangnya kurang.
4. Struk dibuat otomatis begitu transaksi selesai. Struk bisa diunduh sebagai file teks, dicetak, dan dibuka lagi kapan pun dari riwayat transaksi.
5. Stok setiap menu berkurang otomatis mengikuti penjualan. Menu yang habis tidak bisa dipesan sampai stoknya ditambah lagi dari tab Stok, yang juga menyediakan tombol restok cepat.
6. Setiap transaksi yang lunas langsung masuk ke dashboard: omzet hari ini, jumlah transaksi, item terjual, rata-rata per transaksi, grafik penjualan per jam, dan menu paling laris, semuanya dihitung dari transaksi yang benar-benar tercatat.
7. Dari dashboard, pemilik bisa membuat rekap penjualan dalam format pesan WhatsApp dan menyalinnya. Nama toko, alamat, dan nomor WhatsApp pemilik diatur di tab Stok dan Pengaturan, dan nama toko itu yang tercetak di kepala struk.

### 3. Isi Starter Pack

Satu box Starter Pack berisi:

- Aplikasi KasirKu yang sudah terpasang, akun toko aktif, dan menu contoh terisi
- Printer thermal Bluetooth 58mm, tanpa kabel, baterai isi ulang
- Stand akrilik QRIS dengan kode toko tercetak anti air
- Stand tablet atau HP lipat untuk perangkat kasir
- 5 roll kertas thermal dan stiker "Kami Menerima QRIS"
- Buku panduan bergambar
- Pelatihan online 1 jam untuk pemilik dan kasir

## Harga

| Paket | Harga | Isi utama |
| --- | --- | --- |
| Aplikasi Saja | Rp49rb per bulan per toko | Aplikasi kasir, QRIS dinamis dan tunai, laporan harian via WhatsApp, 1 akun kasir |
| Starter Pack | Rp499rb sekali bayar, termasuk aplikasi 3 bulan | Semua fitur Aplikasi Saja, printer thermal, stand QRIS dan stand HP, kertas dan stiker, manajemen stok, 3 akun kasir, pelatihan |
| Paket Lengkap | Rp1,29jt | Paket untuk toko yang lebih besar, perangkat dan akun lebih banyak |

Semua paket tanpa kontrak jangka panjang. Berhenti kapan saja.

## Menjalankan demo

Cukup buka file `index.html` di browser. Tidak ada proses build, tidak ada dependensi, dan tidak perlu koneksi ke server mana pun. Semua tombol di halaman berfungsi: demo kasir, pilihan paket, formulir pemesanan (mengeluarkan kode order berformat KK-2026-xxxx), sampai struk yang bisa diunduh.

## Teknologi

- Satu file HTML mandiri berisi HTML, CSS, dan JavaScript
- Tanpa framework, tanpa backend, tanpa database
- Kode QR digambar langsung di browser memakai canvas
- Data demo (transaksi, stok, pengaturan toko) tersimpan di localStorage browser, jadi tidak hilang saat halaman dimuat ulang. Dashboard berangkat dari data contoh yang diberi label jelas di dalam aplikasi dan bisa dikosongkan dengan satu tombol

## Catatan

Web ini adalah dummy untuk keperluan tugas kelompok, jadi pembayaran QRIS di dalamnya adalah simulasi tampilan dan alur, bukan koneksi ke gateway pembayaran asli. Menu dan data penjualan awal adalah contoh untuk keperluan demo.
