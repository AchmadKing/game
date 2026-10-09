# Pixel Story Adventure — Workspace Pengembangan

Repositori ini adalah lingkungan kerja untuk pengembangan SATU game mobile pixel-art bergenre **Story Adventure** menggunakan **Godot Engine 4** dengan bantuan **Antigravity AI**.

Proyek ini dirancang secara terukur untuk satu pengembang pada perangkat spesifikasi hemat daya (RAM 4 GB, Intel Celeron/Pentium, SSD).

---

## 1. Struktur Workspace

```text
D:\game\
├── .agents\                 # Aturan AI agent
│   └── rules\
│       ├── safety.md        # Aturan keselamatan modifikasi & Git
│       └── workflow.md      # Aturan persetujuan per-fase & pelaporan
├── docs\                    # Dokumentasi desain game (Single Source of Truth)
│   ├── GAME_DESIGN.md       # Konsep, target audiens, core loop
│   ├── STORY_BIBLE.md       # Premis, karakter, latar dunia (khusus game ini)
│   ├── TECHNICAL_DESIGN.md  # Konfigurasi engine & spesifikasi teknis
│   └── ASSET_GUIDE.md       # Standar pixel art, palet, dan audio
├── plans\                   # Manajemen fase dan keputusan
│   ├── ROADMAP.md           # Peta perjalanan 8 fase proyek
│   ├── CURRENT_PHASE.md     # Pelacak fase aktif (Fase 1: Setup)
│   ├── DECISIONS.md         # Catatan keputusan arsitektur (ADR)
│   └── CHANGELOG.md         # Log riwayat perubahan proyek
├── game\                    # Root Proyek Godot Sesungguhnya
│   ├── project.godot        # Konfigurasi Godot 4.7.2
│   ├── scenes\              # File scene (.tscn)
│   ├── scripts\             # Skrip GDScript (.gd)
│   ├── assets\              # Aset gambar, audio, dan font
│   └── data\                # File data/resource (.tres, JSON)
├── .gitignore               # Pengecualian cache .godot/ & build artifacts
├── AGENTS.md                # Instruksi utama AI Agent
└── README.md                # Dokumen panduan ini
```

> **Mengapa Proyek Godot Berada di `game/`?**  
> Godot Engine otomatis memindai seluruh file yang berada di folder yang sama dengan `project.godot`. Memisahkan proyek ke folder `game/` mencegah Godot memindai file dokumentasi markdown, menghindari pembuatan cache `.import` yang tidak perlu, dan menghemat konsumsi memori laptop.

---

## 2. Akses Godot Engine

* **Versi Engine Terverifikasi:** Godot 4.7.2 Stable Win64 (`4.7.2.stable.official.ed1daf0bf`)
* **Lokasi Executable:** `C:\Users\silan\Downloads\Godot_v4.7.2-stable_win64.exe\Godot_v4.7.2-stable_win64.exe`  
  *(Juga dapat diakses melalui shortcut Desktop: `C:\Users\silan\Desktop\Godot.lnk`)*
* **Cara Membuka Proyek:**
  1. Buka Godot Engine.
  2. Pada jendela Project Manager, klik tombol **Import**.
  3. Arahkan dan pilih file `D:\game\game\project.godot`.
  4. Klik **Import & Edit**.

---

## 3. Konfigurasi Git Identity (Langkah Lanjutan)

Sebelum membuat commit pertama di repositori ini, pastikan identitas Git Anda telah disetel. Jalankan perintah berikut di terminal jika belum disetel:

```powershell
git config user.name "Nama Anda"
git config user.email "email@anda.com"
```

Setelah disetel, staging dan commit awal dapat dieksekusi dengan aman.

---

## 4. Alur Kerja AI & Disiplin Fase

Pengembangan dilakukan secara bertahap (*phase-by-phase*) dengan prinsip:
1. **Plan First:** AI selalu membuat rencana implementasi sebelum mengubah file.
2. **Approval Gate:** Perubahan file hanya dilakukan setelah disetujui developer.
3. **Low-Spec Aware:** Tidak menggunakan plugin atau proses background yang memberatkan RAM 4 GB.
4. **Fase Aktif Saat Ini:** **Fase 1 (Initial Workspace Setup)**. Detail pelacakan terdapat pada `plans/CURRENT_PHASE.md`.
