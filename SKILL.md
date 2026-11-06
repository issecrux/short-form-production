---
name: short-form-production
description: Produce short-form clips (25–60s, vertical 9:16) from long-form podcast/talking-head footage using Rima's production system — hook mining, word-guarded cutting, per-line visual planning, HyperFrames build, full sound design, loudness, and frame-by-frame QA. Use this skill whenever starting, mining, building, revising, or QA-ing a clip ('bikin klip', 'mine kandidat dari episode', 'produksi pick berikutnya', 'heavy edit', 'cek render ini'), or any request that turns long footage into a short. Everything here is distilled from Ultimate Editing 2.0 study and verified production runs — do not improvise rules that contradict it.
---

# Short-Form Production (Rima × Luna)

Sistem produksi klip short-form Rima, didistilasi dari Ultimate Editing 2.0
(Joseph) dan SOP terverifikasi dari produksi Pick #1–3. Pustaka sumber:
`~/workspace/Studio Editor/resources/ultimate-editing-2.0/STUDY_NOTES.md`
— baca bab yang dirujuk sebelum menjalankan tahapnya bila ragu. Token visual
terukur: `~/workspace/Studio Editor/style-lab/STYLE.md`.

## Aturan yang mengikat semua tahap

- Jangan mulai membuat video sebelum Rima memberi aba-aba eksplisit.
- Rima mendelegasikan keputusan pilihan ke Luna: putuskan sendiri, beri
  alasan singkat, Rima yang veto. Menyodorkan menu pilihan adalah gesekan.
- Revisi selalu file versi baru (v2, v3, …) dengan bukti before/after
  berlabel. Jangan pernah menimpa versi yang sudah diserahkan.
- Jangan klaim selesai tanpa verifikasi file di disk (ukuran, durasi,
  ffprobe). Panel unduhan dan laporan proses bukan bukti.
- Setiap angka di skill ini berasal dari distilasi atau pengukuran. Bila
  sebuah situasi tidak tercakup, ukur dulu — jangan mengarang parameter.

## Tahap 1 — Mining & cerita (STUDY_NOTES: M4-06, M4-07, M4-08)

Tetapkan **topik short dulu**; semua kandidat diukur terhadap topik itu —
hook bagus untuk topik lain tetap gugur.

Berburu **hook statement**: hanya tiga tipe yang lolos —
1. pernyataan negatif,
2. pertanyaan yang kuat / sering ditanyakan orang,
3. klaim menarik yang belum pernah didengar.

Dua veto yang mengalahkan kualitas isi:
- **Veto delivery**: kata bagus dengan jeda patah-patah = gugur.
- **Veto visual**: segmen yang tidak bisa di-crop vertikal dengan layak
  (whiteboard, intro bermusik+teks, framing upper-third) = gugur.

Merakit hook adalah gerakan standar, bukan kecurangan:
- **Stacking** — gabung dua momen hook (mis. generalisasi + rentetan
  pertanyaan what-if negatif).
- **Splicing** — sambung fragmen lintas timestamp, buang filler di tengah,
  rapatkan jeda internal. Pertahankan kualifikasi yang memuat makna; buang
  yang netral.
- **Transplant** — pinjam transition statement dari bagian lain episode
  bila hook dan payoff tidak menyambung.

Skor kandidat dengan rubrik /25 (kekuatan baris pertama, lengkung+payoff,
arousal, quotability, reaksi host/visual). Rubrik menaikkan peluang, bukan
model prediksi — perlakukan sebagai alat peringkat.

Susun cerita dalam **storytelling order**: explain → pertanyaan baru →
value → kesimpulan. Saat mining, kumpulkan contoh dengan longgar; saat
build, pangkas kejam — sebagian besar contoh memang harus dibuang demi
mencapai kesimpulan secepat mungkin. Satu suara per short: interjeksi host
dibuang dari badan cerita kecuali reaksi penutup.

## Tahap 2 — Cutting (M4-05, M4-07 + SOP produksi)

- Potong silence hanya ANTAR-frasa, persis setelah bicara berhenti dan
  sebelum bicara mulai. Terapkan **word-guard**: jangan pernah memotong di
  dalam [awal kata −0,05 d, akhir kata +0,04 d] — "silence" hasil deteksi
  sering berisi onset kata yang lembut.
- **Lindungi jeda emphasis**: jeda di tengah kalimat tepat sebelum kata
  payoff adalah emphasis, bukan lemak. Diam setelah baris terakhir
  dipertahankan sebagai beat penutup (±0,5–1 d footage hidup).
