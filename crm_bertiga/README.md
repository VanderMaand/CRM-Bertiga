# crm_bertiga

# ☕ Coffee Street

### Sistem Informasi Manajemen Bisnis Coffee Street

**Coffee Street** adalah aplikasi berbasis web yang dibuat untuk membantu pengelolaan operasional kedai kopi secara lebih teratur, mulai dari transaksi penjualan hingga pengelolaan stok, karyawan, penggajian, dan laporan bisnis.

Aplikasi ini dibuat sebagai proyek **Praktikum Rekayasa Kebutuhan Perangkat Lunak**.

---

## 📌 Tentang Aplikasi

Dalam menjalankan kedai kopi, terdapat banyak aktivitas yang perlu dicatat setiap hari, seperti:

* Mencatat transaksi pelanggan
* Mengelola daftar menu
* Memantau persediaan bahan baku
* Mencatat pembelian bahan baku
* Mencatat kehadiran karyawan
* Mengelola penggajian
* Melihat laporan penjualan
* Memantau kondisi keuangan bisnis

Coffee Street dibuat untuk mengumpulkan aktivitas tersebut dalam **satu sistem**, sehingga informasi bisnis dapat dikelola dengan lebih terstruktur dan mudah dipantau.

---

## 🎯 Tujuan

Aplikasi ini bertujuan untuk membantu Coffee Street dalam:

* 🧾 Mencatat transaksi penjualan secara digital
* 📦 Memantau stok bahan baku
* 👥 Mengelola data karyawan
* 💰 Mengelola payroll atau penggajian
* 📊 Membuat laporan penjualan dan keuangan
* 🔐 Membatasi akses berdasarkan peran pengguna
* 📋 Menyediakan data yang dapat digunakan untuk membantu pengambilan keputusan

---

## 👤 Siapa yang Menggunakan?

Coffee Street memiliki beberapa jenis pengguna dengan tugas yang berbeda.

| Pengguna           | Kegunaan                                                               |
| ------------------ | ---------------------------------------------------------------------- |
| 👑 **Owner**       | Memantau bisnis, melihat laporan, dan memberikan persetujuan           |
| 👨‍💼 **Manager**  | Mengelola operasional, karyawan, pembelian, stok, payroll, dan laporan |
| 👨‍🍳 **Karyawan** | Melakukan transaksi penjualan dan absensi                              |

Setiap pengguna hanya mendapatkan akses terhadap fitur yang sesuai dengan perannya.

---

## ✨ Fitur Utama

### 🔐 Login

Pengguna masuk menggunakan akun masing-masing. Sistem akan menyesuaikan halaman dan fitur berdasarkan peran pengguna.

### 🛒 Transaksi Penjualan

Karyawan dapat mencatat pesanan pelanggan, jumlah produk, harga, dan metode pembayaran.

Setelah transaksi berhasil:

**Transaksi → Data tersimpan → Stok diperbarui → Data masuk ke laporan**

### 📦 Pengelolaan Stok

Sistem membantu memantau jumlah bahan baku yang tersedia.

Stok dapat berubah ketika:

* Bahan baku dibeli → stok bertambah
* Produk terjual → stok berkurang

Dengan demikian, kondisi persediaan dapat dipantau secara lebih teratur.

### 🛍️ Pembelian Bahan Baku

Manager dapat mencatat pembelian bahan baku seperti:

* Nama bahan
* Jumlah
* Harga
* Supplier

Pembelian juga dapat melalui proses persetujuan Owner.

### 👥 Data Karyawan

Manager dapat menambahkan dan memperbarui informasi karyawan yang digunakan oleh sistem untuk proses operasional, absensi, dan payroll.

### 🕐 Absensi

Karyawan dapat mencatat kehadiran masuk dan keluar.

Data absensi kemudian dapat digunakan sebagai dasar dalam proses penggajian.

### 💵 Payroll

Sistem membantu Manager menghitung dan mengelola gaji berdasarkan data karyawan dan absensi.

Karyawan dapat melihat informasi paycheck yang telah diproses.

### 📊 Laporan

Sistem menyediakan laporan berdasarkan data operasional, seperti:

* Penjualan
* Pembelian bahan baku
* Payroll
* Laporan keuangan

Laporan dapat digunakan oleh Owner dan Manager untuk memantau kondisi bisnis.

### 🔎 Audit Keuangan

Pihak yang berwenang dapat memeriksa data transaksi, pengeluaran, dan laporan keuangan untuk membantu menjaga konsistensi dan transparansi data.

---

## 🔄 Gambaran Sederhana Cara Kerja

```text
                 COFFEE STREET
                      │
          ┌───────────┴───────────┐
          │                       │
      Karyawan                  Manager
          │                       │
     ┌────┴────┐          ┌───────┼────────┐
     │         │          │       │        │
  Transaksi  Absensi    Stok  Pembelian  Payroll
     │         │          │       │        │
     └────┬────┘          └───────┼────────┘
          │                       │
          └───────────┬───────────┘
                      │
                   DATABASE
                      │
                      ▼
                  📊 LAPORAN
                      │
                      ▼
                    Owner
```

---

