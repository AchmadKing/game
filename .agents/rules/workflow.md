# Workflow Rules — AI Agent Process & Lifecycle

Dokumen ini mendefinisikan alur kerja baku pengembangan berbantuan AI.

## 1. Plan-First & Approval Gates
* Setiap tugas non-trivial wajib diawali dengan pembuatan rencana implementasi (*Implementation Plan*).
* Rencana harus memuat: daftar file target, alasan perubahan, potensi risiko, dan *acceptance criteria*.
* Pekerjaan tidak boleh dieksekusi sebelum menerima persetujuan eksplisit dari developer.
* Persetujuan hanya sah untuk batasan cakupan (*scope*) yang tertera dalam rencana.

## 2. Disiplin Fase Aktif
* AI hanya boleh mengerjakan tugas yang tercantum pada fase aktif di `plans/CURRENT_PHASE.md`.
* Dilarang mencuri start mengerjakan fitur, aset, atau skrip yang diperuntukkan bagi fase mendatang.
* Keputusan desain, cerita, atau mekanik yang belum disepakati wajib ditandai `TBD` (*To Be Determined*).

## 3. Disiplin Perangkat Spesifikasi Rendah (Low-Spec)
* Seluruh solusi teknis harus mempertimbangkan keterbatasan RAM 4 GB dan prosesor hemat daya:
  * Hindari eksekusi proses background yang berat atau berjalan bersamaan.
  * Hindari penambahan addon, framework, atau dependensi berat tanpa kebutuhan mendesak.
  * Pisahkan folder dokumen dari proyek Godot untuk meminimalkan beban I/O engine.

## 4. Standar Pelaporan Verifikasi
* Setiap penyelesaian tugas wajib disertai laporan verifikasi dengan salah satu dari 4 status tegas:
  * **Succeeded**: Pengujian telah dijalankan dan terbukti berhasil sesuai ekspektasi.
  * **Failed**: Pengujian menghasilkan pesan kesalahan atau tidak memenuhi kriteria.
  * **Skipped**: Pengujian sengaja dilewati dengan alasan teknis yang didokumentasikan.
  * **Not Performed**: Pengujian belum dijalankan (misal: membutuhkan interaksi manual user).
* Dilarang menyatakan pengujian berhasil tanpa menyertakan bukti output perintah.
