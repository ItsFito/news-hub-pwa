# Panduan Testing News Hub PWA Secara Lokal

Dokumen ini berisi panduan lengkap untuk test aplikasi News Hub PWA di komputer Anda sebelum deploy ke Vercel.

## 🔧 Prerequisites

### Windows

- Python 3 (atau Python 2)
- Web Browser (Chrome, Edge, Firefox, dll)
- Text Editor (VS Code, Notepad++, dll)

### Instalasi Python (Jika Belum)

1. Download dari https://www.python.org/downloads/
2. Saat install, centang "Add Python to PATH"
3. Verify instalasi:

```bash
python --version
```

## 🚀 Menjalankan Aplikasi Lokal

### Method 1: Menggunakan Python

1. **Buka Command Prompt / PowerShell**

   - Windows: Tekan `Win + R`, ketik `cmd` atau `powershell`

2. **Navigate ke folder project**

   ```bash
   cd c:\Users\Azzam\source\Modul 3
   ```

3. **Jalankan Python Server**

   ```bash
   # Untuk Python 3
   python -m http.server 8000

   # Atau untuk Python 2
   python -m SimpleHTTPServer 8000
   ```

4. **Akses Aplikasi**
   - Buka browser
   - Go to: `http://localhost:8000`
   - Aplikasi akan muncul

### Method 2: Menggunakan Node.js (Alternatif)

1. **Install http-server global**

   ```bash
   npm install -g http-server
   ```

2. **Navigate ke folder**

   ```bash
   cd "c:\Users\Azzam\source\Modul 3"
   ```

3. **Jalankan server**

   ```bash
   http-server -p 8000
   ```

4. **Akses**: `http://localhost:8000`

## ✅ Testing Checklist

### 1. Test Navigation (Halaman)

- [ ] **Halaman Beranda (Home)**

  - [ ] Page muncul dengan hero section
  - [ ] Berita unggulan menampilkan 3 kartu
  - [ ] Setiap kartu punya icon, judul, deskripsi, tanggal

- [ ] **Halaman Artikel**

  - [ ] Page menampilkan daftar artikel
  - [ ] Setiap artikel punya judul, metadata, deskripsi
  - [ ] Minimal 5 artikel ditampilkan

- [ ] **Halaman Kategori**

  - [ ] 6 kategori ditampilkan dalam grid
  - [ ] Setiap kategori punya icon, nama, deskripsi
  - [ ] Jumlah artikel per kategori ditampilkan

- [ ] **Halaman Profil**
  - [ ] Avatar/icon menampilkan
  - [ ] Nama: Muhammad Azzam Ridho ✓
  - [ ] NIM: 2301234567 ✓
  - [ ] Kelompok: Kelompok 3 - Web Development ✓
  - [ ] Program Studi: Teknik Informatika
  - [ ] Section "Tentang Aplikasi" menampilkan features list
  - [ ] Version dan timestamp ada

### 2. Test Responsive Design

**Desktop (1200px+)**

- [ ] Navbar horizontal dengan semua menu
- [ ] Content grid 3 kolom untuk cards
- [ ] Comfortable spacing dan sizing

**Tablet (768px - 1199px)**

- [ ] Layout adjust ke 2 kolom
- [ ] Navbar masih horizontal
- [ ] Content readable

**Mobile (< 768px)**

- [ ] Layout single column
- [ ] Navigation mobile-friendly
- [ ] Text sizes readable
- [ ] No horizontal scroll

**Testing dengan DevTools**

1. Buka DevTools (F12)
2. Click device toggle (Ctrl+Shift+M)
3. Test di berbagai resolusi:
   - iPhone 12 (390x844)
   - iPad (768x1024)
   - Laptop (1920x1080)

### 3. Test Service Worker

**Check Registration**

1. Buka DevTools (F12)
2. Ke tab "Application"
3. Sidebar kiri → "Service Workers"
4. Status harus: "active and running"
5. Scope: `http://localhost:8000/` atau `/`

**Check Cache Storage**

1. Tab Application → Cache Storage
2. Akan ada entry "news-hub-v1"
3. Expand untuk lihat cached files:
   - index.html
   - styles.css
   - manifest.json

**Check Manifest**

1. Tab Application → Manifest
2. Verifikasi:
   - name: "News Hub - Progressive Web App"
   - short_name: "News Hub"
   - display: "standalone"
   - theme_color: "#2196F3"
   - icons muncul dengan proper sizes

### 4. Test Offline Functionality

**Simulasi Offline Mode**

1. DevTools → Application tab
2. Klik "Service Workers"
3. Check: "Offline" checkbox
4. Refresh halaman (Ctrl+R)
5. **Expected**: Aplikasi tetap muncul dan berfungsi
6. **Indikator**: Pesan "Mode Offline" di footer

**Alternative Method**

