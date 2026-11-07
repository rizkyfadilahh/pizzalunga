================================================================================

          PIZZA LUNGA MAKASSAR - CLOUD POS & FINANCIAL ANALYTICS SYSTEM

================================================================================



Live App URL : https://rizkyfadilahh.github.io/pizzalunga/

Repository   : https://github.com/rizkyfadilahh/pizzalunga

Developer    : Registered 2026 Rizky Fadilah POS Development

Management   : Pizza Lunga Makassar



--------------------------------------------------------------------------------

1. DESKRIPSI SISTEM

--------------------------------------------------------------------------------

Pizza Lunga Makassar System adalah aplikasi Kasir (Point of Sale / POS) dan 

Manajemen Keuangan Berbasis Cloud yang dirancang khusus untuk operasional harian 

toko serta pengelolaan booth pada event/festival culinary.



Aplikasi ini berjalan secara 100% Client-Side Single Page Application (SPA) 

melalui GitHub Pages dan terintegrasi secara real-time ke Google Sheets 

Database menggunakan RESTful API Google Apps Script (GAS) Web App.



Sistem dapat diakses secara lancar melalui PC Desktop (Windows/Mac), Tablet, 

maupun Smartphone Android/iOS dengan tampilan antarmuka yang modern, fluid, 

dan responsif.



--------------------------------------------------------------------------------

2. TEKNOLOGI STACK

--------------------------------------------------------------------------------

- Frontend Stack  : HTML5, Tailwind CSS (via CDN), Vanilla JavaScript (ES6+)

- Visual Analytics: Chart.js (Interactive Bar & Doughnut Charts)

- Typography      : Plus Jakarta Sans (Google Fonts)

- Backend Database: Google Sheets (Spreadsheet Database)

- API Engine      : Google Apps Script (doGet & doPost Web App)

- Hosting Platform: GitHub Pages



--------------------------------------------------------------------------------

3. FITUR UTAMA SISTEM

--------------------------------------------------------------------------------

[1] DASHBOARD & ANALYTICS VISUAL INTERAKTIF

    - Summary Metrics Card: Real-time update Total Omzet, Total Pengeluaran, 

      Laba Bersih Murni, Sisa Kas di Tangan, Injected Capital, dan Prive Owner.

    - Grafik Bar Chart (Chart.js): Visualisasi tren perbandingan Omzet vs 

      Pengeluaran harian.

    - Grafik Doughnut Chart (Chart.js): Proporsi breakdown pengeluaran 

      berdasarkan kategori (Bahan Baku, Operasional, Biaya Event, Gaji).



[2] INPUT PENJUALAN POS (POINT OF SALE FIELD & TOKO)

    - Pemilihan Tipe Penjualan: Penjualan Reguler Toko vs Penjualan Event/Festival.

    - Catalog & Custom Add-ons: Pilihan menu pizza lengkap dengan kustomisasi 

      Add-on extra (Mozzarella, Keju Leleh, Saus, dll).

    - Quick Counter: Kontrol kuantitas (+ / -) yang responsif dan fleksibel.

    - Automatic Subtotal & Checkout: Kalkulasi otomatis item & total bayar 

      dengan sync instan ke Google Sheets.



[3] INPUT PENGELUARAN & BIAYA DARURAT EVENT

    - Categorized Expense Logging: Pencatatan Pembelian Bahan Baku, Beban 

      Operasional, Biaya Event Mendadak, Penambahan Modal, dan Penarikan Prive.

    - Event Tagging: Pengait transaksi pengeluaran langsung ke event tertentu 

      untuk perhitungan HPP & Laba Rugi Event secara presisi.



[4] LAPORAN KEUANGAN & MULTI-FILTER DETAILED

    - Filter Rinci: Filter data transaksi berdasarkan Rentang Tanggal (Start/End), 

      Kategori Transaksi, atau Event spesifik.

    - Dynamic Category Cards: Ringkasan akumulasi biaya per kategori berdasarkan 

      filter aktif.

    - Export Data: Ekspor riwayat transaksi ke format Microsoft Excel (.CSV).



[5] KELOLA & LAPORAN LABA/RUGI EVENT

    - Event Setup & Duration Calculator: Pendaftaran event baru dengan estimasi 

      durasi hari otomatis (Tanggal Mulai s/d Tanggal Selesai).

    - Embedded Menu Config: Pengaturan menu & harga khusus untuk event tertentu 

      atau opsi salin menu reguler.

    - Real-time P&L Event: Perhitungan otomatis Total Omzet vs Modal Sewa Stand 

      + Operasional Event -> Penentuan Status Event (● PROFITABLE / ● RUGI).



[6] KALKULATOR GAJI & GENERATOR SLIP GAJI PDF

    - Event Auto-Fill Working Days: Sinkronisasi otomatis hari kerja pegawai 

      berdasarkan durasi event yang dipilih.

    - Flexible Rate & Deductions: Pengaturan Gaji Harian, Bonus/Insentif Event, 

      dan Potongan Kasbon/Pinjaman.

    - Printable PDF Slip Gaji: Format cetak resmi Slip Gaji Pizza Lunga Makassar 

      lengkap dengan rincian penerimaan dan area tanda tangan.

    - Automatic Expense Posting: Otomatis memotong/mencatat gaji pegawai ke 

      dalam pengeluaran kas utama.



[7] RIWAYAT TRANSAKSI & CLOUD SYNCHRONIZATION

    - Live Sync Status Indicator (☁️ Live Google Sheets / 🔄 Syncing).

    - Hapus Data Cloud: Fitur penghapusan transaksi atau event langsung ter-update 

      di Google Sheets.



--------------------------------------------------------------------------------

4. ALUR ARSITEKTUR INTEGRASI CLOUD (GOOGLE APPS SCRIPT)

--------------------------------------------------------------------------------

1. Client (Browser / GitHub Pages) mengirimkan request HTTP GET ke endpoint GAS 

   `doGet(e)` untuk mengambil data JSON (transactions, catalog, events).

2. Helper `getParsedItems()` pada script memastikan item array ter-parse dengan 

   benar meskipun tersimpan sebagai JSON string di sheet.

3. Transaksi baru dikirim via HTTP POST `doPost(e)` yang akan melakukan `appendRow()` 

   pada lembar kerja Google Sheets secara real-time.



--------------------------------------------------------------------------------

5. PETUNJUK DEPLOYMENT & PEMELIHARAAN REPOSITORI

--------------------------------------------------------------------------------

- File Utama: `pizzalunga.html` (Single-file HTML yang mencakup UI, CSS Tailwind, 

  JavaScript Logic, dan Chart Engine).

- GitHub Pages Deployment:

  1. Push file `pizzalunga.html` dan `README.txt` ke branch `main`.

  2. Buka Repository Settings > Pages.

  3. Set Source ke `Deploy from a branch` -> Select `main` / `/ (root)`.

  4. Akses link publik: https://rizkyfadilahh.github.io/pizzalunga/pizzalunga.html



--------------------------------------------------------------------------------

6. KREDIT DAN LISENSI

--------------------------------------------------------------------------------

Sistem dikembangkan dan dipelihara oleh:

- Software Engineer / Developer : Rizky Fadilah (POS Development 2026)

- Client & Business Owner       : Pizza Lunga Makassar



Hak Cipta © 2026 Rizky Fadilah POS Development. All Rights Reserved.

================================================================================
