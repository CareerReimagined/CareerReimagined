# Career Reimagined: Milestone Progression

**Version 1.1** · A Kerbal Space Program career-mode overhaul

Career Reimagined (CareerR) replaces KSP's grindy, repetitive stock contract system with a deliberate, milestone-driven progression. Instead of accepting endless "test part X at altitude Y" contracts, you unlock parts by achieving real spaceflight milestones: reach orbit, land on the Mun, conquer Duna. It's built around a **probes-first** philosophy — you'll fly uncrewed missions to scout and explore before committing Kerbals to the void.

---

## What This Mod Does

- **Milestone-based part unlocks.** Parts are unlocked by completing mission contracts, not by spending science on a sprawling tech tree. Reach a new milestone, get the parts that milestone represents.
- **An overhauled progression tech tree.** Tech tree is laid out as clean horizontal category lanes (boosters, fairings, construction, electrical, propulsion, and so on), each progressing left-to-right with tiered upgrades you earn as you advance. Science is spent on these capability upgrades — bigger fuel tanks, better solar panels, heavier engines — rather than gating every single part behind a tech node.
- **Probes-first career.** Tracking Station gives you patched conics and maneuver-planning support early so you can fly capable uncrewed missions from the start. Crewed missions unlock once you've demonstrated basic orbital operations — first crewed pod becomes available during the Kerbin orbital phase, before you push out to the Mun and beyond.
- **Conquest missions.** Major bodies (the Mun, Minmus, Duna, Eve, Ike, Gilly) culminate in a "Conquest" contract: orbit, land, plant a flag, and return a surface sample.
- **Bonus & feat challenges.** Optional side contracts — collect biome science, set rover speed records, build a crewed station, endure a long-duration mission — reward funds and reputation without disrupting the part economy.
- **A rebalanced economy.** Building upgrade costs, part costs, and contract rewards are tuned for a steady, meaningful progression rather than the stock feast-or-famine.

---

## ⚠️ Required Difficulty Setting (READ THIS FIRST)

CareerR needs **one** difficulty setting to work correctly. Without it, your funds income will be badly inflated by KSP's hardcoded "World Firsts" bonuses, breaking the intended balance.

When you create your career save, set the following in the difficulty options:

- **Funds Gain Multiplier (rewards): `0.1`**

Leave **Science Gain Multiplier at its default (`1.0`)** — the science economy is balanced to work without any adjustment.

The funds setting is also adjustable mid-game via the in-flight pause menu → Settings → Difficulty Options.

**Why just funds?** KSP awards hidden "World Firsts" funds and science during flight that cannot be disabled by config.

- **Funds:** World Firsts funds payouts are large (tens of thousands to over a million each) and can't be neutralized any other way, so CareerR sets the Funds Gain Multiplier to 0.1 and scales its own contract reward values up by 10x to compensate. The net effect: you receive the intended funds from CareerR contracts, while the hardcoded World Firsts funds are reduced to a harmless 10%.
- **Science:** World Firsts science payouts are tiny (a few hundred over an entire career), so no multiplier is needed. CareerR simply tunes its own contract science and reduces experiment science to 50% of stock, leaving World Firsts as negligible background noise.

You will notice that contract **funds** rewards display as 10x larger in Mission Control (e.g. a 50,000-fund reward shows as 500,000). This is intentional — the 0.1 Funds multiplier brings the actual payout back to the intended value. Science rewards display at their true values.

---

## Requirements

**Required dependencies** (install these or the mod will not function):

- **Module Manager**
- **Contract Configurator**
- **Custom Barn Kit**

**Recommended / soft dependencies** (the mod works without them, but some parts won't appear if absent):

- **ReStock + ReStock Plus** — several spaceplane and structural parts in the tech tree reference ReStock+ parts
- **Breaking Ground expansion** — robotics parts (hinges, rotor shrouds) reference Breaking Ground

Parts from missing mods are simply skipped; no errors occur.

---

## Installation

1. Install the required dependencies above (via CKAN or manually).
2. Copy the `CareerR` folder into your `GameData` directory.
3. **Delete `GameData/ModuleManager.ConfigCache`, `GameData/ModuleManager.ConfigSHA`, and `GameData/ModuleManager.TechTree`** if they exist, so Module Manager rebuilds everything from CareerR's patches. (This step is important — without it, the science scaling and tech tree changes may not take effect. The `ModuleManager.TechTree` file in particular is a separate cached copy of the tech tree; if it isn't deleted, an old tree can persist even after the config is fixed.)
4. Launch KSP. Create a **new career save** with the required difficulty settings above.

