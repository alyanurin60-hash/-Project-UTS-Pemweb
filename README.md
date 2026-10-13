# -Project-UTS-Pemweb
# Dokumentasi Projects & System Requirement Specification (SRS) - UTS Pemrograman Web

**Nama:** Alya Nurin Fadilah  
**NIM:** 25091397097  
**Program Studi:** D4 Manajemen Informatika  
**Mata Kuliah:** Pemrograman Web  
**Dosen Pengampu:** Faris Abdi El Hakim, S.Kom., M.Tr.Kom.  

---

## 1. Ringkasan Proyek
Aplikasi web ini merupakan halaman portofolio interaktif multi-halaman yang dibangun untuk menampilkan karya, profil pribadi, serta menyediakan formulir interaktif bagi pengguna. Halaman dibangun dengan standar struktur HTML5 valid, desain gaya Sage Green & Cream yang estetis dan responsif, serta dilengkapi fungsionalitas JavaScript dinamis.

---

## 2. System Requirement Specification (SRS)

### 2.1 Kebutuhan Fungsional (Functional Requirements)
1. **Navigasi Multi-Halaman**:
   - Sistem menyediakan bilah navigasi (Navbar) yang menghubungkan 3 halaman utama: Beranda (`index.html`), Tentang Kami (`about.html`), dan Kontak (`contact.html`).
2. **Fitur Dark Mode Toggle**:
   - Pengguna dapat mengubah mode tampilan web antara Mode Terang (*Light Mode*) dan Mode Gelap (*Dark Mode*) secara real-time pada semua halaman, serta menyimpan preferensi pada *local storage*.
3. **Pencarian & Filter Dinamis (Beranda)**:
   - Pengguna dapat melakukan pencarian/penyaringan proyek pada halaman utama secara langsung berdasarkan kata kunci nama, deskripsi, atau kategori proyek.
4. **Pengaturan Visibilitas Foto Profil (Tentang Kami)**:
   - Pengguna dapat menyembunyikan dan menampilkan kembali foto profil interaktif menggunakan tombol aksi *toggle*.
5. **Validasi Formulir & Notifikasi DOM (Kontak)**:
   - Sistem memvalidasi input formulir (Nama, Email, Pesan). Jika terdapat kolom kosong atau format email tidak sesuai, sistem menampilkan pesan peringatan berwarna merah. Jika validasi berhasil, sistem menampilkan pesan sukses berwarna hijau tanpa me-load ulang halaman.

### 2.2 Kebutuhan Non-Fungsional (Non-Functional Requirements)
1. **Responsivitas**: Tampilan web secara otomatis menyesuaikan resolusi perangkat:
   - Layar Desktop (> 768px): Tampilan Grid 3 Kolom.
   - Layar Tablet (≤ 768px): Tampilan Grid 2 Kolom.
   - Layar Ponsel (≤ 480px): Tampilan Grid 1 Kolom.
2. **Usability & Estetika**: Menggunakan palet warna Sage Green & Cream yang tenang dengan kontras rasio teks tinggi agar mudah dibaca.
3. **Kepatuhan Standar**: Menggunakan elemen HTML5 semantik (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`) serta CSS3 murni tanpa dependensi *library* luar.

---

## 3. Penjelasan Struktur Kode & Fungsionalitas

### 3.1 Struktur HTML5
- Menggunakan struktur hierarki semantik lengkap untuk aksesibilitas dan SEO.
- Penggunaan atribut `data-category` pada elemen artikel untuk mendukung filter pencarian JavaScript.

### 3.2 Desain CSS3 & Responsivitas
- **Flexbox Layout**: Digunakan pada struktur Navbar dan tata letak Halaman About agar elemen tersusun seimbang.
- **CSS Grid Layout**: Digunakan pada galeri kartu portofolio halaman Beranda dengan konfigurasi `repeat(3, 1fr)`.
- **Media Queries**: Digunakan untuk menangani breakpoint responsif pada tablet dan mobile.

### 3.3 Interaksi JavaScript
Implementasi 4 modul utama interaktivitas:
1. **Event Handling**: Menangani event `click`, `keyup`, dan `submit`.
2. **DOM Manipulation**: Mengubah konten teks (`textContent`), kelas CSS (`classList.toggle`), dan visibilitas elemen (`style.display`).
3. **Style & Animation**: Mengubah tema warna elemen secara dinamis untuk mode gelap/terang.
4. **Form Validation**: Memeriksa kelengkapan input dan validasi pola alamat email menggunakan Regular Expression (Regex).

---

## 4. Panduan Menjalankan & Tautan Live Hosting

1. Clone repositori ini:
   ```bash
   git clone [https://github.com/alyanurin60-hash/uts-pemweb.git]

Buka file index.html langsung pada peramban web (browser) favorit Anda.
Live Server GitHub Pages: https://github.com/alyanurin60-hash/

---
