# StitchCast

Hands-free craft studio for following YouTube crochet and knitting tutorials. Mirrors the video for left-handed crafters and lets you control playback by voice, so your hands stay on the yarn.

## Features
- **Left-hand mirror** - flips the video horizontally (remembered between visits)
- **Voice remote** - say `rewind`, `play`, `pause`, `next row`, `previous row`, `slower`, `faster`, `mirror`
- **Wake word (optional)** - require "Stitch" before each command so the tutorial's own narration can't trigger them
- **Row counter** - saved per video, with reset
- **Wrist/elbow tap zones** - big targets for rewind 10s and next row
- **Keep-awake** - screen stays on while the voice remote is active (where supported)
- **Keyboard shortcuts** - `R` rewind, `N` next row, `B` previous row, `M` mirror

## Use
Open `index.html` in a browser (or host it on GitHub Pages), paste a YouTube link, press **Load**. Tap **Voice Remote** and allow the microphone.

## Browser support
Voice needs the Web Speech API: Chrome, Edge, Safari. Firefox has no voice, but everything else works. Needs an internet connection for YouTube.

## Tech
Single `index.html`, vanilla JS, YouTube IFrame API, Web Speech API, localStorage, Screen Wake Lock API. No build step.

## Known limits
- On some phones the OS pauses the video when the mic starts; StitchCast resumes it automatically in the first 1.5 seconds.
- Voice is English (en-US) only.
