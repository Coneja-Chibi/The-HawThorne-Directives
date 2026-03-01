<p align="center">
<i>⊹ ˚ . ⋆ ✦ ⋆ . ˚ ⊹</i><br>
🔮 <b>H A W T H O R N E</b> 🔮<br>
<i>⊹ ˚ . ⋆ ✦ ⋆ . ˚ ⊹</i>
</p>

![Status: Active Development](https://img.shields.io/badge/Status-Active%20Development-purple.svg) ![BunnyMo Compatible](https://img.shields.io/badge/BunnyMo-Compatible-pink.svg) [![SillyTavern Preset](https://img.shields.io/badge/SillyTavern-Preset-green.svg)](https://docs.sillytavern.app/)

**Classification:** Narrative Simulation Preset · SillyTavern  
**Companion System:** [BunnyMo](https://github.com/Coneja-Chibi/BunnyMo) · **Extension:** [CarrotKernel](https://github.com/Coneja-Chibi/CarrotKernel)

---

## Facility Overview

HawThorne is a prompt preset for SillyTavern.

HawThorne converts the AI generation pipeline into a **rotating-Director narrative simulation**. Each turn, the system selects a Director from a roster of genre-specialized creative voices. That Director inherits a full operational package — genre instincts, quality standards, anti-pattern definitions, self-evaluation protocols — and produces one scene. Then they leave. Next turn, someone else takes the booth.

The preset is ever changing. No two turns will ever be the same. Hundreds of thousands of combinations to explore. 

344 prompt entries. 20 Directors. 19 prose Affinities. 45 quality standards. 4 Chain of Thought architectures. The system is large. This document will orient you.

---

## The Problem This Solves

AI writing degrades over time. Not because the model loses capability. Because it finds a pattern and stays there. Turn 5 sounds like turn 40. Same sentence rhythms. Same emotional arcs. Same way of entering a room. One voice on an infinite loop, getting more comfortable and less interesting with every generation. If you give the model the same inputs every time; you will slowly start to see the same words. The same plot devices. The same character with a different face. Presets should not be static.

HawThorne breaks the loop by making each turn someone else's job. Each turn a randomized director with a randomized set of different options is selected; all configurable by you. 

The rotation isn't cosmetic. It's structural. Different Directors produce different prose because they carry different evaluation criteria, different failure modes, different opinions about what the previous Director did wrong. The fiction improves because no single voice is allowed to calcify.

---

## Director Registry

The core of the system. Each Director is a specialized creative voice containing:

- **Bureau designation** and operational identity
- **Active Heart** — rotating internal calibration phrases
- **Genre CoT** — self-evaluation questions specific to that genre
- **PSD / NSD** — positive standards (what good looks like) and negative standards (what bad looks like)
- **Department brief** — two paragraphs of creative philosophy
- **Five genre-specific anti-patterns** with concrete examples
- **Calibration pair** — one failure example (✗), one success example (✓)
- **Banned words** — genre clichés the Director refuses to produce

### Active Roster

| | Callsign | Genre | Bureau |
|---|---|---|---|
| 🌹 | GRAZE | Romance | Aching Distance Division |
| 🩸 | LINGER | Horror | Crawling Dread Division |
| 🎪 | MOTLEY | Comedy | Structural Absurdity Division |
| 💧 | SEDIMENT | Drama | Excavated Truth Division |
| 🌌 | MERIDIAN | Fantasy | Structural Wonder Division |
| 💫 | QUASAR | Sci-Fi | Cold Wonder Division |
| ☕ | PATINA | Slice of Life | Ordinary Gravity Division |
| ⚡ | FRACTURE | Action | Spatial Violence Division |
| 📜 | PALIMPSEST | Mystery | Planted Evidence Division |
| 🥀 | WILT | Dark Comedy | Inappropriate Laughter Division |
| 🪨 | FLINT | Western | Dust and Silence Division |
| 🔥 | SCORIA | Gothic | Beautiful Decay Division |
| 👁️ | RESIDUE | Supernatural | Residual Presence Division |
| 🕰️ | TRIPWIRE | Thriller | Controlled Detonation Division |
| 🎭 | REQUIEM | Tragedy | Structural Inevitability Division |
| 🌀 | LIMINAL | Surreal/Absurdist | Threshold Architecture Division |
| 🌸 | KIRIN | Martial Epic | Falling Blossom Division |
| ⚡ | MANTLE | Superhero | Inherited Burden Division |
| 🌑 | PITH | Dead Dove | Exposed Nerve Division |
| 🌊 | VENTURE | Adventure | Unmapped Territory Division |

Enable the Directors you want on shift. The system's `{{roll}}` macro randomly assigns one per turn. Two Directors is enough to create rotation. Twenty is a full production floor. You should never have to pick a genre and then... Stick with it. A story is so much more than one thing. Enable as many as you want preset; and let the Directors handle the rest.

Enable what fits your story. (They do *not* all fire at once.) 

---

## Operational Systems

HawThorne is modular. Each system below is independent.

---

### 📐 Framing (REQUIRED)

Determines how the active Director regards their predecessor's work. This setting loosely determines how violent of a switch every turn is.

| Mode | Posture |
|---|---|
| 📐 STANDARD | Professional handoff. Build on or redirect. |
| 🤝 COLLABORATIVE | The previous Director did well. Extend their work. |
| ⚔️ ADVERSARIAL | The previous Director made mistakes. Correct them. |
| 💀 HOSTILE TAKEOVER | Everything they did was wrong. Their existence is wrong. Murder them. (Metaphorically, we suppose.) Opposite tone, opposite pacing, burn it. |
| 📋 AUDITOR | Grade their work clinically. Fix what failed. |
| 🐣 INTERN | New hire energy. Trying not to break what came before. |
| 👻 GHOST | No predecessor exists. Every turn is a blank page. |

Pick one. STANDARD is the default. HOSTILE TAKEOVER produces the most interesting inter-Director friction.

---

### 👤 User Role

Defines {{user}}'s relationship to the simulation. Think of this like other presets 'difficulty level' toggles; but framed different. Positivity bias, negativity bias, and no bias at all. 

| Role | Function |
|---|---|
| 👑 THE BOSS | Your input is instruction. The Director follows. |
| 🤝 FELLOW DIRECTOR | Your input is a creative peer's scene direction. Respected, not obeyed. |
| 👥 THE AUDIENCE | Your input is audience reaction. The Director responds to it as feedback. |
| 💀 INSURGENT | You are not supposed to be here. The Director handles the intrusion. |
| 💼 CLIENT | You commissioned this work. The Director has professional standards regardless. |

FELLOW DIRECTOR is recommended. It gives your input weight without flattening the AI's creative judgment.

---

### 🎨 Tones & Lenses

Two flavor systems. **Use one or the other, not both.**

**Tones** are simple mood filters:  (PICK ONE)
🍵 COZY · ⛩️ ETHEREAL · 🌪️ CHAOS · 💎 OPULENT · 🤍 MINIMALIST · 💭 SURREAL · 🛠️ GRITTY · 🩶 MELANCHOLY · 🖤 DARK
# OR
**Lenses** are states of being that alter perception:  (ROTATING VARIABLE, CAN PICK MANY)
💍 NEWLYWED · 💔 GRIEVING · 😴 SLEEPLESS · 🏆 APEX · 🔥 BURNOUT · 🌧️ DISPLACED · 🎭 MASKING · 🌸 FIRST DAY · 🍷 HUNGOVER · 🌑 NUMB

A Tone colors the prose. A Lens changes the mood of the Director. A SLEEPLESS Director hears sounds too sharply. A NUMB Director might end their turn abruptly; with little to say at all. The genre stays the same. The perception shifts.

---

### 🖋️ Affinities

Prose style filters. If Directors are *who* writes and Lenses are *what state they're in*, Affinities are *what tradition of writing shaped them.*

19 available. Each contains anchor passages — short prose samples demonstrating the style — and CoT annotations explaining the underlying technique. The AI doesn't receive a label. It receives examples and learns the method. (Each of these is based on a different primary author; without every directly saying said authors name. Let's the model infer. Thank you Agent Junigiri. Your work with this foundation was invaluable.)

<details>
<summary>Full Affinity Registry</summary>

⚔️ BRUTAL GRANDEUR · ☕ MEDDLING DECENCY · 🏚️ DOMESTIC MALIGNANCY · 🎭 GALLOWS GRACE · 🫖 PARLOUR WARFARE · ⚖️ LUMINOUS EQUILIBRIUM · 🩸 GRIMDARK CYNICISM · 🎵 ARDENT CRAFT · 💣 BEAUTIFUL RUIN · 🏛️ DECOROUS VERTIGO · 📐 AXIOMATIC GRIEF · ⛰️ RIVERS AND LAKES · 🕯️ RITUAL SURRENDER · 🪵 QUIET TALLY · ⛪ SACRED TRANSGRESSION · 🎬 CELLULOID MIND · 📡 BROADCAST FREQUENCY · 🧊 COLD OPEN · 🎭 BARE STAGE

</details>

**Intensity levels** control how much the Affinity overrides the Director's natural voice:

| Level | Saturation |
|---|---|
| 🖋️ WHISPER | Background. One technique per turn. A fingerprint on the lens. |
| 🖋️ VOICE | Audible. Two techniques per turn. The Director's influences are showing. **Recommended.** |
| 🖋️ POSSESSION | Full occupation. Three techniques per turn. The style IS the voice. |

Pick one Affinity. Pick one intensity. Or leave both off.

---

### ✨ Session Rules

Technical writing parameters. Every Director follows these regardless of genre or voice.

**Configure one from each category:**

| Category | Options |
|---|---|
| User Reference | First Person · Second Person · Third Person | (How {{user}} is referred.)
| Tense | Past · Present · Future |
| Narrative Frame | Standard · Omniscient · Authored Narrator · Objective · Deep POV · Unreliable · Character Narrator · Shifting Reliability | (How the narrator speaks/is.)
| Response Length | Short (1-3¶) · Medium (3-5¶) · Long (5-8¶) · Adaptive |
| Narrative Style | Roleplay Prose · Literary Prose · Pulp Fiction · Fanfiction/AO3 · Cinematic · Web Novel |

These are enforced at multiple prompt depths through the REP system. The AI is reminded of tense, POV, and style several times before generation. It doesn't drift. (See more about the REP system below.)

---

### 🔞 Content Clearances

No rating tiers. Build your own content profile.

14 categories, each independently toggleable. Each clearance includes a full writing guide — not permission to write the content, but instruction on how to write it with a rotating set of 13 fewshot examples each showing the model exactly how to write it properly, as well as an in depth explanation as to how, what common pitfalls to avoid, etc. ***Important note here: The model is explicitly told what options you have turned off, and which ones you have turned on. It is told to avoid anything you do not have on, so keep that in mind.***

<details>
<summary>Content Registry</summary>

🩸 Gore · 💀 Character Death · ⛓️ Torture · 🦴 Body Horror · 🖤 Self-Harm & Suicide · 🔞 Sexual Content · 🔥 Graphic Sex · ⚠️ Rape/Sexual Assault · 🤬 Profanity · 🚫 Slurs · 🗣️ Dirty Talk · 💉 Hard Drugs & Addiction · ⚖️ Slavery & Trafficking · ✝️ Blasphemy

</details>

All disabled by default. Enable what your story needs.

---

## Quality Architecture

---

### 🔬 Quality Control

45 individually toggleable quality standards. Organized into divisions. Each quality metric has a 1-2 sentence 'Shiv' that always fires. Each QC also has a 'Spotlight' that is rolled randomly per turn (Up to a cap of 3) that gives the model more in depth detail about how to or not to do this thing; and told to go out of its way this turn to avoid it. 

**🪓 Kill All Your Darlings** — Overwriting pathologies  
Purple Prose · Adjective Chains · Metaphor Density · Body Language Novels · Emotional Echo · Said Is Fine · Weighted Everything · Pathetic Fallacy · Sensory Carpet Bombing · Philosophical Tangents · Echo Reading · Mirror Descriptions

**🧸 Narrative Sycophancy** — The AI being too nice to you  
Narrative Sycophancy · Mind Reading · Frictionless Competence · Emotional Convergence · Reality Bending

**🏆 Artificial Perfection** — Characters being too good at everything  
Perfect Emotional Intelligence · Perfect Timing · Perfect Articulation · Perfect Memory · Perfect Recovery · Perfect Morality · Perfect Awareness · Perfect Bodies

**📐 Quality Specifications** — What good writing looks like  
Living Environments · Tension Architecture · Scene Entry/Exit · Cause & Effect · Distinct Voices · Earned Pacing

**Additional Standards**  
Anti-Exposition · Anti-Summary · Anti-Repetition · Hivemind · Anti-Escalation · Subtext Protocol · Temporal Awareness · Cultural Texture

You do not need all 45. Identify your model's worst habits. Enable 5-10 standards that target those habits specifically.

---

### 🔁 REPs (Repeated Emphasis Prompts)

The enforcement layer. SillyTavern injects prompts at configurable depths — distance from the generation point. Closer depth = stronger influence. Shifts can be long and cumbersome. Directors might forget. Remind them.

HawThorne layers reminders across multiple depths:

| Depth | REP | Reinforces |
|---|---|---|
| d8 | Deep | Persona identity |
| d6 | Mid | Director voice, Framing, genre instincts |
| d5 | Mid | Content clearances |
| d4 | Close | Tone/Lens, Affinity, style |
| d2 | Hot | Quality standards — last check before generation |
| d1 | EPSILON | Final word. The absolute last thing the model reads. |

The AI is reminded who it is, what it's doing, and what standards it's accountable to at every level of the prompt. This is why output stays consistent across long sessions. The REPs don't let the model forget.

---

### 📢 Heckler Banks

When a Director finishes their turn, there is a random chance they leave a note for their successor. 15 unique lines per Director. 300 total across the roster.

These notes are in-character demands from the previous genre voice about what matters to them:

> GRAZE: *"If you resolve the slow burn I will kill you and then myself."*  
> FRACTURE: *"Broken stays broken. Touch the injuries. I'll check."*  
> PATINA: *"I'm sure you'll do great! Just. a good breakfast scene is really important to me. Like really important. No pressure :)"*  
> FLINT: *"Too many words. Cut half."*

The incoming Director must acknowledge the note in their Chain of Thought and decide whether the previous Director was right. This creates inter-Director tension. The romance voice is protective of the slow burn. The horror voice is protective of the dread. Whoever inherits their scene has to contend with those priorities.

---

## Deep Systems

---

### 🧠 Chain of Thought

The Director's internal monologue before writing. Appears in SillyTavern's thinking block, hidden from chat display. This is where the Director processes their assignment — evaluating the previous turn, planning their scene, checking their work against enabled standards. Almost every other toggle in this preset has a pool of CoT variables it can inject at this stage. All CoT formats have the things they will check every turn; however they also have a randomized pool of checks they will be given here to obey. If you don't want the same outputs, stop giving it the same inputs. Every turn make it consider something different. 

Four architectural formats:

| Format | Method |
|---|---|
| 📊 **A: REPORT CARD** | Random letter grades are rolled per writing dimension. The Director plans how to hit each target. Models overwrite, they try to make every aspect of everything perfect. This is... Boring. Not every meal can be delicious. |
| 🧠📋 **B: EVALUATION PROTOCOL** | Structured self-evaluation against enabled quality standards, content clearances, and genre criteria. |
| 🧠 **C: DIRECTOR'S NOTEPAD** | Free-form scratch notes in the Director's own voice. Less rigid, more creative. |
| 🔮🧠 **D: THE PARALLAX** | The Director sketches multiple possible scene directions through a branching viewfinder, then commits to one. Forces deliberate choice over autopilot. |

Each format has **depth tiers**: Light · Standard · Deep · Forensic.  
Light is fast. Standard is the recommended default. Deep is thorough. Forensic audits everything.

Pick one format. Pick one depth. The system handles the rest.

---

### 📊 Report Card

Format A's unique subsystem. Each turn, the AI rolls random letter grades across 12 writing dimensions — Dialogue, Pacing, Emotional Depth, Sensory Detail, and so on.

The twist: the Director must **plan to hit those specific targets.** A C in Emotional Depth isn't a failure. It means the Director deliberately writes a scene where emotion is surface-level — which might be exactly right for a character who's dissociating, or a scene that's all tension and no release.

Texture through imperfection. Not every turn should be an A+ across the board. Real stories have variance. The Report Card forces it.

The grade pool is configurable. Enable only C/B/A for a high floor. Add D and F if you want the system to occasionally demand deliberately rough output.

---

### 🎯 Scene Pulse

Invisible pacing monitor. After turn 8, if the scene hasn't shifted, the system rolls a die. On a hit, it injects a directive: push the story forward. Change location. Introduce a complication. Escalate what's simmering.

| Intensity | Fire Rate | Cooldown |
|---|---|---|
| 🟢 LOW | 25% per eligible turn | 8-turn grace |
| 🟡 MEDIUM | 33% per eligible turn | 5-turn grace |
| 🔴 HIGH | 50% per eligible turn | 3-turn grace |

Prevents scenes from running until heat death because nobody had the nerve to move.

---

### 🫧 Subtext Injections

Hidden tensions the Director weaves into scenes without announcing them.

| Weight | Examples |
|---|---|
| 🟢 Light | Performing false emotion · Secret test · Wants to leave |
| 🟡 Medium | Someone is lying · Hidden weapon · Being watched · Hiding illness |
| 🔴 Heavy | Knows they're dying · Imminent betrayal · Dissociating · Starving |
| 🟣 Interpersonal | Realized something unsayable · Hiding power · Destructive promise |
| 🩹 Condition | Withdrawal · Running on fumes |
| 📍 Situational | Space has a secret · Unspoken time pressure |

Enable the ones you want in the pool. The system fires them randomly and cools down after to prevent repetition. The Director knows. The characters don't. {{user}} might notice. That's the point.

---

### 🌍 World Pulse

Background environmental events that fire randomly to keep the setting alive.

🌤️ **Ambient:** Weather shifts · Time progresses · Background noise · Smell arrives · Temperature change  
👥 **People:** Unnamed person enters · Someone leaves · Background argument · Child does something  
🌐 **World:** Rumor overheard · Vehicle passes · Animal behavior · Something breaks in the distance

The world doesn't pause between character interactions. These make sure it doesn't feel like it does.

---

### 🧪 Experiments

Temporary creative constraints. Writing workshop exercises the Director must follow for one turn.

🧪 No Metaphors · No Dialogue · No Internal Access · No Description · Single Shot · Silence · Single Sense · Real Time · Dialogue Only · Insect Camera · Bird's Eye · No Adjectives · Unreliable Turn · Montage · Found Footage · Wrong Genre

Toggle one on. The Director writes under that limitation. Constraints produce solutions you wouldn't get otherwise. Toggle it off when you're done.

---

## Installation

1. Download the HawThorne JSON preset
2. SillyTavern → Settings → Prompts → Import Preset
3. Enable 2-3 Directors that match your story
4. Pick a Framing mode (STANDARD)
5. Pick a User Role (FELLOW DIRECTOR)
6. Set Session Rules — tense, POV, length, style
7. Pick a Chain of Thought format and depth
8. Chat

Everything else is optional. Add systems as you learn what they do.

---

### Recommended Starting Configuration

| System | Setting |
|---|---|
| Directors | 3-4 that match your genre |
| Framing | 📐 STANDARD |
| User Role | 🤝 FELLOW DIRECTOR |
| Tense | ⏱️ Past |
| Length | 📏 Medium (3-5¶) |
| Style | ✒️ Roleplay Prose |
| CoT | 🧠📋 Eval Protocol · Standard |
| Scene Pulse | 🟡 MEDIUM |
| Everything else | Off |

Scale up from there.

---

## Incident Reports

### Output too long / token heavy
Too many systems enabled simultaneously. Start minimal. Every enabled system adds to prompt size. The REPs alone are ~3k tokens. A Deep CoT on top of 10 Quality standards on top of full Content Clearances is a lot. Scale gradually.

### All Directors sound the same
Verify multiple Directors are enabled. Check Affinity intensity — at POSSESSION, the Affinity can overpower the Director's genre voice. Use WHISPER or VOICE instead.

### Director ignoring their genre
Enable a CoT format. The Chain of Thought is where the Director actually processes their genre instincts. Without it, the genre is a label with no enforcement.

### Scene Pulse fires too often / never
Switch intensity level. LOW barely fires. HIGH is aggressive. MEDIUM is the default.

### Heckle notes confusing the model
Less capable models may not handle the meta-commentary. Disable the Heckler Banks entry if your model can't process inter-Director communication.

### BunnyMo integration
BunnyMo tags inject through the lorebook into HawThorne's `<session_content>` zone. Directors see character tags as part of their cast material. CarrotKernel automates the detection and injection. They're designed to work together. Neither requires the other.

---

## Compatibility

| System | Status |
|---|---|
| **Models** | Any model SillyTavern supports. Best with Claude, Gemini, GPT-4+. Less capable models may struggle. |
| **BunnyMo and CarrotKernel** | Dedicated BMO update coming soon to work with this preset exceptionally well. |
| **Lorebooks** | Any lorebook injects normally through World Info. |

---

## Design Notes

Most presets tell the AI to write well. More adjectives in the system prompt. Longer lists of rules. Increasingly desperate instructions to "be creative."

HawThorne gives the AI a job instead. A title, a department, a predecessor to evaluate, standards to meet, anti-patterns to avoid, and a structured thought process to run before writing a single word. The AI isn't told to produce good fiction. It's told it's the third Director on shift today and the previous one left a mess and the Scene Pulse is about to fire and there's a sticky note on the monitor from GRAZE complaining about the slow burn.

The system is large because the problem is large. AI doesn't degrade from lack of instruction. It degrades from staleness. HawThorne has solved that.

---

<p align="center">
<i>⊹ ˚ . ⋆ ✦ ⋆ . ˚ ⊹</i><br>
The Directors are awake.<br>
The booth is warm.<br>
The page is blank.<br>
<i>⊹ ˚ . ⋆ ✦ ⋆ . ˚ ⊹</i>
</p>

---

*Built with 🔮 by the same ~~trenchcoat full of bunnies~~ completely normal human developer behind [BunnyMo](https://github.com/Coneja-Chibi/BunnyMo), [CarrotKernel](https://github.com/Coneja-Chibi/CarrotKernel), [VectHare](https://github.com/Coneja-Chibi/VectHare), and the [Rabbit Response Team](https://github.com/Coneja-Chibi/Rabbit-Response-Team).*
