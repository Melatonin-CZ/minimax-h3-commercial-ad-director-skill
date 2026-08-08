# Commercial Advertisement Style Library — Prompt Vocabulary Translations

A commercial ad prompt has two independent dimensions, same pattern as the Instagram-style sister skill:

- **Structure** — the beat-by-beat construction of the spot in time: where the hook sits, how the middle is paced, where and how it closes. This is the equivalent of a format in the Instagram library.
- **Category playbook** — the industry-specific visual language: lighting, grade, shot types, mood. Independent of structure: a Product Hero Showcase can be shot in a Tech/Gadget playbook or a Beauty playbook; a Testimonial can sell software or skincare.

Pick one structure + one category playbook per prompt. Almost every structure (the 6-second bumper is the partial exception) also closes with the **universal end-card/CTA convention** described at the end of this file — treat that as a near-mandatory final beat, not an optional extra.

Real-world commercial ads often run 15-60 seconds; MiniMax H3 caps a single generation at 15 seconds. Don't try to cram a 30s spot's full arc into 15s — instead, either (a) generate the strongest single beat-cluster (hook + one proof beat + CTA) as its own complete 15s piece, or (b) pick a structure that's naturally short (6-second bumper, before/after) and let it run at its native length. Say which approach you're taking when you pick the structure.

Trends current as of August 2026; two are flagged below as fast-moving production trends rather than settled visual conventions.

---

## Quick-pick table — structures

| Structure | Hook | Body pacing | Close |
|---|---|---|---|
| Hook-Problem-Solution-CTA | 1-3s, visual claim or pattern interrupt | Hard cuts every 2-3s, one claim per cut, cutaway to product as resolution | Benefit-repeating CTA text + spoken CTA, often with compact social proof |
| Lifestyle / brand story | Soft, scene-setting, no claim | Slow, dissolve-friendly, emotional-beat-driven, 3-5s+ per shot | Soft logo beat, minimal/no hard sell |
| Product hero showcase | Cold open on product in negative space | Measured, deliberate, 1-3s per shot, turntable/macro rhythm | Hero "final form" hold + wordmark, rarely a hard CTA |
| Testimonial / UGC-style | Hook line spoken to camera | Compressed monologue (natural pauses trimmed) + B-roll cutaways | Spoken CTA reinforced by on-screen caption |
| Before/after or comparison | Establish "before" state | Near-instant transition/reveal at the pivot | Labeled "after" state hold, minimal CTA |
| 6-second bumper | Brand/product visible within 1s | At most 1-2 cuts total, often a single shot | CTA embedded in the one message, not a separate beat |

## Quick-pick table — category playbooks

| Category | Lighting/grade | Shot types | Mood/pacing |
|---|---|---|---|
| Tech / gadget | Multi-backlight rim rig, neutral-cool, high clarity, no stylized LUT | Motion-control turntable, macro focus-pulls across material | Unhurried, confident, restrained |
| Automotive | Golden/blue-hour exterior, teal-and-orange grade | Low-angle tracking hero pass, wheel/interior detail, aerial establishing | Rhythmic, controlled precision |
| Beauty / skincare | Soft even daylight-balanced (~5500K), true-to-color | Macro texture/swatch shots, hand-in-frame application, slow drips/swirls | Sensory, deliberate, ASMR-adjacent |
| Food & beverage | Backlit liquid/steam glow, saturated warmth | Macro condensation/fizz, motion-control tabletop passes, high-speed splash/pour | Sensory, tactile, reveal-timed |
| Fashion / luxury | Directional/dramatic, deep-neutral palette, sparing color | Slow orbit/tracking, extreme fabric close-ups, negative-space wides | Slow, deliberate, editorial |
| FMCG / household | Bright, high-key, high-saturation, category-coded color | Fast in-use demo inserts, ingredient flythroughs, graphic overlays | Upbeat, high cut-rate, jingle-driven |
| Finance / insurance / pharma | Warm, soft, naturalistic, minimalist | Relatable domestic/workplace scenes, medium-close on faces | Measured, narrative-first, VO-led |

---

## Structures in detail

### Hook-Problem-Solution-CTA (direct-response)
**Use for:** performance/DTC ads, app installs, limited-time offers — anything meant to drive an immediate action.
- **Hook (0.0-3.0s):** the visual must carry the tension by itself, not just the voiceover — open on the problem or the pattern-interrupt moment, not on the brand.
- **Body:** cut to a new claim or proof point every 2-3s; every claim gets a cutaway to the product-as-resolution rather than a static "explaining" shot. Camera: handheld or short-throw static setups, fast reframing on each new claim.
- **Close:** CTA text that repeats the benefit, not a generic "Learn More" — pair with urgency language ("today," "now") and, time permitting, compact social proof (a quote, a star rating).
- **On-screen text:** bold caption-style burned-in text reinforcing every spoken claim, native-caption look rather than a polished lower-third.

