# 🔮 [H A W T H O R N E](https://github.com/Coneja-Chibi/The-HawThorne-Directives) 🔮

## V.2 Changelog

> *The facility underwent a full renovation. The Directors have new voices, new instincts, and new toys. The hallways are cleaner but the gripes to the AI are still just as unhinged.*

⊹ ── ✧ ── ⊹

### 🧬 Director Voice System (Every Director)

Every Director now carries a full **personality kit** — 7 new variables per Director across all 21 genres:

- **Genre Anchor** — A pool of 5-10 famous media touchstones (shows, films, games, anime) that the Director writes toward. Randomized per turn so the AI gets a different reference each time.
- **Genre Voice** — Prose mechanics. How the Director's writing *feels*: sentence rhythm, paragraph structure, dialogue ratio, where the detail lives.
- **Genre Opening** — First-beat strategy. How this Director starts a response.
- **Genre REP** — What failure looks like for *this* genre specifically. Not "write better" — genre-specific failure modes.
- **Genre CoT Checks** — Self-evaluation questions unique to each Director, randomized into CoT planning.
- **Genre RC Dimensions** — 2 hyper-specific Report Card dimensions per Director (e.g., HEARTTHROB gets *Proximity Mapping* and *Unspoken Want*; MOTLEY gets *Setup Invisibility* and *Absurd Logic*).
- **Genre RC Priorities** — Which of the 16 universal dimensions matter most for this Director.

This is the biggest change in V.2. The goal: Directors should produce **meaningfully different prose**, not just different editorial philosophy. A MOTLEY turn should *feel* different from a SEDIMENT turn at the sentence level.

### ✨ New Entries

- 💋 **HEARTTHROB** — New Director. Romance but make it messy. Split from GRAZE, which was retired.
- 🫦 **SLICK** — New Director. Built for smut. Anchor pool is famous hentai and ecchi.
- 🔥 **HEATED** — New Tone. Turns the temperature up. Sexual tension, charged atmosphere.
- ⏳ **PENT-UP** — New Lens. Characters are holding something back. Pressure building.
- 🧠 **MINDBROKEN** — New Lens. Characters past the breaking point.
- 🛏️ **MESSY SHEETS** — New Affinity. Prose school for writing that lives in the body.
- 🔗 **Adjective Budget (0-4)** — New QC. Rolls a random budget (0-4 adjectives) each turn. Forces prose density without a full ban.
- 🌐 **Language Selector** — New Session Rule. Type any language and the AI writes in it. Wired into Session Rules display + Final Trigger.
- ⛔ **Anti-Drafting Enforcement** — Baked into all 11 non-Parallax CoT formats. Shorthand-mode enforcement at top and bottom of `<think>` to stop models from drafting prose inside planning. Parallax is exempt (imagination IS the format).
- 🫙 **VESSEL** — New User Role. Full embodiment mode — the AI writes your character's actions, dialogue, and thoughts based on your direction. All "OFF LIMITS" protections conditionally bypass when active.
- 📑 **README entries for every section** — 30+ new README entries explaining how each section works, visible in SillyTavern's prompt list but cost zero tokens.

### 🔧 Fixes

- **Fixed DODGE vs COMMIT bug in Content Warnings** — Community-reported (thanks afinalsin). The label text was inside `{{random::` as the first option in 3 entries (death, sex, slurs), causing the AI to sometimes output the label as content. Labels are now properly outside the random block.
- **Fixed RC grading when RC is off** — Community-reported (thanks Clockwork_Gryphon). REP-Zeta was showing `Previous grade: B. Do better.` unconditionally, causing models to self-grade in `<think>` even when Report Card wasn't selected. Now gated behind `self_grade_lowest` being set.
- **QC/RC conflict resolution** — 12 direct conflicts between QC bans and RC dimensions identified and fixed. When a conflicting QC is enabled (e.g., "Purple Prose" vs. RC Vocabulary dimension), the RC roller now **skips** that dimension entirely. No more conflicting instructions fighting each other.
- **{{trim}} sweep** — Added `{{trim}}` to all 196 entries that were missing it. Every content-bearing entry (332 total) now has trailing trim to prevent blank line leakage.
- **Cleaned marker entries** — 3 CoT format label markers had leftover `{{// comment}}` content. Markers are now properly empty.
- **Section openers emptied** — All section `_open` entries moved their content into dedicated README entries or `_close` entries. Openers are now zero-token structural markers.
- **Content Warning preamble trims** — CW entries had redundant multi-line preambles explaining the CW system. Compressed to single-line format. ~6,189 chars saved.
- **XML open tags added** — 5 entries (`ht_directors_open`, `ht_cot_open`, `ht_final_trigger`, `ht_rep_hot`, `ht_rep_mid`) were missing their XML open tags (`<directors>`, `<plan_format>`, etc.), relying on the AI to infer structure. Tags restored.
- **Random Events variable leak** — Scene trigger text (`scene_trigger_text`) was never reset in `ht_top_init`. Disabling Random Events mid-session left stale "HAWTHORNE DIRECTIVE: push for a transition" text in the variable, causing phantom scene pushes. Now properly cleared every turn.
- **Acrostic reduced to 2 letters** — Experiment was rolling 4 constrained sentences, now rolls 2. Anti-draft CoT check added to all 14 CoT formats.
- **Setting/Sound dim scene awareness** — Setting (⑩) and Sound (⑪) now include a clause: during intimate or focused character scenes, apply to the immediate space only. Prevents "a wolf howled in the distance" during sex scenes.

