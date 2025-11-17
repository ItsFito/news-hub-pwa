# 🚀 Quick Start Guide - News Hub PWA

Panduan cepat untuk memulai dengan News Hub PWA dalam 5 menit!

## 1️⃣ Jalankan Aplikasi Lokal (2 menit)

### Buka Command Prompt/PowerShell

- Windows: Tekan `Win + R` → ketik `cmd` → Enter

### Jalankan command:

```bash
cd c:\Users\Azzam\source\Modul 3
python -m http.server 8000
```

### Buka di Browser

```
http://localhost:8000
```

✅ **Selesai! Aplikasi sudah berjalan**

---

## 2️⃣ Test Offline (1 menit)

1. Buka DevTools: `F12`
2. Tab "Application" → "Service Workers"
3. Check "Offline" checkbox
4. Refresh page (`F5`)

✅ **Aplikasi tetap berfungsi tanpa internet!**

---

## 3️⃣ Test Installation (1 menit)

### Di Chrome/Edge

- Chrome: Klik icon install di address bar
- Atau klik tombol "⬇️ Install Aplikasi" di navbar

### Di Smartphone

- Chrome: Menu (⋮) → "Install app"
- Safari: Share → "Add to Home Screen"

✅ **Aplikasi siap diinstal di home screen!**

---

## 4️⃣ Deploy ke Vercel (1 menit)

### Option A: Via Web (Paling Mudah)

1. Go to https://vercel.com
2. Klik "Add New" → "Project"
3. Select GitHub repo `news-hub-pwa`
4. Click "Deploy"
5. **Tunggu 1-2 menit sampai selesai**

### Option B: Via CLI

```bash
# Install Vercel CLI (sekali saja)
npm install -g vercel

# Deploy (di folder project)
vercel
```

✅ **Aplikasi live di internet!**

---

## 📋 Checklist

- [ ] Aplikasi berjalan di localhost:8000
- [ ] Service Worker registered (DevTools)
- [ ] Offline mode berfungsi
- [ ] Installation prompt muncul
- [ ] Deploy ke Vercel berhasil
- [ ] Vercel URL accessible
- [ ] Profil page menampilkan data Anda

---

## 🔗 Important Links

| Item                   | Link                           |
| ---------------------- | ------------------------------ |
| **Local Server**       | `http://localhost:8000`        |
| **Vercel Dashboard**   | `https://vercel.com/dashboard` |
| **Repository**         | GitHub repo Anda               |
| **Full Documentation** | Lihat `README.md`              |
| **Deployment Guide**   | Lihat `DEPLOYMENT.md`          |
| **Testing Guide**      | Lihat `TESTING.md`             |

---

## ❓ Troubleshooting

### Aplikasi blank di localhost

```bash
# Pastikan di folder yang benar
cd c:\Users\Azzam\source\Modul 3

# Jalankan ulang server
python -m http.server 8000
```

### Service Worker tidak muncul

- Buka DevTools → Clear site data
- Refresh browser (Ctrl+Shift+R)

### Deploy fail di Vercel

- Push ke GitHub dulu
- Cek files terupload ke repo
- Try import ulang project

---

## 📞 Next Steps

1. ✅ **Test Lokal** → Baca `TESTING.md`
2. ✅ **Deploy ke Vercel** → Baca `DEPLOYMENT.md`
3. ✅ **Submit Link** → Paste Vercel URL ke form

---

## 🎉 Success!

Jika semua di atas berhasil, PWA Anda siap production!

**Selamat mengerjakan! 💪**
