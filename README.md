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

Butuh koneksi internet untuk font (Google Fonts) dan library `docx` untuk export Word Surat Jawaban & Perjanjian.

## Known issues

- Download Word untuk Surat Jawaban & Surat Perjanjian gagal: URL library `docx` di cdnjs 404, dan kode memakai `Packer.toBuffer()` yang hanya jalan di Node.js.
- Export Word Surat Tugas, Penyerahan Sampel, dan Kaji Ulang hanya mengisi sebagian data (sisanya template kosong).
