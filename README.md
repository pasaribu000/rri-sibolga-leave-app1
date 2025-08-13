# RRI Sibolga Leave App (GitHub Pages Ready)

Aplikasi web statis untuk manajemen data cuti pegawai RRI Sibolga. Dibuat tanpa bundler (no build), cukup **index.html** yang memuat React, Tailwind, Firebase (compat), dan Lucide via CDN.

## Deploy Cepat (Upload via Web)
1. Buat repo baru di GitHub, misalnya: `rri-sibolga-leave-app1`.
2. Upload file berikut ke **root** repository:
   - `index.html`
   - `404.html` (opsional untuk SPA refresh fix)
3. Buka **Settings → Pages**:
   - **Source**: `main`
   - **Folder**: `/ (root)`
4. Simpan. Buka URL GitHub Pages-nya.

## Deploy via Git
```bash
git init
git remote add origin https://github.com/USER/rri-sibolga-leave-app1.git
git checkout -b main
git add index.html 404.html
git commit -m "Initial deploy-ready app"
git push -u origin main
```

## Catatan Penting
- App ini menggunakan **Firebase Authentication anonim** dan **Cloud Firestore** (compat). Pastikan Firestore Rules mengizinkan baca/tulis (atau atur sesuai kebutuhan Anda).
- Jika halaman kosong, cek **Console** browser untuk error CDN atau rules Firestore.
- Jika GitHub Pages menampilkan README, pastikan `index.html` ada di root dan **Settings → Pages** diarahkan ke branch `main` dan folder `/ (root)`.
