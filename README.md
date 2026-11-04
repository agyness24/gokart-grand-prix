# Gokart Grand Prix

Game balap gokart 3D: championship dengan save slot, quick race, time attack, 2 pemain split screen, online, tutorial buat pemain baru, 10 sirkuit dunia, siang, malam dan hujan.

## Download

Semua versi ada di halaman **Releases** repo ini (kolom kanan, "Releases"), dibuat otomatis tiap ada perubahan.

| Perangkat | Cara pasang |
| --- | --- |
| Windows | `Gokart-Grand-Prix-Setup.exe` buat install plus shortcut di desktop, atau `Gokart-Grand-Prix-Portable.exe` yang tinggal klik dua kali tanpa install. Kalau muncul "Windows protected your PC", klik **More info** lalu **Run anyway** (aplikasinya belum ditandatangani resmi). |
| Mac | Buka `Gokart-Grand-Prix-Mac.dmg`, seret ke Applications. Pertama kali buka: klik kanan, pilih **Open**. |
| Android | Buka `Gokart-Grand-Prix-Android.apk` di HP, izinkan "install dari sumber ini". |
| iPhone / iPad | Buka link web-app di Safari (lihat di bawah), tekan tombol **Share**, pilih **Add to Home Screen**. |
| Linux | `Gokart-Grand-Prix-Linux.AppImage`, jadikan executable lalu jalankan. |

Link web-app: `https://agyness24.github.io/gokart-grand-prix/`
Kalau link itu belum jalan setelah build pertama: buka **Settings > Pages** di repo ini, pilih Source **Deploy from a branch**, branch **gh-pages**, lalu Save.

## Main online

Online di aplikasi nggak butuh server dan nggak butuh akun:

1. Host pilih mode **Online**, klik **Host a game**, lalu kirim **invite code** ke teman (WhatsApp, Discord, apa aja).
2. Teman paste kode itu, klik **Join**, lalu kirim balik **reply code**.
3. Host paste reply code, klik **Connect**. Ulangi buat tiap teman (maksimal 8 pemain).
4. Host klik **Start online race**.

Semua versi bisa main bareng: Windows, Mac, Android, iPhone dan browser. Sebagian jaringan kantor atau sekolah memblokir koneksi langsung, coba pakai jaringan lain atau hotspot HP.

## Kontrol

- Keyboard: `W` `A` `S` `D` atau panah, `Space` drift, `C` kamera, `R` balik ke lintasan, `Esc` pause, `F11` layar penuh (desktop)
- Controller (PlayStation, Xbox): `R2` atau `X` gas, `L2` atau kotak rem, stik kiri setir, bulat drift, segitiga kamera, `Options` pause
- HP: tombol sentuh di layar, mainkan dalam posisi landscape

Bantuan nyetir (steering assist, braking assist) dan grafik (Low buat HP) ada di **Settings**, juga dari menu pause.

## Struktur project

- `web/index.html`: seluruh game (satu file), plus `manifest.webmanifest` dan `sw.js` buat web-app offline
- `electron/main.js`: pembungkus aplikasi desktop
- `capacitor.config.json` dan `build/android-icons/`: aplikasi Android
- `.github/workflows/build.yml`: build otomatis semua versi dan rilisnya
