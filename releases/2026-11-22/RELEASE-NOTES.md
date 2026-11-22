**Pack version:** `2026-11-22`. To update: replace the files in `userscripts\` with the ones of this pack and restart
the client; your settings stay. No new files. Everything new is **off** except for YWC, where it matches the author's play.
This is the version shown in the YWC tutorial video.

- **First attack home** (per adventure): the generals of the first attack go home as soon as they are free, so the next
  run can start sooner. On for YWC. A run picked up again after a restart leaves them home.
- **Close at once** (per adventure): when the last camp falls the adventure is closed right away, without waiting for
  recovering generals. On for YWC.
- **No more loose troops travelling home on their own.** After the last attack no general goes to the star any more (the
  star empties a general). Measured on YWC: before, about 2 500 troops travelled home loose; now they come home inside the
  generals.
- **Landing fields are read from the game** for every adventure, shown in the ADVS row with a colour (green = game,
  blue = online, grey = not seen yet). The general "8 landing spots" setting is gone.
- **Every general of the load must be home before a run starts.** DMA reads from the game who is on the way home, when
  they arrive and with what troops, and starts by itself after the last arrival. A general still on another adventure is
  named.
- **Speed-ups that do not stack no longer stop a run.** When the game does not take a travel speed-up because another one
  already runs, DMA says so and starts anyway; with no speed-up running at all it still stops.
- **Control run (author, 2026-11-22):** YWC in 26 minutes, all 20 camps, GHOST1 home after the first attack, the adventure
  closed at once, and **0 loose troops** at the end (3 641 troops came home inside the generals).
- **Zingu's feedback** on YWC (first ghost home, close on completion) is in this pack: thank you.
- See [09-adventures.md](see docs/09-adventures.md in the zip#first-attack-home-close-at-once-landing-fields-from-2026-11-22).

Install: see the README of this repository, or `docs/01-install.md` in the zip.
