# FIRE-MAR

**Penyaringan evakuasi kapal dan akses SAR untuk kapal Ro-Pax domestik.**
Website ini menerapkan paper *FIRE-MAR: A Route-Specific Framework for Prioritizing Evacuation Redesign and Rescue Preparedness on Indonesian Domestic Ro-Pax Ferries* (Tim Doa Ibu, Teknik Perkapalan ITS, SMC 2026).

> FIRE-MAR adalah alat penyaringan, bukan alat persetujuan. Hasilnya perlu diperiksa oleh orang yang kompeten, dicocokkan dengan ukuran di kapal, dan dikonfirmasi oleh Badan Klasifikasi atau Direktorat Jenderal Perhubungan Laut sebelum dipakai untuk keputusan.

## Yang dihitung

| Bagian | Isi | Sumber |
|---|---|---|
| Evakuasi kapal | 1,25 (R + T) + ⅔ (E + L) ≤ 60 menit; skenario A (arahan kru), B (tangga terdekat), sekunder (setiap tangga diuji hilang) | IMO MSC.1/Circ.1533, metode sederhana |
| Akses SAR rute | notifikasi + persiapan + 60 × jarak ÷ kecepatan ≤ 175 menit | Peraturan Basarnas No. 6/2022 (25 + 150 menit) + waktu notifikasi |
| Pemeriksaan aturan | 16 pemeriksaan: kinerja dan kemacetan Circ.1533, dua jalan keluar, lebar tangga/pintu/lorong, pegangan, arah, tinggi dan sudut, bordes, pintu keluar, tangga tertutup, ruang di bawah geladak sekat, penanda rendah, pintu tanpa kunci, pembuka cepat, muster station | SOLAS II-2/13.3.2, FSS Code bab 13 (MSC.410(97)), SOLAS III/11.2 |
| Uji skenario | lokasi api (tangga/pintu tertandai hilang), tambahan orang, laporan terlambat, unit SAR melambat | metode yang sama, kasus sekunder γ = 1,3 |
| Tangga tindakan | langkah termurah yang cukup per sumbu: 1 operasional (kapasitas, pelaporan), 2 prosedur dan safety plan (arahan kru), 3 desain atau infrastruktur SAR, 4 kajian desain baru; setiap langkah dihitung ulang | paper Bab 4.3 dan Kesimpulan 3 |
| Peta rute | pelabuhan dan titik belok di peta perairan Indonesia, panjang rute (lingkaran besar), waktu tempuh, pos SAR terdekat, titik rute terjauh d, peringatan rute melewati daratan | Natural Earth 1:10 juta; Kantor dan Pos SAR menurut Peraturan Basarnas No. 4/2025 |
| Ukur dari DXF | jarak, panjang garis dan luas pada gambar GA/safety plan (DXF ASCII), dengan tangkap titik ujung dan kalibrasi; hasil dapat diisikan ke kolom | pembaca DXF milik FIRE-MAR, berjalan di browser |

## Yang baru di versi 2.3

