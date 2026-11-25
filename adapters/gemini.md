# Penggunaan pada Gemini

## Gem atau project

1. Buat Gem atau project khusus skripsi.
2. Tempelkan instruksi ringkas dari `GEMINI.md`.
3. Unggah atau tambahkan berkas `config/` sebagai konteks.
4. Unggah satu skill yang relevan jika platform mendukung Knowledge atau file attachment.
5. Mulai setiap tugas dengan menyebut mode yang digunakan.

## Prompt per tugas

```text
Gunakan mode ACADEMIC REWRITE.
Bacalah konteks skripsi pada berkas yang dilampirkan.
Susun ulang argumen secara logis dan berbasis bukti.
Pertahankan semua sitasi, variabel, angka, satuan, dan hipotesis.
Jangan menambahkan referensi baru.
```

## Aturan pencarian

Aktifkan pencarian hanya jika pengguna secara eksplisit meminta verifikasi sumber. Pisahkan hasil pencarian dari perbaikan bahasa. Jangan mengubah sitasi lama menjadi referensi lain hanya karena hasil pencarian tampak serupa.
