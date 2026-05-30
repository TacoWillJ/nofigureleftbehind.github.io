# No Figure Left Behind — Claude Code README

## Last updated: 30 May 2026

This file is for Claude Code. It contains the current project state,
what was done in the last session, and priority tasks for next session.
For full project context and design conventions read CONTEXT.md first.

-----

## What was done in the last mobile session

### New Recruit catalogue — first build

Created the first homebrew supplement catalogue for New Recruit/BattleScribe.
File is currently at: `catalogues/NFLB - Astra Militarum.cat`

**Key decisions:**

- Supplement approach (not standalone) — inherits from official AM catalogue
  so players get ALL standard AM units PLUS NFLB homebrew in the same army
- Units tagged [NFLB] so players can identify homebrew entries
- Game system ID: `sys-352e-adc2-7639-d6a9`
- Official AM catalogue ID inherited: `b0ae-12a5-c84-ea45`

**Infantry Platoon v3 is in the catalogue:**

- Platoon Command Squad — 40pts flat, 4 models, Issue Orders ability
- Infantry Squads — 55pts flat per 10-model squad, 2 minimum 5 maximum
- Chain of Command platoon ability
- Weight of Numbers platoon ability

### README.md updated

Full public-facing project description written and committed.

### How to add custom source in New Recruit iOS (for reference)

Menu → My Games → green + button → scroll down → GitHub/URL field

-----

## Priority tasks for this session

### PRIORITY 1 — Fix New Recruit discoverability (blocking)

The catalogue is on GitHub but New Recruit cannot find it.

Tested URLs and results:

- `https://github.com/TacoWillJ/nofigureleftbehind.github.io` → Not found
- `https://github.com/TacoWillJ/nofigureleftbehind.github.io/tree/main/catalogues` → Not found
- `https://raw.githubusercontent.com/TacoWillJ/nofigureleftbehind.github.io/main/catalogues/NFLB%20-%20Astra%20Militarum.cat` → No error but nothing loads

The raw file IS accessible and public. The problem is New Recruit needs
a proper index/discovery file to recognise the repo as a valid data source.

**Steps needed:**

1. Read the BSData hosting guide:
   `https://github.com/BSData/catalogue-development/wiki/Hosting-repositories`
1. Move `catalogues/NFLB - Astra Militarum.cat` to the root of the repo
   (New Recruit expects .cat files at root level, not in subfolders)
1. Generate the required index/.bsi file
1. Set up GitHub Actions for auto-generating releases if needed
1. Push everything and confirm the repo appears in New Recruit

### PRIORITY 2 — Verify profile typeIds

The .cat file uses typeIds inferred from BSData XML — verify these against
the actual 10e .gst file at:
`https://github.com/BSData/wh40k-10e/blob/main/Warhammer%2040%2C000.gst`

TypeIds to verify:

- Unit profile typeId: `800f-21d0-4387-c943`
- Weapon profile typeId: `d5f97c0b-9fc9-478d-aa34-a7c414d3f5ce`
- Troops category targetId: `3d52-fccf-a302-troops`
- Infantry category targetId: `96c1-32dc-d9dc-4678`
- Faction: Astra Militarum targetId: `fa45-57e-930e-602b`
- Imperium targetId: `8d6d-8c4b-f475-e74a`

### PRIORITY 3 — Test in New Recruit

Once discoverable, test by:

1. Adding repo URL in New Recruit iOS
1. Building an Astra Militarum list
1. Confirming “Infantry Platoon [NFLB]” appears in Troops alongside standard units
1. Confirming points calculate correctly
1. Confirming faction keywords appear correctly

-----

## Planned future catalogues

Once Infantry Platoon test is confirmed, same supplement pattern for all factions:

```
NFLB - Astra Militarum.cat     Infantry Platoon, Last Chancers, etc.
NFLB - Space Marines.cat        Badab War characters, FW named characters
NFLB - Mechanicum.cat           HH Mechanicum units
NFLB - Horus Heresy.cat         HH Space Marine universal units
NFLB - Tau.cat                  The Eight, FW battlesuits
NFLB - Drukhari.cat             Vect, named characters
NFLB - Chaos.cat                Hellforged Adept, Lost & Damned detachments
```