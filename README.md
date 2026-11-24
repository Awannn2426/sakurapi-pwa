# SakuRapi (PWA)

Isi folder ini:

- `index.html`            : aplikasi (satu file)
- `manifest.webmanifest`  : nama, warna, dan ikon aplikasi
- `sw.js`                 : service worker (offline + pembaruan otomatis)
- `icons/`                : ikon aplikasi

## 1. Taruh di internet (pilih salah satu, semuanya gratis)

### Netlify (paling mudah)
1. Buka https://app.netlify.com/drop
2. Tarik **seluruh isi folder ini** (atau folder yang sama setelah di-unzip) ke halaman itu.
3. Kamu langsung dapat link, misalnya `https://nama-acak.netlify.app`.
   Nama bisa diganti di Site settings > Change site name.

### GitHub Pages
1. Buat repositori baru di GitHub, unggah semua file ke root repositori.
2. Settings > Pages > Source: pilih branch `main`, folder `/ (root)`.
3. Link: `https://username.github.io/nama-repo/`

Aplikasi HARUS dibuka lewat `https://` agar bisa dipasang dan jalan offline.
Jangan membuka `index.html` langsung dari penyimpanan HP.

## 2. Pasang di HP

- **Android (Chrome):** buka link, ketuk menu titik tiga, pilih "Pasang aplikasi" / "Tambahkan ke layar utama".
- **iPhone (Safari):** buka link, ketuk tombol Bagikan, pilih "Tambah ke Layar Utama".

## 3. Cara memperbarui aplikasi

1. Ganti file yang berubah (biasanya `index.html`) dengan versi baru.
2. Buka `sw.js`, naikkan angka versi: `sakurapi-v1` menjadi `sakurapi-v2`, dan seterusnya.
3. Unggah ulang (Netlify: tarik folder lagi ke halaman Deploys; GitHub: commit file baru).
4. Di HP, tutup lalu buka aplikasi dua kali. Versi baru muncul otomatis.

## Yang perlu diketahui

- Data tersimpan di browser tiap perangkat, tidak tersinkron antar HP. Jangan hapus data situs/browser, karena catatan ikut hilang.
- Login hanya memisahkan akun di satu perangkat dan bukan keamanan sungguhan. Jangan pakai kata sandi yang sama dengan akun penting lain.
- Scan struk, baca foto mutasi, dan baca teks struk membutuhkan Claude dan hanya jalan di claude.ai.
  Di luar itu, tombolnya menampilkan pesan dan kamu tetap bisa mencatat manual, impor CSV, atau tempel teks mutasi.
- Untuk dipakai banyak orang, langkah berikutnya adalah backend (login, database, dan scan lewat server).
