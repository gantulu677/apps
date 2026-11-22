FRONTEND E-COMMERCE — APPROVED REQUIREMENTS

Dokumen: Approved & Locked Requirements
Versi dokumen: 1.0
Tanggal: 23 November 2026
Cakupan: Frontend Only
Status: Baseline Disetujui

1. Requirement Registry

ID

Requirement

Priority

Version

Status

R-001

Single Store E-Commerce Architecture

HIGH

1.0

LOCKED

R-002

React + Vite + TypeScript Frontend

HIGH

1.0

LOCKED

R-003

Responsive Mobile-First Application Design

HIGH

1.0

LOCKED

R-004

Complete Storefront, Customer Account & Checkout Pages

HIGH

1.0

LOCKED

R-005

Modern Minimalist E-Commerce Storefront Design

HIGH

1.0

LOCKED

R-007

Responsive Mobile Design System & Native Mobile UI Experience

HIGH

1.0

LOCKED

R-008

Browser Zoom Restriction

MEDIUM

1.0

LOCKED

R-009

Customer Authentication & Account Access

HIGH

1.0

LOCKED

R-010

Phone-Based Login & Registration Flow

HIGH

1.0

LOCKED

Total: 9 requirement terkunci.

2. Functional & Non-Functional Requirements

R-001 — Single Store E-Commerce Architecture

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST menggunakan model bisnis Single Store dengan satu entitas toko, satu storefront, dan satu akun administrator utama.

Sistem tidak menyediakan:

Multi-vendor.

Multi-store.

Akun staf.

Multi-admin.

R-002 — React + Vite + TypeScript Frontend

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST menggunakan React sebagai library utama frontend, Vite sebagai development server dan build tool, serta TypeScript sebagai bahasa pemrograman frontend.

Implementasi MUST menggunakan arsitektur component-based yang modular, reusable, konsisten, dan mudah dipahami, dikembangkan, serta dipelihara oleh AI Agent.

R-003 — Responsive Mobile-First Application Design

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Seluruh aplikasi MUST menerapkan Mobile-First Responsive Design, mencakup Storefront dan Admin Dashboard.

Semua halaman, komponen, navigasi, layout, serta interaksi MUST responsif dan optimal untuk:

Mobile.

Tablet.

Desktop.

Batasan Cakupan

Admin Dashboard tidak termasuk dalam cakupan implementasi frontend proyek ini berdasarkan keputusan audit AUD-001.

Requirement R-003 tetap dipertahankan tanpa perubahan. Penyebutan Admin Dashboard tidak memperluas cakupan implementasi frontend proyek ini.

R-004 — Complete Storefront, Customer Account & Checkout Pages

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST mencakup Storefront, Customer Account, dan Checkout & Transaction.

Setiap kelompok MUST memiliki halaman yang dibutuhkan sesuai daftar yang telah disepakati, dengan arsitektur halaman dan komponen modular, reusable, konsisten, serta mudah dikembangkan dan dipelihara oleh AI Agent.

Admin Dashboard tidak termasuk dalam cakupan frontend aplikasi ini.

Approved Page Registry

A. Storefront

No.

Page

1

Home

2

Product Listing

3

Product Detail

4

Category

5

Search

6

Wishlist

7

Cart

B. Customer Account

No.

Page

1

Login

2

Register

3

Forgot Password

4

Profile

5

Address Management

6

Order History

7

Order Detail

C. Checkout & Transaction

No.

Page

1

Checkout

2

Shipping Selection

3

Payment Selection

4

Order Confirmation

5

Payment Result

6

Order Tracking

Catatan Implementasi Forgot Password

Halaman Forgot Password tercantum dalam Page Registry yang telah disetujui.

Namun, mekanisme pemulihan password belum tersedia pada tahap frontend berbasis localStorage. Oleh karena itu:

Tidak dibuat simulasi pemulihan password yang seolah-olah benar-benar memproses perubahan password.

Fungsionalitas pemulihan password ditunda sampai mekanisme pendukung tersedia.

Keputusan ini tidak mengubah Page Registry R-004.

R-005 — Modern Minimalist E-Commerce Storefront Design

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Storefront MUST menggunakan desain Modern Commerce dengan pendekatan modern minimalis yang berorientasi pada kemudahan berbelanja.

Desain MUST mengutamakan:

Navigasi kategori yang jelas.

Presentasi produk yang informatif.

Grid produk yang tertata.

Visibilitas harga dan informasi produk.

Seluruh halaman Storefront MUST memiliki visual language yang konsisten, hierarki informasi yang jelas, tata letak bersih, dan mengikuti Responsive Mobile-First Design pada R-003.

R-007 — Responsive Mobile Design System & Native Mobile UI Experience

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST menerapkan Mobile Design System yang konsisten dengan pendekatan Native-Like UI & Interaction pada seluruh halaman Storefront.

Tampilan dan interaksi mobile MUST memberikan pengalaman yang menyerupai aplikasi mobile modern, mencakup:

Pola navigasi mobile.

Bottom navigation.

Touch feedback.

Gesture yang relevan.

Perilaku komponen yang dioptimalkan untuk perangkat layar sentuh.

