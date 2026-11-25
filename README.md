# Generator Surat Pengujian – LPBJ JTB 2026

Aplikasi web satu file (`index.html`) untuk membuat dokumen pengujian Laboratorium Pengujian Bahan Jalan Wilayah Jawa Timur dan Bali (BBPJN Jatim-Bali):

1. Surat Jawaban Permohonan Pengujian
2. Surat Perjanjian Pengujian (Kontrak)
3. Surat Tugas Pengujian
4. Penyerahan Sampel Uji
5. Form Penerimaan Sampel Uji (LPBJ/F-3/PP-04)
6. Kaji Ulang Permintaan Pengujian

## Cara pakai

Buka `index.html` di browser (Chrome disarankan). Tidak perlu instalasi atau server. Isi form, klik **⚡ Generate Semua Dokumen**, lalu cetak/PDF atau download Word dari tab **Preview & Cetak**.

Butuh koneksi internet untuk font (Google Fonts) dan library `docx` (jsDelivr, cadangan unpkg) untuk export Word Surat Jawaban & Perjanjian.

## Export

- **Word (.docx)** — tombol *Download Word* di dialog Cetak/PDF dan tombol 📝 Word di kartu dokumen memakai jalur yang sama (`doWord`).
  - Surat Jawaban & Perjanjian dibuat dengan library docx.js (KOP di header halaman 1, nomor halaman mulai halaman 2).
  - Surat Tugas, Penyerahan, Penerimaan & Kaji Ulang memakai template Word yang tertanam (`TPL_*`, docxtemplater), diisi dari data form dengan logika yang sama seperti preview.
- **Cetak/PDF** — membuka jendela cetak browser; nomor halaman memakai `@page` margin box (Chrome/Edge 131+).

## Known issues

- Tombol Word di tab **History** masih memakai export HTML lama (`.doc`): KOP bisa terpotong dan layout Nomor/Sifat/Hal berantakan.
- Hasil **✏ Edit Teks** di preview tidak ikut ke file Word (Word dibuat ulang dari data form).
- Ejaan "LABOTORIUM" di KOP Surat Tugas & Penyerahan perlu dicocokkan dengan form resmi.
