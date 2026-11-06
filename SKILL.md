---
name: short-form-production
description: The short-form editing system distilled from Ultimate Editing 2.0 (Joseph) — hook mining and storytelling, cutting and pacing, per-line visual planning, B-roll, the text system (default captions, designed stacks, scene-integrated text), and the sound framework. Use this skill whenever mining hooks from long footage, cutting a short, planning an edit, designing text for a short, or designing its sound ('bikin klip', 'mine kandidat dari episode', 'susun rencana edit', 'heavy edit', 'cek render ini'). Content is study material only; check STUDY_NOTES for the chapters still being distilled before claiming coverage.
---

# Short-Form Production — the studied system

Everything in this skill is distilled from one resource: the Ultimate
Editing 2.0 course (Joseph), studied in two channels (transcripts + visual
frame checks) and translated into HyperFrames equivalents. Full notes:
`~/workspace/Studio Editor/resources/ultimate-editing-2.0/STUDY_NOTES.md`.
Measured caption tokens from the style study:
`~/workspace/Studio Editor/style-lab/STYLE.md`.

Fidelity rule: every number here comes from the course material or from
measuring its reference footage. Do not invent parameters the resource
does not contain.

## 1 — Mining & story (M4-06, M4-07, M4-08)

Set the **short's topic first**; every candidate is measured against that
topic — a great hook serving another topic is still rejected.

Hunt for a **hook statement**: only three types qualify —
1. a negative statement,
2. a strong question / one people commonly ask,
3. an interesting claim nobody has heard before.

Two vetoes override content quality:
- **Delivery veto**: good words with jittery, broken-up pauses = rejected.
- **Editability veto**: segments that cannot be cut into a viable vertical
  short (music+text intros, whiteboards, upper-third framing) = rejected.

Assembling a hook is a standard move, not cheating:
- **Stacking** — combine two hook moments (e.g. a generalization + a battery
  of negative what-if questions).
- **Splicing** — join fragments, cut the filler inside the hook itself,
  tighten internal pauses. Keep qualifiers that carry meaning; cut the
  neutral ones.
- **Transplant** — borrow a transition statement from elsewhere in the
  footage when the hook and the payoff do not connect.

Arrange the story in **storytelling order**: explain → new question → value
→ conclusion. During mining, collect examples generously; during the trim
pass, delete most of them to reach the conclusion as fast as possible.

## 2 — Cutting & pacing (M4-05, M4-07)

- Cut silence only BETWEEN phrases — exactly after speech stops and before
  it starts, never into a word. Detected silences can hide soft word
  onsets; check before cutting.
- **Protect emphasis pauses**: a mid-sentence pause right before the payoff
  word is emphasis, not fat. The silence after the last line is kept on
  purpose — it emphasizes the closing statement.
- **J/L-cuts** serve three functions: more time on the speaker's face
  before the next line, the cut point on the right visual moment (e.g.
  while the subject still looks at camera), and breathing room after an
  emphasized line, proportional to its weight. The speaker's breaths are
  usable J-cut material.
- Split at shot boundaries. One voice carries the story; interjections are
  cut from the body except a closing reaction.

## 3 — Per-line visual plan (M4-04, M4-09 to M4-12)

Plan every line BEFORE building: which shot, which word gets highlighted,
which text technique. The plan is made from a style breakdown — pillars
extracted from ±10 inspiration reels.

- Block structure: hook → **3 B-roll+text scenes** → **pattern break**
  (back to the speaker, simple text — brings the viewer "back to zero") →
  repeat. Repetition lines are planned as match cuts.
- Style composition: ±40% footage, 40% cinematic text, 20% sound design.
- **B-roll-free zones: the hook and transition statements.** Transitions
  are deliberately empty — viewer rest is a design decision.
- B-roll's job: turn the VALUE in the footage into something seen, felt, or
  understood. Selection: script → highlight the value/emotion → footage
  that literally shows it. Reuse an emotion scene when the same word
  returns (zero cost). Contrast lines "X instead of Y" → split screen.
  Turning points → full cinematic text treatment. Dense educational
  stretches → stay on the speaker with simple subtitles. The ending returns
  to the speaker's face.
