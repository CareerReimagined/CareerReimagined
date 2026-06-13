v1.0

Career Reimagined: Milestone Progression

Version 1.0 · A Kerbal Space Program career-mode overhaul

Career Reimagined (CareerR) replaces KSP's grindy, repetitive stock contract system with a deliberate, milestone-driven progression. Instead of accepting endless "test part X at altitude Y" contracts, you unlock parts by achieving real spaceflight milestones: reach orbit, land on the Mun, conquer Duna. It's built around a probes-first philosophy — you'll fly uncrewed missions to scout and explore before committing Kerbals to the void. What This Mod Does

Milestone-based part unlocks. Parts are unlocked by completing mission contracts, not by spending science on a sprawling tech tree. Reach a new milestone, get the parts that milestone represents.
A reorganized tech tree. Science is reserved for a small set of optional "capability" upgrades, laid out as clean horizontal category lanes (boosters, fairings, construction, electrical, and so on), each progressing left-to-right by size and capability.
Probes-first career. Tracking Station gives you patched conics and maneuver-planning support early so you can fly capable uncrewed missions from the start. Crewed missions come later, as a deliberate step up.
Conquest missions. Major bodies (the Mun, Minmus, Duna, Eve, Ike, Gilly) culminate in a "Conquest" contract: orbit, land, plant a flag, and return a surface sample. The Apollo moment, formalized.
Bonus & feat challenges. Optional side contracts — collect biome science, set rover speed records, build a crewed station, endure a long-duration mission — reward funds and reputation without disrupting the part economy.
A rebalanced economy. Building upgrade costs, part costs, and contract rewards are tuned for a steady, meaningful progression rather than the stock feast-or-famine.

⚠️ Required Difficulty Setting (READ THIS FIRST)

CareerR needs one difficulty setting to work correctly. Without it, your funds income will be badly inflated by KSP's hardcoded "World Firsts" bonuses, breaking the intended balance.

When you create your career save, set the following in the difficulty options:

Funds Gain Multiplier (rewards): 0.1

Leave Science Gain Multiplier at its default (1.0) — the science economy is balanced to work without any adjustment.

The funds setting is also adjustable mid-game via the in-flight pause menu → Settings → Difficulty Options.

Why just funds? KSP awards hidden "World Firsts" funds and science during flight that cannot be disabled by config.

Funds: World Firsts funds payouts are large (tens of thousands to over a million each) and can't be neutralized any other way, so CareerR sets the Funds Gain Multiplier to 0.1 and scales its own contract reward values up by 10x to compensate. The net effect: you receive the intended funds from CareerR contracts, while the hardcoded World Firsts funds are reduced to a harmless 10%.
Science: World Firsts science payouts are tiny (a few hundred over an entire career), so no multiplier is needed. CareerR simply tunes its own contract science and reduces experiment science to 50% of stock, leaving World Firsts as negligible background noise.

You will notice that contract funds rewards display as 10x larger in Mission Control (e.g. a 50,000-fund reward shows as 500,000). This is intentional — the 0.1 Funds multiplier brings the actual payout back to the intended value. Science rewards display at their true values. Requirements

Required dependencies (install these or the mod will not function):

Module Manager
Contract Configurator
Custom Barn Kit

Recommended / soft dependencies (the mod works without them, but some parts won't appear if absent):

ReStock + ReStock Plus — several spaceplane and structural parts in the tech tree reference ReStock+ parts
Breaking Ground expansion — robotics parts (hinges, rotor shrouds) reference Breaking Ground

Parts from missing mods are simply skipped; no errors occur. Installation

Install the required dependencies above (via CKAN or manually).
Copy the CareerR folder into your GameData directory.
Delete GameData/ModuleManager.ConfigCache, GameData/ModuleManager.ConfigSHA, and GameData/ModuleManager.TechTree if they exist, so Module Manager rebuilds everything from CareerR's patches. (This step is important — without it, the science scaling and tech tree changes may not take effect. The ModuleManager.TechTree file in particular is a separate cached copy of the tech tree; if it isn't deleted, an old tree can persist even after the config is fixed.)
Launch KSP. Create a new career save with the required difficulty settings above.

CareerR is designed for new career saves. Adding it to an in-progress career may produce inconsistent results, because building upgrade levels and accepted contracts are partly baked into the save at creation.

WARNING: I AM NOT A CODER. THIS WAS A FUN SIDE PROJECT I ATTEMPTED BECAUSE I WANTED A MOD LIKE THIS. I DID USE CLAUDE AI TO HELP CODE. THIS IS VIBE CODED AND TESTED BY ONLY ME. IF YOU HAVE SUGGESTIONS ON HOW TO IMPROVE THE CODE-I AM ALL EARS.
