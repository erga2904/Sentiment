# Panduan Deployment Backend ke Vercel 🌐

Karena Anda menggunakan **Vercel**, proses deployment backend Python (`server.py`) menjadi sangat terintegrasi. Berikut adalah langkah-langkahnya:

## 1. Persiapan Struktur File
Pastikan file-file berikut ada di root repositori Anda:
- `server.py` (Backend utama)
- `requirements.txt` (Daftar library Python)
- `vercel.json` (Konfigurasi routing Vercel yang baru saya buat)

## 2. Langkah Deployment di Dashboard Vercel
1. Login ke [Vercel](https://vercel.com).
2. Klik **"Add New"** > **"Project"**.
3. Hubungkan repositori GitHub Anda.
4. Vercel akan otomatis mendeteksi konfigurasi dari `vercel.json`.
5. Klik **"Deploy"**.

## 3. Menghubungkan Frontend (GitHub Pages) ke Vercel
Setelah deployment selesai, Vercel akan memberikan URL (misal: `https://sentiment-analysis-backend.vercel.app`).

1. Buka file `sentiment.html`.
2. Ganti nilai `PRODUCTION_API_URL` (Baris ~1350) dengan URL dari Vercel:
   ```javascript
   const PRODUCTION_API_URL = "https://nama-project-anda.vercel.app";
   ```
3. Commit dan Push perubahan tersebut ke GitHub.

## Mengapa Vercel?
- **Serverless**: Anda tidak perlu mengelola server manual.
- **Auto-scaling**: Backend akan otomatis menyesuaikan dengan jumlah pengunjung.
- **Gratis**: Paket Hobby Vercel sudah sangat cukup untuk kebutuhan portofolio.

Sekarang dashboard Anda sudah siap dijalankan secara live! 🚀
