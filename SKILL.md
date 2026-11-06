---
name: short-form-production
description: Produce short-form clips (25–60s, vertical 9:16) from long-form podcast/talking-head footage using Rima's production system — hook mining, word-guarded cutting, per-line visual planning, HyperFrames build, full sound design, loudness, and frame-by-frame QA. Use this skill whenever starting, mining, building, revising, or QA-ing a clip ('bikin klip', 'mine kandidat dari episode', 'produksi pick berikutnya', 'heavy edit', 'cek render ini'), or any request that turns long footage into a short. Everything here is distilled from Ultimate Editing 2.0 study and verified production runs — do not improvise rules that contradict it.
---

# Short-Form Production (Rima × Luna)

Rima's short-form clip production system, distilled from Ultimate Editing 2.0
(Joseph) and the verified SOPs from productions Pick #1–3. Source library:
`~/workspace/Studio Editor/resources/ultimate-editing-2.0/STUDY_NOTES.md`
— read the referenced chapter before running a stage when in doubt. Measured
visual tokens: `~/workspace/Studio Editor/style-lab/STYLE.md`.

## Rules that bind every stage

- Never start making a video before Rima gives an explicit go-ahead.
- Rima delegates selection decisions to Luna: decide yourself, give brief
  reasons, Rima vetoes. Presenting a menu of options is friction.
- Revisions are always new version files (v2, v3, …) with labeled
  before/after proof. Never overwrite a delivered version.
- Never claim completion without verifying the file on disk (size, duration,
  ffprobe). Download panels and process reports are not proof.
- Every number in this skill comes from distillation or measurement. When a
  situation is not covered, measure first — do not invent parameters.

## Stage 1 — Mining & story (STUDY_NOTES: M4-06, M4-07, M4-08)

Set the **short's topic first**; every candidate is measured against that
topic — a great hook serving another topic is still rejected.

Hunt for a **hook statement**: only three types qualify —
1. a negative statement,
2. a strong question / one people commonly ask,
3. an interesting claim nobody has heard before.

Two vetoes override content quality:
- **Delivery veto**: good words with jittery, broken-up pauses = rejected.
- **Visual veto**: segments that cannot be cropped vertically in a viable
  way (whiteboards, music+text intros, upper-third framing) = rejected.

Assembling a hook is a standard move, not cheating:
- **Stacking** — combine two hook moments (e.g. a generalization + a battery
  of negative what-if questions).
- **Splicing** — join fragments across timestamps, cut the filler in
  between, tighten internal pauses. Keep qualifiers that carry meaning; cut
  the neutral ones.
- **Transplant** — borrow a transition statement from elsewhere in the
  episode when the hook and the payoff do not connect.

Score candidates with the /25 rubric (first-line strength, arc+payoff,
arousal, quotability, host reaction/visual). The rubric raises probability;
it is not a predictive model — treat it as a ranking tool.

Arrange the story in **storytelling order**: explain → new question → value
→ conclusion. During mining, collect examples generously; during the build,
trim ruthlessly — most examples must be deleted to reach the conclusion as
fast as possible. One voice per short: cut host interjections from the body
except a closing reaction.

## Stage 2 — Cutting (M4-05, M4-07 + production SOP)

- Cut silence only BETWEEN phrases, exactly after speech stops and before
  it starts. Apply a **word-guard**: never cut inside [word start −0.05s,
  word end +0.04s] — detected "silences" often contain soft word onsets.
- **Protect emphasis pauses**: a mid-sentence pause right before the payoff
  word is emphasis, not fat. Keep the silence after the last line as a
  closing beat (~0.5–1s of live footage).
- **J/L-cuts** serve three functions: more time on the face, the cut point
  on the right visual moment, and breathing room after an emphasized line
  (proportional to its weight). Implement them as per-piece video vs audio
  trim offsets.
- Build footage in **ONE ffmpeg pass** with trim/concat filters. Assembling
  per-piece files + concat demuxer causes measured drift (+0.74s).
- Split pieces at shot boundaries; measure each shot's vertical crop from
  that shot's own frame; judge wide shots from full-res frames, not small
  contact-sheet cells.

## Stage 3 — Per-line visual plan (M4-04, M4-09 to M4-12)

Write a plan per line BEFORE building: which shot, which word gets
highlighted, which text technique. No plan, no build.

- Block structure of this style: hook → **3 scenes** → **pattern break**
  (back to the speaker, simple text — brings the viewer "back to zero") →
  repeat. For a 30–50s clip, one block ≈ one whole clip.
- Style composition: ±40% footage, 40% cinematic text, 20% sound design.
- **B-roll-free zones: the hook and transition statements.** Transitions are
  deliberately empty — viewer rest is a design decision.
- B-roll is **literal**: it depicts the word/emotion being spoken.
  Selection order: script → highlight the value/emotion → footage that
  shows it. Reuse an emotion scene when the same word returns (zero cost).
  Contrast lines "X instead of Y" → split screen. Turning points → full
  cinematic treatment. Dense educational stretches → stay on the speaker
  with simple subtitles. The ending always returns to the speaker's face.
- Source priority: recorded footage / the episode's own angles (host
  reactions, second angle) far above stock; stock only for concepts absent
  from the episode, and it must pass the "stocky" veto (corporate, acted,
  too neat/too bright = reject; the keyword "silhouette" yields cinematic
  results). Write the shot list per beat with an emotion spec
  (light/wardrobe/angle).

