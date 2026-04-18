# Deploy GitHub Pages

File yang dipakai untuk frontend publik:

- `index1.html`
- `index.html`
- `config.js`
- `.nojekyll`

`config.js` sudah diisi ke endpoint Apps Script ini:

`https://script.google.com/macros/s/AKfycbwtlGXMATvF06y61X5j67IiRfJUfoXBe8Lc6eXLnNTHAPjWH3Jjmq5uj5TakPXMyWFY/exec`

Jika nanti URL deployment Apps Script berubah, cukup edit `config.js`.

## Checklist 5 Menit

1. Pastikan Apps Script sudah di-deploy sebagai web app.
2. Pastikan akses web app diset ke publik.
3. Upload file frontend ke repository GitHub.
4. Aktifkan GitHub Pages dari branch `main`.
5. Buka URL GitHub Pages Anda.

## Step by Step Dari Nol

### A. Deploy backend Apps Script

1. Buka project Apps Script Anda.
2. Klik `Deploy` > `New deployment`.
3. Pilih tipe `Web app`.
4. Isi deskripsi bebas, misalnya `public-api`.
5. Set `Execute as` ke akun Anda sendiri.
6. Set `Who has access` ke `Anyone`.
7. Klik `Deploy`.
8. Salin URL yang berakhiran `/exec`.
9. Jika URL baru berbeda, buka `config.js` lalu ganti nilai `apiBaseUrl`.

### B. Buat repository di GitHub

1. Login ke GitHub.
2. Klik `New repository`.
3. Isi nama repo.
   Contoh: `ogi-family-menu`
4. Set repo ke `Public`.
5. Klik `Create repository`.

### C. Upload file website

Upload file berikut ke root repository:

- `index.html`
- `index1.html`
- `config.js`
- `.nojekyll`

Cara paling mudah di web GitHub:

1. Masuk ke repository.
2. Klik `Add file` > `Upload files`.
3. Drag semua file di atas.
4. Scroll ke bawah.
5. Klik `Commit changes`.

### D. Aktifkan GitHub Pages

1. Buka repository GitHub Anda.
2. Klik tab `Settings`.
3. Di sidebar, klik `Pages`.
4. Pada bagian `Build and deployment`, pilih `Source: Deploy from a branch`.
5. Pilih branch `main`.
6. Pilih folder `/ (root)`.
7. Klik `Save`.
8. Tunggu sekitar 1 sampai 10 menit sampai deployment selesai.

### E. Buka link publik

Setelah aktif, URL biasanya menjadi:

- `https://USERNAME.github.io/NAMA-REPO/`

Contoh:

- `https://wisnuadhi.github.io/ogi-family-menu/`

Karena root file kita adalah `index.html`, halaman akan langsung diarahkan ke `index1.html`.

## Cara Update Website Nanti

1. Edit file lokal.
2. Upload ulang file yang berubah ke repository GitHub.
3. Commit perubahan.
4. Tunggu GitHub Pages deploy ulang.

## Jika Website Tidak Muncul

1. Cek repository harus `Public` jika memakai GitHub Free.
2. Cek file `index.html` ada di root repository.
3. Cek `Settings` > `Pages` memang memakai branch `main` dan folder `/ (root)`.
4. Cek `config.js` memakai URL Apps Script `/exec`, bukan `/dev`.
5. Cek deployment Apps Script masih aktif dan aksesnya `Anyone`.

## Referensi Resmi

- GitHub Pages quickstart: https://docs.github.com/en/pages/quickstart
- Create a GitHub Pages site: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- Google Apps Script web apps: https://developers.google.com/apps-script/guides/web
