# TumpangGo — Redesign & Premium Removal

## Perubahan

- Mengganti sistem visual global ke palet hijau hutan, permukaan off-white, batas yang lebih lembut, dan tipografi Plus Jakarta Sans/Inter.
- Menyatukan warna aksen yang sebelumnya rose menjadi hijau brand agar tampilan portal customer, merchant, admin, dan driver lebih konsisten.
- Memperbarui font Google Fonts, metadata halaman, dan warna tema PWA.
- Menghapus UI Merchant Premium/PRO dan kategori Premium dari katalog customer.
- Menghapus panel lisensi dari dashboard admin dan fitur aktivasi kode lisensi dari portal merchant.
- Menghapus endpoint API pembuatan lisensi dan redeem lisensi.
- Menghapus model, tipe, seed, dan sinkronisasi lisensi dari database aplikasi serta skema lisensi dari blueprint Firestore.
- Menambahkan migrasi lokal yang membersihkan metadata lisensi lama dari file database ketika aplikasi dimulai. Pengaturan pre-order tetap dipertahankan dan tidak lagi bergantung pada status Premium.
- Mempertahankan alur pesanan, pembayaran pelanggan, QRIS, bukti pembayaran, verifikasi admin, komisi, settlement, dan data operasional yang tidak terkait lisensi.

## Validasi

- Pemeriksaan statis dilakukan dengan TypeScript compiler global. Tidak ditemukan kesalahan sintaks TypeScript/JSX pada file yang diubah.
- Validasi penuh TypeScript/build belum dapat diselesaikan karena dependensi proyek tidak tersedia di lingkungan kerja ini; instalasi dependensi berhenti karena timeout. Compiler melaporkan error akibat modul/deklarasi yang belum terpasang dan beberapa error tipe di file yang tidak diubah.
- Belum dilakukan pengujian browser, transaksi pembayaran nyata, atau deployment. Jalankan `npm install`, lalu `npm run lint` dan `npm run build` di lingkungan proyek sebelum deployment.