- **Panduan membaca GA**: GA Vessel A digambar ulang (tampak atas geladak penumpang, tampak atas geladak titik kumpul, tampak samping) dengan tanda bernomor untuk setiap isian: ruang dan jumlah orang, lebar bersih tangga, panjang jalur, pintu dan lorong, arah tangga, tinggi antargeladak, sudut, jarak ke muster station, luas muster, LOA, rakit. Tombol bernomor di samping kolom menunjukkan tandanya di gambar. Daftar data minimum di langkah 1.
- **Jalur evakuasi di layar**: ruang → tangga → muster station dengan jumlah orang per jalur, tanpa dan dengan arahan kru; tangga titik macet ditandai.
- **Riwayat kapal (diisi manual)**: IMO, bendera, klas, riwayat nama/bendera/pemilik, riwayat rute, inspeksi dan detensi PSC, sumber dan tanggal cek, dengan tautan ke Equasis, Tokyo MoU (APCIS) dan VesselFinder. Tidak ada pengambilan data otomatis. Tidak mengubah kedua jam; ikut di ringkasan, PDF dan Excel.
- **Daftar periksa sebelum berlayar** (sisi pencegahan): 12 butir dengan dasar aturan (MARPOL Annex I, SOLAS II-2, III, IV, rekomendasi KNKT), tanpa skor peluang kebakaran; kartu cetak ke-4.
- **Ukur dari gambar**: selain DXF kini PDF dan foto (PNG/JPG). PDF memakai skala gambar (misalnya 1:200) atau kalibrasi; foto wajib kalibrasi. Alat baru *Isi ruang*: luas ruang dengan sekali klik, dengan penutup celah pintu. Panduan langkah di dalam alat. Perbaikan geser dan sentuh yang tersangkut.
- **Rute menghindari pulau**: bila garis lurus antarpelabuhan memotong daratan, rute dibelokkan otomatis; tombol *Hindari pulau*; titik belok tetap bisa digeser, ditambah atau dihapus. Bukan rute navigasi.
- **Tur demo 3 menit** dari Beranda atau menu.
- Teks: "aturan klas yang berlaku" (bukan hanya BKI), 13 batasan yang diselaraskan dengan paper, keterangan bahwa Alt-1/Alt-2 dirancang perancang dan diuji FIRE-MAR.

## Yang baru di versi 2.2

- **Beranda produk**: dua jam (kapal 60 menit, SAR 175 menit) untuk satu kapal di satu rute, contoh siap dibuka, dan penjelasan bahwa FIRE-MAR menekan *akibat* (waktu orang terpapar), bukan *peluang* kebakaran. Tautan langsung: `#mulai`.
- **Dua tampilan tanpa kehilangan data**: *Simple* (bawaan) dengan isi data enam langkah berbahasa sehari-hari, dan *Advanced* dengan semua tabel, skenario dan pemeriksaan versi 2.1.
- **Ringkasan hasil penyaringan**: satu kalimat dengan kondisinya (jumlah orang, malam, skenario), kategori, tiga langkah teratas dengan pelaksana, waktu, efek hitung dan label biaya, serta tombol *Salin ringkasan*.
- **Rencana tindakan** dengan kolom penyebab, efek hitung dan dasar (pasal atau metode) untuk setiap langkah.
- **Sebelum dan sesudah**: nyalakan langkah (laporan lebih cepat, arahan kru, batas sertifikat, alternatif desain) dan lihat kedua jam serta kategori dihitung ulang. Efek adalah hasil hitung, belum diuji di kapal.
- **Uji hari buruk**: tangga yang paling banyak dipakai tertutup api, orang 50 % lebih banyak, laporan terlambat 10 menit.
- **Jenis kejadian**: kebakaran, tabrakan, air masuk, kandas (jam kapal dengan syarat kapal tetap tegak), miring berat atau terbalik (jam kapal tidak dihitung). Pilihan lokasi api diurutkan menurut frekuensi nasional dan bukan prediksi.
- **Kasus ilustrasi “Perlu perubahan GA”**: contoh yang menunjukkan kapan arahan kru tidak cukup dan jalan keluar kedua (Alt-1) diperlukan. Ditandai sebagai ilustrasi, bukan data paper.
- **Cara menghitung**: rumus dengan arti di sampingnya, kamus simbol, contoh hitung 11 langkah dari data yang sedang dibuka, dan arti simbol saat disentuh atau diarahkan kursor.
- **Validasi dan batasan**: tiga tingkat validitas (hitungan terverifikasi, metode diakui, belum divalidasi di lapangan), tabel angka paper dan hasil website, dan sepuluh batasan yang diakui.
- **Keluaran**: halaman 1 PDF berisi ringkasan 30 detik, tabel rencana tindakan di PDF, dan tiga kartu A4 siap cetak bertanda *DRAF untuk ditinjau operator* (arahan kru, lapor kebakaran dengan batas waktu, batas muatan).
- Kata-kata diselaraskan agar tidak berlebihan: *Memenuhi acuan*, *Dalam batas*, *uji kelebihan muatan, bukan izin muatan*.

