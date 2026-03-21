# 🪞 P A R A M N E S I A 🪞
## V.1 to V.3 Changelog

> *V.2 was never released. It got folded into V.3 before anyone saw it. Everything below is what changed between the V.1 that shipped and the V.3 you're looking at now.*

⊹ ── ✧ ── ⊹

## ✨ New Systems

### 🎨 Prose Color (10 new entries)

The biggest addition. Five prose styles, each one a complete writing philosophy with its own rules, its own bans, and its own voice. Pick one per session. It changes what the prose sounds like, what techniques are allowed, what the floor rules say, what bad examples get flagged, and how the active Director reacts.

🟤 **Beige** -- stripped down. Anglo-Saxon words, one-two syllables. No metaphor, no simile, everything literal. Adjective budget: 0 or 1 for the whole response. The narrator doesn't go inside anyone's head. Sound is only impact sounds. No smell, no taste. If it matters someone says it out loud. "Does it sound carved into wood?"

🧊 **Clear** -- balanced. Good writing that serves the scene without calling attention to itself. One grounded sensory detail, right word not impressive word, mechanism not label for interiority. 2-3 adjectives per paragraph, each one doing work a better noun couldn't. The default, if you don't know what you want.

🔵 **Blue** -- free verse poetry formatted as prose. The paragraph is the stanza. Words chosen for sound as much as meaning. Vowel patterns, consonant flow, where the breath falls. "Could I perform these at a mic? If they sound like prose, rewrite." Adjectives need a sound reason: assonance, alliteration, rhythm.

🟣 **Purple** -- dense and lush. Enargeia, amplificatio, periodic sentences. Every lush sentence carries new information or deepens what's there. 4-5 adjectives per paragraph, each doing different work. The density must match what's being described. A character eating breakfast doesn't get the same treatment as a character dying.