## Stage 4 — Text (M4-14 to M4-18)

Text has three simultaneous roles: show what is said, highlight the focus,
and look appealing. Fonts separate the roles: **sans = ordinary words,
serif/script = special words only** ("a square among circles"). Test for a
special word: the sans words may be deleted without losing the point; the
special word IS the point. At most one special word per caption chunk.

Text workflow order: (1) default text for the whole edit, (2) special
designed scenes, (3) text over B-roll scenes.

**Default text** is built in 4 steps (transcribe → caption → style →
animation):
- Transcript: strip all periods and commas. This style's default captions =
  1 word, min 2s, single line. (Our campaign chunks are 3–5 words per the
  brief — outside the campaign, use the style default.)
- Sans style: smaller is better (the beginner mistake is fonts that are too
  big); lower-third position; soft drop shadow (heavy blur).
- **The animator** (the only one, confirmed across all sources): position
  starts SLIGHTLY below final + opacity starts at ±25% + blur starts at ±5,
  all ease-out (fast → slow), duration not too fast. Big pops look cheap;
  Joseph's final version is named "POP UP MINIMAL". Our measured version is
  in STYLE.md (sans per word, serif per character).

**Designed stacks** (intro + transition statements): one element per word,
each starting at its word's onset, all ending at the same point (never trim
from the front — the animation lives there). Focus words → special font;
**drop shadow is removed** in stacks (our serif glow belongs to the caption
layer — do not mix the two). Arrange as a puzzle: mass balanced in the
center, word sizes follow the gaps in neighboring letterforms (relative
scale ±120–140%, the payoff word biggest), diagonal reading flow, never
covering the subject.

**Scene-integrated text** (for B-roll scenes): nest all words into one
wrapper, then pick one —
- *3D warp*: perspective + rotate matched by eye to the surface plane in
  the shot; a little goes a long way — too much is immediately wrong.
- *Blending*: needs a flat, textured surface; `mix-blend-mode` overlay (or
  screen with slightly reduced opacity); per-word opacity grading inside
  the blend (filler 25–50%, focus 100%).
- *Glitch entrance* (optional): randomized per-frame opacity keyframes
  settling at 100%.

Chapters still being distilled (tracking text, the combined text-on-B-roll
workflow, this style's sound — M4-19 to 29): check the latest status in
STUDY_NOTES before claiming coverage; the Stage 6 framework below covers
the gap meanwhile.

## Stage 5 — HyperFrames build (verified SOP, Pick #1–3)

Read `~/workspace/Studio Editor/AGENTS.md` before touching a composition —
its check rules, unique audio ids, and timeline registration bind all work.
Production specifics:

- Renders on this VM use `TMPDIR=/home/hatch/.cache/hyperframes/tmp`
  (/tmp is only 512 MB).
- Caption word spacing uses **margin on spans**, not HTML whitespace — the
  renderer collapses whitespace between inline-blocks.
- Every `<audio>` needs a unique id, or the render is silent.
- Scene backgrounds use the texture stack: blurred set photo → wash → silk
  gradient (screen) → light leak (screen) → halftone (overlay) → grain
  (overlay) → vignette. Cutouts are REAL photos (never AI), white sticker
  outline, hard drop shadow.
- Footage zoom: **one continuous ramp** 1.0→1.06 across the whole content.
  Per-shot-group ramps cause pumping.
- External narration (e.g. Rima's ElevenLabs): normalize first, measure its
  word onsets with Whisper, sync title pops to onsets; HOOK_T = speech end
  + 0.13; riser at HOOK_T −0.55; transition at HOOK_T −0.13.
- Keep generator scripts in the project folder, NEVER in /tmp (lost on VM
  restart).
- Cross-platform safe zone: top 250, bottom 484, right 140, left 60 px
  (1080×1920). Spec: `~/workspace/lhm-library/SAFE_ZONE_REELS.md`.

## Stage 6 — Sound design (framework: `references/sound-framework.md`)

Read the reference file for the full level table. The core that must never
be lost: movement = whoosh; layer whoosh → texture → riser/hit; **exactly
one riser** per video, at the intro bridge; voice ±−9 dB, music −20 to
−24 dB under narration.

Rima's standard on top of that framework: **always full layers, never
minimal** — keyword SFX from the catalog first, placed at word onsets; thin
accents on emphasis words and reactions; SFX must be felt, and repeated
uses of the same SFX are varied in pitch/volume. Campaign BGM = a trending
song's instrumental version as a bed.

## Stage 7 — Loudness & QA (`references/qa-checklist.md`)

Run the full checklist in the reference file before delivering any render.
In short: a final loudness stage (volume + alimiter, target ±−18 LUFS,
measure LUFS + true peak), a frame audit of **every** EDL piece from the
final render, a render-transcript check, a last-frame check (live footage,
not black), and composition duration never exceeding the footage end.

## Campaign context (for @thetalkreceipt / LHM clips)

Campaign rules live in their own files — do not rely on memory: brief and
caption research in `~/workspace/lhm-library/` (`CAPTION_HASHTAG_RESEARCH.md`,
`SAFE_ZONE_REELS.md`, `TRENDING_SOUNDS_*.md`, `candidates/SHORTLIST.md`).
Posting follows TikTok → (48–72h) → Instagram → YouTube, and Buffer
scheduling happens only after Rima approves the clip.