1. DevTools → Network tab
2. Dropdown "Throttling" → pilih "Offline"
3. Refresh page
4. Aplikasi tetap responsive

### 5. Test Installation Prompt

**Desktop (Chrome/Edge)**

1. Buka DevTools (F12)
2. Console tab
3. Jalankan command:
   ```javascript
   let event = new Event("beforeinstallprompt");
   window.dispatchEvent(event);
   ```
4. Tombol "⬇️ Install Aplikasi" harus muncul di navbar
5. Klik tombol → browser akan tampil install dialog

**Manual Test**

1. Chrome/Edge → Buka aplikasi di tab baru
2. Tunggu beberapa detik
3. Icon install mungkin muncul di address bar
4. Klik untuk install

### 6. Test UI/UX

**Styling**

- [ ] Colors match design (blue #2196F3)
- [ ] Fonts readable dan consistent
- [ ] Shadows dan borders ada
- [ ] Spacing/padding consistent

**Animations**

- [ ] Page transitions smooth (fade in)
- [ ] Hover effects pada cards (lift up)
- [ ] Smooth color transitions

**Interactive Elements**

- [ ] Links berfungsi
- [ ] Navigation items respond to clicks
- [ ] Active navigation indicator
- [ ] No console errors (F12 → Console)

### 7. Test Performance

**Network Performance**

1. DevTools → Network tab
2. Refresh halaman
3. Check:
   - index.html: 100-200KB
   - styles.css: 8-10KB
   - Total: < 300KB (tidak termasuk favicon)
   - Load time: < 2 seconds

**Performance Metrics**

1. DevTools → Lighthouse
2. Generate report:
   - Performance: > 90
   - Accessibility: > 80
   - Best Practices: > 80
   - SEO: > 80

### 8. Test Navigasi Hash

**URL Hash Testing**

- [ ] Click Home → URL menjadi `http://localhost:8000/#/`
- [ ] Click Artikel → URL menjadi `http://localhost:8000/#/articles`
- [ ] Click Kategori → URL menjadi `http://localhost:8000/#/categories`
- [ ] Click Profil → URL menjadi `http://localhost:8000/#/profile`
- [ ] Back button browser → Navigate ke halaman sebelumnya
- [ ] Forward button browser → Navigate ke halaman berikutnya

### 9. Console Errors Check

1. Buka DevTools Console (F12)
2. Cek tidak ada error messages (warna merah)
3. Warning boleh ada (warna kuning)
4. Expected messages:
   - "Service Worker registered" (info)
   - Tidak boleh ada "404" atau "failed to fetch"

## 🔍 Debug Tips

### Service Worker tidak ter-register

**Kemungkinan penyebab**:

- File sw.js tidak ada di root directory
- Syntax error di sw.js
- Path di index.html salah

**Solution**:

```javascript
// Di index.html, cek bagian registration
if ("serviceWorker" in navigator) {
  navigator.serviceWorker
    .register("sw.js")
    .then((registration) => console.log("Registered:", registration))
    .catch((error) => console.log("Failed:", error));
}
```

### Cache tidak update

**Solution**:

1. Buka DevTools
2. Application → Service Workers
3. Klik "Unregister" (jika ada)
4. Klik "Clear site data"
5. Refresh halaman

### Manifest tidak load

**Check**:

1. Verifikasi link di HTML: `<link rel="manifest" href="manifest.json">`
2. Cek manifest.json valid JSON (gunakan https://jsonlint.com/)
3. Check DevTools Console untuk error

## 📊 Testing Report Template

Gunakan template ini untuk dokumentasi testing:

```
Testing Report - News Hub PWA
Date: [Tanggal Testing]
Tester: [Nama]
Environment: [Windows/Mac/Linux] - [Chrome/Firefox/Safari]
Test Duration: [Jam]

✅ PASSED
- [Feature 1]
- [Feature 2]

⚠️ WARNINGS
- [Issue 1]
- [Issue 2]

❌ FAILED
- [Bug 1]
- [Bug 2]

Overall Status: [PASS/FAIL]
Ready to Deploy: [YES/NO]
```

## 🎯 Pre-Deployment Verification

Sebelum upload ke Vercel, pastikan:

- [ ] Semua file ada di folder project
- [ ] index.html valid dan tidak ada syntax error
- [ ] styles.css applied dengan benar
- [ ] sw.js registered dan active
- [ ] manifest.json valid
- [ ] Data profil sudah update dengan data Anda
- [ ] Offline mode berfungsi
- [ ] Responsive design tested
- [ ] No console errors
- [ ] Service Worker cache working

## 🚀 Siap untuk Deploy

Jika semua checklist terpenuhi, aplikasi siap untuk deploy ke Vercel!

Lanjut ke: **DEPLOYMENT.md**

---

**Testing Completed**: ****\_\_\_****
**Tester Name**: ****\_\_\_****
**Status**: [ ] PASS [ ] FAIL
