# Sistem Admin Gym - Final Siap Upload

Paket ini dibuat supaya repo GitHub kamu tidak bingung lagi antara root dan folder `frontend`.

## Struktur final repo

Upload semua file/folder ini langsung ke root repo:

```text
index.html
404.html
README.md
backend-google-apps-script/
  Code.gs
  appsscript.json
```

Setelah upload, link web kamu adalah:

```text
https://hantugur.github.io/NAMA-REPO/
```

Contoh:

```text
https://hantugur.github.io/SISTEM-FC/
```

Jangan buka `/frontend/` karena paket ini sudah tidak pakai folder frontend.

## Setup backend Google Apps Script

1. Buka Google Sheet kamu.
2. Klik `Ekstensi -> Apps Script`.
3. Buka file `Code.gs`.
4. Hapus semua isi lama.
5. Copy semua isi dari `backend-google-apps-script/Code.gs`.
6. Paste ke `Code.gs` di Apps Script.
7. Klik Save.
8. Pilih function `setupGymSheets`.
9. Klik Run, lalu izinkan akses.
10. Klik `Deploy -> New deployment` atau `Deploy -> Manage deployments`.
11. Type: `Web app`.
12. Execute as: `Me`.
13. Who has access: `Anyone`.
14. Deploy.
15. Copy Web App URL yang berakhir `/exec`.

## Pasang URL backend ke web

1. Buka `index.html`.
2. Cari bagian ini:

```javascript
SCRIPT_URL: "PASTE_APPS_SCRIPT_WEB_APP_URL_HERE",
```

3. Ganti dengan URL Apps Script kamu:

```javascript
SCRIPT_URL: "https://script.google.com/macros/s/AKfycbxxxxxxx/exec",
```

4. Commit ke GitHub.
5. Tunggu 1-2 menit.
6. Buka link GitHub Pages root repo.

## Sheet yang dipakai

Jangan ubah nama tab ini:

```text
LOG_GYM
DATA_KUNCI
MEMBER_LIFETIME
```

## Kolom audit

Tab `LOG_GYM` akan otomatis berisi:

```text
ID | Timestamp | Tanggal | Jam | Nama Pelanggan | No Kunci | Status | Admin
```

## Untuk teman kerja

Teman kerja cukup buka link web GitHub Pages. Mereka tidak perlu deploy Apps Script dan tidak perlu akses edit Google Sheet.
