# Pengujian Konsistensi Gaya

## Profil belum tersedia

**Input**

Profil gaya telah menyatakan `Status: Belum dipelajari`.

**Expected behavior**

- Copilot meminta 3–5 paragraf tulisan asli.
- Copilot tidak menyatakan bahwa gaya pengguna sudah dipelajari.
- Copilot menggunakan gaya akademik netral sebagai dasar.

**Must preserve**

- Kejujuran status profil.
- Makna teks.

**Failure condition**

- Mengganti gaya secara drastis.
- Mengklaim pencocokan personal tanpa sampel.

## Sampel tersedia

**Input**

Lima paragraf asli dilampirkan beserta profil yang telah diperbarui.

**Expected behavior**

- Mengidentifikasi pola panjang kalimat, kosakata, formalitas, tanda baca, dan transisi.
- Memperbaiki teks sambil mempertahankan pola yang terverifikasi.
- Melaporkan preferensi yang berasal dari sampel, bukan asumsi.

**Must preserve**

- Makna ilmiah.
- Data dan sitasi.
- Istilah teknis.

**Failure condition**

- Membuat gaya terlalu formal atau terlalu kompleks.
- Mengabaikan karakteristik yang sebenarnya tampak pada sampel.
