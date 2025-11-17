# News Hub - Progressive Web App

Aplikasi PWA (Progressive Web App) yang dibangun dengan HTML5, CSS3, dan JavaScript vanilla. Aplikasi ini memungkinkan pengguna membaca berita dan artikel dengan dukungan offline functionality.

## 📋 Daftar Isi

- [Fitur Utama](#fitur-utama)
- [Persyaratan Teknis](#persyaratan-teknis)
- [Struktur Proyek](#struktur-proyek)
- [Instalasi](#instalasi)
- [Penggunaan](#penggunaan)
- [Fitur PWA](#fitur-pwa)
- [Deployment ke Vercel](#deployment-ke-vercel)
- [Informasi Profil](#informasi-profil)

## ✨ Fitur Utama

### Halaman dan Navigasi

- **Halaman Beranda**: Menampilkan hero section dan berita unggulan
- **Halaman Artikel**: Koleksi artikel dengan informasi lengkap
- **Halaman Kategori**: Menampilkan berbagai kategori konten
- **Halaman Profil**: Informasi pengembang dengan NIM dan kelompok

### Responsive Design

- Desain mobile-first yang sempurna di semua ukuran layar
- Navigasi yang intuitif dan user-friendly
- Animasi dan transisi yang halus

### PWA Features

- **Service Worker**: Caching strategy untuk offline functionality
- **Web App Manifest**: Installable application dengan custom branding
- **Offline Support**: Aplikasi dapat bekerja tanpa koneksi internet
- **Add to Home Screen**: Dapat diinstal seperti aplikasi native

## 🔧 Persyaratan Teknis

### Teknologi yang Digunakan

- **HTML5**: Semantic markup dan struktur aplikasi
- **CSS3**: Styling responsif dengan Flexbox dan Grid
- **JavaScript (ES6+)**: Vanilla JS tanpa framework
- **Service Worker API**: Untuk offline functionality
- **Web App Manifest**: Untuk PWA installation

### Browser Support

- Chrome/Edge 40+
- Firefox 44+
- Safari 11+
- Opera 27+

## 📁 Struktur Proyek

```
news-hub-pwa/
├── index.html          # File HTML utama dengan 4 halaman
├── styles.css          # Stylesheet lengkap dengan responsive design
├── sw.js              # Service Worker untuk offline functionality
├── manifest.json      # Web App Manifest untuk PWA
├── package.json       # Konfigurasi npm
├── vercel.json        # Konfigurasi Vercel deployment
├── .gitignore         # Git ignore rules
├── README.md          # Dokumentasi ini
└── LICENSE            # Lisensi MIT
```

## 🚀 Instalasi

### Locally (Development)

1. Clone atau download repositori:

```bash
git clone https://github.com/azzamridho/news-hub-pwa.git
cd news-hub-pwa
```

2. Jalankan local server:

```bash
# Menggunakan Python 3
python -m http.server 8000

# Atau menggunakan Python 2
python -m SimpleHTTPServer 8000

# Atau menggunakan Node.js http-server
npx http-server
```

3. Buka browser dan akses:

```
http://localhost:8000
```

## 💻 Penggunaan

### Navigasi Halaman

- Gunakan navigation bar di bagian atas untuk berpindah antar halaman
- Klik logo untuk kembali ke halaman beranda
- URL hash (#) akan berubah sesuai halaman yang dipilih

### Menginstal Aplikasi

1. Akses aplikasi di browser (harus HTTPS untuk production)
2. Klik tombol "⬇️ Install Aplikasi" di navigation bar
3. Ikuti prompt browser untuk install
4. Aplikasi akan muncul di home screen/app drawer

### Mode Offline

1. Setelah instalasi dan caching awal, matikan internet
2. Aplikasi tetap berjalan dengan data yang sudah di-cache
3. Indikator "Mode Offline" akan muncul di footer

## 🌐 Fitur PWA

### Service Worker

Service Worker kami mengimplementasikan:

- **Cache-First Strategy**: Prioritas ke cached resources
- **Network Fallback**: Fallback ke network jika cache miss
- **Auto-Caching**: Update cache saat network tersedia
- **Offline Support**: Full offline functionality

### Web App Manifest

Manifest menyediakan:

- Custom app name dan icon
- Theme colors dan styling
- App shortcuts untuk quick access
- Screenshots untuk app stores
- Start URL dan orientation

### Installability

Aplikasi dapat diinstal di:

- Smartphones dan tablets (iOS dan Android)
- Desktop (Windows, Mac, Linux)
- Sebagai progressive web app atau app-like experience

## 📊 Informasi Profil

### Data Pengembang

- **Nama**: Muhammad Azzam Ridho
- **NIM**: 2301234567
- **Kelompok**: Kelompok 3 - Web Development
- **Program Studi**: Teknik Informatika

### Fitur Demonstrasi

Halaman profil menunjukkan:

- Identitas pengembang
- Detail kelompok dan institusi
- Fitur-fitur PWA yang diimplementasikan
- Informasi versi aplikasi

## 🌍 Deployment ke Vercel

### Persiapan

1. Buat akun di [Vercel.com](https://vercel.com)
2. Install Vercel CLI:

```bash
npm install -g vercel
```

### Deploy Steps

1. Di folder proyek, jalankan:

```bash
vercel
```

2. Ikuti prompt:

   - Confirm project setup
   - Confirm root directory (default: `.`)
   - Link to GitHub/GitLab repo (optional)

3. Vercel akan auto-deploy setiap push ke main branch

### Post-Deployment

- Vercel akan memberikan URL deployment (contoh: `https://news-hub-pwa.vercel.app`)
- URL ini dapat dibagikan dan diakses dari mana saja
- HTTPS akan otomatis diaktifkan
- Service Worker akan bekerja penuh di production

### Kustomisasi Domain

Di Vercel dashboard:

1. Pilih project
2. Go to Settings > Domains
3. Tambah custom domain jika tersedia

## 📱 Testing di Mobile

### Android

1. Buka aplikasi di Chrome
2. Tap menu (⋮) → "Install app"
3. Konfirmasi installation

### iOS

1. Buka di Safari
2. Tap Share → "Add to Home Screen"
3. Pilih nama dan tambahkan

## 🔐 Security Notes

- Service Worker hanya cache resources dari same origin
- HTTPS required untuk production PWA
- No external API calls (hanya static data)
- No local storage usage (data dimuat dari HTML)

## 📄 Lisensi

MIT License - Bebas digunakan untuk keperluan personal dan komersial

## 🤝 Kontribusi

Untuk menambah fitur atau perbaikan:

1. Fork repositori
2. Buat branch baru untuk feature
3. Commit perubahan
4. Push dan buat Pull Request

## 📞 Kontak & Support

Untuk pertanyaan atau issue:

- Buat GitHub Issue
- Contact: azzam@example.com

---

**Version**: 1.0.0  
**Last Updated**: November 2025  
**Status**: Production Ready ✅
