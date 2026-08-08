---
name: minimax-h3-commercial-ad-director
description: Write MiniMax H3 (Hailuo 3.0) video-generation prompts for commercial advertisements — Hook-Problem-Solution-CTA direct-response ads, lifestyle/brand-story spots, product hero showcases, testimonial/UGC-style ads, before/after comparisons, and 6-second bumpers, across category playbooks (tech/gadget, automotive, beauty/skincare, food/beverage, fashion/luxury, FMCG/household, finance/insurance/pharma) — using the official field syntax from VIDEO_PROMPT_WRITING_GUIDE_base_en.md / _ref_en.md plus a frame-accurate 0.1-second timeline with protected hook and CTA/end-card timing. Use whenever the user wants an ad, a commercial, a product video, a brand spot, a promo video, or mentions a CTA, a call-to-action, an end-card, a hook-problem-solution structure, a testimonial ad, a before/after ad, or a bumper ad. Trigger even without "MiniMax," "H3," or "commercial" explicitly named — "make me a product ad," "I need a promo video for my app," "write a video ad script" all qualify.
---

# MiniMax H3 Commercial Ad Prompt Writer

Write a single MiniMax H3 prompt for a commercial advertisement — a specific **structure** (the beat-by-beat construction: Hook-Problem-Solution-CTA, Lifestyle/Brand Story, Product Hero Showcase, Testimonial/UGC-style, Before/After, 6-Second Bumper) combined with a specific **category playbook** (the industry visual language: Tech/Gadget, Automotive, Beauty/Skincare, Food & Beverage, Fashion/Luxury, FMCG/Household, Finance/Insurance/Pharma) — output strictly in the field syntax defined by `references/VIDEO_PROMPT_WRITING_GUIDE_base_en.md` and `references/VIDEO_PROMPT_WRITING_GUIDE_ref_en.md`.

This is a sister skill to `minimax-h3-director-prompt` (cinematic/arthouse director styles) and `minimax-h3-instagram-style-director` (social-native content). All three share the same underlying prompt syntax and 0.1s timeline discipline, but each draws from a different vocabulary because each content type is judged by a different standard: a cinematic clip is judged on mood and craft, Instagram content is judged on whether it hooks and feels native to the platform, and a commercial ad is judged on whether it actually sells — which means a hook that lands fast, claims that read clearly, and a CTA/brand moment that doesn't get cut off.

**Compatibility:** like its sister skills, this one only relies on the common Agent Skills baseline (`name`/`description` frontmatter, plain-prose instructions, relative-path reference files) with no Claude-only extensions, so it runs the same way under Claude Code/Cowork and Codex CLI. See `INSTALL.md`.

## Before you start: gather what you need

1. **Task type** — reference image/video/audio present, or pure text-to-video? See `references/VIDEO_PROMPT_WRITING_GUIDE_base_en.md` §1, or `references/VIDEO_PROMPT_WRITING_GUIDE_ref_en.md` for full-reference mode (common here when the user supplies an actual product photo, a logo asset, or reference footage to composite).
2. **Duration and scope** — 5-15 seconds. A real-world commercial format often runs 15-60s; MiniMax H3 caps at 15s. Decide with the user (or infer, then say so) whether you're generating the strongest single beat-cluster of a longer format, or a structure that's naturally short (6-second bumper, before/after) at its native length. Don't silently promise a full 30s arc's worth of content in 15s.
3. **Structure** — which of the six structures in `references/commercial_ad_styles.md` fits the goal? A performance/direct-response ask ("get people to click," "drive signups") points to Hook-Problem-Solution-CTA; a brand-awareness ask points to Lifestyle/Brand Story; a product launch points to Product Hero Showcase; a trust/social-proof ask points to Testimonial; a visible-transformation product points to Before/After; a single reinforcing message points to the 6-Second Bumper.
4. **Category playbook** — which of the seven fits the product/industry? Match directly where possible; if the user's category doesn't map cleanly, pick the closest and say so.
5. **The actual content** — product/brand specifics, the core claim or story, any exact on-screen text (claims, CTA wording, disclaimer) or spoken line the user cares about.

## The workflow

### 1. Read the model facts once

`references/model_facts.md` has the same hard limits and tested model behaviors as the sister skills (camera drifts unless forbidden, timed beats need a stated end-state, observable behavior beats emotion words, the last beat in a sequence risks compression). These apply here exactly as much as elsewhere — and the "last beat gets compressed" risk is precisely why this skill's timeline methodology reserves CTA/end-card time first rather than last.

### 2. Pick a structure and a category playbook

Open `references/commercial_ad_styles.md`. Pick exactly one structure and exactly one category — they're independent variables (see the "Combining structure + category" section at the end of that file). Note whether the chosen structure closes with the universal end-card/CTA convention (most do), closes softly (Lifestyle/Brand Story, Product Hero Showcase), or embeds its CTA in a single message (6-Second Bumper) — this determines how you sequence the timing chart in the next step.

### 3. Build a 0.1-second timing chart

Follow `references/timeline_methodology.md` — it's tuned specifically for commercial content: for end-card structures, **reserve the closing 2.0-5.0s before planning anything else**, then budget the hook (1.0-3.0s), then fill whatever remains with the structure's own beat rhythm (DR claim-cuts every 2.0-3.0s, Product Hero beats 1.0-3.0s, a Testimonial's narrative stages as continuous spans, etc.). This reversed planning order — ending first — is specific to this skill; the sister skills plan front-to-back.

**Show this chart to the user** as part of your output, the same way the sister skills do — it's what proves the hook lands fast enough and the CTA actually gets legible held time before a generation is spent on it.

### 4. Compress the chart into the actual prompt syntax

Convert into the exact field structure from `references/VIDEO_PROMPT_WRITING_GUIDE_base_en.md` (or `_ref_en.md` for full-reference mode, common for real product/logo assets): `[Shot N]` blocks only at true cuts respecting the structure's own cut-count convention (DR: frequent hard cuts; Lifestyle: few, slow; Bumper: at most 1-2), camera motion in the §4.3 vocabulary only, on-screen claim/CTA/end-card text as exact verbatim strings per §4.5, spoken VO/testimonial dialogue via `(S1)` and `<d>...</d>` per §4.4 with on-screen CTA text matching the spoken CTA wording, and `overall_soundscape`/`non_diegetic_music` matching the structure's audio convention. State claim-to-cutaway causality explicitly in the same sentence. `references/worked_examples.md` shows this done end to end for four structure×category combinations at four different durations, including the 6-second bumper.

### 5. Certify before handing it back

Run the finished prompt through `references/certification_checklist.md`. Confirm briefly in your response: the end-card (where used) got its reserved time and is legible for at least ~1.0s, the hook is fast enough to function as an ad hook rather than an establishing shot, on-screen claim/CTA text is verbatim, and the category playbook's mood didn't override the structure's pacing requirements (a direct-response ad still needs its claim-cut rhythm even in a slow-native category like Fashion/Luxury).

## Output format

Give the user, in this order:
1. A short line naming the task type, duration/scope decision, chosen structure, and chosen category playbook (and why, if the user didn't specify one or both).
2. The 0.1s timing chart (a markdown table — event rows only, with the reserved end-card beat and the hook clearly marked).
3. The final prompt, in a fenced code block, in the exact field syntax it needs to be pasted into the model as.
4. One or two lines confirming the certification checks that mattered most for this particular prompt.

Keep the chart and the final prompt visually separable (e.g. a `---` between them).
