# soundgo

Play chords and melodies with your hands through your webcam — no MIDI controller, no install.

## Try it

[soundgo.vercel.app](https://soundgo.vercel.app) (TBD)

## What it does

Two modes, switchable from the bottom controls:

**Two-hand Chord** (default)
- Left hand picks the chord root from a circular wheel
- Right hand picks the quality (`maj`, `maj7`, `7`, `sus4`, `m`, `m7`, `dim`, `aug`)
- Move the index fingertip into the wheel's center to silence the chord
- Built for jazz progressions like ii–V–I in seconds

**Melody + Chord**
- Right hand plays melody on a piano-style keyboard at the bottom-right
  - X = pitch, Y = volume
  - Pinch thumb + index to gate sound on
- Left hand plays accompaniment chords on the wheel
  - Pinch = Minor, open = Major

## How to play

- The **index fingertip** is your cursor — a large dot with a white ring shows where you're pointing
- Both wheels have an inner OFF zone so you can rest without sound
- The "Simple (ABCDEFG)" toggle reduces the chord wheel to 7 diatonic roots (great for beginners)

## Stack

- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) — on-device hand tracking, no video uploaded
- [Tone.js](https://tonejs.github.io/) — Web Audio synthesis
- Plain HTML/CSS/JS, single file, no build step

## Run locally

`getUserMedia` requires HTTPS or `localhost`, so just opening the file won't work.

```bash
python3 -m http.server 8765
open http://localhost:8765
```

## Privacy

The webcam stream stays in your browser. No frames are uploaded anywhere.

## License

MIT
