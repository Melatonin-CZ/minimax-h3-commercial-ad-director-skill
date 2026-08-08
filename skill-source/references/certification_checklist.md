# Master Certification Guide — MiniMax H3 Commercial Ad Prompts

A prompt is "certified" under this system when it satisfies every item below. This guide layers on top of `VIDEO_PROMPT_WRITING_GUIDE_base_en.md` and `VIDEO_PROMPT_WRITING_GUIDE_ref_en.md`, informed by the structure/category vocabulary in `commercial_ad_styles.md` and the timing method in `timeline_methodology.md`.

## Stage 0 — Choose the task type and scope

Confirm the mode (T2VA/I2VA/FL2VA/L2VA, or full-reference mode if the user supplied brand assets — a real product photo, logo, or prior footage to composite). Commercial requests are frequently I2VA (an actual product photo to animate) or full-reference mode (a product shot + a logo asset + maybe a reference ad for pacing). Also confirm scope: is this the full arc of a real-world 30-60s spot compressed into 15s (risky — say so if the brief implies more than 15s can carry), or the strongest single beat-cluster, or a naturally-short structure (bumper, before/after) at its native length? State which approach you're taking.

## Stage 1 — Pick a structure and a category playbook

From `commercial_ad_styles.md`, choose exactly one **structure** (Hook-Problem-Solution-CTA, Lifestyle/Brand Story, Product Hero Showcase, Testimonial/UGC, Before/After, 6-Second Bumper) and exactly one **category playbook** (Tech/Gadget, Automotive, Beauty/Skincare, Food & Beverage, Fashion/Luxury, FMCG/Household, Finance/Insurance/Pharma). Note whether the structure closes with the universal end-card/CTA convention (most do) or closes softly (Lifestyle/Brand Story, Product Hero Showcase) or embeds its CTA in the single message (6-Second Bumper).

## Stage 2 — Build the 0.1s timing chart

Follow `timeline_methodology.md`:

- [ ] For structures that use the universal end-card, that closing beat (2.0-5.0s) is budgeted and reserved *before* the body is planned, not fit in afterward.
- [ ] The hook (1.0-3.0s for DR/testimonial-style structures) is charted as its own deliberate beat.
- [ ] A DR body's claim-cut rhythm is charted explicitly, one row per claim, each 2.0-3.0s.
- [ ] A Product Hero Showcase's beats (reveal, macro, demo, hero hold) are each budgeted 1.0-3.0s.
- [ ] A Testimonial's narrative stages are charted as continuous spans (hook line, backstory, discovery, proof, CTA), not artificially chopped into many short rows.
- [ ] A Before/After pivot is charted as a near-instant marker (0.0-0.3s), with real time budgeted to the before-hold and after-hold on either side.
- [ ] A 6-Second Bumper charts brand/product visibility starting at or before 1.0s and at most one internal cut.
- [ ] The end-card, where used, includes at least 1.0s of the logo/CTA actually holding still and legible, not still animating in when the clip ends.

## Stage 3 — Compress into prompt syntax

- [ ] Shots are grouped only at true cuts; the structure's own cut-count convention is respected (DR: frequent hard cuts; Lifestyle: few, slow; Product Hero: measured; Bumper: at most 1-2 total).
- [ ] Every shot after the first uses `[Shot N] At MM:SS.mmm, ...` matching the chart exactly.
- [ ] Camera motion uses only vocabulary from `VIDEO_PROMPT_WRITING_GUIDE_base_en.md` §4.3.
- [ ] On-screen claim text and end-card text are exact verbatim strings in quotation marks per §4.5 — not paraphrased summaries of what the text should convey.
- [ ] Where the structure has a spoken CTA, the on-screen CTA text and the `<d>...</d>` spoken line match in wording.
- [ ] Claim-to-cutaway causality is stated explicitly ("as she says X, the shot cuts to Y"), not left as two separate unlinked facts.
- [ ] Any speaker (testimonial narrator, VO announcer) uses a stable `(S1)` ID with verbatim `<d>[Language] ...</d>` content per §4.4.
- [ ] `overall_soundscape` and `non_diegetic_music` match the structure's audio convention (DR: often music-under-VO with claim-synced stingers; Lifestyle: music-led, sparse VO; Testimonial: natural room tone, no score or very sparse; FMCG: upbeat/jingle-adjacent; Finance/Insurance: calm, warm, VO-led).
- [ ] The category playbook's lighting/grade/shot-type language appears in the opening style clause and stays consistent across shots.
- [ ] Where the category and structure pull in different directions (e.g. a DR structure in a Luxury playbook), the structure's pacing wins per the combining note in `commercial_ad_styles.md` — the prompt shouldn't quietly drift toward the category's native pacing at the expense of what the user actually asked the ad to do.
- [ ] Finance/Insurance/Pharma prompts include a brief on-screen compliance/disclaimer line if the request implies a regulated claim, since that convention is near-universal in the category.

## Stage 4 — Duration budget check

- [ ] Total charted duration matches the requested duration (5-15s) exactly.
- [ ] For end-card structures, the reserved closing beat is actually present in the final compressed prompt, not lost during compression.
- [ ] If compressing a longer real-world format down to 15s, the chosen beat-cluster is coherent on its own (a hook + one strong proof beat + CTA, not three under-developed claims each getting a third of a real claim's usual time).

## Stage 5 — Structure and category fidelity check

- [ ] Camera behavior matches the chosen structure's entry, not a generic commercial default.
- [ ] Cut count and rhythm match the structure.
- [ ] Lighting, grade, wardrobe/prop/set language matches the chosen category playbook, and the playbook's mood doesn't override the structure's pacing requirements.
- [ ] The universal end-card convention's content rules (logo, ≤2 CTAs, matched spoken/on-screen CTA wording) are honored wherever it's used, with its visual treatment adapted to the category's grade.

## Stage 6 — Final read-through

- [ ] The Part One instruction line (I2VA/FL2VA/L2VA/full-reference only) is present, correctly formatted, first line of the prompt, followed by a blank line before the core fields.
- [ ] All required core fields are present, correctly labeled, in the required order.
- [ ] Read the whole prompt at normal pace: does the hook actually land fast enough to work as an ad hook (not a scene-setting establishing shot)? Does the end-card, where present, get enough held time to actually be readable? If either feels rushed or absent on the page, it will be rushed or absent on generation.

A prompt that clears all six stages is certified: unambiguous about mode, structure, category, and CTA/end-card timing, and budgeted in a way that respects both this model's known behavior (`model_facts.md`) and what actually makes a commercial ad do its job in 15 seconds or fewer.