Seluruh komponen interaktif MUST dapat digunakan tanpa ketergantungan pada hover.

Implementasi MUST tetap menggunakan responsive web application sesuai teknologi frontend pada R-002 dan prinsip Responsive Mobile-First Design pada R-003.

R-008 — Browser Zoom Restriction

Priority: MEDIUM
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST menerapkan pembatasan zoom untuk mempertahankan skala tampilan yang konsisten.

Pembatasan MUST mencakup pinch-to-zoom dan double-tap zoom pada perangkat mobile, serta mekanisme browser-level zoom yang dapat dikendalikan oleh aplikasi.

Implementasi MUST mengupayakan pemblokiran zoom melalui interaksi keyboard dan browser.

Pembatasan berlaku sejauh diizinkan oleh kemampuan browser dan sistem operasi yang digunakan.

Acceptance Criteria

Pinch-to-zoom diblokir pada browser yang mendukung pembatasan.

Double-tap zoom diblokir pada browser yang mendukung pembatasan.

Browser-level zoom dibatasi sejauh memungkinkan.

Keterbatasan browser dan OS didokumentasikan.

Tampilan tetap responsif sesuai R-003.

Accessibility Consideration

Risiko aksesibilitas akibat pembatasan zoom harus didokumentasikan.

R-009 — Customer Authentication & Account Access

Priority: HIGH
Version: 1.0
Status: LOCKED

Requirement

Aplikasi MUST menyediakan autentikasi pelanggan menggunakan nomor telepon dan password.

Setelah autentikasi berhasil, sistem MUST menyediakan Access Token yang divalidasi oleh backend. Frontend MUST menyimpan Access Token dan informasi sesi yang diperlukan di localStorage.

Sistem MUST NOT menggunakan Refresh Token.

Status autentikasi MUST dapat dipulihkan setelah browser ditutup dan dibuka kembali selama Access Token masih berlaku.

Ketika Access Token kedaluwarsa atau tidak valid, aplikasi MUST mengakhiri sesi dan meminta pelanggan melakukan login kembali.

Password pelanggan MUST NOT disimpan di browser.

Saat logout, aplikasi MUST menghapus Access Token dan informasi sesi terkait dari localStorage.

Sistem MUST membatasi akses terhadap data Customer Account hanya kepada pelanggan yang terautentikasi dan berhak mengakses data tersebut.

Batasan Implementasi

Requirement ini merupakan bagian dari baseline yang telah dikunci.

Implementasi backend, validasi token oleh backend, dan layanan autentikasi akan diproses secara terpisah. Tahap proyek saat ini berfokus pada frontend.

R-010 — Phone-Based Login & Registration Flow

Priority: HIGH
Version: 1.0
Status: LOCKED
Scope: Frontend Only

Requirement

Frontend MUST menyediakan alur Login dan Register dinamis berdasarkan keberadaan nomor telepon di localStorage.

Ketentuan:

Jika nomor telepon ditemukan di localStorage, frontend MUST menampilkan form Login dengan input password.

Jika nomor telepon tidak ditemukan di localStorage, frontend MUST menampilkan form Register dengan input nama dan password.

Setelah registrasi frontend berhasil melewati validasi dan simulasi registrasi, nomor telepon MUST disimpan ke localStorage.

Nomor telepon yang sudah dicatat MUST dikenali kembali setelah browser ditutup dan dibuka.

Password MUST NOT disimpan di localStorage.

Mekanisme ini hanya digunakan untuk menentukan tampilan autentikasi frontend dan bukan sebagai validasi akun backend.

Acceptance Criteria

No.

Kriteria

Expected Result

1

Nomor telepon belum tercatat

Form Register ditampilkan

2

Nomor telepon sudah tercatat

Form Login ditampilkan

3

Registrasi frontend berhasil

Nomor telepon dicatat ke localStorage

4

Browser ditutup dan dibuka kembali

Nomor yang pernah dicatat tetap dikenali

5

Password dimasukkan

Password tidak disimpan ke localStorage

Batasan Implementasi

Pencatatan nomor telepon merupakan mekanisme pengenalan lokal pada browser.

Mekanisme ini bukan bukti bahwa akun pelanggan telah terdaftar atau tervalidasi di backend.

3. Approved Supporting Specification

Mobile UI & Layout Specification v1.0

Parent Requirements: R-003 dan R-007
Status: APPROVED

Spesifikasi ini menggabungkan keputusan audit AUD-002 sampai AUD-005.

AUD-001 — Admin Dashboard Scope

Status: RESOLVED

Admin Dashboard sepenuhnya berada di luar cakupan frontend proyek ini.

Frontend proyek ini mencakup Storefront, Customer Account, dan Checkout & Transaction.

Akun administrator utama tetap menjadi bagian dari model bisnis R-001.

Admin Dashboard dapat dikembangkan sebagai proyek atau sistem terpisah.

R-003 tetap LOCKED tanpa perubahan.

AUD-002 — Native-Like Interaction Details

Status: RESOLVED

Bottom Navigation

Bottom Navigation digunakan pada enam halaman utama:

Home.

