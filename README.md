# Lockpick subtitles

Fan-made English subtitles for the voice-over of **Resident Evil (1996, PC)**, made for accessibility. The original
release has no subtitles for its voiced scenes.

This pack is an optional download for [Lockpick](https://github.com/mscrnt/lockpick), a free, open-source companion
app for the game. Lockpick never downloads it unless you turn subtitles on.

## Notice

- **The dialogue belongs to Capcom.** This is a transcription of the game's voice-over, shared freely for
  accessibility; it is not affiliated with or endorsed by Capcom.
- It is **not** covered by Lockpick's MIT license, and no license is granted for it here.
- Nothing is sold, and no game audio or other game files are included — only text and timings.
- If you represent the rights holder and want it removed, open an issue or contact the maintainer and it will be
  taken down.

## Contents

`re1/en/voice.json` — one entry per voice file in the game's `USA\Voice` folder:

| Field | Meaning |
|---|---|
| `id` | Voice file name without extension, e.g. `v004_00` |
| `kind` | `dialogue` or `scream` (screams and grunts are captioned `[screams]`) |
| `seconds` | Length of the voice file |
| `text` | The line |
| `segments` | Timed parts of the line (`start`/`end` in seconds from the start of the file) |
| `sha256` | Fingerprint of the voice file the line was made from, so a mismatched game version is detected |

Voice files without speech (effects, breathing) are left out. The game's videos (logos, endings, credits) contain no
transcribable dialogue.

## How it was made — and how to help

The lines are a **machine transcription** that has not yet been checked by ear: Whisper large-v3 (two passes, given the
character names) cross-checked against NVIDIA Canary-Qwen 2.5B. A line is included only when at least two passes agree,
so most lines should be right, but mistakes are possible — especially names, shouted words and overlapping speech.

Corrections are very welcome: open a pull request that changes the `text` (and `segments`) of the lines you fixed, and
say how you checked them (e.g. listened in game). Please keep changes to transcription only; no audio or other game
files.
