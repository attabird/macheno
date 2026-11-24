# Macheno

A browser instrument by Henrik (attabird). Public repo: github.com/attabird/macheno, MIT. Live at https://attabird.github.io/macheno/ via GitHub Pages from `main`, root folder. Every push to `main` goes live.

## Rules

- Everything stays in `index.html`. No frameworks, no build step, no dependencies, no audio samples. Plain ES5-style JavaScript inside one IIFE, matching what is there.
- All sound is synthesized with the Web Audio API.
- Keep the code comments: they explain why each sound is built the way it is.
- Any change to controls must also update the guide panel in `index.html` and the controls table in `README.md`.
- Test in a real browser before pushing. Audio needs a click on the page before it starts.
- Henrik's writing style: no em dashes, short sentences, plain words.

## Known issues and next steps

In priority order:

1. **Timing.** Notes are triggered from `requestAnimationFrame`, so grid hits can land up to a frame late (audible as flams) and the beat stops when the tab is in the background. Replace with a lookahead scheduler that books each hit at its exact time on the audio clock.
2. **Grain latency.** The bitcrusher uses `ScriptProcessorNode`, which adds roughly 46ms of delay to every sound, even at zero grain. Bypass it when grain is 0, then move it to an `AudioWorklet`.
3. **Share by link.** Encode the scene (stars, drums, drones, key, grid) in the URL hash so a piece can be sent to someone.
4. **Record.** Capture canvas and audio together to a video file, for posting.
5. **Demo scene** on first visit, so new visitors hear something before reading the controls.
6. **Mobile.** Most actions need ctrl, shift, alt or a scroll wheel. Add a mode switch (star, drum, drone, select).
7. **Music.** BPM control (techno sits around 125 to 140), swing, undo.
