# 🪞 P A R A M N E S I A 🪞
### ✧ The H.T. Case Files ✧
V.1 Changelog — The Visual Update

> The directors are all seeing things differently now. 48 visual tags that transform plain bracketed text into fully styled, themed HTML. Every document, screen, sign, and spell in the scene now looks like the thing it is. No extensions. No imports. No setup. It's all in the preset.

⊹ ˚ ⟡ ⋆ ✧ ˚ ◇ ⋆ ⊹ ˚ ✦ ˚ ⊹ ⋆ ◇ ˚ ✧ ⋆ ⟡ ˚ ⊹

🎨 The Visual Tag System

This is a first for SillyTavern presets. Not a handful of HTML templates. Not "the AI writes divs and hopes for the best." This is a complete, 48-tag semantic rendering layer that lives entirely inside the preset file.

The AI writes `[NOTE]don't open the blue door[/NOTE]`. The regex engine transforms it into a handwritten sticky note with cursive font, ruled lines, and a slight rotation. The AI never sees HTML. It never writes CSS. It just wraps text in a tag and the preset handles the rest.

Every tag was hand-designed against an approved visual preview. 24 of the 48 tags use `<style>` blocks with class-based CSS. 15 use `@keyframes` animations. 10 use `::before`/`::after` pseudo-elements. The terminal has CRT scanlines and a moving scan bar. The HUD pulses. The neon sign flickers. The camera feed has a vignette. The runes glow and flicker. None of this was possible with inline styles alone.

**Two rendering modes. Pick one, or pick both.**

🎨 **Tag Reference (REGEX mode)** — The AI gets a reference sheet of every tag. Simple tags just list the `[TAG]text[/TAG]` syntax. Attribute tags show the full format: `[TICKET event="name" venue="place" date="when" gate="X" seat="Y"]`. The model doesn't need to know what a TICKET renders as. It knows what a ticket IS. The regex handles the rest.

✨ **Freeform HTML (FREEFORM mode)** — For when the scene has an object that doesn't match any predefined tag. The AI gets a design language guide: dark palette for digital (`#0d0d0d` to `#1a1a2e`), warm parchment for physical (`#e8d5b0`), typography rules, layout constraints. It builds inline-styled HTML that matches the visual language of the existing tags. Max 2 per response. The story must work if the HTML is stripped. Never decorative. Only real objects.

🎨 All 48 Tags by Category

**Communication (6):** `[PHONE]` · `[CALL]` · `[EMAIL]` · `[LETTER]` · `[NOTE]` · `[CHAT]`
iMessage bubbles, incoming call screens, Gmail-style email, wax-sealed letters, handwritten notes with ruled lines, Discord-style messages with reaction badges.

**Technology (5):** `[TERMINAL]` · `[SCREEN]` · `[ERROR]` · `[HUD]` · `[CAMERA]`
CRT green-phosphor terminals with scanlines and cursor blink. Blue-glow system screens. Red-flash error alerts. Tactical HUDs with corner brackets and pulse animation. Surveillance feeds with REC indicator and vignette overlay.

**Physical World (7):** `[SIGN]` · `[SCROLL]` · `[BOOK]` · `[NEWSPAPER]` · `[POSTER]` · `[GRAVE]` · `[CARVING]`
Wooden signboards with inner borders. Parchment scrolls with edge gradients. Book pages with spine shadows. Newspapers with mastheads and two-column layouts. Event posters. Weathered gravestones. Ancient stone carvings.

**Documents (5):** `[CONTRACT]` · `[RECEIPT]` · `[MAP]` · `[DIARY]` · `[REPORT]`
Formal documents, itemized receipts, exploration maps, personal diary entries, classified field reports.

**Magic (4):** `[RUNE]` · `[SPELL]` · `[PROPHECY]` · `[ENCHANT]`
All four have visible animations. Runes glow and flicker with brightness shifts. Spells pulse and float. Prophecies breathe with scaling and border-color animation. Enchanted items have boosted text-shadow glow.

