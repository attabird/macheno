# Macheno

A browser instrument. You plant stars, drums and drones on a night sky, and they play.

**Play it:** https://attabird.github.io/macheno/

Everything is synthesized live with the Web Audio API. No samples, no audio files, no libraries, no build step. The whole instrument is one HTML file.

## How it works

Position is the interface. There are no sliders for pitch or tempo. Where something sits on screen is what it sounds like:

- **Up and down** is pitch, locked to the selected key
- **Left and right** is how often it repeats
- **Dragging it around** stretches how long its notes ring

## What you can plant

- **Stars.** Melodic voices in six timbres, color coded. Each one plays a short pattern on a loop, with a little timing and velocity drift so it never sounds mechanical.
- **Drums.** Kick, snare and hat, built from scratch on every hit. Height damps them: higher on screen is tighter.
- **Drones.** Draw a line. Its length sets how slowly it breathes. A line across the full width holds forever.

## Controls

| Do this | And this happens |
| --- | --- |
| Tap empty sky | Plant a star |
| Ctrl/Cmd + tap empty sky | Plant the selected drum |
| Shift + drag empty sky | Draw a drone |
| Tap a star | Start or stop it |
| Double-tap a star or drone | Remove it |
| Drag a star | Retune and retime it |
| Flick a star | Throw it. It bounces off the edges with little plucks |
| Scroll on a star | Add grain (a bitcrusher) |
| Shift + drag a star or drone | Volume |
| Scroll on a drone | Filter wobble speed |
| Alt + scroll on a drone | Filter register |
| Drag empty sky | Select a group, then drag one to move them all |
| `m` | Mute or unmute the selection |
| `\` | Delete the selection |
| `space` | Pause. Notes already ringing finish naturally |
| `1` to `6` | Star color |
| `7` to `9` | Kick, snare, hat |

The **grid** button snaps new and moved stars and drums to a 16-step bar at 120bpm. **Chromatic** frees everything from the scale. The arrows change the key.

## Run it locally

Open `index.html` in a browser. That's it.

## License

MIT. See [LICENSE](LICENSE).

Made by Henrik Pultz Melbye at [attabird](https://www.attabird.com).
