# Skripsi Assistant

Repository panduan dan kumpulan *skills* untuk membantu GitHub Copilot melakukan penyuntingan dan peninjauan skripsi berbahasa Indonesia secara akademik, konsisten, dan berintegritas.

Repository ini ditujukan bagi mahasiswa non-IT. Anda tidak perlu menulis kode. Cukup buka folder repository ini di VS Code, aktifkan GitHub Copilot Chat, lalu berikan instruksi dan teks skripsi.

## Tujuan

Asisten ini membantu:

- memeriksa ejaan dan tata bahasa Indonesia;
- memperbaiki kalimat agar alami tetapi tetap formal dan ilmiah;
- meninjau kesatuan paragraf dan hubungan antarkalimat;
- mencocokkan revisi dengan gaya bahasa pengguna;
- mendeteksi frasa generik atau repetitif;
- memeriksa konsistensi sitasi dan integritas akademik;
- meninjau tulisan berdasarkan konteks skripsi.

Asisten tidak menjamin lolos Turnitin, tidak memprediksi skor deteksi AI, dan tidak menjamin tulisan bebas plagiarisme.

## Fitur utama

| Mode | Fungsi |
|---|---|
| `HUMANIZE` | Memperhalus tulisan tanpa mengubah fakta atau makna ilmiah |
| `PROOFREAD` | Memeriksa ejaan, tanda baca, tata bahasa, dan kalimat efektif |
| `ACADEMIC REWRITE` | Menyusun ulang paragraf agar sistematis dan ilmiah |
| `STYLE MATCH` | Menyesuaikan revisi dengan profil gaya bahasa pengguna |
| `AI SLOP CHECK` | Menandai kalimat generik, klise, atau kurang spesifik |
| `PARAGRAPH REVIEW` | Meninjau koherensi, kesatuan gagasan, dan transisi |
| `CITATION CHECK` | Memeriksa konsistensi sitasi dan melacak sumber yang perlu diverifikasi |
| `THESIS REVIEW` | Meninjau tulisan terhadap konteks skripsi |
| `EXPLAIN REVISION` | Menjelaskan alasan perubahan |

## Struktur repository

```text
.github/
  copilot-instructions.md
  skills/<nama-skill>/SKILL.md
skills/<nama-skill>/SKILL.md
config/
prompts/
examples/
tests/
.vscode/settings.json
```

Folder `.github/skills/` memuat format *skill* yang dikenali GitHub Copilot dengan lebih spesifik. Folder `skills/` berisi dokumentasi dan versi sumber yang mudah dibaca dan dipelihara.

## Penggunaan lintas AI agent

Repository ini juga menyediakan instruksi lintas platform:

- `AGENTS.md`: instruksi umum untuk agen yang membaca berkas repository.
- `CLAUDE.md`: instruksi tambahan untuk Claude dan Claude Code.
- `GEMINI.md`: instruksi tambahan untuk Gemini.
- `adapters/chatgpt.md`: instruksi untuk ChatGPT, termasuk custom instructions dan project.
- `adapters/claude.md`: cara menggunakan Claude Projects atau Knowledge.
- `adapters/gemini.md`: cara menggunakan Gemini Gem atau project.
- `adapters/README.md`: ringkasan penggunaan lintas platform.

Karena GitHub Copilot, Claude, Gemini, dan ChatGPT menggunakan mekanisme konteks yang berbeda, skill tidak selalu dapat dipanggil otomatis pada semua platform. Cara paling andal adalah mengunggah atau menempelkan `AGENTS.md` beserta berkas `config/` pada awal percakapan proyek.

Lihat [adapters/README.md](adapters/README.md) untuk petunjuk lengkap.

## Instalasi

1. Pastikan GitHub Copilot dan GitHub Copilot Chat tersedia untuk akun Anda.
2. Buka folder repository ini sebagai workspace VS Code.
3. Tunggu Copilot memuat workspace.
4. Buka **Chat** dan gunakan mode **Ask** atau **Agent**.
5. Sunting file pada folder `config/` sebelum mulai menulis.

