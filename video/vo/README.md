# Voice over clips

Drop the narration here as `01.mp3` through `10.mp3`, one file per panel,
matching the panel numbers in the film.

| file | panel |
|------|-------|
| `01.mp3` | Where / why |
| `02.mp3` | Marcus |
| `03.mp3` | Two bodies |
| `04.mp3` | One thing between |
| `05.mp3` | Pull back |
| `06.mp3` | Here to there |
| `07.mp3` | Picture of you |
| `08.mp3` | The practice |
| `09.mp3` | It sharpens |
| `10.mp3` | The console |

A panel that has a clip is timed by that clip: its hold becomes the clip's
duration plus the tail, and the audio drives the clock so the panels cannot
drift from the read. A panel with no clip keeps the hold derived from its
narration word count, so the film runs at any stage of recording.

You do not need all ten to start. Record one, drop it in, reload.

## Conventions

- **Format** mp3. Mono is fine, 96 to 128 kbps is plenty for speech.
- **Trim** the head tight. Leave the pause after the line to the `tail`
  setting in the Timing panel, so it stays consistent across panels.
- **Take names** if you want to keep alternates, name them freely and point
  a panel at one with `AUDIO.files` at the top of the script in
  `../index.html`, e.g. `files: { 2: 'marcus-take3.mp3' }`.

## Notes

- The browser will log a 404 for each missing clip. That is expected while
  the set is incomplete, and the Timing panel reports what actually loaded.
- Audio cannot start on page load; a browser needs a click first. "Run
  through" is that click.
- Clips are not inlined into the published artifact. That page falls back to
  derived timing and runs silent.
