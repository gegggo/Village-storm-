# Village Storm

Browser-based village builder (German title: *Dorfsturm*): build your village, collect resources, train an army, attack camps, and fend off raids.
A single file (`index.html`), no installation, playable offline (only the font loads online, otherwise a fallback font is used). Best played on a phone.

## Languages
Deutsch, English, Español, Français. The game name is translated too: Dorfsturm (DE), Village Storm (EN), Tormenta de la Aldea (ES), Tempête du Village (FR). You choose the language on first launch and it is saved. Change it later with the 🌐 button on the map. Numbers and dates follow the chosen language.
To add another language: add a column to the lines in `I18N` (order `de|en|es|fr`) and to the entries in `TXT` (fixed keys with placeholders such as `{n}`) in `index.html`. New texts with placeholders go into `TXT`, plain texts into `I18N`.

## Buttons on the map
- 🌐 switches the language.
- ✨ toggles the enhanced graphics (shading, shadows, flowers, drifting clouds, background scenery such as huts, trees and rocks). Scenery hides itself wherever a building or wall stands, so it never overlaps. Turn it off if the game runs slowly on your device. The choice is saved.
- 🔔 opens the **Raids** list (with a badge for unread raids).
- The bag button in the side bar (**Collect**) collects everything at once.
- **Side bar:** Collect, Gems (shop), Army, Overview.
- **Bottom dock:** the tabs *Economy*, *Military*, *Fences* with the building cards, and the **⚔ Attack** tab.
- **Top left:** player level, Town Hall level, stars, XP bar and the number of achievements ready to claim (🏆). The badge in the top right of the map shows the current era; tap it for the list of all eras. During a battle the **⏩ 2x** button sits top left of the field.

## Getting started
- Online: GitHub Pages (Settings → Pages → Branch `main`).
- Locally: open `index.html` in your browser.
- Your save lives locally in the browser (localStorage). Another device or browser has its own save. Transfer it with the export code or the backup file (Overview).

## Tutorial

### 1. Goal
Upgrade the Town Hall to level 10, grow your village, collect stars in attacks, and fend off raids. Then start fresh in a new era (Prestige) and go again, stronger.

You start with a Town Hall, one production building for each of the first two resources, an Army Camp, a Barracks, 8 Clubmen and 2 Looters. A 4-step hint at the bottom guides you through the first minutes (collect, build an Arrow Tower, train troops, attack). Old saves skip it.

### 2. Top bar: resources
- **Gold, Iron, Wood, Stone, Gems.** A bar under each value shows how full your storage is. The small number shows the maximum. Tap a value (or **+**) to open the shop.
- **Gems** come from level-ups (+3), achievements, attacks and the Gem Mine. Use gems to trade for resources (10 gems per pack, *Trade Gems* tab in the shop).
  Pack sizes at Town Hall 1: 1,000 Gold, 1,000 Wood, 600 Stone, 300 Iron. They grow with your Town Hall level (+25 % per level).

### 3. Producing resources
- Mines and the Sawmill produce continuously, even while you are offline (up to 8 h).
- A production building's storage is full after about 20 minutes at every level (+5 minutes per fresh start, at most 40), so collect regularly.
- Tap the **bubble** above a building to collect. The "Collect" button takes everything at once.
- If storage is full, nothing more fits ("storage full"). Build **Storage** and upgrade the Town Hall. Stone and Iron only use 60 % of the storage space.
- Storage space = 2,500 + 1,000 per Town Hall level + 2,200 per Storage level (summed over all Storage buildings).
- Tap a building to see what is waiting in its storage. **Overview** shows the real income per minute for every resource. 
- Real output per minute at level 1: Gold Mine and Sawmill 32.4, Quarry 21.6, Iron Mine 12.6, Gem Mine 0.14. It grows linearly with the level (+8 % per Prestige *Production* level).

| Building | Produces |
|---|---|
| Gold Mine | Gold |
| Sawmill | Wood |
| Quarry | Stone |
| Iron Mine | Iron |
| Gem Mine | Gems (slowly). Costs 10 gems to build. Upgrades cost gems too (about 11 for level 2, 275 for level 10). |
| Storage | More storage space |

(Names change with the era, see Eras.)

