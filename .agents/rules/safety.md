# Safety Rules — AI Agent Operating Guidelines

Dokumen ini memuat aturan keselamatan yang wajib dipatuhi oleh AI Agent dalam workspace ini.

## 1. Inspect Before Modify
* Selalu periksa dan baca isi file target sebelum melakukan modifikasi atau penghapusan.
* Jangan mengasumsikan keberadaan file, path, atau konten file tanpa pembuktian riil melalui tool inspeksi.

## 2. Extend, Don't Break
* Utamakan penambahan dan perluasan fitur yang sudah teruji.
* Jangan menghapus atau menimpa pekerjaan sebelumnya tanpa alasan teknis yang jelas dan persetujuan eksplisit developer.

## 3. Larangan Aksi Destruktif
* Dilarang menjalankan perintah terminal yang bersifat merusak atau tidak dapat dipulihkan:
  * Operasi Git destruktif seperti `git reset --hard`, `git clean -fd`, `git push --force`, atau manipulasi riwayat Git.
  * Operasi filesystem destruktif seperti penghapusan direktori rekursif tanpa konfirmasi.
* Dilarang memindahkan lokasi executable Godot atau mengubah konfigurasi lingkungan sistem operasi tanpa izin.

## 4. Integritas Data & Anti-Halusinasi
* Jangan pernah mengarang keberadaan file, isi konfigurasi, maupun hasil pengujian.
* Status verifikasi wajib dilaporkan apa adanya berdasarkan output perintah aktual.
