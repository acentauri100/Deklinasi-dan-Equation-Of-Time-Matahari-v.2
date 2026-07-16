# Instrumen Data Matahari — SamawatLab

Aplikasi web untuk menghitung **azimuth, altitude, deklinasi, dan equation of time (perata waktu)** matahari — per jam (hingga interval 1 menit), per hari, atau per bulan — lengkap dengan tabel, grafik naik-turun, dan ilustrasi interaktif yang dapat digeser waktunya.

- Algoritma perhitungan: **Jean Meeus** — *Astronomical Algorithms* (posisi matahari, nutasi, obliquity, equation of time), dengan polinomial ΔT Espenak–Meeus.
- Implementasi & pengembangan: **Muhammad Thoyfur**.
- Satu file HTML mandiri (`index.html`) — tidak perlu server backend, database, atau build step apa pun.

## Menjalankan secara lokal

Cukup buka `index.html` langsung di browser (butuh koneksi internet untuk memuat font Google Fonts: Amiri & Cairo). Tidak ada instalasi atau `npm install` yang diperlukan.

## Deploy ke GitHub Pages (langkah demi langkah)

### 1. Buat repository baru
1. Buka [github.com/new](https://github.com/new).
2. Beri nama repo, misalnya `instrumen-data-matahari`.
3. Set ke **Public**, lalu klik **Create repository**.

### 2. Unggah `index.html`
**Cara termudah (lewat browser, tanpa terminal):**
1. Di halaman repo, klik **Add file → Upload files**.
2. Seret (drag-and-drop) file `index.html` dari folder ini.
3. Klik **Commit changes**.

**Atau lewat Git di terminal:**
```bash
git clone https://github.com/USERNAME/instrumen-data-matahari.git
cd instrumen-data-matahari
cp /path/ke/index.html .
git add index.html
git commit -m "Tambah Instrumen Data Matahari"
git push
```

### 3. Aktifkan GitHub Pages
1. Di repo, buka **Settings → Pages** (menu kiri).
2. Pada **Build and deployment → Source**, pilih **Deploy from a branch**.
3. Pada **Branch**, pilih `main` dan folder `/ (root)`, lalu **Save**.
4. Tunggu 1–2 menit. GitHub akan menampilkan URL situs, biasanya:
   ```
   https://USERNAME.github.io/instrumen-data-matahari/
   ```
5. Karena nama filenya sudah `index.html`, situs langsung terbuka di URL tersebut tanpa perlu menuliskan nama file.

### 4. Update di kemudian hari
Setiap kali `index.html` diedit dan di-*commit* ulang (upload ulang lewat web, atau `git push`), GitHub Pages otomatis memperbarui situs dalam waktu singkat — tidak perlu langkah tambahan.

## Struktur proyek

```
index.html   ← seluruh aplikasi (HTML + CSS + JS) dalam satu file
README.md    ← panduan ini
```

## Ringkasan fitur

- **Lokasi**: input lintang/bujur format DMS, atau isi otomatis lewat GPS perangkat.
- **Zona waktu**: preset WIB/WITA/WIT/UTC atau offset kustom.
- **3 mode data**: Per Jam (interval hingga 1 menit), Per Hari (rentang tanggal + jam acuan), Per Bulan (rentang bulan/tahun + tanggal & jam acuan).
- **Ilustrasi interaktif**: geser slider jam-dalam-sehari atau hari-dalam-setahun untuk melihat deklinasi & equation of time berubah langsung, atau tekan "Animasikan Setahun".
- **Grafik naik-turun** deklinasi dan equation of time sepanjang periode yang dipilih.
- **Tabel data** dengan ekspor CSV.

---
مِنَ الْحِسَابِ إِلَى الْبَصِيرَة — *dari perhitungan menuju pemahaman*