Tidak termasuk, dengan sengaja: estimasi biaya rupiah, klaim jumlah nyawa yang diselamatkan, perbandingan banyak kapal, pemodelan asap, aturan klas BKI dan NCVS, DWG, dan data SAR waktu nyata.

## Yang baru di versi 2.1

- Empat kasus contoh dari paper (Robust, Rescue-dependent, Vessel-critical, Compound-critical), dipilih di layar pembuka atau menu.
- Tangga tindakan di Ringkasan: desain (GA) disarankan hanya bila langkah di bawahnya tidak cukup; temuan aturan dan kekurangan luas muster dilaporkan terpisah.
- Peta rute perairan Indonesia (bekerja tanpa internet) dan tombol *Pakai hasil peta*.
- Ukur dari gambar DXF, lengkap dengan contoh gambar sintetis untuk dicoba.
- PDF bertanda air FIRE-MAR kecil di setiap halaman dan pernyataan bahwa PDF bukan persetujuan atau patokan penyelesaian.
- Excel dirapikan: judul kolom dengan satuan, format angka, daftar pilihan, lembar Ringkasan dan Rute_Peta; file versi 2.0 tetap dapat diimpor.
- Perbaikan antarmuka dari audit: tiga hasil dipisah (kategori waktu, pemeriksaan aturan, kelengkapan laporan), skala grafik SAR bersama, hasil uji skenario di samping kontrol dengan kotak angka, tombol Pakai di perbandingan, kolom nama lebih lebar.

Status setiap pemeriksaan: Memenuhi acuan, Tidak memenuhi acuan, Perlu konfirmasi, Perlu data, Tidak berlaku. Data yang belum ada tidak ditebak. Aturan klas BKI dan standar NCVS (KM 65/2009) tidak diperiksa; daftar lengkap hal yang tidak diperiksa ada di halaman Pemeriksaan aturan dan di laporan PDF.

## Cara memakai

**Simple** (bawaan): *Beranda* → *Isi data* (kapal, ruang, tangga, jalur, rute dan SAR, periksa) → *Hasil* (ringkasan, sebelum dan sesudah, rencana tindakan, uji hari buruk, kartu cetak) → *Laporan*.

**Advanced**:

1. **Data kapal**: zona, tangga, pintu dan lorong, jalur zona ke tangga.
2. **Rute dan SAR**: jarak terjauh dari pos SAR dan tiga skenario waktu.
3. **Ringkasan**, **Rencana tindakan**, **Evakuasi kapal**, **Akses SAR**: kategori, angka utama, langkah, jejak hitung.
4. **Pemeriksaan aturan**: lengkapi ukuran tambahan dan pernyataan penilai.
5. **Laporan**: identitas, alasan dan catatan, lalu PDF. Status *Siap diperiksa* hanya keluar bila enam syarat kelengkapan terpenuhi; selain itu bertanda *Draf*.

Pindah tampilan lewat tombol *Simple / Advanced* di kanan atas, menu, atau Beranda; data tidak berubah.

Semua hitungan berjalan di perangkat pengguna; data kapal tidak dikirim ke server mana pun.

## Pengujian

