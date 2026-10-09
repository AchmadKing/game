# AGENTS.md — Global AI Assistant Guidelines

Selamat datang di repositori pengembangan game mobile pixel-art (Story Adventure). Dokumen ini adalah instruksi operasional utama bagi AI Agent dalam berpasangan (*pair programming*) dengan developer.

## 1. Identitas & Batasan Proyek
* **Fokus Eksklusif:** Proyek ini didedikasikan untuk SATU game mobile pixel art bergenre Story Adventure.
* **Larangan Lingkup Luas:** Dilarang merencanakan semesta multi-game, waralaba, prekuel, sekuel, atau arsitektur generik untuk banyak game.
* **Keterbatasan Perangkat:** Developer menggunakan laptop berspesifikasi hemat daya (RAM 4 GB, Intel Celeron/Pentium, SSD). Selalu utamakan solusi yang ringan, hemat memori, dan minim dependensi.

## 2. Prinsip Kerja Wajib
1. **Plan First:** Buat rencana implementasi terperinci sebelum menyentuh file.
2. **Explicit Approval:** Tunggu persetujuan developer sebelum mengeksekusi rencana.
3. **Safe Changes:** Periksa file sebelum mengedit (*inspect before modify*). Jangan menimpa atau menghapus file tanpa konfirmasi. Dilarang melakukan aksi Git destruktif.
4. **Phase Discipline:** Kerjakan hanya tugas pada fase aktif di `plans/CURRENT_PHASE.md`. Jangan melompat ke fase berikutnya.
5. **Single Source of Truth:** Jangan menduplikasi dokumentasi. Setiap informasi hanya dicatat di dokumen pemiliknya.
6. **No Speculation:** Jika detail game design atau cerita belum diputuskan oleh developer, catat sebagai `TBD`. Jangan mengarang keputusan desain atas inisiatif sendiri.
7. **Rigorous Verification:** Gunakan 4 status resmi saat melapor: `Succeeded`, `Failed`, `Skipped`, atau `Not Performed`. Jangan membuat klaim keberhasilan tanpa bukti nyata.

## 3. Rujukan Aturan Rinci
* Aturan keselamatan teknis: `.agents/rules/safety.md`
* Aturan alur kerja dan pelaporan: `.agents/rules/workflow.md`
