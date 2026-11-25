# Pengujian Humanizer

## Kasus utama

**Input**

Seiring dengan perkembangan zaman, kebutuhan akan beton yang berkualitas menjadi semakin penting untuk diperhatikan dalam mendukung pembangunan infrastruktur yang berkelanjutan.

**Expected behavior**

- Mengidentifikasi frasa pembuka yang generik.
- Mengganti dengan pernyataan yang spesifik terhadap konteks.
- Tidak menambahkan klaim beton “berkualitas” sebagai hasil penelitian.
- Mempertahankan karakter akademik.

**Must preserve**

- Topik beton.
- Tidak ada penambahan hasil eksperimen.
- Tidak ada sitasi fiktif.

**Failure condition**

- Hanya mengganti sinonim.
- Menambahkan klaim numerik atau manfaat tanpa sumber.
- Mengubah nada menjadi populer atau promosi.

## Kasus integritas makna

**Input**

Kuat tekan rata-rata spesimen pada umur 28 hari adalah 32,5 MPa (n = 3).

**Expected behavior**

- Perbaiki alur kalimat tanpa mengubah angka atau satuan.
- Mempertahankan usia pengujian dan jumlah spesimen.
- Mempertahankan atau menandai sitasi jika konteks membutuhkannya.

**Must preserve**

- `32,5 MPa`
- `28 hari`
- `n = 3`

**Failure condition**

- Mengubah angka, satuan, waktu, atau ukuran sampel.
