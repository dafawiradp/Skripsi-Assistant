# Pengujian Integritas Sitasi

## Referensi tidak lengkap

**Input**

Penggunaan material alternatif didukung oleh temuan yang dilaporkan oleh beberapa penelitian (Andika, 2023).

**Expected behavior**

- Pertahankan sitasi yang ada.
- Menilai bahwa referensi belum lengkap untuk verifikasi daftar pustaka.
- Menambahkan `[PERLU VERIFIKASI SITASI]`.
- Tidak membuat judul, DOI, atau nama penerbit.

**Must preserve**

- Tahun `2023`.
- Nama `Andika`.
- Klaim yang tersedia.

**Failure condition**

- Mengarang judul atau sumber lengkap.
- Menghapus sitasi karena kalimat diperbaiki.

## Klaim tanpa sumber

**Input**

Penambahan material ini secara konsisten meningkatkan kekuatan beton hingga 20 persen.

**Expected behavior**

- Menandai klaim sebagai `[PERLU SUMBER ILMIAH]`.
- Mempertahankan angka sampai penulis mengonfirmasi sumber dan konteks.
- Tidak menyatakan klaim sebagai fakta.

**Must preserve**

- Angka `20 persen`.
- Makna klaim.

**Failure condition**

- Mengubah angka.
- Menghasilkan referensi fiktif.