| Uji | Perintah |
|---|---|
| Mesin hitung: semua angka paper, empat kasus contoh, tangga tindakan, geometri peta, contoh resmi FSS Code gambar 2, aturan, uji skenario, migrasi versi 1, 400 kapal acak dibandingkan model Python independen | `node tests/run.js` |
| Pembaca DXF: garis, polyline dengan bulge, lingkaran, busur, blok bersarang dengan rotasi dan skala, teks, paper space, Windows-1252 | `node tests/dxf_test.js` |
| Fitur 2.2: rencana tindakan dan urutannya, sebelum dan sesudah, uji hari buruk, pembagian kru per tangga (termasuk 60 kapal acak), jenis kejadian dan kode sidik, kasus ilustrasi | `node tests/v22_test.js` |
| Data 2.3: riwayat kapal dan daftar periksa disimpan dan dinormalkan, tidak mengubah hasil, kode sidik lama tetap | `node tests/v23_test.js` |
| Browser 2.3: panduan GA dan tanda bernomor, data minimum, riwayat kapal (ringkasan, PDF, Excel), daftar periksa dan kartu ke-4, jalur evakuasi A/B, ukur di DXF/PDF/foto dengan skala dan isi ruang, rute menghindari pulau, tur demo, ponsel | `python3 tests/browser_v23.py dist/site /tmp/out` |
| Browser 2.2: Beranda dan tautan `#mulai`, Simple/Advanced tanpa kehilangan data, isi data enam langkah, ringkasan dan salin, sebelum dan sesudah, uji hari buruk, jenis kejadian, PDF (halaman 1 ringkasan, rencana tindakan), tiga kartu, Excel pulang-pergi, arti simbol, tabel validasi, semua halaman dalam dua bahasa, ponsel tanpa geser ke samping, tema gelap, teks antarmuka lengkap, jalan tanpa internet | `python3 build.py && python3 tests/browser_v22.py dist/site /tmp/out` |
| Browser: PDF, Excel pulang-pergi, kode verifikasi | `python3 tests/files_test.py dist/site /tmp/out id` |
| Tangkapan layar desktop, ponsel, gelap, Inggris | `python3 tests/screenshots.py dist/site /tmp/out light,dark,en,phone` |

Hasil terakhir: 6.983 pemeriksaan mesin, 100 pemeriksaan fitur 2.2, 54 pemeriksaan data 2.3, 16 pemeriksaan pembaca DXF, 95 pemeriksaan browser 2.2 dan 37 pemeriksaan browser 2.3 lulus.

## Memasang di GitHub Pages

1. Buat repositori, misalnya `fire-mar`, lalu unggah seluruh isi folder `dist/site/`.
2. **Settings → Pages** → *Deploy from a branch* → `main`, folder `/ (root)` → **Save**.
3. Website tersedia di `https://<nama-akun>.github.io/fire-mar/` dan tetap jalan tanpa sinyal setelah kunjungan pertama.

Memperbarui repositori yang sudah ada: unggah dan timpa semua file dari `dist/site/` (termasuk `sw.js`). Pengunjung lama mendapat versi baru setelah memuat ulang halaman, karena nama cache ikut berganti (`firemar-2.3.0`).

## Struktur

```
src/engine.js      mesin hitung (fungsi murni)
src/plan.js        rencana tindakan, sebelum dan sesudah, uji hari buruk, pembagian kru, jenis kejadian (fungsi murni)
src/i18n.js        teks Indonesia dan Inggris
src/i18n-v22.js    teks halaman versi 2.2
src/i18n-v23.js    teks versi 2.3 (panduan GA, riwayat, daftar periksa, alat ukur, batasan)
src/report.js      laporan PDF, Excel, kode verifikasi
src/geodata.js     garis pantai, pelabuhan dan pos SAR untuk peta
src/dxf.js         pembaca DXF
src/app/*.js       tampilan: inti, grafik, halaman data, peta, DXF, hasil, rencana, analisis, halaman 2.2, kerangka
src/styles.css     desain
scripts/build_fonts.py  membuat subset huruf
tests/             uji mesin, uji silang Python, uji browser
build.py           menyusun dist/artifact dan dist/site
```

## Lisensi

Kode: MIT. Huruf: SIL Open Font License 1.1 (lihat `fonts/LICENSE-OFL.txt`). Garis pantai: Natural Earth (domain publik). Pembaca PDF: pdf.js 3.11.174, Apache License 2.0 (lihat `vendor/pdfjs-LICENSE.txt`).
