# Portfolio — Aaron Howard

Static single-page portfolio. No build step, no dependencies.

## Files

```
index.html                    everything: markup, CSS, and the sonar animation
images/hand-schematic.png     KiCad schematic for the hand controller card
resume.pdf                    ← add this yourself (linked from nav, hero, and contact)
```

## Deploy to GitHub Pages

1. Create a repo named `Portfolio` under `github.com/ahowa47`.
2. Push these files to the root of `main`.
3. Settings → Pages → Source: **Deploy from a branch** → `main` / `(root)`.
4. Live in about a minute at `https://ahowa47.github.io/Portfolio/`.

## Things to finish

- **Add `resume.pdf`** to the root. Three links point at it right now and all three 404 until it's there.
- **Add photos.** Two project cards show a placeholder telling you the filename to drop in:
  - `images/sonar-bench.jpg` — the taped-together breadboards with the L-array, or an oscilloscope
    capture of the oscillator waveform
  - `images/ignition-bench.jpg` — the ignition build, or the capacitor charging curve
  Once a file exists, replace that card's `<div class="card-figure empty">…</div>` with the same
  `<figure class="card-figure">` block used on the hand controller card.
- **Repository links.** The hand controller card and the contact section both point at
  `github.com/ahowa47`. Swap in the actual repo URL for the PCB once it's public.
- **Class year.** The hero says class of 2029 — fix if that's wrong.

## Editing notes

- All colors are CSS variables at the top of the `<style>` block (`--paper`, `--ink`, `--signal`,
  `--live`). Change them there and the whole page follows.
- The hero animation is the sonar direction finder: an object orbits the three-mic L-array, the
  microphone circles scale with received amplitude, and the four direction LEDs are driven by the
  same comparator logic the real board used — the divider output against a −4.8 V threshold for the
  vertical axis, right-versus-bottom amplitude for the lateral axis. It renders a single static
  frame for anyone with reduced motion turned on.
- To add a project, copy an `<article class="card rise">` block and edit it. The `specs` list should
  hold real measured numbers — that's the whole point of it.
