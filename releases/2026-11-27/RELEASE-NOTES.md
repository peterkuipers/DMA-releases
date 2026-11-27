# Release notes

## Tester pack 2026-11-27

**Pack version:** `2026-11-27`. To update: replace the files in `userscripts\` with the ones of this pack and restart the
client; your settings stay. No new files. The manual now has **pictures** of the console pages, and a table of what is
**ready** and what is **beta** ([README.md](README.md#what-is-ready-and-what-is-beta-pack-2026-11-27)).

- **Four ways to play a Mundane**, each clearly marked. See
  [09-adventures.md](09-adventures.md#four-ways-to-play-a-mundane-from-2026-11-27).
  1. An existing Mundane 1:1 — **ready**.
  2. **New:** an existing Mundane 1:1 with your own generals of the same type — **ready**. Only the generals change: for
     each of the author's generals, the one of yours of that type that carries his army, the most skilled first.
  3. With your own generals of other types too (*Use with my generals*) — **beta**. A camp now keeps the author's own
     attack when your generals of his types win it.
  4. Your own Mundane (*Make new*, *Optimise*) — **beta**.
- **Plans DMA makes keep their generals out of interceptions.**
  - When a general needs another starting spot, DMA picks one whose way is clear of camps that are still standing.
  - Before every step, DMA checks the way against the game's own interception picture.
  - (Found on the First Thief: a general sent past a camp nobody attacked arrived with 3 of his 155 troops.)
- **The battle calculator was checked against published worked attacks.** 31 camps of the settlersonlinewiki guides
  for the First and Second Thief, 11 of them with a Younger Gemini or Nusala wave first. 30 match the guide's losses
  closely; the one open case is named in the known limitations.
- **Barracks queue at the top of the TROOPS page.** Several rows of one unit kind can now wait in the barracks at once, so the
  barracks keep training (and your barracks buffs keep working) while you are away on adventures. You choose:
  - how many rows wait at once;
  - the row size;
  - which unit kinds come first;
  - balanced building (one row of each kind in turn) or your order.

  The choices are at the top of the TROOPS page. The default is unchanged (1 row at a time). See [02-console-tour.md](02-console-tour.md#troops). (Thanks to SirBirk.)
- **The CAP of a resource comes from the game.** The game knows, for your island, every place where a geologist can find a
  deposit of a resource; that depends on your sectors and islands. DMA now takes the CAP from there (on the author's
  island: Stone 9, Granite 8, Iron 22, Marble 13). Before, DMA guessed it from geologists that came back empty, and a find on
  a place it had seen before was wrongly read as "the limit is reached" (Granite fell to 1). Hover over CAP to see the source.
- **Times in an opened resource stand under TIME and are measured.** A searching geologist shows the time left as the game
  gives it. A deposit shows when it is expected to be empty, from its amount and how fast that amount goes down on your
  island (stone, marble and granite included); "—" while nobody works it or it has not been measured for 15 minutes yet.
- **Arrows between the attacks.** In a plan with destroy arrows, each arrow now goes out at its own moment between the
  attacks, as the author timed it, also when a general before it is left out. (Thanks to Sizzler79.)

## Tester pack 2026-11-26

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

## Tester pack 2026-11-22

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
- See [09-adventures.md](09-adventures.md#first-attack-home-close-at-once-landing-fields-from-2026-11-22).

## Tester pack 2026-11-20

**Pack version:** `2026-11-20`. For the five guild testers. To update: replace the files in `userscripts\` with the
ones of this pack (two new files: `user_dma_supply_graph.js`, `user_dma_adventure_manager.js`) and restart the client;
your settings stay. Everything new is **off** until you switch it on.

- **ADVS page rebuilt, top to bottom:** **Run** (adventure, version, *once / keep running / number of runs*, Start/Stop),
  **Speed it up** (travel speed-ups from your star and the Observatory; choices that exclude each other are greyed out;
  every tick kept at once), **All adventures**, the adventures, **Advanced**. Every block folds. A new version made in
  an adventure's row appears in Run by itself. See [09-adventures.md](09-adventures.md#the-advs-page-top-to-bottom-from-2026-11-20).
- **Keep an adventure running:** the adventure manager starts the next run when the last one is home, up to a number of
  runs or until you stop it.
- **Make the next round ready while one fights**, for every adventure.
- **Retreat on interception** is your choice (all adventures); YWC has its own rule and plays your Mundane as it is.
- **Worked example: YWC**, step by step, in [09-adventures.md](09-adventures.md#worked-example-ali-baba-the-young-woodcutter-ywc).
- **Adventure guides** link to settlersonlinewiki.eu.
- **DMA never asks the guild without your permission** (purchases, round trades, star trades are held and reported to you).
- **Granite goes to the mason upgrades first**, and the fastest geologists search granite.
- **Supply map:** DMA knows every way to obtain a good (production, merchant, adventure loot) and forecasts shortages.
- **Tester feedback (Zingu, 2026-11-20).** The switch **Demo** is now called **Demolish**. On the choice screen of a list
  rule (for example *Resources DMA searches for*), **Back to rules** returns to the RULES page instead of the main
  page. See [02-console-tour.md](02-console-tour.md).
- **WORKFLOWS button**, with the first workflow, **Deposit Cycling** (thanks to Zingu): keep the scripts' geologists
  (copper: Gingerbread, Geologist on Vacation, Marathon; iron: Diligent) searching on spots you pick, for the extra loot.
  A mine is demolished only after it is finished, so the deposit vanishes and the spot is free again. Off by default.
  See [03-features.md](03-features.md#workflows-deposit-cycling) and scenario T-11 in [10-testing.md](10-testing.md).
- **Labels for every deposit spot**: all spots of a resource are listed in a fixed order, the same on every home island,
  and you can give each one your own label.
- **Geologist names come from the game.** DMA's own list had most types wrong; the normal copper search now prefers the
  types it meant to prefer, and the Conscientious "always an extra deposit" is credited to the right geologist.

## Tester pack 2026-11-18b (update)

- **FEEDBACK button** on the console: write in your own words what you saw, press **Make report**, paste the text in
  #test-corner and attach the report file it writes. See [07-reporting.md](07-reporting.md).
- Everything else is as in 2026-11-18. To update: replace the files in `userscripts\` with the ones of this pack
  (one new file, `user_dma_report.js`) and restart the client; your settings stay.

## Tester pack 2026-11-18

**Pack version:** `2026-11-18`. For five guild testers (Leroybrown, SirBirk, Sizzler79, Mickepedia and, new, Zingu),
built from `main` after all tests of the gate passed. Everything is still **off** in a new installation.

### New since 2026-11-17

- **A RULES page** in the console with **every** business rule, grouped and filterable; each rule has its own control
  (tick, number with its range, list, text, or a grouped checklist of resources). No setting needs a hand edit of
  `dma-policy.json` any more. ([02-console-tour.md](02-console-tour.md#rules-every-business-rule))
- **The trade-office rules are yours:** the 30 minutes a resource must be short, the 1.5× better than the market price and
  the never-pay list each have their own on/off and value; the never-pay list is a checklist (default Oilseed, Oil). The
  buyer itself stays inert in this pack.
- **The client no longer restarts itself unless you switch that on** (`control.selfRestart.on`, off). When on, a restart
  also needs the stock to stand still: explorers that come back at once are not enough on their own.
- **Adventures:** the five phases are shown in the status and the log; the star method (everything to the star on
  arrival, marshals included; marshals back on the island before closing so every troop is loaded); a load margin for
  versions that reload between waves (`adv.waves.loadMargin`, 25 %); carriers are unloaded before the first wave; a
  run that is resumed sends who is still home; a general whose spot is held attacks from where it stands; troop counts per
  general in every run's record. ([09-adventures.md](09-adventures.md))
- **The author's Bonaberti Business "two waves" Mundane** is in the pack as a shared folder, to analyse against your own
  generals.
- **Troops:** fast barracks (400 % speed) no longer cause false refusals.
- **This manual:** new chapters [09 Adventures](09-adventures.md) and [10 How to test](10-testing.md), and as one PDF.
- **Feedback** goes to the Discord channel **test-corner** ([07-reporting.md](07-reporting.md)).

### Coming in the first update

- **The Mundane generator:** a known adventure (Bonaberti Business first) rebuilt for **your** generals and skills: your
  own generals put in the author's places, every camp simulated again with your skills, the troops in front sized for
  the bad case (not the average) so the expensive units in the back are not lost, and the load with the margin and the
  carriers it needs, written as your own Mundane folder from the ADVS page.
- The trade office buyer as a tick on the RULES page, once it has been proven on a real purchase.

### Known issues and gaps

1. Making a Mundane for **your** generals (re-simulating every camp with your skills) is not in this pack; the
   analysis of a shared Mundane is. First update.
2. The trade office buyer does not buy (no confirmation file is shipped).
3. No recommended geologist builds; set skills by hand.
4. The quest manager does not do the guild quest "buff a friend's buildings"; do it by hand.
5. Demolishing and upgrading are irreversible and spend materials: keep **Demo** off for the first days.

## Tester pack 2026-11-17

**Pack version:** `2026-11-17` (written in `pack-manifest.json` as `packVersion`; the module versions are in the same
file, with a checksum per file). For the four guild testers, built from `main` after all tests of the gate passed.

### What is in it

37 script files (`userscripts\`) and this manual (`docs\`). All features are **available** and **all are off**: every
switch of the switch bar, every adventure, the zombie hunt, premium, round, help and star trades, the supply
manager and the trade office buyer (which is, in addition, inert without a confirmation file that is not shipped).

Features: island observation; geologists and explorers; build, upgrade, buff and demolish of mines; chat watcher and
round trades, help trades and star trades; mail loot collecting; quest book; event manager; troops; zombie hunt; premium;
adventures with loot spots; supply; the value list; the transactions page. See [03-features.md](03-features.md).

### New since the previous pack (what changed for a stranger's island)

- **The author's island is no longer inside the pack.** The geologist preset builds are empty; the guild-chat name
  "Kuipje" is no longer special in round trade and help parsing (the player's own chat reply word and in-game name
  are used); no player name is in the help noise words; the examples in the console are "Joe"; the default explorer
  template is `Daily` (was `Event`); the stale-client restart does nothing while every switch is off.
  (decision 0078, `docs/reviews/2026-11-17-tester-pack-specifics-audit.md`)
- **A fresh installation does nothing.** Verified by a test that loads the whole pack with a new policy and checks that
  nothing acts (`tests/integration/pack-fresh-policy-nothing-acts.test.js`).
- **The pack runs without a developer session.** Nothing depends on files that only a developer's tool writes. See the
  audit page.
- **This manual** is part of the pack (`docs\`), with a checksum per page.

### Known issues and gaps

1. No console control for `premium.setting`, `zombie.auto`, `zombie.generals`, the `supply.*` sub-rules,
   `trade.ask.on`, `trade.rt.ask.*`: set them in `dma-policy.json` ([04-settings-reference.md](04-settings-reference.md)).
2. The trade office buyer does not buy: it needs a confirmation file that is not shipped.
3. No recommended geologist builds; set skills by hand.
4. No adventure templates are supplied.
5. The restart of a stuck client is on by default once any automation is on (`control.staleRestartMin`, 10 minutes).
6. Demolishing and upgrading are irreversible and spend materials: keep **Demo** off for the first days.

### Open decisions for the author

- Whether the trade office should be able to buy in a tester pack at all (now: no).
- Whether the missing console controls (known issue 1) are built before or after the test round.
- Whether the stuck-client restart should default to off in a tester pack.

### How a tester sends findings

See [07-reporting.md](07-reporting.md).