- **J/L-cut** melayani tiga fungsi: waktu lebih lama di wajah, titik potong
  di momen visual yang benar, dan ruang napas setelah baris yang ditekankan
  (sebanding bobot emphasis-nya). Implementasikan sebagai offset trim
  video vs audio per piece.
- Footage dibangun dalam **SATU pass** trim/concat-filter ffmpeg. Merakit
  file per-piece + concat demuxer menimbulkan drift terukur (+0,74 d).
- Split piece di batas shot; crop vertikal diukur dari frame tiap shot
  sendiri; shot wide diputuskan dari frame full-res, bukan sel kecil.

## Tahap 3 — Rencana visual per baris (M4-04, M4-09 s.d. M4-12)

Tulis rencana per baris SEBELUM build: shot apa, kata mana yang
di-highlight, teknik teks mana. Tanpa rencana, tidak ada build.

- Struktur blok style ini: hook → **3 scene** → **pattern break** (kembali
  ke pembicara, teks sederhana — membawa penonton "back to zero") → ulangi.
  Untuk klip 30–50 d, satu blok ≈ satu klip utuh.
- Komposisi style: ±40% footage, 40% teks sinematik, 20% sound design.
- **Zona bebas B-roll: hook dan transition statement.** Transisi sengaja
  kosong — jeda istirahat penonton adalah keputusan desain.
- B-roll **literal**: menggambarkan kata/emosi yang sedang diucapkan.
  Urutan seleksi: script → highlight value/emosi → footage yang
  menunjukkannya. Scene emosi dipakai ulang saat kata yang sama kembali
  (nol biaya). Kalimat kontras "X instead of Y" → split screen. Titik balik
  → perlakuan sinematik penuh. Materi edukatif padat → tetap pembicara +
  subtitle sederhana. Penutup selalu kembali ke wajah pembicara.
- Prioritas sumber: footage rekaman/angle asli episode (reaksi host, angle
  kedua) jauh di atas stock; stock hanya untuk konsep yang tidak ada di
  episode, dan harus lolos veto "stocky" (korporat, akting, terlalu rapi/
  terlalu terang = tolak; kata kunci "silhouette" menghasilkan sinematik).
  Shot list ditulis per beat dengan spec emosi (cahaya/kostum/angle).

## Tahap 4 — Teks (M4-14 s.d. M4-18)

Teks punya tiga peran sekaligus: menunjukkan apa yang dikatakan, menyorot
fokus, dan terlihat menarik. Font memisahkan peran: **sans = kata biasa,
serif/script = kata spesial saja** ("kotak di antara lingkaran"). Uji kata
spesial: kata sans boleh dihapus tanpa menghilangkan poin; kata spesial
adalah poinnya. Maksimum satu kata spesial per chunk caption kita.

Urutan workflow teks: (1) teks default untuk seluruh edit, (2) scene desain
khusus, (3) teks di atas scene B-roll.

**Teks default** dibangun 4 langkah (transcribe → caption → style → animasi):
- Transkrip: hapus semua titik dan koma. Caption default style ini =
  1 kata, min 2 d, satu baris. (Chunk campaign kita 3–5 kata mengikuti
  brief — di luar campaign, pakai default style.)
- Style sans: lebih kecil lebih baik (kesalahan pemula = font terlalu
  besar); posisi lower-third; drop shadow lembut (blur besar).
- **Animator** (satu-satunya, terkonfirmasi di semua sumber): posisi mulai
  SEDIKIT di bawah final + opacity mulai ±25% + blur mulai ±5, semuanya
  ease-out (cepat → melambat), durasi jangan terlalu cepat. Pop besar
  terlihat murahan; versi final Joseph bernama "POP UP MINIMAL". Detail
  terukur versi kita ada di STYLE.md (sans per kata, serif per karakter).

**Stack desain** (intro + transition statement): satu elemen per kata,
mulai di onset katanya, semua berakhir di titik yang sama (jangan trim dari
depan — animasi hidup di sana). Kata fokus → font spesial; **drop shadow
dibuang** di stack (glow serif kita hanya untuk lapisan caption, jangan
dicampur). Susun sebagai puzzle: massa seimbang di tengah, ukuran kata
mengikuti celah bentuk huruf tetangganya (skala relatif ±120–140%, kata
payoff terbesar), alur baca diagonal, tidak menutupi subjek.