### Lifestyle / brand story
**Use for:** brand awareness, emotional positioning, aspirational categories where a hard sell would undercut the tone.
- **Camera:** sweeping wide or drone establishing shots for scale, medium shots for relationships between people, close-ups reserved for the emotional peak, frequent POV/over-the-shoulder to place the viewer inside the moment.
- **Pacing:** slow, dissolve-friendly (use a `cross-dissolve` only if explicitly requested per the base guide's cut-type rule; otherwise favor long held shots over frequent cuts), edits land on emotional beats or music swells rather than on claims.
- **On-screen text:** none until a soft brand line/tagline at the very end — no feature callouts.
- **Product presence:** brief, often just a glimpse; the logo/brand arrives last, not as a hard sell.

### Product hero showcase
**Use for:** tech launches, beauty hero products, any category where the object itself is the star.
- **Beat shape:** cold open on the product in negative space → slow rotation/reveal → macro material/detail inserts → a feature-demo beat → a hero "final form" hold → wordmark.
- **Camera:** `Arc Shot` (constant-speed turntable or partial arc) for the reveal, `Static Shot` with a slow `Push In` for macro detail racks, shallow depth of field implied by describing focus pulling across the surface.
- **Pacing:** measured — each shot gets 1-3s to let material/texture actually register, unlike the DR structure's rapid claim-cutting.
- **Close:** a held hero shot plus the wordmark; a hard CTA is rare here — confidence, not urgency, is the tone.

### Testimonial / UGC-style
**Use for:** trust-building, social proof, categories where authenticity outperforms polish.
- **Camera:** handheld, selfie-style or a single fixed "creator" framing; a slight, natural imperfection (minor handheld drift) is deliberate — overproduction reads as "ad" and suppresses trust, so don't ask for a locked-off tripod shot here.
- **Structure:** hook line to camera → brief problem/backstory → discovery/solution moment → proof (result or product-in-use) → spoken CTA reinforced by on-screen caption.
- **Editing feel:** the format simulates trimmed real conversation — write it as continuous natural speech with the throat-clearing and setup already cut, not as a scripted-sounding read.
- **Lighting:** natural/available light only — no studio three-point setup.

### Before/after or comparison
**Use for:** skincare, haircare, cleaning products, fitness, any category where visible proof substitutes for a claim.
- **Structure:** establish the "before" state → a near-instant transition or reveal at the pivot → the "after" state, held.
- **Camera:** the before and after shots must share matched framing and angle — same composition, changed subject — so the comparison reads instantly; describe both shots with identical camera language and only vary the subject's state.
- **On-screen text:** "BEFORE"/"AFTER" labels or a day/week counter overlaying each side, must be legible without sound.
- **Scope discipline:** keep it a single-variable, one-step transformation — resist stacking multiple changes into one comparison.

### 6-second bumper
**Use for:** frequency/reinforcement alongside a longer hero spot, or any single-idea message that doesn't need explanation.
- **Constraint:** one idea only — if the brief has two claims, that's two bumpers, not one crowded one.
- **Camera:** minimal movement, tight framing; essentially one strong static or near-static image/moment, not a narrative arc.
- **Structure:** brand or product visible within the first 1.0s; the CTA is embedded in the core message itself, not a separate closing beat (there usually isn't time for one).
- **On-screen text:** large, bold, legible at a glance — text is doing real work here because duration prevents any spoken narrative from landing.
- **Mood:** bright, high-contrast, and often built around a single humor/twist/unexpected moment, since memorability at 6s depends on one strong beat rather than accumulation.

### Universal end-card / logo-lockup / CTA convention
Applies as the terminal 2.0-5.0s beat of nearly every structure above except the bumper (which embeds its CTA in the single message) and the pure lifestyle/brand-story close (which keeps this beat soft, logo-only, no CTA text).
- **Content:** brand logo/wordmark, one unambiguous CTA action (never more than two), increasingly a repeated benefit or offer line rather than a generic "Learn More."
- **Voice/text match:** if there's a spoken CTA, the on-screen CTA text should repeat it, not introduce new wording — matching reinforces retention.
- **Platform register:** a clean, polished end-slate (logo on a plain or brand-color background) reads correctly for broadcast/YouTube-style delivery; if the request is explicitly for a native social feel (see the Instagram-style sister skill), prefer a text overlay on continuing footage instead of a hard cut-away card.

---

## Category playbooks in detail

**Tech / gadget:** multi-point backlight rig with rim-lighting to define edges while suppressing surface detail elsewhere, soft frontal fill, a signature 45-degree specular highlight on screens/glass. Neutral-to-cool, near-colorless grade, high clarity, no stylized color treatment — restraint reads as premium. Motion-control turntable and macro focus-pulls across material (aluminum, glass) are the default shot vocabulary; reflections should read as practical, not obviously synthetic. Pacing is unhurried and confident — cuts breathe rather than rush.

**Automotive:** golden-hour or blue-hour exterior light to sculpt body contours, avoiding harsh overhead sun; a teal-and-orange or similarly high-end-commercial color grade with the road/asphalt darkened and pushed toward the complementary of the paint color so the vehicle reads as the brightest, most saturated element in frame. Low-angle tracking hero passes, wheel-level detail inserts, and aerial/drone establishing shots for scale are the core shot types. Pacing is rhythmic and music-synced, evoking controlled precision rather than chaos.

**Beauty / skincare:** soft, even, daylight-balanced light (roughly 5500K) for authentic skin tone rather than glossy over-retouched studio light. True-to-color grade — avoid a strong stylized LUT, since texture and shade claims need to stay credible. Macro/probe-lens texture shots (formula swirls, skin-contact close-ups revealing matte/satin/glossy finish) are the primary proof device; hand-in-frame application shots add a narrative, lifestyle-adjacent layer. Pacing is sensory and deliberate, close to ASMR in its unhurried attention to material behavior.

**Food & beverage:** backlighting is the dominant convention — rim/back-light on a liquid pour creates a glow while keeping any label legible, and steam should be backlit so it reads as visible. Saturated, appetizing warmth in the grade. Macro extreme close-ups (condensation beads, fizz, a drip) and motion-control tabletop passes are standard, often paired with a slowed-down "hero moment" (a pour, a splash, a crust breaking) for sensory impact. Pacing is tactile, with cuts timed to land exactly on the reveal moment.

**Fashion / luxury:** directional, deliberately dramatic lighting with real shadow — the opposite of flat, even commercial lighting; light is used to create mystery and depth rather than to simply illuminate. Deep-neutral palette (obsidian, anthracite, bone, raw gold), desaturated overall with sparing, deliberate color accents. Generous negative space (a majority of the frame can be empty) around the subject or product. Slow tracking or orbiting camera moves, extreme close-ups on fabric and stitching, and wide shots built around negative space are the core vocabulary. Pacing is slow and editorial — the goal is desire, not information.

**FMCG / household:** bright, high-key, high-saturation lighting — the near-opposite of the luxury playbook, designed to be immediately eye-catching. Category-coded color (green reads nature/health, blue reads clean/fresh, warm tones read comfort/indulgence). Fast product-in-use demonstration inserts, ingredient or element flythroughs (fabric and flowers for a detergent's freshness cue, grain or produce for a snack's wholesomeness cue), and satisfying swirl/splash/pour transitions are the standard shot vocabulary. Pacing is upbeat and high-cut-rate, often built to feel musical even without an explicit jingle.

**Finance / insurance / pharma:** warm, soft, naturalistic lighting and a minimalist, uncluttered composition — the visual register is reassurance and trust, not spectacle, so camera movement should stay restrained rather than flashy. Real-life, relatable domestic or workplace settings with medium-to-close shots on human faces for empathy. Pacing is measured and narrative-first, built around a simple incident-response-resolution arc rather than feature claims. On-screen text often carries a concise clarifying callout, and this category is one of the few where a small compliance/disclaimer line at the end is a near-universal, expected convention rather than clutter.

---

## Combining structure + category

Write the category playbook's lighting/grade/shot-type language into the shot's opening style clause, and let the structure govern the beat sequencing, cut rhythm, and on-screen text/CTA behavior. For example, a Product Hero Showcase (structure) in the Beauty playbook (category) keeps the showcase's cold-open-then-reveal-then-hero-hold beat shape, but the macro shots are of formula texture and skin contact rather than metal and glass, and the light is soft daylight-balanced rather than a cool rim-light rig. Don't let the category's mood override the structure's pacing — a Hook-Problem-Solution-CTA in the Fashion/Luxury playbook still needs hard cuts every 2-3s in the body, even though luxury's native pacing is slow; the DR structure's urgency and the luxury category's restraint are in real tension, and the prompt should resolve it in the structure's favor since the user asked for a direct-response ad, not a lifestyle piece that merely uses luxury imagery.

The universal end-card convention's content (logo, CTA text, benefit line) doesn't change by category, but its visual treatment should still borrow the category's grade — a Tech/Gadget end-card sits on a clean neutral background, a Fashion/Luxury end-card sits on a deep-neutral background with generous negative space, an FMCG end-card can be brighter and more colorful.