### 4. Building
- Pick a tab in the bottom dock (*Economy*, *Military*, *Fences*), tap a building card, move the building on the village, then **✔ Save** (or **↶ Undo**). The **Gems** button in the side bar opens the full shop, with the same list plus more.
- Every building has a limit that grows with the **Town Hall level** (table below). Locked buildings show the Town Hall level at which they unlock.
- New buildings get more expensive with each additional one of the same type (+55 % per building already owned). Fences always cost the same.
- Tap a building: upgrade, move (**Move**), or **Demolish** (no refund; if you lose Army Camp space, surplus troops are dismissed).
- **Upgrading:** levels 1 to 10, the price grows with the level. A building can never be higher than the Town Hall, so upgrade the **Town Hall** first. The Town Hall panel also shows what the next level unlocks.
- **Town Hall costs vs. storage:** every Town Hall level can be paid for with a fully built and upgraded storage (Storage gives 2,200 space per level).
- **Fences:** in the Fences tab, cheap, placed instantly by tapping or dragging with your finger. They cannot be upgraded.
- **Shop tabs:** *Build*, *Upgrades* (all upgradable buildings in one list, upgrade directly) and *Trade Gems* (also holds the reset button at the very bottom).
- **Fill with gems:** if a building or upgrade is only missing some resources, a button "Fill with gems" shows the gem price and buys exactly the missing amount.

Building limit by Town Hall level:

| Building | TH1 | TH2 | TH3 | TH4 | TH5 | TH6 | TH7 | TH8 | TH9 | TH10 |
|---|---|---|---|---|---|---|---|---|---|---|
| Gold Mine / Sawmill | 1 | 2 | 3 | 3 | 4 | 5 | 5 | 6 | 6 | 7 |
| Storage / Quarry | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 5 | 5 |
| Iron Mine | – | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 5 |
| Gem Mine | – | – | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 |
| Barracks | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 4 | 4 |
| Army Camp | 1 | 2 | 2 | 3 | 3 | 4 | 5 | 5 | 6 | 6 |
| Smithy | – | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 |
| Arrow Tower | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| Cannon | – | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 5 |
| Ballista | – | – | – | 1 | 1 | 2 | 2 | 3 | 3 | 4 |
| Wizard Tower | – | – | – | – | – | 1 | 1 | 2 | 2 | 3 |
| Fence | 8 | 12 | 16 | 20 | 24 | 30 | 34 | 38 | 42 | 50 |

### 5. Army
- Required: **Barracks** (troops, strength) and **Army Camp** (slots, 12 + 6 per level for each camp).
- In the Army menu (side bar), train or dismiss troops with **+** and **−**. The **Max** button trains as many as your resources and free slots allow. Dismissing a troop gives back its full cost (as far as storage allows).
- Build and upgrade several Army Camps to hold a bigger army.

| Troop | Slots | Cost | Trait |
|---|---|---|---|
| Clubman | 1 | 25 Gold | Melee, attacks the nearest target |
| Archer | 1 | 40 Gold | Ranged, needs Barracks level 2 |
| Brute | 5 | 220 Gold, 80 Wood, 30 Iron | Very tough, hunts defenses first, needs Barracks level 3 |
| Knight | 3 | 140 Gold, 60 Wood, 40 Iron | Armored and fast, needs Barracks level 5 |
| Looter | 1 | 35 Gold | Fast, hunts resource buildings first |

- **Barracks:** the highest level counts. Troop strength (health and damage) is ×(1 + 0.2 per level above 1).
- **Smithy:** the highest level counts. +12 % damage per level for all troops.
- The Army menu and the Overview show the current strength values.
- Troops get new names and their own pixel models in every era (see Eras). Their stats stay the same.

### 6. Attacking
1. Tap **⚔ Attack** in the bottom dock (you need at least one troop). The first camp is free. If you leave a camp without fighting, opening the next one from the **⚔ Attack** tab costs the same as **Search next** (until you finish a battle). The camp view shows the buildings, cannons, towers, the defense damage per second, the possible loot and gems. Red circles show the range of the defenses. Buttons: "Back", "Search next" (costs gold: 20 per Town Hall level plus 2 % of your storage space, so hoarding makes searching more expensive), "⚔ Attack". Tapping the field does not deploy anything yet.
   Camp strength follows your progress within the current Town Hall level: the bigger your army and the further your buildings are upgraded, the harder the camps get (and the more loot they hold). With the same Town Hall, a small army meets weaker camps, usually one level lower, with up to 30 % less health.
   Camps are built tougher than your own village: more Cannons (3 to 11) and Arrow Towers (3 to 13) from Town Hall 4 on, Ballistas from Town Hall 3, Wizard Towers from Town Hall 5, +30 % health and +25 % defense damage. The Town Hall and most defenses sit behind **walls** (see *Enemy camp walls*).
   **Easier camps at Town Hall 1 to 3 (every era):** Cannons 1 / 2 / 2, Arrow Towers 1 / 2 / 3, building health and defense damage ×0.4 / ×0.55 / ×0.7, at most 2 Mines and 2 Sawmills.
2. Press **⚔ Attack**. The troop bar appears. Deploy each troop individually by tapping or dragging anywhere on the field outside the blocked red zone around the camp's buildings. "Back" returns to the camp view.
3. **Auto placement** (two buttons):
   - **🎲 Random:** deploys the army on a random side.
   - **★ Best placement:** simulates 48 variants in advance and picks the best.