Product Listing.

Category.

Search.

Wishlist.

Cart.

Contextual Navigation

Product Detail menggunakan contextual back navigation.

Customer Account menggunakan account/contextual navigation.

Checkout & Transaction menggunakan focused transaction navigation.

Gesture

Swipe digunakan untuk product carousel dan image gallery.

Scroll digunakan untuk navigasi konten.

Aksi penting harus memiliki kontrol visual yang jelas.

Aksi penting tidak boleh hanya mengandalkan gesture tersembunyi.

Gesture harus familiar, intuitif, dan konsisten.

AUD-003 — Touch Target & Touch Feedback

Status: RESOLVED

Minimum ukuran target interaktif adalah 44 × 44 CSS pixels.

Spacing harus memadai untuk mencegah kesalahan sentuh.

Elemen interaktif harus memberikan touch feedback ketika ditekan.

Komponen harus memiliki status disabled, loading, success, dan error yang jelas.

Interaksi tidak boleh bergantung pada hover.

AUD-004 — UI States

Status: RESOLVED

Seluruh Storefront, Customer Account, dan Checkout & Transaction harus menggunakan standar UI states yang konsisten:

Loading.

Empty.

Error.

Success.

AUD-005 — Sticky Elements & Root Layout

Status: RESOLVED

Root layout menggunakan struktur flex column.

Root Layout Rules

Root mengisi viewport menggunakan height: 100dvh.

Root menggunakan display: flex dan flex-direction: column.

Root menggunakan overflow: hidden.

Header berada secara natural di bagian atas, di luar area scroll.

Header tidak menggunakan fixed atau sticky positioning.

Main content menggunakan flex: 1, min-height: 0, dan overflow-y: auto.

Bottom area berada di bagian bawah, di luar area scroll.

Bottom area menampung Bottom Navigation dan/atau Bottom Action sesuai kebutuhan halaman.

Bottom Navigation hanya ditampilkan pada halaman yang telah ditentukan.

Bottom Action ditampilkan sesuai kebutuhan halaman.

Safe area perangkat harus diperhitungkan.

Elemen bottom tidak boleh menutupi konten.

Contoh Struktur JSX

<div className="app-layout">
  <header className="app-header">
    Header
  </header>

  <main className="app-content">
    Page Content
  </main>

  <footer className="app-bottom">
    Bottom Navigation / Bottom Action
  </footer>
</div>

Contoh CSS

.app-layout {
  display: flex;
  flex-direction: column;
  height: 100dvh;
  overflow: hidden;
}

.app-header {
  flex-shrink: 0;
}

.app-content {
  flex: 1;
  min-height: 0;
  overflow-y: auto;
}

.app-bottom {
  flex-shrink: 0;
  padding-bottom: env(safe-area-inset-bottom);
}

AUD-006 — Specification Consolidation

Status: RESOLVED

Keputusan AUD-002 sampai AUD-005 dikonsolidasikan menjadi Mobile UI & Layout Specification v1.0.

Spesifikasi ini merupakan spesifikasi turunan dari R-003 dan R-007, bukan requirement baru yang mengubah requirement terkunci.

4. Project Scope & Implementation Boundary

4.1 Included Scope

Tahap proyek saat ini mencakup:

Storefront.

Customer Account.

Checkout & Transaction.

React + Vite + TypeScript frontend.

Component-based architecture.

Responsive Mobile-First Design.

Modern Commerce visual direction.

Native-Like Mobile UI & Interaction.

Mobile UI & Layout Specification.

Frontend Login/Register flow.

Pengenalan nomor telepon melalui localStorage.

Frontend validation dan simulasi interaksi.

UI states: Loading, Empty, Error, Success.

4.2 Excluded Scope

Hal-hal berikut berada di luar cakupan implementasi frontend saat ini:

Admin Dashboard.

Backend implementation.

Database implementation.

Authentication API.

Backend credential validation.

OTP/SMS service.

Backend session management.

Forgot Password processing.

Password recovery mechanism.

Backend akan diproses secara terpisah.

5. Baseline Governance

Semua requirement berstatus LOCKED merupakan baseline yang telah disetujui.

Requirement terkunci tidak boleh diubah secara sepihak.

Perubahan terhadap requirement terkunci harus melalui proses change discussion dan persetujuan eksplisit.

Supporting Specification merupakan turunan requirement dan tidak boleh bertentangan dengan parent requirement.

Implementasi frontend harus mengikuti batas cakupan proyek yang telah disepakati.

Backend tidak boleh ditambahkan sebagai cakupan implementasi dalam tahap ini.

Requirement baru harus memiliki ID baru dan melalui proses analisis, pembahasan, serta persetujuan.

Keputusan yang belum disetujui tidak boleh dianggap sebagai bagian dari baseline.

6. Baseline Summary

Kategori

Jumlah

Approved & Locked Requirements

9

Approved Supporting Specification

1

Resolved Audit Decisions

6

Active Project Scope

Frontend Only

Dokumen ini merupakan kompilasi requirement dan spesifikasi yang telah disetujui atau dikunci berdasarkan keputusan diskusi sampai 23 November 2026.
