# Roadmap Pengembangan Proyek

Dokumen ini memuat garis besar 8 fase pengembangan dari penyiapan awal hingga rilis game mobile pixel art ini.

---

## Ringkasan 8 Fase

### Fase 1: Initial Workspace Setup (Fase Aktif)
* **Tujuan:** Menyiapkan struktur workspace yang bersih, aturan AI agent, template dokumentasi, konfigurasi Godot minimal, dan baseline Git.
* **Deliverable:** Repositori terinisialisasi, `game/project.godot` terverifikasi parsing oleh engine, dokumen panduan siap pakai.

### Fase 2: Game Preproduction
* **Tujuan:** Menentukan konsep inti game, premis cerita, target audiens, dan pilar desain gameplay.
* **Deliverable:** `GAME_DESIGN.md` dan `STORY_BIBLE.md` terisi dengan keputusan yang disetujui developer.

### Fase 3: Storyboard & Detailed Game Design
* **Tujuan:** Merancang alur adegan cerita, antarmuka pengguna (UI/HUD), dan spesifikasi mekanik interaksi secara mendalam.
* **Deliverable:** Dokumen storyboard adegan dan alur layar permainan.

### Fase 4: Asset Creation Guidelines & Initial Assets
* **Tujuan:** Menentukan palet warna definitif, resolusi piksel dasar (grid), dan aset dasar (karakter utama, tile lingkungan dasar, font).
* **Deliverable:** `ASSET_GUIDE.md` terisi penuh dan aset esensial pertama diimpor ke `game/assets/`.

### Fase 5: Technical Prototype
* **Tujuan:** Memvalidasi mekanik gerak dasar, performa input sentuh mobile, dan kestabilan rendering engine pada perangkat target.
* **Deliverable:** Prototipe playable minimal berisi pergerakan karakter dan interaksi dasar.

### Fase 6: Gameplay & Narrative Implementation
* **Tujuan:** Mengintegrasikan seluruh adegan cerita, sistem dialog, teka-teki/eksplorasi, dan audio ke dalam alur game utuh.
* **Deliverable:** Game lengkap yang dapat dimainkan dari awal hingga akhir (*vertical slice* ke versi utuh).

### Fase 7: Testing, Optimization & Polish
* **Tujuan:** Pengujian stabilitas performa (RAM/FPS), perbaikan bug, penyempurnaan animasi, dan pengujian responsivitas kontrol.
* **Deliverable:** Game stabil tanpa *crash* dan memenuhi standar pengalaman bermain yang mulus.

### Fase 8: Mobile Build & Release Preparation
* **Tujuan:** Konfigurasi export Android (keystore, manifest, icons, splash screen) dan pembuatan build rilis (`.apk` / `.aab`).
* **Deliverable:** File instalasi final siap uji coba perangkat dan siap rilis.
