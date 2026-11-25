# Penggunaan pada Claude

## Claude Projects

1. Buat Project baru.
2. Unggah [AGENTS.md](../AGENTS.md), [CLAUDE.md](../CLAUDE.md), dan berkas pada `config/`.
3. Tambahkan ringkasan instruksi pada Project Instructions.
4. Unggah skill atau contoh yang relevan secara bertahap.
5. Mulai percakapan proyek untuk setiap bab atau kelompok paragraf.

## Prompt per tugas

```text
Gunakan mode THESIS REVIEW berdasarkan berkas konteks dalam Knowledge.
Jangan menganggap contoh pada thesis-context sebagai fakta final.
Tandai klaim yang memerlukan sumber dengan [PERLU SUMBER ILMIAH].
Tandai referensi yang perlu diperiksa dengan [PERLU VERIFIKASI SITASI].
Jangan mengubah data atau membuat referensi baru.
```

Jika Claude tidak dapat mengakses berkas otomatis, tempel isi `AGENTS.md` dan berkas `config/` pada awal percakapan.
