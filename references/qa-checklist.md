# Final Render QA Checklist — run ALL of it before delivering a clip

Every past failure slipped through because one step on this list was
skipped. Never rely on sampling.

## Visual

- [ ] Frame audit of **every EDL piece** from the final render (contact
      sheet), plus full-res checks for wide shots — small cells mislead.
- [ ] Each shot's framing was measured from that shot's own frame (not
      guessed from a neighboring shot); zoom = ONE continuous ramp across
      the whole content, not per shot group (per-group ramps pump).
- [ ] Last frame: live footage (face/reaction), **not black**. Composition
      duration does not exceed the footage end.
- [ ] Titles/text/captions inside the safe zone: top 250, bottom 484,
      right 140, left 60 (file: `~/workspace/lhm-library/SAFE_ZONE_REELS.md`).

## Audio & words

- [ ] Render transcript matches the script: first and last words intact,
      no fragment of the next sentence carried along.
- [ ] No dead silence ≥0.2s at the tail; an intentional closing silence is
      live footage, not emptiness.
- [ ] Loudness measured: integrated LUFS + true peak recorded
      (target ±−18 LUFS).
- [ ] Keyword SFX sit at the correct word onsets; repeated SFX vary in
      pitch/volume; only one riser.

## Captions

- [ ] Chunks of 3–5 words; emphasis words match the transcript and are the
      words carrying the point (test: the sans words may vanish without
      losing the point, the emphasis word may NOT).
- [ ] Caption word spacing uses margins on spans — HyperFrames collapses
      whitespace between inline-blocks.

## Handover

- [ ] File carries a new version name (v2, v3, …) — never overwrite a
      delivered version.
- [ ] Report: duration, measured LUFS/TP, and what changed from the
      previous version.