### ✂️ Removed (Dimensions)

- ❌ **Emotional Restraint (⑫)** — Removed from all RC entries. Redundant with Mess (composure axis) + Subtext (buried feelings). Directors that prioritized it were reassigned: HEARTTHROB→Interiority, WILT→Mess, KIRIN→Subtext, PITH→Mess, SLICK→Body Language.
- ❌ **Ambiguity (⑰)** — Removed from all RC entries. Redundant with Exposition (information delivery) + Subtext (implied meaning). Directors reassigned: QUASAR→Subtext, PALIMPSEST→Subtext, RESIDUE→Exposition, LIMINAL→Exposition.
- Remaining dims renumbered: ⑬→⑫, ⑭→⑬, ⑮→⑭, ⑯→⑮, ⑱→⑯. Universal dim count: 18 → **16** + 2 genre-specific per Director (⑲⑳).

### 🏷️ Renames

- 🎲 **No Mind Reading** → **No Coincidences** — Rewritten from scratch. Now covers the *full* spectrum: NPC psychic reading, model reading user intent, convenient object delivery, scene coincidences. Three rules: NPCs know what they witnessed, objects appear when earned, topics need a reason.
- 🔇 **Echo Reading** → **No Echo** — Cleaner name, sharpened content. Same core rule: don't rephrase what the user already wrote.
- 🌊 **Metaphor Budget** — Expanded from (0-1) to (0-2) range.
- 🌹 **GRAZE** → **HEARTTHROB** — Romance Director renamed and rebuilt.
- 🎯 **Scene Pulse** → **Random Events** — Entire section renamed. Scene Pulse → Event Rate, Scene Pulse Trigger → Event Trigger.
- 🔀 **Pick ONE Affinity** → **AFFINITIES · Pick Many** — Affinities are no longer mutually exclusive.

### ✂️ Removed

- 🎨 **Director Render** / **Lens Render** — Removed. Rendering logic moved into `_close` entries.
- 🚫 **No Adjectives** / **No Metaphors** / **Adjective Ban** / **Metaphor Ban** / **Adjective Budget (0-3)** — Consolidated. Old experiments + old QC bans merged into Adjective Budget (0-4) and Metaphor Budget (0-2).
- 🕵️ **Narration Resolver** — Removed from Session Rules.
- 🌐 **World Pulse Frequency** (Low/Med/High) — Removed. Frequency is now controlled by the Event Rate entries.
- 🧼 **Subtext Close** / **World Pulse Close** — Removed. Close logic absorbed elsewhere.

### 🎲 Report Card Overhaul

- 🔢 **RANGE dimensions now roll actual ranges** — Sentence Length, Scene Speed, Dialogue Ratio, and Humor are typed `[RANGE]` and now roll two dice per turn. The results are sorted and combined as a grade range (e.g., `B-D`). If both dice land the same grade, a single letter is shown. This gives the AI a window to aim for instead of a single target.
- 📊 **CoT dim sampling** — RC CoT formats now probabilistically sample which dims to show each turn instead of listing all 16. Light shows ~3, Standard shows ~6, Deep shows ~10. Genre-specific dims (⑲⑳) always appear. This prevents models from planning 16 strategy slots in `<think>` when they should be writing.

### 🏗️ Architecture Changes

- **Init system** — New `ht_top_init` entry initializes all flag variables, QC conflict flags, and default values in one place. Previously scattered across section openers.
- **Directors Close block** — Now displays the winning Director's **voice kit** (genre_voice, genre_anchor) so the AI sees prose mechanics instructions right after the Director selection.
- **CoT genre integration** — All 14 CoT formats now include conditional blocks for genre-specific RC dimensions, Director CoT checks, and RC priorities.
- **Information Asymmetry Check** — All 14 CoTs now include a "coincidence check" in addition to the knowledge-wall check, targeting the subtler problem of models reading user intent.
- **Anti-drafting language** — New anti-drafting enforcement across all 11 non-Parallax CoT formats. Parallax is exempt.

### 📦 New Preset Versions

- **HawThorne V.2** — 412 entries. Full Director Voice System. All fixes applied.
- **6 V.2 LoadOuts** — Pre-configured loadouts with all sections tuned:
  - 🌐 **General** — 6 Directors, RC Standard, medium length, balanced
  - 🌶️ **Smutty** — SLICK + HEARTTHROB + MOTLEY, EP Standard, Pent-Up + Mindbroken lenses, all sexual content unlocked
  - ⛩️ **Eastern** — KIRIN + Fantasy/Action/Drama/Romance/Adventure, RC Standard, literary prose, RC Explain on
  - 💀 **Dark & Gritty** — LINGER + PITH + SCORIA + TRIPWIRE + REQUIEM, EP Deep, Adversarial frame, heavy content
  - 🧸 **Cozy & Wholesome** — PATINA + HEARTTHROB + MOTLEY + SEDIMENT, RC Light, Collaborative, B/A grades only
  - 🎥 **Epic & Cinematic** — FRACTURE + QUASAR + MERIDIAN + MANTLE + VENTURE, RC Standard, Boss role, long prose

⊹ ── ✧ ── ⊹

-# 🔮 *V.2 — 412 entries. 21 Directors. Every one has a voice now.*