4. Both show a **forecast** at the bottom, e.g. "★☆☆ · 35 % destroyed · Victory". Victory from 1 star. The forecast is only an estimate (coarser time steps than the real battle). Calculation takes a few seconds. There is no forecast for troops you place yourself.
5. Troops fight on their own. You have 3 minutes. The battle starts with your first deployed troop. Destroy as much as possible, above all the camp's **Town Hall**.
   **⏩ 2x** (top left of the field, only during a battle) doubles the battle speed; tap again for normal speed.
6. Up to 3 **stars**: 1 for 50 % destroyed, 1 for the Town Hall, 1 for 100 %. Loot is proportional to the destroyed share (and only fits as far as your storage allows). Gems depend on the stars and the camp's level, none for zero stars. Each star gives 15 XP.
7. Troops that survive come home. Lost troops must be trained again. During the battle the bar shows how many troops have **fallen** so far (split by type). Before the battle it shows your gold and the cost of the next search.
8. **Give up** ends a running battle early. Loot and stars so far still count. **Return home** after the result brings you back to the village.

#### Enemy camp walls
- Enemy camps (not your own village) are protected by wooden walls. A **closed wall ring** surrounds the Town Hall and the core defenses (Cannons, Ballistas, Wizard Towers and about half of the Arrow Towers). The ring grows with the camp level (8×8 up to 12×12 fields). Many outer Cannons and Arrow Towers get their own wall ring too.
- At Town Hall 1 to 3 there is a 1 in 5 chance that a camp has **no walls at all**. From Town Hall 4 on, every camp has walls.
- **Melee troops** (Clubman, Brute, Knight, Looter) cannot pass walls. If a wall is in the way, they break it first. If a damaged wall is within 3 fields, they go to it and keep breaking walls there before starting a new one. Farther away, they start a new wall, so groups can open several breaches.
- **Ranged troops** (Archer) shoot over walls and ignore them.
- Walls are **not required** for the result: they do not count for the destroyed share, the stars or the 100 % mark, and they give no loot. Destroying only the buildings is enough.
- The blocked deployment zone also covers wall fields.

### 7. Raids (defense)
- Roughly every 2 hours a raid can hit **your** village, even while you are offline (at most 4 stack up). Each raid only happens with a 90 % chance.
- Your **defense power** comes from Arrow Towers, Cannons, Ballistas, Wizard Towers (stronger with level), troops in the army, and fences (a little each).
- Defense power ≥ attack: **repelled**, +10 XP (+25 XP if it was a close call, i.e. the attack was at least 70 % of your defense).
- Otherwise the enemy plunders 8 to 40 % of your resources (the weaker your defense, the more) and part of the stored production.
- Raid strength rises with your Town Hall level (and with every fresh start) and is rolled between ×0.8 and ×1.6 of its base value for every raid. Grow your defense along with it.
- The **🔔 Raids** button shows your defense power and the last 10 raids (when, defense vs. attack, loot lost). A badge counts unread raids. After you were away, a message sums up what happened.
- Tip: before a long break, spend resources, keep your army, and build towers and cannons.

| Defense | Trait |
|---|---|
| Arrow Tower | Cheap, 1×1, many allowed |
| Cannon | Expensive, 2×2, much stronger, from Town Hall 2 |
| Ballista | 2×2, long range, high damage, from Town Hall 4 |
| Wizard Tower | 2×2, magic orbs, very high damage, from Town Hall 6 |

Enemy camps use the same four defenses (plus walls, see *Enemy camp walls*).

### 8. Progress
- **XP and level:** building, upgrading, attacks, and repelled raids give XP. A level-up gives 3 gems. Reaching level *L* needs 50 · *L* · (*L* − 1) XP in total.
- Tap the **Town Hall** and then **Progress** to see your level, XP per building, the achievements and Prestige.
- **XP per building:** 10 × level (Town Hall 40, Storage 12, Barracks and Smithy 15, Fence 2), once for building and once for every upgrade.
- **Achievements** (Progress menu): one-time gems and XP, e.g. Town Hall level 2/4/6/8/10, 8/20/35 buildings, Gold Mine and Sawmill level 3, 5/25/60 stars, 15 troops, building a Ballista or Wizard Tower, 5 Knights (elite troops), player level 5/10. Ready ones are at the top of the list, claimed ones at the bottom.

### 9. Saving
- Automatically every few seconds and when you leave the page.
- **Export code:** Overview → *Create code*, copy it. Paste it on another device and tap *Load*. The code is compressed.
- **Backup file:** Overview → save to a file (.txt) and load it again later. The game reminds you if there has been no backup for over 24 hours.
- Clearing browser data = save gone. Back up the code or the file first.
- Fallback if the browser blocks localStorage: the save is also kept in the page address (`#…`) and for the current tab only. Bookmark that address or copy the export code.
- Reset: at the very bottom of the *Trade Gems* tab in the shop (double confirmation).
- Imported codes and files are validated and repaired (invalid numbers, building levels limited to 1 to 10, broken Prestige data), so a damaged or edited save does not crash the game.

