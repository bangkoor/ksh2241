# Panduan memasang di GitHub Pages

Folder ini hanya berisi satu file yang perlu diunggah: `index.html`.
Tidak perlu database dan tidak perlu server. Daftar mahasiswa sudah tertanam
di dalam file dalam bentuk terenkripsi (nama dan NIM tidak tertulis terbuka).

## 1. Buat repository
1. Masuk ke github.com, klik **New repository**.
2. Beri nama, misalnya `tugas-uav`, pilih **Public**, klik **Create repository**.
3. Klik **uploading an existing file**, unggah `index.html`, lalu **Commit changes**.
   (File PANDUAN.md ini tidak perlu diunggah.)

## 2. Aktifkan GitHub Pages
1. Buka **Settings → Pages**.
2. Pada **Source** pilih **Deploy from a branch**, branch **main**, folder **/ (root)**, klik **Save**.
3. Tunggu 1–2 menit. Situs aktif di `https://<username>.github.io/tugas-uav/`.

## 3. Memakai subdomain (opsional)
Subdomain harus berasal dari domain yang DNS-nya bisa Anda atur.

1. Di pengelola DNS domain Anda, buat record:
   - Tipe: `CNAME`
   - Nama/host: `tugas` (atau nama lain yang diinginkan)
   - Nilai/target: `<username>.github.io`
2. Di GitHub, buka **Settings → Pages → Custom domain**, isi `tugas.domainanda.id`, klik **Save**.
3. Setelah pemeriksaan DNS berhasil (bisa beberapa menit sampai beberapa jam), centang **Enforce HTTPS**.
   HTTPS wajib, karena halaman memakai fitur enkripsi browser yang hanya berjalan di HTTPS.

Jika ingin subdomain kampus (misalnya `xxx.ipb.ac.id`), record CNAME di atas harus
dibuatkan oleh unit TI kampus. Ajukan permintaan dengan menyebutkan target `<username>.github.io`.

## 4. Mengubah email, tenggat, atau daftar mahasiswa
Minta Claude membuat ulang `index.html`, lalu unggah dan timpa file lama di repository
(**Add file → Upload files**). Parameter tugas setiap mahasiswa tidak berubah saat dibuat ulang.
