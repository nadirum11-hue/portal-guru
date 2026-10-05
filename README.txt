PORTAL GURU PWA V2 — BACK & EXIT GUARD

ARSITEKTUR
GitHub Pages PWA Shell -> iframe -> Google Apps Script Web App -> Google Spreadsheet

1) GITHUB PAGES
Upload ke ROOT repository GitHub:
- index.html
- manifest.webmanifest
- service-worker.js
- icon-192.png
- icon-512.png

Lalu Settings -> Pages -> Deploy from a branch -> main -> /(root).

2) APPS SCRIPT
File Portal-Guru-Back-Guard.html adalah versi HTML Portal Guru yang sudah ditambahkan:
- riwayat menu untuk tombol/gesture Back
- Back kembali ke menu sebelumnya
- Back saat sudah di Dashboard meminta konfirmasi keluar
- menerima perintah Back dari shell GitHub PWA

Jika project Apps Script Anda memakai file HTML bernama Index.html, buka file HTML tersebut di Apps Script dan ganti ISINYA dengan isi Portal-Guru-Back-Guard.html. Jangan mengganti file Code.gs/backend.

Setelah itu Deploy -> Manage deployments -> Edit -> New version -> Deploy.

PENTING
- Jangan memasukkan index.html GitHub ke project Apps Script.
- Shell GitHub dan HTML Apps Script adalah dua file berbeda.
- Google Spreadsheet/backend tetap digunakan seperti sebelumnya.
- Browser/PWA tidak memberi JavaScript hak untuk memaksa menutup aplikasi seperti aplikasi Android native. Konfirmasi di sini mengamankan aksi Back/keluar yang bisa dikendalikan browser.
- Install PWA setelah versi baru aktif. Jika versi lama masih muncul, buka GitHub Pages sekali di browser biasa, refresh, lalu buka kembali PWA.
