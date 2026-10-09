# Technical Design Document

Dokumen ini mencatat spesifikasi teknis, konfigurasi engine Godot, arsitektur data, dan strategi optimasi untuk perangkat mobile dan laptop pengembang.

---

## 1. Spesifikasi Engine & Lingkungan
* **Engine:** Godot Engine 4 (Versi Terverifikasi: 4.7.2 Stable Win64)
* **Bahasa Pemrograman:** GDScript
* **Kandidat Awal Renderer:** `gl_compatibility` (OpenGL 3)
  > [!NOTE]
  > Pemilihan `gl_compatibility` adalah **konfigurasi awal** untuk memastikan efisiensi memori (RAM 4 GB) dan kompatibilitas luas pada perangkat mobile. Evaluasi performa lanjutan (termasuk pengujian Mobile/Vulkan jika diperlukan) dapat dilakukan pada Fase Prototype Teknis.
* **Target OS Game:** Android

---

## 2. Parameter Display & Viewport
* **Orientasi Layar Target:** TBD (Portrait / Landscape)
* **Resolusi Viewport Dasar (Base Resolution):** TBD (misal: 320x180, 480x270, atau 640x360)
* **Stretch Mode:** `viewport` (skala piksel presisi)
* **Stretch Aspect:** `keep`
* **Default Texture Filtering:** `nearest` (menjaga pixel art tetap tajam)

---

## 3. Arsitektur Proyek
* **Pemisahan Root Proyek:** Proyek engine ditempatkan khusus di dalam direktori `game/` agar Godot tidak memindai dokumen markdown dan file perencana.
* **Struktur Kode & Scene:**
  * Scene game ditempatkan di `game/scenes/`
  * Skrip GDScript ditempatkan di `game/scripts/`
  * Data dan konfigurasi ditempatkan di `game/data/`
  * Aset visual dan audio ditempatkan di `game/assets/`
* **Manajemen State / Save-Load:** TBD (Akan ditentukan pada fase implementasi gameplay)
