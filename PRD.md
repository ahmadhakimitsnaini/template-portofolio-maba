# Product Requirements Document (PRD)
## Proyek: Template Website Portofolio Mahasiswa

---

### 1. Executive Summary
Proyek "Template Website Portofolio Mahasiswa" adalah sebuah inisiatif edukasi yang dirancang untuk Mahasiswa Baru Angkatan IX. Proyek ini bertujuan untuk menyediakan template dasar website portofolio berbasis HTML dan CSS statis. Fokus utama dari proyek ini bukanlah membangun sistem perangkat lunak yang kompleks, melainkan memberikan wadah praktik langsung bagi mahasiswa untuk memahami fundamental web development, alur kerja version control menggunakan Git/GitHub, dan proses deployment secara gratis. Melalui inisiatif ini, mahasiswa didorong untuk membangun kebiasaan mendokumentasikan serta memamerkan hasil karya dan sertifikasi secara profesional dalam ekosistem digital.

### 2. Objectives & Success Metrics

**Objectives:**
*   Mengajarkan fundamental HTML dan CSS kepada mahasiswa baru tanpa framework yang rumit.
*   Melatih alur manajemen *source code* secara kolaboratif menggunakan GitHub.
*   Membantu mahasiswa memahami proses web *deployment* secara langsung melalui GitHub Pages.
*   Menyediakan platform portofolio digital yang mudah diperbarui dan dipelihara secara mandiri.

**Success Metrics:**
*   **Completion Rate:** 100% kelompok berhasil melakukan *deployment* website menggunakan GitHub Pages dan dapat diakses publik tanpa error.
*   **Customization Rate:** 100% kelompok berhasil mengubah konten *default* (teks, gambar, informasi profil, dan struktur portofolio) menjadi data asli kelompok masing-masing.
*   **Git Proficiency:** Terdapat riwayat *commit* yang merepresentasikan kontribusi anggota di dalam repositori GitHub.
*   **Constraint Compliance:** Tidak ada kelompok yang melanggar batasan teknis (bebas dari framework eksternal seperti React, Tailwind, atau rendering array JavaScript).

### 3. User Personas

**1. Pengguna Utama (Pembuat): Mahasiswa Baru Angkatan IX**
*   **Kebutuhan/Kemampuan Target:** Mahasiswa pada tahap ini sedang mempelajari dasar pemrograman web. Mereka diharapkan mampu mengedit tag HTML, memodifikasi styling CSS sederhana, mengganti aset gambar/informasi, menambahkan seksi portofolio dan sertifikat secara manual, mengelola repositori GitHub, dan mengeksekusi deployment GitHub Pages.
*   **Karakteristik Utama:** Membutuhkan struktur kode (template) yang lugas dan tidak *over-engineered*. Mereka ingin dengan cepat melihat hasil perubahan *code* mereka di *browser*.

**2. Pengguna Website (Pengunjung)**
*   **Profil:** Terdiri dari Sesama Mahasiswa, Dosen, Panitia/Penanggung Jawab (PJ), serta pihak eksternal seperti Rekruter.
*   **Kebutuhan:** Ingin melihat profil, karya, dan pencapaian mahasiswa dengan navigasi yang intuitif dan responsif. Mereka membutuhkan tampilan yang profesional, rapi, dan informatif (kontak jelas, deskripsi portofolio valid dan dapat diverifikasi).

### 4. User Stories & Acceptance Criteria

**Epic 1: Manajemen Konten Profil dan Kelompok**
*   **User Story:** Sebagai mahasiswa baru, saya ingin dapat mengganti teks profil dan foto di HTML agar website merepresentasikan identitas diri dan kelompok saya.
    *   **Acceptance Criteria:** File HTML memiliki tag dan penamaan *class* yang eksplisit sehingga mudah diidentifikasi untuk mengubah nama kelompok, deskripsi, dan mengganti path foto anggota tanpa perlu mengubah logika.

**Epic 2: Navigasi dan Hubungan Profesional**
*   **User Story:** Sebagai pengunjung (misal: Rekruter), saya ingin bisa melihat dan mengklik akun sosial media atau profil GitHub anggota kelompok agar saya bisa menghubungi atau mengevaluasi lebih lanjut profil mereka.
    *   **Acceptance Criteria:** Terdapat seksi Contact yang memuat tautan yang valid dan dapat di-klik menuju profil platform profesional (LinkedIn, GitHub, dll) untuk masing-masing anggota.