- Sources: recorded/client footage is strongly preferred ("you want to see
  Hormozi doing what he's talking about"); stock is always worse, free
  stock worst. Veto "stocky" footage (corporate, acted, too neat/too
  bright); the keyword "silhouette" yields cinematic shots. Collect two
  shots per beat (action + face/expression), specify emotion via light,
  wardrobe, and angle in the shot list, rename downloads plainly, and QC
  after downloading.

## 4 — Text (M4-14 to M4-18)

Text has three simultaneous roles: show what is said, highlight the focus,
and look appealing. Fonts separate the roles: **sans = ordinary words,
script = special words only** ("a square among circles" — one different
shape in a uniform pattern wins the eye by itself). Test for a special
word: the sans words may be deleted without losing much value; the script
word IS the point of the scene. Sans in this style: Coolvetica, Montserrat,
SF UI Display. Script: Edwardian Script and similar.

Workflow order: (1) default text for the whole edit, (2) special designed
scenes (intro + transitions), (3) text designed over B-roll scenes.

**Default text** — 4 steps: transcribe → caption → style → animation.
- Transcribe, then **delete all periods and commas** from the script.
- Caption settings: max length in characters — 7 ≈ 1 word, 15–20 ≈
  2 words, 40 ≈ long sentences. For this style he chooses **one-word
  captions**, minimum duration **2s**, **single line**.
- Style: Coolvetica Regular at ±80–90 ("smaller is better" — the most
  common beginner mistake is fonts that are way too big), center-aligned,
  lower-third zone, drop shadow kept but blurred soft (±80). Save as the
  track style so it applies to every caption.
- **The animator**: position starts SLIGHTLY below final (a small offset —
  big pops look cheap) with fast→slow easing; opacity starts at **25–50%**;
  Gaussian blur starts at **5** (10 is too intense, 20 way too intense) and
  ends at 0; shutter angle 180 for motion blur. Slower is nicer. His final,
  reduced version is named "POP UP MINIMAL" — minimal is the doctrine.
  Save the animation as a preset anchored so its length stays constant
  regardless of caption length.

**Designed stacks** — one text element per word, each starting at its
word's onset (read from the waveform), all trimmed to a common END (never
trim the front; the animation lives there). Focus words switch to the
script font. **Drop shadow is removed** for stack words — it does not suit
aligned text. Arrange as a puzzle (the design principles from M4-14): mass
balanced in the center; word sizes follow the gaps in neighboring
letterforms (small words tucked into the space behind a T, between E and
T, behind a Y); relative scale ±120–140% with the payoff word biggest;
reading flow runs diagonally (top-left → bottom-right or mirrored); a
heavy side is counterweighted by the script word on the opposite side;
never cover the subject. Patterns: center stack or diagonal. There is no
single right answer — iterate by eye.

**Scene-integrated text** — prepare the words as a stack, nest them into
one layer (HyperFrames: one wrapper), then apply one effect:
- *3D warp* (Basic 3D): swivel + tilt matched by eye to the plane of the
  wall/surface in the shot; "distance to image" adds perspective — use a
  little, too much looks wrong immediately. Trial and error is part of it.
  No script font for scene text.
- *Blending mode*: requires a flat, textured surface (a wall) — without
  texture there is nothing to blend into. Common picks: **Overlay** (white
  text into the wall) or **Screen** with slightly reduced opacity; overall
  layer opacity ±75%; per-word opacity grading inside the blend (filler
  words 25–50%, focus words 100%) so the focus hierarchy survives.
- *Glitch entrance* (variant): instead of a smooth opacity ramp, randomize
  opacity keyframes frame by frame (25, 0, 100, 0, 40, 0, 100, 50, …)
  until settling at 100%.

Related measured parameters from the masterclass study: Deep Glow Radius
801.00, Exposure 0.20, blend Screen, Chromatic Aberration 0.50%; VR Glow
Luma Threshold 0.00 / Radius 190 / Brightness 1.30 / Saturation 1.00;
caption doctrine (AE-36) max 25–30 characters / min 2s / single line;
zoom doctrine max 120%, never back-to-back zooms; speed-graph spikes
≈4× average speed (≈ GSAP power3.out; serif characters power2.out).

## 5 — Sound (framework: `references/sound-framework.md`)

Read the reference file for the full level table and doctrine from the
Premiere Pro / After Effects masterclasses: movement = whoosh; layering
whoosh → texture → riser/hit; exactly one riser per video; voice −6 to
−12 dB (ideal ±−9), music −20 to −24 dB under narration; export AAC
48 kHz, bitrate 20.

## Coverage status

Distilled and included: M4-04 to M4-18 (short-form cluster, B-roll block,
text block) and the PR/AE masterclass frameworks. Still being distilled:
M4-19 to M4-22 (tracking text, combined text-on-B-roll workflow, practice
builds) and M4-23 to M4-29 (this style's sound & music) — check STUDY_NOTES
for their status before relying on this skill for those topics.
