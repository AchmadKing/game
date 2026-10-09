# Architecture Decision Records (ADR)

Dokumen ini mencatat keputusan arsitektur dan teknis penting yang telah disetujui.

---

## ADR-001: Pemisahan Folder Proyek dan Kandidat Awal Renderer GL Compatibility

* **Status:** Disetujui (Approved)
* **Tanggal:** 2026-10-09
* **Konteks:**
  * Pengembang menggunakan perangkat hemat daya (RAM 4 GB, prosesor Intel Celeron/Pentium, Intel UHD Graphics 600).
  * Target game adalah game mobile 2D pixel art (Story Adventure) menggunakan Godot 4.7.2.
  * Diperlukan struktur workspace yang rapi dan meminimalkan beban I/O serta konsumsi memori.

* **Keputusan:**
  1. **Pemisahan Direktori:** Proyek Godot ditempatkan di subfolder `game/` terpisah dari folder `.agents/`, `docs/`, dan `plans/`. Hal ini mencegah Godot Editor memindai file dokumentasi markdown dan membuat cache `.import` yang tidak perlu.
  2. **Kandidat Awal Renderer:** Konfigurasi `project.godot` awal disetel menggunakan `gl_compatibility` (OpenGL 3) dengan texture filtering `nearest`. Keputusan ini adalah **kandidat awal**, bukan keputusan permanen, dan dapat dievaluasi kembali saat Fase 5 (Technical Prototype).
  3. **Keamanan Git Commit:** Initial commit ditunda sampai developer mengonfirmasi identitas Git (`user.name` & `user.email`) untuk mencegah commit dengan fallback sistem lokal yang tidak diinginkan.

* **Konsekuensi:**
  * **Positif:** Waktu loading Godot cepat, penggunaan RAM rendah, repositori Git bersih dan terstruktur.
  * **Tindak Lanjut:** Melakukan pengujian rendering visual dan komparasi performa pada fase prototype teknis.