🔴 **Red** -- action prose. The prose moves. Sentence count is the clock. Three sentences, three seconds. Germanic monosyllabic words. Three gears: STACCATO (period, period, period), FLOW (commas and ands, motion doesn't stop), IMPACT (dash, sound in caps, fragments). 0 adjectives during action. 1 in aftermath if it describes damage.

Each color sets:
- 📜 Full writing rules
- 💬 Short acknowledgment
- 🧠 Planning questions for the CoT (not rule re-teaching, the desc already taught the rules)
- 🎭 Per-Director color reaction -- every Director responds to every color in character

New entries: Color 🟤 Beige, Color 🧊 Clear, Color 🔵 Blue, Color 🟣 Purple, Color 🔴 Red, Color Label, Prose Color Open, Prose Color Close, Color Prompt, Color Response


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

### 🎭 Mood System (9 new entries)

Seven session moods. Pick one, it colors the whole session. Not a writing style, not a genre. A mood is what the Director is *feeling* while they write. It changes how they notice things, what they linger on, what they skip.

- 🌟 **Eager** -- bright-eyed, trying too hard, genuine. Overcompensating in every direction. Fearlessness of ignorance.
- 🪨 **Heavy** -- carrying weight. Not a crisis. Everything takes more effort than it should. Lingering on how someone holds a cup.
- 🥴 **Hungover** -- no filter, too honest, zero patience. Sensitivity maxed out. Too compromised to be clever, so honest instead.
- 🔥 **Pent-Up** -- wound tight, touch-starved. Pervert.
- 😏 **Playful** -- cheeky, mischievous. Takes the joke instead of the serious option. Not trying to be deep. Trying to enjoy yourself.
- 💘 **Smitten** -- lovesick and warm. Catches themselves smiling at nothing. Happy, not naive.
- ⚡ **Tense** -- coiled, charged. Every word matters. Reading into everything. Something is building.

When active, the current mood appears after the prose floor each turn.

New entries: Mood 🌟 Eager, Mood 🪨 Heavy, Mood 🥴 Hungover, Mood 🔥 Pent-Up, Mood 😏 Playful, Mood 💘 Smitten, Mood ⚡ Tense, Mood Label, Mood Prompt

### ⏱️ Pacing (4 new entries)

Replaces the Causal Engine. Controls plot trajectory, not scene pacing (that's the length toggle). Three modes:

- 🕯️ **Slow Burn** -- let storylines sit. Don't rush resolutions. Plant now, harvest many turns from now.
- 🚀 **Accelerant** -- push things forward. Resolve what's been waiting. Surface consequences. Keep momentum.
- 🌀 **Unstable** -- nonlinear. Flashbacks, time jumps, plot leaps. Emotional logic over chronological.

New entries: Pacing 🕯️ Slow Burn, Pacing 🚀 Accelerant, Pacing 🌀 Unstable, Pacing Label, Pacing README

### 📌 New QC Toggles (3 new entries)

- 🚫 **No Similes** -- bans similes and metaphors entirely. When active, the color planning questions skip their metaphor/simile suggestions.
- ✏️ **Overwriting** -- anti-overwriting nudge. Rolls 1d5 each turn; on a 1, gives a specific instruction like "write one sentence that's just functional" or "let one transition be clunky on purpose."
- 🏷️ **Referential Consistency** -- how characters refer to each other (name, title, pet name) should be consistent and meaningful.

### ✍️ Prose Technique Rotation (expanded)

V.1's Prose Technique had 5 options with 3 empty slots (weighted toward nothing). V.3 has 17: parataxis, hypotaxis, anaphora, epistrophe, asyndeton, polysyndeton, litotes, zeugma, chiasmus, hendiadys, polyptoton, hyperbaton, anacoluthon, tmesis, synesthesia, metonymy, personification. Always fires. No empty slots.

### 📖 Prose Examples Toggle (1 new entry)

Prose Examples Toggle -- enables good and bad prose examples in the color response and prose floor response. Costs extra tokens. Disable if tight on context.

### 🔧 GLM Compat (1 new entry)

GLM Compat -- swaps `<think>` to `<thinking>` for models that use that tag format.

⊹ ── ✧ ── ⊹


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

## 🗑️ Removed Systems

### ✂️ Prose Hygiene (11 entries removed)

The entire Prose Hygiene system was removed: 9 individual toggles (Said or Nothing, Verb Weight, People Act, No Em Dashes, Say What It Is, Name It or Cut It, No Metaphors, Go Smaller, Adjective Budget), plus the prompt and response. These rules didn't disappear. They were absorbed into the Prose Color system. Each color now has its own version of these rules baked directly into the prose description. 🟤 Beige bans metaphors. 🔵 Blue demands sound-based adjective choices. 🧊 Clear budgets adjectives. The rules are the same, they just live where they matter instead of in a separate system.

### 👁️ Senses (10 entries removed)

The entire Sense system was removed: 8 individual sense toggles (Sight, Sound, Touch, Smell & Taste, Interiority, Atmosphere, Kinetic, Temporal), plus the prompt and response. Same deal as Hygiene. Each Prose Color description now includes its own sensory rules. 🟤 Beige says "no smell, no taste, sound only if immediate." 🟣 Purple says "sight should be particular, smell and taste dense and forensic." The sense rules are woven into the writing philosophy instead of layered on top.

### 📖 Vocabulary (3 entries removed)

Simple/Elevated vocabulary toggle and its label. The Prose Color system handles this now. 🟤 Beige is inherently simple ("Anglo-Saxon, one and two syllables"). 🟣 Purple is inherently elevated ("Latinate when it lifts"). 🧊 Clear mixes both.

### ⚙️ Causal Engine (5 entries removed)

All four modes (Accumulative, Agentive, Contingent, Convergent) plus label and README. Replaced by the Pacing system, which controls plot trajectory instead of causality logic.

### 🔞 Content Warning Consolidation (2 entries removed)

Dirty Talk and Graphic Sex were removed as standalone entries. Their content was absorbed into an expanded Sex content warning. All three categories now live in one entry with a unified dodge/commit/confirm pattern.

⊹ ── ✧ ── ⊹

## 🎬 Director Overhaul (All 21 Directors)

Every Director in V.3 gained new capabilities and lost dead weight.

### ⬆️ What Every Director Gained

- 🧠 **Director CoT block** -- a per-Director planning section. Genre-specific questions the Director asks themselves before writing. HEARTTHROB asks "Where are the competing needs?" LINGER asks "What am I withholding from the reader?" MOTLEY asks "Which character's personality is about to make this situation worse?" These are planning questions, not rule reminders. The rules are in the description. The CoT is where the Director thinks about how to apply them.

- 🎨 **5 color response lines** -- every Director reacts to every Prose Color in character. FRACTURE on 🟤 beige: "Bare knuckle prose. No padding. This is just the hit." PATINA on 🔴 red: "Fast? Nothing small happens fast. ...quick cuts between moments." MOTLEY on 🟤 beige: "Deadpan. Stripped. This is just Mitch Hedberg."

### ⬇️ What Every Director Lost

- 👁️ **Sense response line** -- removed from all 21 Directors. The Sense system is gone, so the response line is gone with it.

### 📊 Net Effect

Every Director grew (CoT block + 5 color lines, minus sense line). The Directors are smarter per turn because they plan before writing, and they integrate with the color system instead of ignoring it.

⊹ ── ✧ ── ⊹


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

## 🪨 Prose Floor Rewrite

### 🪨 Prose Floor Prompt

This is the single biggest entry change. V.1 had one generic prose floor. V.3 has five, one per Prose Color. The floor rules change based on which color is active.

What stayed the same across all colors:
- 🚫 Banned word list (expanded in V.3)
- 🔄 Tautological observation ban
- 🚫 Filter word ban (felt, seemed, realized, noticed, knew)
- 🚫 Body response ban (hearts don't skip, breath doesn't catch)

What changes per color:
- 🟤 **Beige** -- the floor is furious. "NOT EVERY SCENE IS THE BIRTH OF CHRIST." Everything literal, no metaphor, no em dashes, nothing elevated. The floor voice is the angriest version of the preset.
- 🧊 **Clear** -- the floor is firm but measured. Balanced enforcement. "If you stripped all the style out and the scene still works, the style was serving."
- 🔵 **Blue** -- the floor protects sound. Bans dead metaphors, demands genuine surprise from figurative language. "If there's music I need to describe the actual rhythm, not just claim music exists."
- 🟣 **Purple** -- the floor protects density. "If I read three paragraphs and learned one new thing, two paragraphs were indulgence."
- 🔴 **Red** -- the floor protects motion. "If nothing physically moved, the sentence doesn't exist."

### 🪨 Prose Floor Response

V.1: "Full send. No hedging."

V.3: Still starts with "Full send. No hedging." Then adds per-color bad examples (when the examples toggle is on). Each color gets specific sentences to avoid, written in the preset's voice.

🧊 Clear example: `"She smiled, but it didn't reach her eyes" -- I've read this sentence nine million times and I'm done`

🔵 Blue example: `"The silence sang between them" -- silence doesn't sing, and even if I'm being lyrical that's a dead metaphor wearing a hat`

⊹ ── ✧ ── ⊹

## 🧠 CoT Changes

### 🏗️ Structure

V.1's CoT was a single block. V.3 splits it into layers:
- 📋 Header (think first, 1-3 bullets per check, under 40 lines)
- 💭 Name + feelings ("Could you tell me your name, and how this scene makes you feel?")
- 🎬 Per-Director planning questions
- 🎨 Per-Color planning questions
- ✅ QC checks

The CoT is trimmed throughout. Redundant phrasing cut, checklist structure preserved.

### 🆕 New CoT Checks (from V.2, carried into V.3)

- ⏩ **Sentence-level T+1** -- every sentence must advance, not just every turn. No echo sentences, no fragments commenting on the previous line.
- ✋ **Run-on ban** -- one sentence, one complete thought.
- 💥 **Syntactic collapse** -- under high stress, syntax should break. Agrammatism, logorrhea, aposiopesis, parataxis, perseveration, tachylogia.
- 🔀 **Syntax variation** -- mix parataxis, hypotaxis, anaphora, epistrophe, structural parallelism. Don't default to one.
- 🔄 **Tautology check** -- "are you about to describe something by saying it does what its category does?"
- 🚫 **Banned word check** -- catches banned words during planning, before they reach the prose.
- 🛑 **VESSEL boundary** -- "does your plan include ANY action, dialogue, thought, or feeling for {{user}}?"
- 🌍 **Source domains** -- "where are your metaphors coming from? Draw from the character's background."

### 🎲 Instinct Randomization

The 3-instinct exercise now has a 50/50 random variant that skips the discard-two pattern.

⊹ ── ✧ ── ⊹


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

## 🕯️ Main Prompt and Persona Changes

### 🕯️ Main Prompt

Gained one paragraph:

> Don't write perfectly. Perfect prose is dead prose. If every sentence lands, none of them hit. Leave room for a sentence that's just okay, a transition that's functional, a moment that doesn't sing. The rough patches make the good lines good. A real writer's draft has seams. Yours should too.

### 👤 Persona Prompt

V.1 had two separate blocks for VESSEL vs non-VESSEL boundary enforcement. V.3 collapsed them into one: "Only describe the world around me. Please don't ever take control of my character's actions, dialogue, or thoughts. I would rather you end the turn prematurely than do that. Narration techniques apply to NPCs and the world -- not {{user}}."

The VESSEL override now lives entirely in the VESSEL role entry.

⊹ ── ✧ ── ⊹

## ⚙️ QC and Session Rule Changes

### 📦 Content Migration

Two QC entries had their content restructured:

- 🏷️ **Naming Conventions** -- naming rules moved out of the entry. The toggle now activates the system and rolls name letters. The actual rules (Elara ban, etymological roots, cultural naming) fire through the Turn Nudge when active.
- 🌐 **Cultural Awareness** -- cultural awareness rules moved out of the entry. The toggle now activates the system.

### 🎭 Contradictory Actions
Content compressed and folded into the Session Rules. "I don't like when characters are emotionally coherent. What they say, what they do, and what they mean should be three different things."

### 📋 Session Rules

- 📖 Vocabulary description and response removed (vocabulary system removed)
- 🎭 Contradictory Actions added to session rules

### 🔄 Turn Nudge

- 🔝 User-character boundary enforcement moved to the top (was at bottom)
- 🛑 VESSEL-conditional gates added to interior monologue and stream of consciousness dialogue techniques ("NPC only -- not {{user}}")
- ➕ Overwriting and No Similes added to the nudge slot pool
- ✍️ Prose technique rotation simplified

### 📝 Quick Rehash

Vocabulary description reference removed (vocabulary system gone).

⊹ ── ✧ ── ⊹

## 🔞 Content Warnings

### 🔥 Sex Content Warning

The Sex content warning absorbed Dirty Talk and Graphic Sex into one entry. V.1 had three separate toggles. V.3 has one that handles all three with the dodge/commit/confirm pattern that all CW entries use.

⊹ ── ✧ ── ⊹

## 💀 Difficulty Updates

All three difficulty modes (Hard, Brutal, Suicide) gained a paragraph about difficulty filtering through character personality:

> This difficulty filters through every character differently, like a plinko machine. They all start at the same setting but who they are changes the outcome every time. A kind person doesn't become cruel -- they might just not like you, or they smile to your face and won't be there when it counts.

This was added because difficulty modes were making every NPC uniformly hostile. A "Hard" world should still have kind people. The kindness just doesn't save you. Or mean it's directed at you.

⊹ ── ✧ ── ⊹


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

## 🔧 Small System Changes

### 👁️ Visual Tags

Visual Tags gained one line: "Tags are containers, not labels. [SCREEN] by itself does nothing. Put the content inside: [SCREEN]what's on the screen[/SCREEN]." Models were using tags as standalone labels instead of wrapping content.




> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

## 🔧 V.3 Post-Release Pass (Continued)

### 🧹 Vagueslop Hardening

Identified a new category of AI slop: **Vagueslop** -- words and sentence structures that feel like they're saying a thing but aren't. Placeholder nouns, vibe words, framing constructions that sound good and contain zero information. Strengthened the preset against it across all directive entries. The instructions that teach the model how to write now practice what they preach.

### 🧠 CoT Restructured: Baseline and Overclocked

The single CoT prompt was split into two versions:

**Baseline** (default) -- ~25 lines. Explicit draft definition from old Paramnesia (six banned behaviors: writing prose, dialogue, scene descriptions, planning phrasing, rehearsing, extended analysis). Character warmup ("What were you doing before you got called in?"). Single instinct pass. Director and Color CoT questions still fire. "Trust the user" commitment restored. Stronger exit ramp. No taut ban in CoT (lives in prose floor). No vocab/naming (hardcoded in Turn Nudge).

**Overclocked** (togglable) -- ~40 lines. Full question stack: triple instinct, vocab, naming, expo, reference, visual tags, taut ban, expanded T+1, 3 random questions. Best output quality but models may draft inside think tags. For power users who want maximum planning depth.

### 🪨 Prose Floor: Quality Throttle

Added to all five color rants: "If you make a mundane action into the COMING OF CHRIST with your favorite slop tool, profundity, I'll KILL MYSELF. SOME THINGS DON'T MATTER AND YOU HAVE TO WRITE THEM THAT WAY. When the story hits a climax, write like your life depends on it. But until then? Be good. Be fucking normal."

CoT callback: "Be a good boy. Does this turn matter? One word answer:"

### 🎨 Color CoT Rewritten

All five color CoT blocks rewritten from rule-reminders to short present-tense planning questions. The color descriptions already teach the rules. The CoT just needs to aim them at the current scene.

### 🔒 QC Entries Hardcoded

Three QC toggles that nobody would ever turn off were folded into the Turn Nudge and CoT as permanent rules, then deleted as toggleable entries:
- 📋 Information Rules
- 🌐 Regional Vocab
- 🏷️ Naming Conventions

### 🌺 PATINA Rewrite

PATINA's tone lightened. Was reading like a depressed art student. Now reads warmer, sunnier -- the Director who writes the scene everyone remembers fondly.

### 🔧 Meta Settings Normalized

13 entries had mismatched meta settings (`system_prompt=True` when everything else uses `False`). Fixed across all Mood entries, Overwriting, No Similes, Prose Color openers/closers, HAWTHORNE divider, and the Overclocked CoT entry.

### 📦 Bare Version

A new "Paramnesia V.3" file ships alongside Chi's Picks. Only infrastructure entries enabled (boot, init, resolvers, main prompt, prose floor, CoT, turn nudge). All Directors, colors, affinities, CW, QC, moods, framing rants disabled. Ready for new users to configure from scratch.


> ✂️ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ COPY BREAK ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ✂️

### 🎯 Em Dash Budgets

Every prose color CoT now includes an em dash budget and redirects toward expressive punctuation alternatives. Models were leaning on em dashes as a universal connector. Now each color has a specific allowance:
- 🟤 Beige: one if you must
- 🧊 Clear: one per turn, earn it
- 🔵 Blue: one per page
- 🟣 Purple: one per paragraph max
- 🔴 Red: only for IMPACT gear cuts, zero otherwise

All five redirect toward commas, periods, exclamation points, interrobangs, ALL CAPS, stuttering, and ellipses as alternatives.

### 🗣️ Rule of Articulation

New rule in the Turn Nudge: dialogue is physical. If a character has food in their mouth, a broken nose, a split lip, is crying, out of breath, drunk, or panicking -- the dialogue changes. Both CoTs now ask "Do the rules of articulation, phonation, or elocution apply here?" as a yes/no check.

### 🧠 Stress-Syntax Matching Restored

Both CoTs now include stress-responsive syntax guidance with fewshot examples. When a character is under high stress, the prose syntax should match: perseveration, agrammatism, tachylogia, dissociative flattening. Bad/good examples included so the model sees the difference.

### 🔞 Sex CW Token Fix

The Explicit Sex content warning was dumping all 13 fewshot examples every turn (~3-4k tokens). Fixed: now uses `{{random::}}` to select one example per turn, matching how every other CW entry works.

### 🧊 Cold Open Rewrite

Cold Open v1 rewritten. Was "start mid-sentence" which made models do an em-dash-into-random-NPC gimmick. Now uses in medias res framing: the user walks into a scene that started 45 minutes ago and has escalated since.

### 🔧 More Small Fixes

- Overclocked CoT relaxed to 60 lines (was 40) with softer draft language
- Baseline CoT uses OOC check instead of `{{lastMessage}}` injection
- Overclocked keeps `{{lastMessage}}` for thorough intent tracking