**Social (2):** `[POST]` · `[PROFILE]`
X/Twitter-style social posts. Profile cards with gradient avatars and bio display.

**Inline (2):** `[WHISPER]` · `[SHOUT]`
Mid-sentence formatting. Whisper fades to italic with reduced opacity. Shout hits bold red with slight scale.

**Misc (14):** `[RADIO]` · `[MUSIC]` · `[NEON]` · `[DREAM]` · `[STICKY]` · `[POLAROID]` · `[TELEGRAM]` · `[VOICEMAIL]` · `[BADGE]` · `[TICKET]` · `[MENU]` · `[WANTED]` · `[SCHEDULE]` · `[COMMENTS]`
Amber radio broadcasts. Centered italic lyrics. Flickering neon signs with 8 color options via CSS variables. Dreamy pastel floaters. Yellow sticky notes with adhesive strips and corner folds. Polaroids with light leak overlays. Uppercase telegrams. Voicemail players with waveform bars. ID badges with barcodes. Event tickets with stub sections. Restaurant menus. Wanted posters with nail dots. Schedules with date headers and badges. Threaded comment sections with avatars.

🎨 Tags with Attributes

Most tags are just `[TAG]text[/TAG]`. These ones accept optional attributes that populate specific slots in the rendered HTML:

`[PHONE from="name"]` · `[CALL from="name"]` · `[EMAIL from="" addr="" to="" subject="" date=""]` · `[LETTER from="name"]` · `[CHAT from="name" react="emoji"]` · `[POST by="name" platform="handle"]` · `[PROFILE name="name"]` · `[VOICEMAIL from="name"]` · `[BADGE name="name"]` · `[NEON color="pink"]` · `[WANTED reward="amount"]` · `[TICKET event="" venue="" date="" gate="" seat=""]` · `[MENU title="name" subtitle="location"]` · `[SCHEDULE date="when" badge="label"]` · `[COMMENTS count="N" sort="method"]`

All attributes are optional. The tag renders fine without them. The AI just includes what makes sense for the scene.

┊ ── ◈ ── ┊

🧠 CoT Visual Check (New)

The CoT Prompt now includes a visual tag check, gated by which mode is active. Three variants:

**REGEX only →** "Visual tags: any physical object in this scene worth a [TAG]? Which tag fits? Don't force one where nothing exists."

**FREEFORM only →** "Visual: anything worth rendering as inline HTML? What is it, what style? Only objects in the fiction. Skip if nothing qualifies."

**BOTH modes →** "Visual: any object worth a [TAG]? Which one? Anything else worth building as custom inline HTML? Pick one approach per object."

Detection uses `vis_has_regex` and `vis_has_freeform` flags. If both toggles are active, `vis_mode` is set to `BOTH` and the combo prompt fires. Local var pattern matches existing Director callsign checks in the CoT.

┊ ── ◈ ── ┊

✂️ Prose Floor Tightened

Anti-slop rules consolidated. Same rules, fewer words. `No [sensation] through/down/in [body part]` collapsed from two separate bullets into one line. `No [tension/silence/words] [hung/crackled/stretched/thickened] in the air` — same treatment. Filtering verbs (felt, seemed, realized, noticed, knew) consolidated into direct instruction. Rhythm instruction folded into existing diction block.

┊ ── ◈ ── ┊

🎯 Turn Nudge Updated

VESSEL role check updated from local var comparison to `getvar` pattern for consistency with the rest of the system.

┊ ── ◈ ── ┊

🔀 Prompt Order Resequenced

`hp_cot_acrostic`: 210 → 180 · `hp_transcript_prompt`: 200 → 212 · `chatHistory`: 201 → 213 · `hp_transmission_end`: 202 → 214

Transcript, Chat History, and Transmission End now fire after Affinity and Prose Floor instead of before them.
