# No Figure Left Behind — Primarch Project
## Context file for Claude.ai on mobile

**How to use this file:** You are Claude running on claude.ai (mobile or web). This file gives you enough context to help brainstorm ideas, design new cards, or plan next steps. At the end of your session, write a short "session note" summarising any decisions, new card designs, or convention changes — the user will paste it into Claude Code to continue the work.

---

## What this project is

A fan-made Warhammer 40K archive with three parts:

1. **Edition Tracker** — spreadsheet (`WH40K_No_Figure_Left_Behind.xlsx`) tracking every WH40K unit across editions 1–11 for 25 factions, cross-referenced against BSData repos
2. **Homebrew Cards** — 10th Edition datacards for units removed from 40K without a Legends or canonical replacement, built as HTML → PDF
3. **Website** — public GitHub Pages site listing all cards, combat patrols, and detachments

**Live site:** https://tacowillj.github.io/nofigureleftbehind.github.io/
**GitHub repo:** https://github.com/TacoWillJ/nofigureleftbehind.github.io
**Local project (PC only):** `C:\Users\willi\Desktop\Primarch Project\`

---

## Key design conventions

Follow these when designing new cards or suggesting changes:

- **Miniature-first** — units without a distinct model become detachment/CP rules, not standalone cards
- **BSData-only for edition marks** — only mark YES for editions with BSData repos (2e, 3e, 4e, 7e, 8e, 9e, 10e). 1st/5th/6th = `?` always
- **HB convention** — when a homebrew card exists for a removed unit, flip its 10th/11th Ed column from X → HB
- **M marker** — unit folded into a canonical successor → mark M, note the successor in Notes column
- **L > M** — if a unit has a 10e Legends datasheet, mark L not M
- **Flat 10e pricing** — homebrew cards use flat per-unit costs, not per-weapon ladders. Vehicle/transport add-ons may still be priced separately
- **Legends convention** — if BSData/GW maintains a 10e Legends datasheet, mark L and skip homebrew (reserve for when 11e drops it)

### HH → 10e translation guide
- Breaching (X+) → Lethal Hits
- Critical Hit (5+) / Shred → Devastating Wounds / Sustained Hits
- Impact (S) → bonus attacks on charge
- Eternal Warrior (2) → subtract 1 from Damage
- HH Gambit → select 2 of 3 selectable abilities

### Card stat anchors
- **Primarchs:** T9 W10 M8" Sv2+ OC4 (M12" for winged: Sanguinius, Corvus Corax)
- **LD:** 5+ Loyalist, 6+ Traitor
- **Chapter Master:** T4/W6/Sv2+/4++ — standard Captain: T4/W5/Sv3+/4++
- **Terminator Captain:** T5/W6/Sv2+/4++ M5"
- **Dreadnoughts:** T9-10/W8-11/Sv2+/5++

---

## What's been built

### Homebrew unit cards (130+)
| Category | Count |
|---|---|
| 18 Primarchs (HH → 10e) | 18 |
| SM Forge World named characters (17 chapters) | 23 |
| HH Space Marines — universal units (4 tiers) | 43 |
| HH Mechanicum (Taghmata + Dark Mechanicum) | ~40 |
| T'au — The Eight (8 standalone + 1 CP) | 9 |
| Other factions (AM, SW, DA, Drukhari, Sororitas, etc.) | ~20 |

### Combat Patrols (20 homebrew)
Aeldari ×7, Astra Militarum ×4, Mechanicum ×2, Space Marines ×3, Orks ×2, T'au ×1, Chaos ×1

### Detachments (6)
Path of the Outcast, Ulthwé Strike Force, Mechanised Strike Force, Taghmata Omnissiah, Dark Mechanicum, Legion of the Damned

### Spreadsheet
25 faction tabs, 2e/3e/4e/7e/8e/9e/10e BSData cross-referenced, ~300+ rows with edition columns, HB Card column, and Notes

---

## Open tasks / good next session ideas

**CSM detachments (designed but not built yet):**
- **Hellforged Adept** — lets Imperial FW vehicles (Contemptor, Spartan, Sicarans, Mastodon, Leviathan, etc.) be used in CSM lists with a chaos/daemon-engine rule overlay
- **Lost & The Damned** — R&H mass infantry (Renegade Militia, Marauder, Disciple, Cultists) as IG-pattern infantry with chaos-flavored stratagems

**HH Space Marines (big backlog):**
- Legion-specific units (~70–100 cards across 18 Legions)
- Rites of War / detachments per Legion

**Small fixes:**
- 4 CSM Renegade rows have doubled Notes text — easy cleanup
- Captain Al'Rahem standalone card at 70 pts (split from platoon arithmetic in v3)
- Infantry Platoon v3 playtest — Heavy Weapons Squad at 75 pts may be too generous

**7e audit candidates not yet added:**
- Eldar Corsairs Codex 2015 (10 more units)
- FW AM characters: Colonel 'Snake' Stranski, Maximillian Weisemann

---

## How sessions work

| Where | What happens |
|---|---|
| **Mobile / claude.ai** | Brainstorm card designs, priorities, conventions — use this file for context |
| **PC / Claude Code** | Actually builds things — scripts, PDFs, spreadsheet updates, GitHub pushes |

**End-of-mobile-session:** ask Claude to write a short session note covering decisions made, new card ideas with key stats/abilities, and any convention changes. Paste that note into Claude Code to continue.

---

## Session notes from mobile

*(Claude.ai: append a dated summary here when the user asks for a session note)*