Tidak ada proses instalasi paket atau dependensi yang diperlukan.

## Aktivasi dan penggunaan

Berikan mode dan tugas secara eksplisit:

```text
Gunakan mode HUMANIZE.
Periksa teks berikut berdasarkan config/thesis-context.md dan config/writing-style-profile.md.
Pertahankan semua sitasi, angka, satuan, dan istilah teknis.
Hanya lakukan perubahan yang dapat dipertanggungjawabkan.
Jangan mengarang sumber.

[tempel tulisan]
```

Contoh prompt lainnya:

```text
/PROOFREAD paragraf ini dan tampilkan Revised Text saja.
```

```text
Gunakan mode AI SLOP CHECK. Jangan mengubah teks. Kembalikan hasil beserta alasan singkat.
```

```text
Gunakan mode CITATION CHECK dan tandai referensi yang tidak lengkap sebagai [PERLU VERIFIKASI SITASI].
```

```text
Gunakan mode THESIS REVIEW berdasarkan config/thesis-context.md.
Tandai klaim yang membutuhkan dukungan sebagai [PERLU SUMBER ILMIAH].
```

Jika pengguna meminta hasil revisi saja, Copilot akan menampilkan teks revisi terlebih dahulu dan menghindari laporan panjang.

## Mengatur konteks skripsi

Sunting file berikut:

1. `config/thesis-context.md`
2. `config/writing-style-profile.md`
3. `config/academic-terms.md`
4. `config/citation-style.md`

Contoh, data pada `config/thesis-context.md` tidak boleh dianggap sebagai fakta skripsi sampai dikonfirmasi pengguna.

## Menambahkan gaya penulisan pribadi

Tulisan akan dicocokkan dengan gaya pengguna hanya jika tersedia sampel asli.

1. Buka `config/writing-style-profile.md`.
2. Tetapkan status profil menjadi belum dipelajari apabila sampel belum ada.
3. Berikan 3–5 paragraf tulisan asli yang pernah dibuat.
4. Mintalah Copilot menganalisis pola, kosakata, panjang kalimat, formalitas, dan tanda baca.
5. Perbarui profil dan pertahankan pencatatan sumber sampel.

Copilot tidak boleh mengklaim sudah mempelajari gaya pengguna sebelum sampel tersedia.

## Contoh alur

| Sebelum | Sesudah |
|---|---|
| *Dalam era globalisasi yang semakin berkembang, hal ini menjadi sangat penting untuk diperhatikan.* | *Pengembangan material konstruksi perlu mempertimbangkan ketahanan, umur layanan, dan dampaknya terhadap lingkungan.* |

Contoh pada `examples/before-after.md` menunjukkan proses yang mempertahankan makna, sitasi, data, dan istilah.

## Prinsip integritas akademik

- Jangan membuat referensi, nama penulis, tahun, judul, DOI, atau URL fiktif.
- Jangan mengubah sitasi yang sudah ada tanpa alasan.
- Jangan menghapus sitasi hanya karena kalimat diperbaiki.
- Jangan mengubah data, angka, satuan, variabel, persamaan, atau hasil penelitian.
- Jangan membuat klaim baru tanpa dukungan sumber.
- Tandai referensi tidak lengkap dengan `[PERLU VERIFIKASI SITASI]`.
- Tandai klaim yang belum memiliki sumber dengan `[PERLU SUMBER ILMIAH]`.
- Jika informasi tidak dapat diverifikasi, katakan tidak dapat diverifikasi dan jangan mengarang jawaban.

## Batasan

Keterampilan ini membantu analisis dan penyuntingan, tetapi bukan pengganti dosen pembimbing, pustakawan, atau sumber akademik resmi. Hasil tetap memerlukan konfirmasi penulis. GitHub Copilot tidak dapat menjamin akurasi seluruh aturan bahasa, kelengkapan referensi, atau status deteksi suatu sistem antiplagiarisme.

## Lisensi

Repository ini menggunakan lisensi MIT. Lihat `LICENSE`.
