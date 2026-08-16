# NANG GitHub Whitelist — Free

Versi ini memakai GitHub Actions sehingga **tidak perlu menyimpan Personal Access Token di HTML**.

## Setup

1. Buat repository GitHub.
2. Upload:
   - `whitelist.json`
   - `.github/workflows/nang-whitelist.yml`
3. Pastikan Actions aktif.
4. Buka tab **Actions → NANG Whitelist Update → Run workflow**.
5. Pilih `add` atau `remove`.
6. Isi Roblox UserId.
7. Jalankan workflow.

Workflow memakai `GITHUB_TOKEN` bawaan GitHub Actions. Token ini dibuat otomatis oleh GitHub untuk setiap workflow run dan tidak perlu kamu tulis ke source.

## Penting

GitHub Pages/HTML statis **tidak bisa secara aman mengubah repository secara langsung tanpa kredensial**. Karena itu versi gratis ini menggunakan halaman Actions GitHub sebagai admin. Jangan membuat PAT lalu menaruhnya di HTML publik.

## Lua

Script Nang membaca:

`https://raw.githubusercontent.com/USERNAME/REPOSITORY/main/whitelist.json`

Ganti URL tersebut di script Lua dengan repository kamu, lalu obfuscate script setelah URL final dipasang.

## Catatan

`GITHUB_TOKEN` hanya tersedia di dalam workflow dan permission `contents: write` dibatasi pada workflow. Jangan memberikan token ini ke client.
