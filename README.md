# 📚 Perpustakaan GMNI Cabang Banjarmasin

> Sistem katalog digital perpustakaan **Gerakan Mahasiswa Nasional Indonesia (GMNI) Cabang Banjarmasin** — membangun intelektual kader bangsa melalui literasi.

---

## 🗂️ Deskripsi Proyek

Aplikasi web statis untuk mengelola dan menampilkan katalog koleksi buku perpustakaan GMNI Cabang Banjarmasin. Dibuat sepenuhnya dengan **HTML, CSS, dan JavaScript murni** (tanpa framework eksternal), sehingga dapat langsung dibuka di browser tanpa server.

---

## ✨ Fitur

| Fitur | Keterangan |
|---|---|
| 🔍 **Pencarian Real-time** | Cari buku berdasarkan judul, penulis, atau kategori |
| 🏷️ **Filter Kategori** | Saring koleksi per kategori (Fiksi, Politik, Psikologi, dll.) |
| ↕️ **Sorting** | Urutkan berdasarkan judul, tahun terbit, penulis, atau rating |
| ❤️ **Favorit** | Tandai buku favorit — tersimpan otomatis di browser (`localStorage`) |
| 📊 **Counter Strip** | Ringkasan jumlah total buku, buku tersedia, dan buku difavoritkan |
| 📱 **Responsive** | Tampilan menyesuaikan layar mobile dan desktop |
| 🎨 **Tema Merah-Emas** | Identitas visual GMNI dengan palet warna merah dan emas |

---

## 🗃️ Struktur Proyek

```
perpustakaan-gmni/
├── index.html               # Halaman utama — katalog buku
├── detail.html              # Halaman detail buku (per id)
├── assets/                  # Folder cover buku lokal
│   ├── Buku Laskar Pelangi.jpg
│   ├── Buku Sapiens.jpg
│   ├── Buku Filosofi Teras.jpg
│   ├── Buku Laut Bercerita.jpg
│   ├── Buku Pemikiran Politik Sukarno.jpg
│   ├── Buku Homo Deus.jpg
│   ├── Buku Negeri 5 Menara.jpg
│   ├── Buku The Communist Manifesto.jpg
│   ├── Buku Ikigai.jpg
│   ├── Buku Sejarah Gerakan Mahasiswa Indonesia.jpg
│   ├── Buku Thinking, Fast and Slow.jpg
│   ├── Buku Pulang.jpg
│   └── Rich Dad Poor Dad.png
└── README.md
```

---

## 📖 Koleksi Buku (15 Judul)

| No | Judul | Penulis | Tahun | Kategori | Status |
|---|---|---|---|---|---|
| 1 | Bumi Manusia | Pramoedya Ananta Toer | 1980 | Fiksi Sejarah | ✅ Tersedia |
| 2 | Laskar Pelangi | Andrea Hirata | 2005 | Fiksi Inspiratif | ✅ Tersedia |
| 3 | Atomic Habits | James Clear | 2018 | Pengembangan Diri | 🔴 Dipinjam |
| 4 | Sapiens | Yuval Noah Harari | 2011 | Sejarah & Ilmu Pengetahuan | ✅ Tersedia |
| 5 | Filosofi Teras | Henry Manampiring | 2019 | Filsafat | ✅ Tersedia |
| 6 | Laut Bercerita | Leila S. Chudori | 2017 | Fiksi Sejarah | ✅ Tersedia |
| 7 | Pemikiran Politik Sukarno | Lambert Giebels | 2001 | Politik & Nasionalisme | ✅ Tersedia |
| 8 | Homo Deus | Yuval Noah Harari | 2015 | Sejarah & Ilmu Pengetahuan | 🟡 Segera Hadir |
| 9 | Negeri 5 Menara | Ahmad Fuadi | 2009 | Fiksi Inspiratif | ✅ Tersedia |
| 10 | The Communist Manifesto | Karl Marx & Friedrich Engels | 1848 | Politik & Nasionalisme | ✅ Tersedia |
| 11 | Ikigai | Héctor García & Francesc Miralles | 2016 | Pengembangan Diri | 🔴 Dipinjam |
| 12 | Sejarah Gerakan Mahasiswa Indonesia | John Ingleson | 1988 | Politik & Nasionalisme | ✅ Tersedia |
| 13 | Thinking, Fast and Slow | Daniel Kahneman | 2011 | Psikologi | ✅ Tersedia |
| 14 | Pulang | Leila S. Chudori | 2012 | Fiksi Sejarah | ✅ Tersedia |
| 15 | Rich Dad Poor Dad | Robert T. Kiyosaki | 1997 | Pengembangan Diri | ✅ Tersedia |

---

## ➕ Cara Menambah Buku Baru

Buka `index.html`, temukan array `daftarBuku` di dalam tag `<script>`, lalu tambahkan objek baru mengikuti format berikut:

```javascript
{
    id: "16",                          // ID unik (lanjutkan dari nomor terakhir)
    judul: "Judul Buku",
    penulis: "Nama Penulis",
    tahun: "2024",
    kategori: "Kategori Buku",         // Sesuaikan atau buat kategori baru
    status: "Tersedia",                // "Tersedia" | "Dipinjam" | "Segera Hadir"
    rating: 4,                         // Angka 1–5
    sinopsis: "Deskripsi singkat buku...",
    cover: "assets/nama-cover.jpg"     // Path lokal atau URL gambar
}
```

> **Catatan:** Pastikan setiap `id` bersifat unik agar fitur favorit dan halaman detail bekerja dengan benar.

---

## 🖼️ Mengganti Foto Background Hero

Pada bagian CSS `.hero-bg`, isi properti `background-image` dengan path foto:

```css
.hero-bg {
    background-image: url('foto-perpustakaan.jpg');
    /* Ukuran foto disarankan minimal 1920×600 px (landscape) */
}
```

Jika tidak diisi, tampilan akan menggunakan gradient merah sebagai fallback otomatis.

---

## 🛠️ Teknologi

- **HTML5** — Struktur halaman
- **CSS3** — Styling, animasi, dan layout responsif (CSS Grid & Flexbox)
- **Vanilla JavaScript** — Logika pencarian, filter, sorting, dan favorit
- **localStorage** — Penyimpanan data favorit di sisi klien
- **Google Fonts** — Tipografi `EB Garamond` (serif elegan) dan `DM Sans` (modern)

---

## 🚀 Cara Menjalankan

Tidak diperlukan instalasi atau server. Cukup:

1. **Clone atau unduh** repositori ini
2. **Buka** file `index.html` langsung di browser

```bash
git clone https://github.com/username/perpustakaan-gmni.git
cd perpustakaan-gmni
# Buka index.html di browser favorit Anda
```

Atau untuk pengalaman terbaik, gunakan ekstensi **Live Server** di VS Code.

---

## 📋 Kategori Koleksi

- 📜 Fiksi Sejarah
- 💡 Fiksi Inspiratif
- 🌱 Pengembangan Diri
- 🏛️ Filsafat
- 🗳️ Politik & Nasionalisme
- 🧠 Psikologi
- 🔬 Sejarah & Ilmu Pengetahuan

---

## 👤 Pembuat

**Musa Al Kadzim**
© 2026 — Perpustakaan GMNI Cabang Banjarmasin

---

> *"Membaca adalah jendela dunia. Literasi adalah senjata perjuangan."*
> — GMNI Cabang Banjarmasin
