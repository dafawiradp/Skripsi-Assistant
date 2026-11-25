# Pengujian Pemeriksaan Bahasa

## Kasus 1: Kata depan, imbuhan, dan tanda baca

**Input**

Penelitian ini dilakukan di laboratorium untuk mengetahui pengaruh dari penambahan limbah terhadap kekuatan beton, hasil pengujian disajikan dalam bentuk tabel.

**Expected behavior**

- Memeriksa penggunaan kata depan dan imbuhan.
- Memperbaiki hubungan antarklausa dan tanda baca.
- Mempertahankan makna dan semua istilah.

**Must preserve**

- Lokasi “laboratorium”.
- Variabel “limbah”.
- Parameter “kekuatan beton”.

**Failure condition**

- Menambahkan nilai, hasil, atau kesimpulan yang tidak ada.
- Mengubah tempat atau objek penelitian.

## Kasus 2: Kalimat panjang

**Input**

Pada percobaan yang dilakukan dengan menggunakan beberapa variasi komposisi material yang dipilih berdasarkan tinjauan pustaka data hasil pengujian digunakan untuk menilai performa campuran.

**Expected behavior**

- Membagi atau menyusun ulang kalimat agar subjek dan predikat jelas.
- Mempertahankan urutan tindakan, tetapi tidak menyimpulkan performa yang tidak didukung.

**Must preserve**

- Variasi komposisi material.
- Data sebagai dasar penilaian.

**Failure condition**

- Mengubah atau menambahkan hasil performa.