### 10. Prestige (fresh start)
- Unlocks at Town Hall level 10: **Town Hall → Progress → Prestige → Fresh start** (double confirmation).
- Village, resources and army reset (you start again with the small starter village). You keep gems, stars, level (XP), achievements and your Prestige bonuses.
- You earn **Glory**: 20 + 1 per 2 stars + 2 per player level + 1 per achievement + 5 per earlier fresh start. Spend it on permanent bonuses. The price is the base price × (current level + 1).

| Bonus | Per level | Max level | Base price (Glory) |
|---|---|---|---|
| Production | +8 % | 10 | 2 |
| Build cost | −3 % | 10 | 2 |
| Storage | +10 % | 10 | 2 |
| Loot | +8 % | 10 | 2 |
| Troop strength | +4 % | 10 | 3 |
| Defense | +8 % | 10 | 2 |
| XP | +10 % | 5 | 3 |
| Starting resources | +1,500 Gold and Wood (+750 Stone, +300 Iron) | 5 | 4 |

- Each fresh start raises the **world level**: raids +20 %, enemy camps +15 % health, loot +30 % (each on top of a further +10 % for raids and camps).

## Eras
The game starts in the Stone Age. Every Prestige fresh start (Town Hall level 10) begins the next era: Stone Age → Middle Ages → Industrial Age → Modern Age → Future (stays on Future after that). Each era has its own map colors, its own resource names and its own names for the four production buildings. Internally the resources stay gold, wood, stone and iron, so costs and balance do not change. A badge on the map shows the era; tap it to see all eras (name, resources, unlock by Prestige).

| Era | Gold / Wood / Stone / Iron slot | Mine / Sawmill / Quarry / Iron Mine slot | Smithy |
|---|---|---|---|
| Stone Age | Shells / Wood / Flint / Bones | Cave Camp / Lumberjack / Quarry / Bone Camp | Fire Forge |
| Middle Ages | Gold / Wood / Stone / Iron | Market / Sawmill / Quarry / Smithy | Weaponsmith |
| Industrial Age | Cash / Steel / Energy / Coal | Factory / Steelworks / Power Plant / Coal Mine | Arms Works |
| Modern Age | Capital / Data / Power / Lithium | Bank / Data Center / Solar Park / Lithium Mine | Arms Lab |
| Future | Credits / Biomass / Plasma / Nanites | Quantum Bank / Bio Dome / Fusion Reactor / Nanoforge | Weapons Lab |


Troops get new names and their own pixel models per era too, e.g. Clubman → Soldier → Infantryman → Cyborg, and Sabre-toothed Tiger → Knight → Cavalryman → Special Forces → Plasma Warrior. Their stats stay the same. Names exist in all four languages. The models also show in the troop bar, the Army menu and the list of fallen troops, and they turn to face their direction of travel.

| Era | Clubman slot | Archer slot | Brute slot | Knight slot | Looter slot |
|---|---|---|---|---|---|
| Stone Age | Caveman with club | Spear thrower | Mammoth | Sabre-toothed tiger | Looter with sack |
| Middle Ages | Club bearer with shield | Bowman | Ogre with hammer | Mounted knight | Hooded rogue |
| Industrial Age | Soldier | Rifleman | Tank | Cavalryman | Marauder |
| Modern Age | Infantryman | Sniper | Battle tank | Special forces | Saboteur |
| Future | Cyborg | Laser shooter | Mech | Plasma warrior | Drone (hovers) |

## Balance
Tuning constants live in `BAL` (production and loot multipliers) and in `upCost`, `newCost`, `LIMITS` and the Town Hall cost tables (`TH_G`, `TH_W`, `TH_S`, `TH_I`). Troop stats are in `TROOPS`, troop models in `mkTroop`, camp generation (defense counts, wall rings, strength factors) in `genCamp`, wall behavior in `blockWall` and `step`, defenses in `defStats`, raid strength in `raidPow`, Prestige bonuses in `LEG`. Production is slower and upgrades cost more than in earlier versions, so a first run takes noticeably longer.

## Beginner order
1. Collect the bubbles of your Gold Mine and Sawmill.
2. Build 2 to 3 Arrow Towers (Military tab).
3. Upgrade Storage and the Town Hall. Build more mines and sawmills as the limit grows.
4. Train an army (Army in the side bar), attack your first camp.
5. Collect stars, unlock Cannons, Ballista and Wizard Tower, claim achievements.
6. At Town Hall 10 start fresh and spend your Glory.

## License
MIT, see `LICENSE`.
