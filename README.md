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

1. Kasir memilih menu yang dipesan pelanggan. Ada 12 menu contoh yang bisa diklik, dan setiap item langsung masuk ke keranjang.
2. Total belanja dihitung otomatis mengikuti isi keranjang. Item bisa ditambah, dikurangi, atau dibatalkan sebelum bayar.
3. Pelanggan memilih cara bayar:
   - **QRIS.** Layar menampilkan kode QR dinamis sesuai nominal belanja, lengkap dengan timer 5 menit. Setelah pembayaran terkonfirmasi, transaksi tercatat sebagai lunas.
   - **Tunai.** Kasir memasukkan jumlah uang yang diterima, lalu sistem menghitung kembaliannya.
4. Struk digital dibuat otomatis begitu transaksi selesai dan bisa diunduh sebagai bukti pembayaran.
5. Setiap transaksi yang lunas langsung masuk ke dashboard. Total pendapatan dan riwayat penjualan bertambah saat itu juga, jadi pemilik bisa memantau omzet hariannya tanpa menunggu rekap malam.

### 3. Isi Starter Pack

Satu box Starter Pack berisi:

- Aplikasi KasirKu yang sudah terpasang, akun toko aktif, dan menu contoh terisi
- Printer thermal Bluetooth 58mm, tanpa kabel, baterai isi ulang
- Stand akrilik QRIS dengan kode toko tercetak anti air
- Stand tablet atau HP lipat untuk perangkat kasir
- 5 roll kertas thermal dan stiker "Kami Menerima QRIS"
- Buku panduan bergambar

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
- Kode QR digambar langsung di browser
- Data transaksi demo hanya hidup selama halaman terbuka dan hilang saat halaman dimuat ulang

## Catatan

Web ini adalah dummy untuk keperluan tugas kelompok, jadi pembayaran QRIS di dalamnya adalah simulasi tampilan dan alur, bukan koneksi ke gateway pembayaran asli. Angka penjualan, testimoni, dan menu adalah contoh.
