# Jelajah Antariksa

Game pesawat luar angkasa 3D yang berjalan langsung di browser. Satu file HTML, tanpa proses build, tanpa server, tanpa akun.

**Dibuat oleh engine Claude Opus 5.5.**

## Tentang game

Kamu mengemudikan pesawat di Sistem Bintang Surya: lewat orbit Merapi, mendekati Kirana dan bulannya, menyusuri Sabuk Kerikil, lalu menembus raksasa gas Bayu menuju Saraswati yang bercincin. Tidak ada timer dan tidak ada musuh yang mengejar. Tujuan permainannya sederhana — terbang sejauh yang kamu mau dan lengkapi jurnal penemuan.

Progres tersimpan otomatis di browser lewat `localStorage`. Tutup tab, buka lagi, lalu lanjutkan dari posisi terakhir.

## Isi

- **Tiga pesawat** dengan karakter berbeda: Rajawali (pencegat lincah), Kelana (penjelajah jarak jauh), dan Pari (sayap manta tercepat).
- **13 objek untuk ditemukan**: Surya, 9 planet dan bulan, serta Sabuk Kerikil. Mendekati objek akan memindainya dan mencatatnya di jurnal.
- **Sistem penerbangan**: dorong maju/mundur, kemudi, guling, naik/turun, boost, dan rem penuh. Ada pembatas kecepatan saat dekat permukaan planet.
- **HUD lengkap**: kompas, radar, penunjuk target, jarak dan waktu tiba, kecepatan, dorongan, koordinat, serta penanda objek di layar.
- **Dua mode kamera**: kokpit atau belakang, plus pandangan bebas dengan mouse.
- **Kontrol keyboard, mouse, dan layar sentuh** — joystick dan tuas dorongan muncul di perangkat sentuh.
- **Suara dan grafis yang bisa diatur**: suara mesin/ambien, opasitas HUD, sensitivitas mouse, inversi sumbu vertikal, dan kualitas grafis.
- **Jurnal penjelajahan** yang mencatat objek sudah ditemukan dan masih belum.

## Cara menjalankan

Buka `index.html` di browser modern (Chrome, Edge, Firefox, atau Safari).

Kalau browser membatasi modul saat dibuka lewat `file://`, jalankan server statis lokal:

```bash
python3 -m http.server 8000
```

Lalu buka `http://localhost:8000`.

Three.js dimuat dari jsDelivr dan font dari Google Fonts, jadi koneksi internet diperlukan saat halaman pertama dibuka. Tidak ada dependensi yang perlu dipasang.

## Kontrol

| Aksi | Keyboard & mouse | Layar sentuh |
|---|---|---|
| Dorong maju / mundur | `W` `S` atau roda mouse | Tuas DORONG |
| Kemudi | Mouse atau `↑` `↓` `A` `D` | Geser sisi kiri layar |
| Guling | `Q` `E` | `⟲` `⟳` |
| Naik / turun | `Space` `C` | `▲` `▼` |
| Boost | `Shift` | Tombol BOOST |
| Rem penuh | `X` | — |
| Ganti target | `T` | `⌖` |
| Arahkan ke target | Tahan `G` | Tahan `◎` |
| Kamera kokpit/belakang | `V` | Tombol kamera di HUD |
| Pandangan bebas | Tahan klik kanan atau `L` | Geser area kosong |
| Garis orbit / HUD | `O` `H` | — |
| Jurnal / jeda | `J` `Esc` | Menu jeda |

Klik layar saat bermain untuk mengunci mouse. Kursor putih menunjukkan arah belok; makin jauh dari tengah, makin cepat pesawat berbelok.

## Teknologi

Seluruh game ada dalam satu `index.html`: HTML, CSS, dan JavaScript. Render 3D memakai [Three.js](https://threejs.org/) 0.186.0 lewat import map. Tekstur planet, model pesawat, dan efek dibuat prosedural di canvas — tidak ada aset gambar atau audio eksternal. Suara dibangkitkan dengan Web Audio API. Tipografi memakai Chakra Petch dan JetBrains Mono.

## Kredit

Game dan kode sumbernya dibuat oleh **Claude Opus 5.5**. Three.js dan font digunakan sesuai lisensi masing-masing.
