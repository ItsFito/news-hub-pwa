# 🎯 START HERE - Instruksi Eksekusi

File ini adalah panduan paling sederhana untuk menjalankan aplikasi News Hub PWA.

---

## ✅ Sebelum Mulai

Pastikan file-file berikut sudah ada di folder:

```
c:\Users\Azzam\source\Modul 3\
```

**Cek dengan:**

```powershell
cd c:\Users\Azzam\source\Modul 3
dir
```

**Harus ada file:**

- index.html ✅
- styles.css ✅
- sw.js ✅
- manifest.json ✅

---

## 🚀 Langkah 1: Jalankan Lokal (1 menit)

### Buka PowerShell/Command Prompt

- Windows: Tekan `Win + R`
- Ketik: `powershell` atau `cmd`
- Enter

### Copy-Paste Command Ini:

```powershell
cd c:\Users\Azzam\source\Modul 3
python -m http.server 8000
```

### Expected Output:

```
Serving HTTP on 0.0.0.0 port 8000
```

✅ **Server berjalan!**

---

## 🌐 Langkah 2: Buka di Browser (30 detik)

1. Buka browser (Chrome, Firefox, Edge, dll)
2. Klik address bar
3. Ketik: `http://localhost:8000`
4. Press Enter

✅ **Aplikasi muncul!**

---

## 🧪 Langkah 3: Test Offline Mode (1 menit)

### Test Service Worker:

1. Press `F12` (buka DevTools)
2. Klik tab "Application" (atas)
3. Klik "Service Workers" (sidebar kiri)
4. Lihat status: harus "active and running" ✅

### Test Offline:

1. Tab "Service Workers" (terbuka)
2. Centang checkbox "Offline"
3. Refresh page (`F5`)
4. Aplikasi tetap berfungsi ✅

---

## 👤 Langkah 4: Update Profil (2 menit)

### Edit Profile Data:

1. Buka file `index.html` dengan text editor
2. Press `Ctrl+F` cari: `Muhammad Azzam Ridho`
3. Ubah menjadi: `NAMA ANDA`
4. Cari: `2301234567`
5. Ubah menjadi: `NIM ANDA`
6. Cari: `Kelompok 3 - Web Development`
7. Ubah menjadi: `KELOMPOK ANDA`
8. Save file (`Ctrl+S`)

### Refresh browser:

- Press `Ctrl+R` atau `F5`
- Klik "Profil" di navbar
- Data sudah terupdate ✅

---

## 🌍 Langkah 5: Deploy ke Vercel (5 menit)

### Option A: Via Web (Paling Mudah)

1. Go to: https://vercel.com/signup
2. Sign up dengan GitHub
3. Authorize Vercel
4. Di dashboard, klik "Add New" → "Project"
5. Pilih repo: `news-hub-pwa` (atau import baru)
6. Click "Import"
7. Click "Deploy"
8. **Tunggu 2 menit** sampai selesai
9. Copy URL yang diberikan

### Option B: Via CLI (Alternatif)

```powershell
# Install Vercel (sekali saja)
npm install -g vercel

# Deploy (di folder project)
cd c:\Users\Azzam\source\Modul 3
vercel

# Follow prompts
# Copy URL hasil deployment
```

✅ **Aplikasi live di internet!**

---

## 📋 Final Checklist

Sebelum submit, pastikan:

- [ ] Aplikasi berjalan di localhost:8000
- [ ] Service Worker active di DevTools
- [ ] Offline mode tested & working
- [ ] Profil data sudah update dengan data Anda
- [ ] Deploy ke Vercel sukses
- [ ] Vercel URL bisa diakses di browser
- [ ] Vercel URL link sudah dicopy

---

## 🔗 Link Penting

| Yang perlu        | Link                           |
| ----------------- | ------------------------------ |
| Local Server      | `http://localhost:8000`        |
| Vercel            | `https://vercel.com`           |
| Create Repo       | `https://github.com/new`       |
| Vercel Dashboard  | `https://vercel.com/dashboard` |
| Your Deployed App | Diberikan oleh Vercel          |

---

## ⚠️ Jika Error

### "python not found"

```powershell
# Install Python dari: https://python.org
# Check: python --version
```

### "Port 8000 in use"

```powershell
# Gunakan port lain:
python -m http.server 9000
# Visit: http://localhost:9000
```

### "Service Worker not showing"

1. DevTools (F12) → Clear site data
2. Close semua tab localhost
3. Hard refresh: `Ctrl+Shift+R`
4. Reload page

### "Deploy fail"

1. Pastikan push ke GitHub dulu:
   ```bash
   git add .
   git commit -m "Update"
   git push origin main
   ```
2. Try import ulang di Vercel

---

## 📞 Butuh Bantuan?

**Docs Lengkap di folder project:**

- `QUICK_START.md` - 5 menit intro
- `TESTING.md` - Test detail
- `DEPLOYMENT.md` - Deploy detail
- `README.md` - Dokumentasi lengkap
- `DOCUMENTATION_INDEX.md` - Daftar semua docs

---

## 🎉 Success Indicators

✅ **Berhasil jika:**

1. ✅ Aplikasi berjalan di localhost:8000
2. ✅ Bisa navigate ke 4 halaman
3. ✅ Service Worker registered
4. ✅ Offline mode works
5. ✅ Deploy ke Vercel complete
6. ✅ Vercel URL accessible
7. ✅ Profil menampilkan data Anda

---

## 🚀 Next Steps

Setelah semua di atas berhasil:

1. **Copy Vercel URL** (contoh: `https://news-hub-pwa.vercel.app`)
2. **Paste ke form submission** yang sudah diberikan
3. **Submit!**

---

## ⏱️ Time Estimate

| Task          | Time        |
| ------------- | ----------- |
| Run lokal     | 1 min       |
| Test offline  | 1 min       |
| Update profil | 2 min       |
| Deploy Vercel | 5 min       |
| Test Vercel   | 2 min       |
| **Total**     | **~11 min** |

---

## 📝 Commands Quick Reference

```powershell
# Run local server
cd c:\Users\Azzam\source\Modul 3
python -m http.server 8000

# Deploy to Vercel
vercel

# Push to GitHub
git add .
git commit -m "message"
git push origin main

# Clear browser cache
# DevTools (F12) → Application → Clear site data
```

---

**Good luck! You got this! 💪**

**Selamat mengerjakan! 🎊**