**Teks menyatu scene** (untuk scene B-roll): nest semua kata jadi satu
wrapper, lalu pilih satu —
- *3D warp*: perspective + rotate dicocokkan dengan mata ke bidang
  permukaan di shot; sedikit saja, kebanyakan langsung salah.
- *Blending*: butuh permukaan datar bertekstur; `mix-blend-mode` overlay
  (atau screen, opacity turun sedikit); gradasi opacity per kata di dalam
  blend (filler 25–50%, fokus 100%).
- *Glitch entrance* (opsional): keyframe opacity acak per frame sampai
  menetap di 100%.

Bab yang masih didistilasi (tracking text, workflow teks-B-roll gabungan,
sound versi style ini — M4-19 s.d. 29): cek status terakhir di STUDY_NOTES
sebelum mengklaim cakupan; kerangka Tahap 6 di bawah menutup sementara.

## Tahap 5 — Build HyperFrames (SOP terverifikasi Pick #1–3)

Baca `~/workspace/Studio Editor/AGENTS.md` sebelum menyentuh komposisi —
aturan check, id audio unik, dan registrasi timeline ada di sana dan
mengikat. Yang spesifik produksi:

- Render di VM ini memakai `TMPDIR=/home/hatch/.cache/hyperframes/tmp`
  (/tmp hanya 512 MB).
- Spasi antar kata caption memakai **margin pada span**, bukan whitespace
  HTML — renderer meruntuhkan whitespace antar inline-block.
- Setiap `<audio>` wajib id unik, atau render bisu.
- Background scene memakai tumpukan tekstur: foto set ter-blur → wash →
  silk gradient (screen) → light leak (screen) → halftone (overlay) →
  grain (overlay) → vignette. Cutout foto ASLI (bukan AI), outline stiker
  putih, bayangan keras.
- Zoom footage: **satu ramp kontinu** 1,0→1,06 sepanjang konten. Ramp per
  kelompok shot menimbulkan pumping.
- Narasi eksternal (mis. ElevenLabs dari Rima): normalisasi dulu, ukur
  onset katanya dengan Whisper, sinkronkan pop judul ke onset; HOOK_T =
  akhir bicara + 0,13; riser di HOOK_T −0,55; transisi di HOOK_T −0,13.
- Script generator disimpan di folder proyek, JANGAN di /tmp (hilang saat
  VM restart).
- Zona aman lintas platform: atas 250, bawah 484, kanan 140, kiri 60 piksel
  (1080×1920). Spec: `~/workspace/lhm-library/SAFE_ZONE_REELS.md`.

## Tahap 6 — Sound design (kerangka: `references/sound-framework.md`)

Baca file referensi untuk tabel level lengkap. Inti yang tidak boleh
hilang: movement = whoosh; lapis whoosh → texture → riser/hit; **tepat
satu riser** per video, di jembatan intro; voice ±−9 dB, musik −20 s.d.
−24 dB di bawah narasi.

Standar Rima di atas kerangka itu: **selalu full layer, tidak pernah
minimal** — keyword SFX dari katalog dulu, ditempatkan di onset kata;
aksen tipis di kata emphasis dan reaksi; SFX harus terasa, dan pengulangan
SFX yang sama divariasikan pitch/volume-nya. BGM campaign = lagu trending
versi instrumental sebagai bed.

## Tahap 7 — Loudness & QA (`references/qa-checklist.md`)

Jalankan checklist lengkap di file referensi sebelum menyerahkan render
apa pun. Ringkasnya: tahap loudness terakhir (volume + alimiter, target
±−18 LUFS, ukur LUFS + true peak), audit frame dari **setiap** piece EDL
pada render final, cek transkrip render, cek frame terakhir (footage
hidup, bukan hitam), dan durasi komposisi tidak melebihi akhir footage.

## Konteks campaign (bila klip untuk @thetalkreceipt / LHM)

Aturan campaign hidup di file khususnya — jangan mengandalkan ingatan:
brief & riset caption di `~/workspace/lhm-library/` (`CAPTION_HASHTAG_RESEARCH.md`,
`SAFE_ZONE_REELS.md`, `TRENDING_SOUNDS_*.md`, `candidates/SHORTLIST.md`).
Posting mengikuti urutan TikTok → (48–72 jam) → Instagram → YouTube, dan
jadwal Buffer hanya setelah Rima menyetujui klipnya.
