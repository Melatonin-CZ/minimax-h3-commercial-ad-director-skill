# Frame-Accurate (0.1s) Timeline Methodology — Commercial Advertisement

MiniMax H3 renders at 24 fps, so one frame ≈ 0.0417s and 0.1s ≈ 2.4 frames. As in the sister skills, this 0.1s chart is a private planning artifact compressed into the natural-language shot/camera-motion vocabulary the model actually reads. What's specific to commercial ad content: the hook has to work in less time than even Instagram content typically allows (a direct-response ad's hook is 1.0-3.0s, sometimes under a second for a bumper), and the CTA/end-card beat is close to non-negotiable — an ad that runs out of time before showing the brand or the offer has failed at its actual job, in a way a cinematic or lifestyle clip never quite "fails."

## Two things commercial content needs that the sister skills don't

**1. The CTA/end-card beat is protected time, not leftover time.** For every structure except Product Hero Showcase and Lifestyle/Brand Story (which close softly) and the 6-second bumper (which embeds its CTA in the single message), budget the closing 2.0-5.0s for the end-card *first*, before planning the body. Build the body to fit what's left, not the other way around — the opposite of typical chart-building order, where you'd plan the important middle beat first and let the ending absorb whatever time remains.

**2. Claim-cut rhythm in DR structures is a pacing requirement, not a stylistic choice.** A Hook-Problem-Solution-CTA body needs a new claim or cutaway roughly every 2.0-3.0s — slower than that and the ad stops feeling like a direct-response spot and starts feeling like a lifestyle piece; faster than that and individual claims stop registering. Chart this rhythm explicitly as a repeating beat, not as one long body segment.

## Chart columns (same structure as the sister skills)

| Column | What goes here |
|---|---|
| `t` | Timestamp to 0.1s, e.g. `0.0s`, `1.4s`, `1.4s–2.6s` |
| `shot` | Which `[Shot N]` this falls in |
| `camera` | Camera state: framing, and if a move is active, its type + amplitude + speed |
| `subject` | Product/subject/prop state, on-screen text state |
| `audio` | VO line, claim, music beat, or SFX event |
| `note` | Which structure/category rule this beat is honoring |

## Timing conventions, commercial-tuned

- **DR hook (Hook-Problem-Solution-CTA, or the equivalent moment in a testimonial):** 1.0-3.0s, budgeted first and never absorbed into a longer establishing hold — this is tighter than the Instagram sister skill's 2.0s hook default because performance-ad hooks are conventionally even shorter.
- **DR claim-cut beat:** 2.0-3.0s per claim, each ending on a cutaway to the product as resolution — chart each claim as its own row even if several repeat the same camera grammar.
- **Product Hero Showcase beat:** 1.0-3.0s per shot (reveal, macro detail, feature demo, hero hold) — slower than a DR claim-cut, faster than a Lifestyle establishing shot.
- **Lifestyle/Brand Story beat:** 3.0-5.0s+ per shot, driven by an emotional turn rather than a fixed budget — the longest holds in this system, comparable to the cinematic director-style sister skill's contemplative defaults.
- **Testimonial monologue beat:** written as continuous natural speech, not chopped into many short rows — chart it as one continuous span per narrative stage (hook line, backstory, discovery, proof, CTA) rather than at 0.1s granularity throughout, since the "compression" already happened at the scripting stage, not the shot-cutting stage.
- **Before/after pivot:** the transition itself is near-instantaneous (0.0-0.3s) — chart the before-hold and after-hold as the two real durations, and treat the pivot as a marker, not a beat with its own budget.
- **6-second bumper:** the entire clip is close to one beat — budget brand/product visibility starting at or before 1.0s, and don't plan more than one internal cut.
- **End-card/CTA beat:** 2.0-5.0s, planned first per the rule above; within it, budget at least 1.0s of the logo/CTA actually holding still and legible — a card that's still animating in when the clip ends hasn't done its job.

## Sequencing rule, adapted

The general "last beat gets compressed" risk still applies to everything *before* the end-card, which is exactly why the end-card gets budgeted first here rather than last. The safe shape for a 15-second DR or testimonial-structured clip:

1. **End-card, reserved:** 2.0-5.0s, subtracted from the total before planning anything else.
2. **Hook:** 1.0-3.0s, budgeted in full from what remains.
3. **Body:** whatever remains, filled with claim-cut beats (DR) or the narrative stages (testimonial) at their per-beat budgets above — if the remaining time doesn't fit a clean number of beats, cut a beat rather than compressing all of them evenly.

Product Hero Showcase and Lifestyle/Brand Story don't reserve end-card time the same way (their close is soft, often just a hold-and-wordmark that can flow naturally from the last body beat), so for those two, sequence normally: hook → body → close, same as the sister skills.

## Compression into prompt syntax

Follow the same compression process as the sister skills (group into shots at true cuts, merge continuous camera rows into one motion phrase, merge action rows into observable-behavior sentences, use `[Shot N] At MM:SS.mmm` at real cuts, carry sound into `overall_soundscape`/`non_diegetic_music`), with commercial-specific additions:

1. **On-screen claim text and end-card text both get the base guide's §4.5 exact-verbatim treatment.** A DR ad's burned-in caption reinforcing a spoken claim is not decorative — write the precise string.
2. **When a structure has a spoken CTA, make the on-screen CTA text match it**, per the universal end-card convention — write both the `<d>...</d>` spoken line and the on-screen quoted string with the same wording.
3. **State claim-to-cutaway causality explicitly**: "as she says [claim], the shot cuts to [product resolution]" reads more reliably than describing the claim and the cutaway as two unlinked facts, the same principle as beat-sync in the Instagram sister skill.
