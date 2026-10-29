# DESIGN.md — Panduan Token & Sistem Desain ShelfSystem

Dokumen ini mendefinisikan standar token desain visual dan aksesibilitas (WCAG compliant) untuk aplikasi perpustakaan **ShelfSystem**.

---
s
## 1. Palet Warna & Aksesibilitas (Colorblind-Friendly)
Setiap informasi status atau pesan penting **tidak boleh hanya mengandalkan warna**, melainkan wajib disertai ikon dan label teks yang kontras.

| Peran Token | Warna Nama | Kode Hex / Nilai | Penggunaan Utama |
| :--- | :--- | :--- | :--- |
| **Primary** | Deep Slate Blue | `#1E3A8A` | Warna utama, header, tombol navigasi, dan elemen branding. |
| **Action / Secondary** | Dark Teal | `#0D9488` | Tombol aksi utama, tautan, dan elemen interaktif sekunder. |
| **Success / Available** | Forest Green | `#15803D` | Status buku tersedia, konfirmasi berhasil. |
| **Warning / Danger** | Deep Crimson | `#B91C1C` | Status denda, keterlambatan, tombol hapus/peringatan. |
| **Neutral Text** | Slate Gray | `#0F172A` | Warna teks utama agar kontras di atas latar belakang terang. |

---

## 2. Tipografi
Menggunakan kombinasi font modern yang bersih dan sangat mudah dibaca untuk mendukung aksesibilitas layar.

- **Font Judul (Headings)**: `Plus Jakarta Sans` (Tebal, tegas, dan modern untuk judul halaman & card).
- **Font Isi (Body / Text)**: `Inter` (Sangat optimal untuk teks paragraf, form, dan tabel dengan ukuran minimum 16px).

---

## 3. Spasi & Tata Letak (Spacing & Layout)
- **Jarak Dasar (Base Spacing)**: `16px` (`1rem`) sebagai kelipatan standar margin dan padding antar elemen.
- **Sudut Lengkung (Border Radius)**: `8px` (`0.5rem`) untuk komponen card, modal dialog, dan tombol.

---

## 4. Variabel CSS (Implementasi ke Kode)
Nantinya pada tahap pembuatan kode (Hari 2 dan seterusnya), token di atas dapat didefinisikan ke dalam variabel CSS berikut:

```css
:root {
  --warna-utama: #1E3A8A;
  --warna-aksi: #0D9488;
  --warna-sukses: #15803D;
  --warna-bahaya: #B91C1C;
  --warna-teks: #0F172A;
  --font-judul: 'Plus Jakarta Sans', sans-serif;
  --font-isi: 'Inter', sans-serif;
  --jarak: 1rem;
  --sudut: 0.5rem;
}