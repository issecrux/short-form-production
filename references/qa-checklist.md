# Checklist QA Render Final — jalankan SEMUA sebelum menyerahkan klip

Kegagalan yang pernah terjadi semuanya lolos karena satu langkah di daftar
ini diskip. Jangan mengandalkan sampel.

## Visual

- [ ] Audit frame dari **setiap piece EDL** pada render final (contact
      sheet), plus cek full-res untuk shot wide — sel kecil menyesatkan.
- [ ] Framing tiap shot diukur dari frame shot itu sendiri (bukan menebak
      dari shot tetangga); zoom = SATU ramp kontinu untuk seluruh konten,
      bukan per kelompok shot (ramp per kelompok menimbulkan pumping).
- [ ] Frame terakhir: footage hidup (wajah/reaksi), **bukan hitam**.
      Durasi komposisi tidak melebihi akhir footage.
- [ ] Judul/teks/caption di dalam zona aman: atas 250, bawah 484,
      kanan 140, kiri 60 (file: `~/workspace/lhm-library/SAFE_ZONE_REELS.md`).

## Audio & kata

- [ ] Transkrip render cocok dengan naskah: kata pertama dan terakhir
      utuh, tidak ada fragmen kalimat berikutnya yang ikut terbawa.
- [ ] Tidak ada silence mati ≥0,2 d di ujung; diam penutup yang disengaja
      adalah footage hidup, bukan kekosongan.
- [ ] Loudness terukur: LUFS terintegrasi + true peak tercatat
      (target ±−18 LUFS).
- [ ] Keyword SFX duduk di onset kata yang benar; pengulangan SFX
      bervariasi pitch/volume; satu riser saja.

## Caption

- [ ] Chunk 3–5 kata; kata emphasis sesuai transkrip dan memang kata yang
      memuat poin (uji: kata sans boleh hilang tanpa menghilangkan poin,
      kata emphasis TIDAK boleh).
- [ ] Spasi antar kata caption memakai margin pada span — HyperFrames
      meruntuhkan whitespace antar inline-block.

## Serah terima

- [ ] File bernama versi baru (v2, v3, …) — tidak pernah menimpa versi
      yang sudah diserahkan.
- [ ] Laporkan: durasi, LUFS/TP terukur, dan apa yang berubah dari versi
      sebelumnya.
