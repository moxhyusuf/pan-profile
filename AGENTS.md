## Instruksi untuk Agent
- Baca file ini sebelum memulai task apapun.
- Setelah menyelesaikan task, update bagian "Status Halaman" dan catat konvensi baru jika ada.

# Project Memory: PAN Web Profile

## 1. Project Overview
- **Nama Project:** Web Profil DPD PAN Probolinggo
- **Tujuan:** Membangun website profil partai statis yang responsif, modern, informatif, dan memiliki visual *premium* bagi audiens lokal.
- **Tech Stack:** HTML5, CSS3 (Vanilla), Bootstrap 5 (grid & utility), Bootstrap Icons, AOS (Animate On Scroll), GLightbox, Swiper.

## 2. Struktur File
- **`index.html`** — Beranda utama web profil.
- **`visimisi.html`** — Informasi tentang Visi & Misi partai.
- **`fraksi.html`** — Halaman profil struktur dan daftar anggota Fraksi PAN DPRD.
- **`program.html`** — Daftar program kerja (*grid cards*) dan list agenda mendatang.
- **`galeri.html`** — Halaman galeri foto dokumentasi.
- **`kontak.html`** — Halaman informasi lokasi (peta), kontak, dan form pesan.
- **`berita.html` & `berita-detail.html`** — Halaman template artikel/berita.
- **`assets/css/main.css`** — Base CSS dan deklarasi desain global proyek.
- **`quick-count.html`** — Data estimasi Quick Count internal partai (Chart.js).
- **`perolehan-suara.html`** — Rekapitulasi suara resmi KPU (Chart.js donut).
- **`sebaran-tps.html`** — Sebaran TPS, saksi, dan pemantauan per kecamatan.
- **`evaluasi-program.html`** — Evaluasi dan capaian program kerja (Chart.js bar).
- **`struktur-relawan.html`** — Kordes, Korcam, Korkab (Tab + Filter JS).
- **`spesifikasi-gen.html`** — Spesifikasi Generasi Muda PAN, sayap organisasi pemuda.
- **`assets/css/main.css`** — Base CSS dan deklarasi desain global proyek.
- **`assets/img/dummy.jpg`** — Aset gambar *placeholder* standar.

## 3. Design System
Mengacu secara garis besar pada `design.md` dan struktur `index.html`:
- **Warna Aksen Utama:** Biru PAN (`#0154a2`) dan variasi gelapnya (`#04415f`).
- **Radius (Border-Radius):** Menggunakan radius melengkung yang modern, utamanya `15px` untuk *card* utama dan `8px` untuk *badge*/tombol.
- **Shadow:** Menggunakan *soft shadow* untuk elemen interaktif.
  - *Default:* `rgba(0, 0, 0, 0.06) 0px 10px 30px 0px`
  - *Hover:* `rgba(0, 0, 0, 0.1) 0px 4px 15px 0px` atau translasi ke atas (*elevate*).
- **Animasi/Transisi:** Semua interaksi hover pada *card* dan *button* menggunakan efek `transition: all 500ms ease;` dipadu `transform: translateY(-5px);`.

## 4. Konvensi Kode
- **Penggunaan CSS:** Jangan menuliskan deklarasi blok `<style>` di tag `<head>` HTML yang masif (terutama jangan pernah mendeklarasikan ulang variabel `:root`). Selalu gunakan `assets/css/main.css`. Hanya gunakan `<style>` kustom untuk gaya yang sangat spesifik pada halaman tersebut (contoh: desain kelas `.info-item` di kontak).
- **Penamaan Class:** Gunakan *kebab-case* dan hindari menumpuk kelas bawaan framework tanpa perlu.
- **Struktur Komponen:**
  - Header, menu navigasi dropdown (`navmenu`), dan struktur footer **wajib seragam dan konsisten** tautannya di semua file `.html`.
  - Judul setiap sub-halaman dibalut dalam komponen `.page-title` dengan background warna biru utama dan teks `h1` berwarna putih (`color: white;`).

## 5. Status Halaman

| Halaman | Fungsi / Fitur Utama | Status |
|---|---|---|
| `index.html` | Landing page web profil | ✅ Selesai |
| `visimisi.html` | Visi & Misi | ✅ Selesai (CSS teroptimasi) |
| `fraksi.html` | Pimpinan & Anggota Fraksi | ✅ Selesai (CSS teroptimasi) |
| `kontak.html` | Form & Lokasi | ✅ Selesai (CSS teroptimasi) |
| `program.html` | Daftar Program Kerja & Agenda | ✅ Selesai |
| `galeri.html` | Foto Dokumentasi Kegiatan | ✅ Selesai |
| `berita.html` | List Daftar Berita | ⏳ Belum Dirombak (Masih Template) |
| `quick-count.html` | Estimasi Suara & Grafik Quick Count | ✅ Selesai (Menggunakan Chart.js) |
| `perolehan-suara.html` | Rekapitulasi Suara Resmi KPU & Grafik Donut | ✅ Selesai (Menggunakan Chart.js) |
| `sebaran-tps.html` | Sebaran TPS, Saksi, dan Pemantauan | ✅ Selesai (Vanilla JS Filter) |
| `evaluasi-program.html` | Evaluasi Program & Grafik Target vs Realisasi | ✅ Selesai (Chart.js) |
| `struktur-relawan.html` | Kordes, Korcam, Korkab (Tab + Filter JS) | ✅ Selesai |
| `spesifikasi-gen.html` | Spesifikasi Gen (Sayap Pemuda PAN) | ✅ Selesai |

## 6. Aturan untuk Agent

- **HARUS** merujuk pada `main.css` dan `design.md` ketika memerlukan nilai parameter visual (warna, ukuran font, margin) sebelum menetapkan atribut *custom*.
- **HARUS** memelihara integritas navigasi (*global link*). Apabila sebuah *path* baru ditambahkan atau file HTML baru dibuat, **wajib** memperbarui semua tautan navigasi terkait di `<header>` dan `<footer>` pada **seluruh file HTML** yang ada (jangan biarkan *oncoming.html* jika file sudah dibuat).
- **HARUS** menggunakan aset `assets/img/dummy.jpg` sebagai *placeholder* gambar untuk konten yang belum tersedia datanya (contoh: foto galeri, thumbnail berita).
- **HARUS** memuat library pihak ketiga melalui CDN yang terpercaya jika membutuhkan visualisasi dinamis (contoh: Chart.js untuk grafik data).
- **TIDAK BOLEH** menaruh *inline styles* (`style="..."`) jika gaya tersebut dapat digunakan berulang; buatlah kelas di dalam blok `<style>` di `<head>`.
- **TIDAK BOLEH** mendeklarasikan variabel `:root` CSS di dalam file HTML individu.
- **TIDAK BOLEH** memodifikasi kelas `.page-title` sehingga visualnya berbeda dengan halaman lain (pastikan background biru dan tulisan putih).
- **HARUS** melakukan `git commit` setiap kali ada perubahan signifikan (pembuatan halaman baru, perbaikan navigasi global, dll).