> CareerR is designed for new career saves. Adding it to an in-progress career may produce inconsistent results, because building upgrade levels and accepted contracts are partly baked into the save at creation.

---

## How Progression Works

### Main milestone missions

The backbone of the mod. Each completed mission unlocks a batch of parts. The Kerbin progression runs:

First Flight → Reach 18km → Reach 45km → First Suborbital → First Orbit → Survive Re-entry → First Satellite → First Rendezvous → First Docking

From there, the program branches outward to the Mun, Minmus, and the interplanetary bodies. Each moon and planet has its own progression, ending in a Conquest mission for the major bodies.

### Conquest missions

For the Mun, Minmus, Duna, Eve, Ike, and Gilly, the capstone is a Conquest contract requiring you to orbit the body, land on it, plant a flag, and return a surface sample to Kerbin. (Eve's sample requirement allows transmitting instead of returning, in recognition of its brutal ascent.) These can be completed across multiple vessels — launch a separate orbiter, lander, and sample-return craft if you prefer.

### Reconnaissance missions

The outer bodies pair each Conquest with a lighter Reconnaissance mission: simply enter the body's sphere of influence and transmit science home. A flyby is enough — no orbit required. This rewards early scouting before you commit to a full landing campaign.

### Science & the tech tree

Science is **not** the main driver of progression — most parts come from missions. Science is spent on a focused set of optional upgrade nodes (larger fuel tanks, better solar panels, spaceplane parts, and so on), organized into clean category lanes. Each lane progresses left-to-right, and later tiers require the earlier ones.

Where does the science come from? **Main milestone missions** are the primary source — they're tuned to scale meaningfully across the entire progression, from early Kerbin flights up through interplanetary Conquests. **Running experiments** and **bonus contracts** round out your income for finishing the tree. The total science you can earn sits a little above what's needed to unlock every node, so a diligent player will finish the tree comfortably, while a casual player will need to make meaningful choices about which lanes to prioritize.

### Bonus & feat contracts

Optional challenges, sorted into per-body bonus tabs in Mission Control (Kerbin (Bonus), Mun (Bonus), Minmus (Bonus)). Bonus contracts award roughly two-thirds of an equivalent main mission's reward — they're true side content rather than a required part of the progression. Science-collection bonuses (gather data from a specific biome, etc.) supplement your main income. Feat-style bonuses (speed records, crewed stations, long-duration missions) reward funds and reputation. None of them gate essential parts, so you can ignore them or chase them as you like.

---

## Building Upgrades (Custom Barn Kit)

CareerR retunes all the KSC facilities. A few highlights worth knowing:

- **Tracking Station** gives patched conics (the orbit display needed for maneuver planning) from the very first level, with deep-space network range and conic-patch depth scaling up as you upgrade.
- **Mission Control** must reach level 2 to unlock the maneuver-node tool (this is a stock requirement that pairs with the Tracking Station).
- **R&D** level 2 unlocks surface samples and in-flight fuel transfer.
- **Astronaut Complex** level 2 unlocks EVA on other bodies, flag planting, clambering, and EVA parachutes.
- Facility levels use a 6-tier cost ladder, with the visual building tiers arranged so that stock-gated abilities (like surface samples) become available at the first upgrade.

---

## Compatibility Notes

- CareerR disables stock contracts and stock Administration strategies, since progression is mission-driven.
- A compatibility patch is included for KSP Community Fixes' recovery-refund behavior.
- The mod assumes a stock-scale system. It has not been tested with rescale mods (2.5x, JNSQ, RSS) and the contract difficulty/economy balance is tuned for stock scale.

---

## Known Limitations

- **Flag-planting parameters** complete only after the Kerbal re-boards the vessel (a Contract Configurator behavior, not a bug). Plant your flag, then return your Kerbal to the craft for the parameter to register.
- Surface samples require **both** R&D and Astronaut Complex at level 2. Plan your building upgrades before attempting a Conquest mission.
- After editing any CareerR config file, delete the Module Manager cache (see Installation step 3) for changes to take effect.

---

## Credits

- Built on **Contract Configurator** by nightingale, **Custom Barn Kit** by sarbian, and **Module Manager** by sarbian/blowfish.
- Stock-contract-disabling approach adapted from Malah's public-domain StockNoContracts.

---

## Feedback

Found a contract that won't complete, a part in the wrong place, or a balance issue? Reports are welcome — please include your `KSP.log` and a description of what you were doing when the issue occurred.