## 🧑‍💻 Teknologi yang Digunakan

Walaupun pengguna tidak perlu memahami teknologi untuk menggunakan aplikasi ini, sistem dikembangkan menggunakan beberapa teknologi berikut:

| Teknologi         | Kegunaan                           |
| ----------------- | ---------------------------------- |
| **PHP**           | Menjalankan logika aplikasi        |
| **MySQL/MariaDB** | Menyimpan data aplikasi            |
| **Bootstrap**     | Membantu membuat tampilan aplikasi |
| **HTML & CSS**    | Membentuk tampilan halaman         |
| **JavaScript**    | Membantu interaksi pada halaman    |
| **Apache**        | Menjalankan aplikasi web           |

Sistem dirancang sebagai aplikasi web yang dapat diakses melalui browser seperti **Google Chrome, Mozilla Firefox, dan Microsoft Edge**.

---

## 🖥️ Tampilan Aplikasi

Beberapa halaman yang dirancang dalam proyek ini antara lain:

* 🔐 Halaman Login
* 📊 Dashboard
* 🛒 Transaksi
* ☕ Manajemen Menu
* 📦 Stok Bahan Baku
* 👥 Data Karyawan
* 🕐 Absensi
* 💰 Payroll
* 📈 Laporan

Desain antarmuka menggunakan konsep yang sederhana, responsif, dan berorientasi pada kemudahan penggunaan.

---

## 📁 Struktur Proyek

```text
Coffee-Street/
│
├── 📁 assets/
├── 📁 database/
├── 📁 pages/
├── 📁 controllers/
├── 📁 models/
├── 📁 views/
├── 📁 config/
│
├── 📄 index.php
├── 📄 README.md
└── 📄 ...
```

> Struktur folder dapat berubah mengikuti perkembangan implementasi aplikasi.

---

## 🚀 Cara Menjalankan

### 1. Persiapkan perangkat

Pastikan komputer sudah memiliki:

* Web server seperti **XAMPP**
* PHP
* MySQL/MariaDB
* Browser seperti Chrome, Firefox, atau Edge

### 2. Download project

Clone repository:

```bash
git clone https://github.com/USERNAME/NAMA-REPOSITORY.git
```

Kemudian masuk ke folder project:

```bash
cd NAMA-REPOSITORY
```

### 3. Jalankan Web Server

Buka **XAMPP**, kemudian aktifkan:

```text
Apache
MySQL
```

### 4. Siapkan Database

Buat database untuk Coffee Street melalui **phpMyAdmin**, kemudian import file database yang tersedia di repository.

### 5. Buka Aplikasi

Setelah server aktif, buka browser dan akses:

```text
http://localhost/NAMA-REPOSITORY
```

---

## 🔒 Keamanan

Aplikasi dirancang dengan beberapa mekanisme keamanan, antara lain:

* Login pengguna
* Hak akses berdasarkan peran
* Penyimpanan password menggunakan mekanisme hashing
* Validasi input
* HTTPS ketika sistem dijalankan secara online

Tujuannya adalah agar setiap pengguna hanya dapat mengakses fungsi yang sesuai dengan tanggung jawabnya.

---

## 📚 Dokumentasi

Dokumentasi lengkap mengenai kebutuhan dan rancangan sistem tersedia dalam dokumen **Software Requirements Specification (SRS)**.

Dokumen tersebut menjelaskan:

* Tujuan sistem
* Fitur aplikasi
* Jenis pengguna
* Kebutuhan sistem
* Use Case Diagram
* Activity Diagram
* Class Diagram
* Sequence Diagram
* Kebutuhan non-fungsional

Dokumen SRS juga menjadi dasar dalam proses perancangan sistem ini.

---

## 🎓 Konteks Proyek

Proyek ini dikembangkan sebagai bagian dari:

**Mata Kuliah:** Praktikum Rekayasa Kebutuhan Perangkat Lunak
**Proyek:** Sistem Informasi Manajemen Bisnis Coffee Street
**Versi Dokumen:** 1.0

### 👨‍💻 Tim Pengembang

* **124240066 — Sepi Ananda**

---

## 📌 Status Project

**Status:** 🚧 Dalam Pengembangan

Project ini dikembangkan secara bertahap berdasarkan kebutuhan bisnis dan hasil perancangan sistem.

---

## 💡 Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan di masa mendatang:

* 📱 Peningkatan tampilan untuk perangkat mobile
* 💳 Integrasi pembayaran digital
* 🧾 Integrasi dengan sistem POS
* 📧 Notifikasi otomatis
* 📈 Dashboard analitik yang lebih lengkap
* 🧮 Integrasi dengan sistem akuntansi
* ☁️ Deployment ke server online

---

## 📄 Lisensi

Project ini dibuat untuk keperluan **akademik dan pembelajaran**.

---

### ☕ Coffee Street

**Mengubah pengelolaan kedai kopi menjadi lebih teratur, terintegrasi, dan mudah dipantau.**


## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Learn Flutter](https://docs.flutter.dev/get-started/learn-flutter)
- [Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Flutter learning resources](https://docs.flutter.dev/reference/learning-resources)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
