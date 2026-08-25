# Roadmap Pengembangan Website Portofolio (Phases)

Dokumen ini memuat tahapan-tahapan (roadmap) pembuatan dan penyesuaian "Template Website Portofolio Mahasiswa" secara sistematis. Roadmap ini dibagi menjadi 2 fase utama: **Fase Pengembangan Template (oleh Panitia/PJ)** dan **Fase Implementasi (oleh Mahasiswa Baru)**.

---

## 🏗️ FASE A: Pengembangan Template (Oleh Panitia / PJ)
Fase ini berfokus pada pembuatan struktur dasar yang bersih, *bug-free*, dan siap dikembangkan oleh mahasiswa.

### Phase 1: Setup Project & Arsitektur Dasar
*   **Tujuan:** Membangun fondasi folder dan file yang rapi.
*   **Langkah-langkah:**
    1.  Buat folder project utama (contoh: `template-portofolio`).
    2.  Buat file inti di *root directory*: `index.html`, `portfolio.html`, dan `contact.html`.
    3.  Buat file styling utama: `style.css`.
    4.  Buat struktur folder aset:
        *   `assets/images/` (untuk foto profil, hero, *dummy* portofolio).
        *   `assets/certificates/` (untuk *dummy* sertifikat).
    5.  Tambahkan *boilerplate* HTML5 dasar (tag `<html>`, `<head>`, `<body>`) pada semua file HTML.

### Phase 2: Pembuatan Struktur HTML (Kerangka)
*   **Tujuan:** Menyusun struktur elemen *semantic* HTML tanpa memikirkan desain visual terlebih dahulu.
*   **Langkah-langkah:**
    1.  **Global:** Buat `<nav>` dan `<footer>` standar yang dapat di-*copy-paste* ke ketiga halaman.
    2.  **Home:** Buat struktur *Hero Section* (nama, teks, kontainer foto) dan *About Section*.
    3.  **Portfolio:** Buat kerangka untuk *grid* atau *list* penampung *card*. Buat satu HTML `div` *card* sebagai standar (*blueprint*) untuk *Project* dan *Sertifikat*.
    4.  **Contact:** Buat daftar atau tabel sederhana untuk menampung nama anggota dan *link* media sosial.

### Phase 3: Styling Dasar dan Responsiveness (CSS)
*   **Tujuan:** Memberikan tampilan visual yang profesional dan memastikan layout tidak berantakan di *handphone*.
*   **Langkah-langkah:**
    1.  Atur *reset CSS* (margin, padding, box-sizing) dan tentukan *font-family* utama (contoh: *Google Fonts*).
    2.  Gunakan **Flexbox** untuk mengatur posisi elemen di *Navbar*, *Hero Section*, dan *Card Layout*.
    3.  Berikan gaya visual (warna latar, warna teks, *border-radius*, bayangan/shadow pada *card*).
    4.  Implementasikan *Media Queries* (`@media (max-width: 768px)`) untuk membuat susunan grid berubah menjadi vertikal di ukuran layar HP.

### Phase 4: Finalisasi Template & Publikasi Repositori
*   **Tujuan:** Memastikan template siap digunakan dan diunduh (di-*fork* / di-*clone*) oleh mahasiswa baru.
*   **Langkah-langkah:**
    1.  Masukkan data *dummy* / *placeholder* (misal: "Nama Kelompok", foto ilustrasi anonim, dsb).
    2.  Berikan **komentar HTML** (`<!-- ... -->`) yang jelas di area yang harus diubah oleh mahasiswa (contoh: `<!-- GANTI FOTO DISINI -->`).
    3.  Lakukan pengujian (tes *klik link*, tes buka di *mobile*).
    4.  Inisialisasi Git (`git init`), buat *commit* pertama, dan dorong (push) ke *Repository Template* di GitHub publik.

---

## 🚀 FASE B: Implementasi & Deployment (Oleh Mahasiswa Baru)
Fase ini dilakukan oleh mahasiswa baru menggunakan repositori template yang sudah disediakan di *Fase A*.

### Phase 5: Kloning & Penyesuaian Profil Kelompok
*   **Tujuan:** Memiliki salinan *code* secara mandiri dan mengganti identitas standar.
*   **Langkah-langkah:**
    1.  Salah satu perwakilan kelompok melakukan **Fork** repositori template ke akun GitHub sendiri, lalu melakukan *Clone* ke laptop.
    2.  Edit file `index.html`: Ubah nama kelompok, ganti deskripsi, dan perbarui struktur navigasi jika diperlukan.
    3.  Ganti *file* gambar di dalam folder `assets/images/` dengan foto asli kelompok, lalu perbarui *path* fotonya di tag `<img>`.
    4.  Edit file `contact.html`: Masukkan nama anggota asli dan tautkan (link) ke *URL* Instagram/LinkedIn masing-masing.

### Phase 6: Pemasukan Data Portofolio & Sertifikat
*   **Tujuan:** Mengisi halaman portofolio dengan pencapaian nyata (tidak menggunakan *dummy*).
*   **Langkah-langkah:**
    1.  Siapkan *file* gambar sertifikat dan gambar tangkapan layar *project*, simpan ke folder aset yang sesuai.
    2.  Buka `portfolio.html`.
    3.  Temukan blok kode HTML untuk *Card*.
    4.  Ubah isi *Card Dummy* pertama dengan data asli (Judul, Gambar, Tahun).
    5.  Jika ada lebih dari satu sertifikat, blok atau *highlight* keseluruhan elemen `<div class="card">...</div>`, lakukan *copy*, lalu *paste* tepat di bawahnya. Ulangi proses pengubahan teks dan gambar.

### Phase 7: Version Control & Deployment (Go-Live!)
*   **Tujuan:** Menyimpan seluruh perubahan dengan aman dan menayangkannya ke internet.
*   **Langkah-langkah:**
    1.  Buka terminal/command prompt.
    2.  Jalankan perintah Git secara berurutan:
        *   `git add .` (Memasukkan seluruh file yang berubah).
        *   `git commit -m "feat: perbarui data kelompok dan tambah sertifikat"` (Memberikan label sejarah perubahan).
        *   `git push origin main` (Mengirim ke GitHub).
    3.  Buka repositori GitHub kelompok di browser.
    4.  Masuk ke menu **Settings > Pages**.
    5.  Pilih *source branch* (biasanya `main` atau `master`) dan simpan.
    6.  Tunggu 1-5 menit hingga GitHub memunculkan pesan centang hijau beserta URL situs.
    7.  Website kelompok resmi **Live** dan tautannya dapat diserahkan ke Panitia/Dosen!
