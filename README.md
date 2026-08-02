# WebNES (embedded)

This is peteward44's WebNES emulator (https://github.com/peteward44/WebNES),
used here under its MIT license (see LICENSE-WebNES.txt). It's the actual
project you linked, not a rebuild — I pulled the pre-built `gh-pages`
version so there's no compiling required, just static files.

## What's included / excluded

Included: the compiled emulator core (`js/nes.min.js`,
`js/nes.components.min.js`), its stylesheet + jQuery UI theme (`css/`),
post-processing shaders (`shaders/`), and the controller-remap diagram
(`images/`).

Excluded on purpose:
- **The 60+ commercial ROMs** bundled in the original repo (Zelda, Mega
  Man, Contra, Metroid, etc.) — those are copyrighted and I can't
  redistribute them. `index.html` still has the "load ROM" UI, it just
  starts empty instead of pre-listing pirated games.
- **The Game Genie code database** (`js/db/`, ~1500 files) — cheat codes
  keyed to those same commercial ROMs, not needed for basic emulation.
- **Facebook/Twitter/Google+ share widgets** that were in the original
  page — third-party trackers you almost certainly don't want on your site.

## Using it

Drop the whole `webnes-site` folder into your site (or copy `index.html`'s
`<div id="content">...</div>` block plus the `css`, `js`, `shaders`, and
`images` folders into your existing page). Open `index.html` — you'll get
the WebNES UI with an empty ROM list; drag and drop a `.nes` file (or a
zipped one) onto the screen to play it.

Only load ROMs you actually have the rights to — your own dumps,
homebrew, or public-domain titles. Commercial NES ROMs are copyrighted
even though this emulator can run them.

## Controls

Z = A, X = B, C = Select, V = Start, Arrow keys = D-pad. There's also a
control bar (load/reset/play/sound/screenshot/save state/game genie/
keyboard remap) and a shader dropdown for CRT-style post-processing.
