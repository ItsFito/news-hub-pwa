# Cara Mengupdate Data Profil Anda

File ini menjelaskan bagaimana mengupdate data profil di halaman "Profil" aplikasi News Hub PWA dengan data Anda yang sebenarnya.

## 📝 Langkah-Langkah Update Profile

### 1. Buka File `index.html`

Gunakan text editor apapun (VS Code, Notepad++, Sublime, dll):

```
c:\Users\Azzam\source\Modul 3\index.html
```

### 2. Cari Section Profile

Gunakan `Ctrl+F` untuk cari: `Profile Page`

Atau scroll ke bawah sampai menemukan kode:

```html
<!-- Profile Page -->
<div id="profile-page" class="page"></div>
```

### 3. Update Data

#### Nama

Cari:

```html
<label>Nama Lengkap:</label>
<p>Muhammad Azzam Ridho</p>
```

Ubah menjadi:

```html
<label>Nama Lengkap:</label>
<p>NAMA ANDA DI SINI</p>
```

#### NIM (Nomor Induk Mahasiswa)

Cari:

```html
<label>Nomor Induk Mahasiswa:</label>
<p>2301234567</p>
```

Ubah menjadi:

```html
<label>Nomor Induk Mahasiswa:</label>
<p>NOMOR_NIM_ANDA</p>
```

#### Kelompok

Cari:

```html
<label>Kelompok:</label>
<p>Kelompok 3 - Web Development</p>
```

Ubah menjadi:

```html
<label>Kelompok:</label>
<p>Kelompok NOMOR - NAMA_KELOMPOK_ANDA</p>
```

#### Program Studi (Opsional)

Cari:

```html
<label>Program Studi:</label>
<p>Teknik Informatika</p>
```

Update sesuai kebutuhan Anda.

#### Institusi (Opsional)

Cari:

```html
<label>Institusi:</label>
<p>Universitas/Sekolah</p>
```

Update dengan nama institusi Anda.

### 4. Ganti Avatar (Opsional)

Cari:

```html
<div class="profile-avatar">👨‍💻</div>
```

Ganti emoji sesuai selera (contoh: 👩‍💼, 🧑‍💻, dll)

## ✅ Verifikasi Update

1. Simpan file (Ctrl+S)
2. Refresh browser (Ctrl+F5) atau F5
3. Klik menu "Profil"
4. Verifikasi data sudah terupdate

## 💾 Save Changes

Jika menggunakan Git:

```bash
git add index.html
git commit -m "Update profile with personal data"
git push origin main
```

Vercel akan otomatis redeploy dengan data baru!

## 📋 Contoh Data Lengkap

Jika Anda seorang mahasiswa:

```html
<label>Nama Lengkap:</label>
<p>Budi Santoso</p>

<label>Nomor Induk Mahasiswa:</label>
<p>2301234567</p>

<label>Kelompok:</label>
<p>Kelompok 2 - Frontend Development</p>

<label>Program Studi:</label>
<p>Teknik Informatika</p>

<label>Institusi:</label>
<p>Universitas Negeri XYZ</p>
```

## ⚠️ Penting

- Jangan hapus tag HTML, hanya ubah text di antara `<p>` dan `</p>`
- Pastikan format tetap sama
- Save file dengan encoding UTF-8
- Test di browser sebelum deploy

## 🚀 Deploy Updated Profile

Setelah update:

1. Test lokal: `http://localhost:8000`
2. Push ke GitHub
3. Vercel akan otomatis redeploy
4. Check Vercel URL untuk verifikasi

Done! ✅