**Epic 3: Manajemen Portofolio dan Sertifikat**
*   **User Story:** Sebagai mahasiswa baru, saya ingin bisa menambahkan *card* sertifikat baru hanya dengan melakukan *copy-paste* kode HTML agar saya dapat dengan cepat memperbarui portofolio setiap kali mendapatkan sertifikat baru.
    *   **Acceptance Criteria:** Struktur *card* portofolio/sertifikat dibangun murni dengan HTML/CSS tanpa sistem *rendering* JavaScript loop/array. Penambahan konten dilakukan secara eksplisit dengan menyalin elemen `div` *card* ke baris berikutnya.
*   **User Story:** Sebagai dosen atau rekruter, saya ingin melihat rincian dari setiap pencapaian agar dapat memvalidasi perkembangan mahasiswa.
    *   **Acceptance Criteria:** Setiap *card* menampilkan aset gambar, judul/nama, lembaga/platform penerbit, tahun pencapaian, dan tautan (jika ada) ke dokumen asli.

**Epic 4: Deployment dan Aksesibilitas**
*   **User Story:** Sebagai mahasiswa baru, saya ingin mempublikasikan portofolio kelompok saya secara mudah dan gratis agar bisa dibagikan (di-share) ke khalayak umum.
    *   **Acceptance Criteria:** Repositori GitHub terstruktur dengan file utama `index.html` di *root directory*. Pengaturan GitHub Pages dapat diaktifkan tanpa konfigurasi *build step* yang kompleks. URL publik dapat diakses tanpa hambatan.

### 5. Functional Requirements

Template portofolio secara minimum harus mencakup struktur halaman/seksi berikut:

*   **Global Navigation (Navbar):**
    *   Terletak di semua halaman.
    *   Berisi nama/logo kelompok.
    *   Memiliki tautan navigasi statis: `Home`, `Portfolio`, `Contact`.
*   **Halaman Home (`index.html`):**
    *   **Hero Section:** Menampilkan nama kelompok, *tagline* atau deskripsi singkat, dan foto representatif kelompok. Desain dapat mengadopsi layout CSS Flexbox sederhana.
    *   **About / Informasi Kelompok:** Menyajikan detail singkat mengenai anggota, minat studi, atau latar belakang pembentukan kelompok.
*   **Halaman Portfolio (`portfolio.html`):**
    *   **Seksi Projects:** Katalog *project* dalam format *card*. Memuat: Gambar, Judul, Deskripsi singkat, Tahun, dan Link (jika tersedia).
    *   **Seksi Certifications:** Katalog sertifikat dalam format *card*. Memuat: Gambar sertifikat, Nama/Judul sertifikat, Platform penyelenggara, Tahun, dan Link kredensial (opsional).
    *   *Catatan:* Struktur *card* wajib didesain seragam agar mudah di-copy-paste mahasiswa.
*   **Halaman Contact (`contact.html`):**
    *   Menampilkan daftar seluruh anggota kelompok.
    *   Terdapat tautan langsung ke Instagram, LinkedIn, GitHub, atau platform lain yang relevan.
*   **Responsiveness:**
    *   Semua halaman harus disesuaikan agar dapat ditampilkan dengan baik di ukuran layar desktop, tablet, maupun *mobile* (responsif).

### 6. Technical & System Constraints

Proyek ini sangat mengedepankan kesederhanaan untuk tujuan edukasi dasar. Oleh karena itu, batasan teknis berikut wajib ditaati:

*   **Murni HTML/CSS:** Dilarang menggunakan *framework* atau *library* CSS (seperti Tailwind CSS, Bootstrap, Bulma, dsb).
*   **JavaScript Minimalis:** Penggunaan JS sangat dibatasi. Hanya diperbolehkan untuk interaksi UI yang mendasar (seperti *hamburger menu toggle*). Dilarang keras menggunakan JS untuk *rendering list*, *looping array*, *state management*, atau menyimpan data portofolio di variabel JS.
*   **No Backend, No Database, No API:** Website bersifat 100% statis. Dilarang menggunakan sistem CMS, koneksi database, ataupun proses autentikasi (Login).
*   **Deployment Wajib via GitHub Pages:** Situs harus dan hanya boleh di-*deploy* menggunakan infrastruktur GitHub Pages dari *repository* publik terkait. Tidak boleh menggunakan platform lain seperti Vercel, Netlify, atau layanan hosting *cloud* lainnya.
*   **Struktur Folder Standar & Bersih:**
    *   `index.html`, `portfolio.html`, `contact.html` berada langsung di direktori *root*.
    *   Satu file `style.css` untuk tata letak visual global.
    *   Pengelompokan gambar diatur dalam folder `assets/images/` dan `assets/certificates/`.
