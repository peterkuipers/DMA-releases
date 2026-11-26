**Pack version:** `2026-11-26`. To update: replace the files in `userscripts\` with the ones of this pack and restart
the client; your settings stay. **Six new files:** `transaction-framework.js`, `user_dma_adv_camps_online.js`,
`user_dma_battlesim.js`, `user_dma_camp_solver.js`, `user_dma_mundane_gen.js`, `user_dma_unit_facts.js`. Everything new
is **off** until you use it.

- **Your own Mundane runs exactly as you made it.** Its order, its timings and its arrows in their place, for every
  adventure. DMA no longer re-plans it. A changed plan only comes from *Make my Mundane* or *Save my copy*, after you
  approve it, and is saved as a **new version**; your own stays as it is. (Thanks to Sizzler79.)
- **Everything is checked before a run starts:** the adventure in the star, your own generals, armies that fit their
  generals, every arrow and every speed-up you chose. When something is missing, the ADVS page names it and nothing is
  sent. See [09-adventures.md](09-adventures.md#your-own-mundane-as-written-from-2026-11-26).
  - A general that is travelling, recovering or not on your home island is named, and the run is not promised.
  - A request that comes in while another adventure runs waits in its place until that run ends; then everything is
    checked again for it.
  - When the star cannot be read yet, DMA waits for the next reading instead of saying "none in the star".
  - Runs in a row (*runs in a row* on the adventure) count: the adventures and arrows must be there for all of them.
- **Saving never overwrites.** A second version on the same day gets its own number, e.g. "my author 2026-11-26 (2)".
  Each saved version records that DMA made it and which version it came from.
- **Arrows learn from the game.** Every destroy arrow DMA puts on a camp is noted: did the camp fall? What the game
  shows beats the table from the wiki, and a camp of unknown size gets no arrow (the plan says so).
- **Make my Mundane, three ways.** Every adventure row has three buttons: **Use with my generals** (a chosen Mundane,
  your generals in the author's places), **Optimise for my generals** (the chosen Mundane planned again) and **Make new**
  (from the camps and your generals alone). Pick scenarios — *quick loot*, *most XP*, *fastest*, *fewest losses*,
  *cheapest*, *quickest rebuild*, *multiple runs*, *only arrows* — and a **loss limit** (at most n of one troop type).
  The versions are shown side by side; **Save** adds the one you choose as a new version. See
  [09-adventures.md](09-adventures.md#make-my-mundane-from-2026-11-26).
- **Beta: quick loot and destroy arrows.** DMA works out which camps must fall to finish the adventure (the quest camps
  and what stands in their way) and gives the camps a Small or Big Catapult from your star can take to the arrow. *Only
  arrows* makes a plan without generals. Please test it and send FEEDBACK.
- **Check my versions.** When you get a new general or skill one, DMA tells you which saved versions were made for other
  generals and offers to analyse them again.
- **The battle simulator is in the pack.** Make my Mundane uses it to calculate every camp with your generals.
- **Adventures run more reliably:**
  - an attack only counts once the game has really taken it; an attack the game did not take is sent again;
  - a general attacks from its own spot or close to it, never from far away;
  - when a step gets stuck (a spot that cannot be used, a general that cannot land), DMA finds another spot and goes
    on instead of stopping;
  - after a client restart DMA first visits the adventure, then carries on;
  - an adventure the game still marks as active after its last camp is closed.
- **Troops for a run:** a run that cannot start for want of troops gets those troops trained first; planned adventure
  troops come before topping up your target strength.
- **Quests:** a quest that asks for an adventure has that adventure run by the adventure part of DMA.
- **Gunpowder loot spots** are offered as "GP" in the chat.
