# Proyek Praktikum Pemrograman Mobile - CRUD Data Barang

Ini adalah proyek aplikasi Android sederhana yang dibuat sebagai bagian dari Laporan Praktikum Inhall Pemrograman Mobile. Aplikasi ini mendemonstrasikan fungsionalitas **CRUD (Create, Read, Update, Delete)** dasar menggunakan database lokal **Room** dari Android Jetpack.

Aplikasi ini berfokus pada pengelolaan daftar "Barang"

## 📸 Tampilan Aplikasi

Aplikasi ini memiliki satu layar utama (`MainActivity`) yang menampilkan daftar barangPengguna dapat melihat daftar barang yang telah disimpan dan (kemungkinan) menambahkan barang baru menggunakan tombol tambah (+)



## 🚀 Fitur Utama

* Menampilkan daftar barang (Meja, Semen, Triplek, Pasir, dll.) dalam sebuah `RecyclerView`
* Menyimpan data barang secara persisten di database lokal perangkat menggunakan **Room**
* Menggunakan `AppExecutor` untuk menjalankan operasi database di *background thread*

## 🛠️ Teknologi & Arsitektur

* **Bahasa:** Kotlin
* **Database:** Android Room (Lokal Database)
* **Komponen UI:** RecyclerView, Activity
* **Arsitektur:**
    * **`Barang.kt` (Model/Entity):** Mendefinisikan struktur data untuk tabel "Barang" di database
    * **`BarangDAO.kt` (DAO):** *Interface* yang berisi fungsi-fungsi untuk mengakses database (seperti `@Insert`, `@Query`)
    * **`DatabaseBarang.kt` (Database):** Kelas utama pemegang database Room
    * **`BarangAdapter.kt` (Adapter):** Menghubungkan data (daftar `Barang`) ke `RecyclerView` untuk ditampilkan di UI
    * **`MainActivity.kt` (View/Controller):** Aktivitas utama yang menampilkan daftar dan mengelola logika UI
    * **`AppExecutor.kt` (Utility):** Kelas utilitas untuk mengelola *threading* operasi database
