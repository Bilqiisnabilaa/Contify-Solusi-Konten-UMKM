# RINGKASAN SISTEM & FITUR PROTOTIPE CONTIFY 🚀
*(Dokumentasi Resmi untuk Keperluan Presentasi Tugas Akhir)*

---

## 1. Konsep Utama Aplikasi
**Contify** adalah platform *marketplace* layanan kreatif yang menjembatani UMKM (yang membutuhkan konten seperti video, foto, atau copywriting) dengan para *Freelancer* Kreatif. 

Sistem ini dirancang dengan antarmuka modern (bertema gelap/glassmorphism) dan dibangun sebagai **Prototipe Frontend (MVP)** menggunakan HTML, CSS, dan Vanilla JavaScript. Karena ini adalah prototipe demo, semua data disimpan secara sementara di memori *browser* (tidak menggunakan *database* asli), namun dirancang agar terasa seperti "sistem utuh" (Full System) saat dipresentasikan.

---

## 2. Hak Akses & Akun Demo
Untuk memudahkan pengujian dan presentasi, sistem memiliki 3 gerbang akses utama yang bisa digunakan saat *Login*:
1. **Klien / UMKM** (Username: `a` | Password: `a`)
2. **Admin Sistem** (Username: `b` | Password: `b`)
3. **Freelancer** (Username: `f` | Password: `f`)

---

## 3. Fitur Utama Berdasarkan Peran (Role)

### A. Alur Publik & Klien (User)
- **Katalog & Kalkulator Harga:** Pengunjung bisa melihat berbagai paket layanan kreatif (Video, Foto, Copywriting). Harga akan otomatis diakumulasikan berdasarkan kecepatan pengerjaan (Reguler/Kilat) dan tambahan opsi lainnya.
- **Form Pemesanan 4 Langkah (Seamless Order):**
  1. Rincian Paket.
  2. Upload Brief/Aset Mentahan Klien.
  3. Pemilihan Tanggal Pengerjaan (Kalender yang sudah terhubung dengan waktu *real-time* bulan saat ini).
  4. Checkout & Pemilihan Metode Pembayaran (QRIS, e-Wallet, Transfer Bank).
- **Simulasi Payment Gateway Otomatis:** Begitu klien mengeklik "Bayar Sekarang", sistem menyimulasikan jeda pemrosesan *payment gateway* (selama 2 detik), lalu secara otomatis memvalidasi pembayaran dan memasukkan pesanan Klien langsung ke dalam "Antrean Pengerjaan". Klien tidak perlu mengirim bukti transfer manual.
- **Dashboard Pelacakan:** Klien memiliki halaman dasbor sendiri untuk memantau status pesanan mereka secara langsung.

### B. Alur Kandidat & Freelancer Aktif
- **Pendaftaran Publik (Karier):** Siapapun bisa mendaftar menjadi Freelancer melalui tautan "Gabung Freelancer" di bagian *Footer* website. Form ini meminta Nama, Keahlian, Pengalaman (Tahun), dan Link Portofolio.
- **Bursa Pekerjaan (Job Board):** Freelancer aktif (akun `f/f`) dapat melihat daftar proyek yang masuk dari Klien dan mengklik "Ambil Pekerjaan".
- **Ruang Kerja (My Tasks):** Freelancer bisa melihat detail proyek yang diambil, mengunduh (*download*) aset/brief yang dikirim Klien, dan menekan tombol untuk mengunggah (*upload*) hasil pekerjaan jika sudah selesai.
- **Penarikan Saldo:** Freelancer memiliki dasbor keuangan untuk menarik uang bayaran mereka ke rekening pribadi.

### C. Alur Administrator (Pengelola Contify)
- **Papan Kanban Interaktif (Manajemen Proyek):** Admin bisa melihat semua pesanan Klien yang sudah dibayar. Kartu pesanan bisa dipindah secara visual ke kolom: *Antrean* ➔ *Sedang Diproses* ➔ *Review Hasil* ➔ *Selesai*. Di setiap kartu, Admin bisa mengeklik tombol **Download Aset** untuk meneruskan file Klien ke Freelancer.
- **Persetujuan Freelancer Baru:** Data pelamar kerja yang mendaftar dari halaman depan akan masuk ke dasbor Admin. Admin bisa melihat Portofolio dan Pengalaman mereka, lalu menekan tombol "Terima" atau "Tolak".
- **Simulasi Integrasi WhatsApp API:** Saat Admin menerima/menolak kandidat Freelancer, sistem menyimulasikan proses pengiriman notifikasi otomatis (*broadcast*) ke nomor WhatsApp pelamar.
- **Log Transaksi Pembayaran:** Admin tidak perlu lagi menyetujui pembayaran secara manual. Sistem mencatat semua keberhasilan pembayaran dari Klien di tab "Log Transaksi", dan Admin hanya perlu turun tangan jika ada pesanan berstatus *Gagal/Problem*.
- **CMS (Content Management System):** Admin memiliki akses khusus untuk menambah/mengedit paket layanan dan voucher diskon yang tampil di halaman depan.

---

## 4. Cara Menjalankan (Buku Petunjuk Demo)
1. Buka file `contify-v3.html` di browser (disarankan Google Chrome).
2. Tampilkan fitur **Pendaftaran Publik** dengan menggulir halaman ke bawah (Footer) lalu klik "Karier (Gabung Freelancer)".
3. Coba **Pesan Paket** tanpa login, sistem akan memaksa Anda login. Masukkan username `a` & password `a`.
4. Lakukan pemesanan hingga tahap akhir dan lihat bagaimana sistem Pembayaran Otomatis bekerja.
5. *Logout*, lalu masuk sebagai Admin (`b` & `b`).
6. Buka tab **Kanban** untuk menggeser status proyek yang baru saja Anda pesan tadi, lalu periksa tab **Freelancer** untuk mencoba menyetujui kandidat pelamar.

*(Dokumen ini dibuat otomatis sebagai panduan presentasi Tugas Akhir startup Contify).*
