# Panduan Penggunaan dengan Berbagai AI Agent

Repository dapat digunakan lintas platform melalui instruksi sistem, instruksi proyek, konteks workspace, atau file instruksi yang otomatis dibaca.

| Agent/platform | Cara penggunaan | Pengaturan repositori |
|---|---|---|
| GitHub Copilot | Membaca instruksi workspace | `.github/copilot-instructions.md`, `.github/skills/` |
| Claude | Projek/Knowledge atau instruksi proyek | Lampirkan berkas relevan dan gunakan `CLAUDE.md` |
| Gemini | Gem, proyek, atau instruksi khusus | Lampirkan berkas relevan dan gunakan `GEMINI.md` |
| ChatGPT | Project instructions atau custom instructions | Lampirkan atau tempelkan isi `AGENTS.md` dan berkas `config/` |
| Claude Code/Codex/agent coding | Instruksi repository | `AGENTS.md` |
| Cursor atau IDE lain | Rule/Instruction/Context | Lampirkan `AGENTS.md` atau isi `.github/copilot-instructions.md` |

Nama atau lokasi fitur dapat berubah mengikuti versi platform. Gunakan mekanisme instruksi yang tersedia pada platform yang digunakan.

## Cara universal

1. Buat percakapan baru yang khusus untuk skripsi.
2. Unggah atau tempel isi `AGENTS.md`.
3. Unggah atau tempel isi empat berkas dalam `config/`.
4. Pilih satu mode dari README atau folder `prompts/`.
5. Lampirkan teks yang akan direvisi.
6. Jelaskan bagian yang boleh dan tidak boleh diubah.

Contoh prompt awal:

```text
Gunakan instruksi berikut sebagai aturan utama:
[tempel atau unggah AGENTS.md]

Gunakan konteks berikut:
[lampirkan config/thesis-context.md]
[lampirkan config/writing-style-profile.md]
[lampirkan config/academic-terms.md]
[lampirkan config/citation-style.md]

Gunakan mode HUMANIZE.
Pertahankan semua sitasi, angka, satuan, variabel, dan istilah teknis.
Jangan mengarang sumber.
Berikan Revised Text terlebih dahulu.
```
