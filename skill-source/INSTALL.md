# Installing this skill

Same Agent Skills open-standard format as its sister skills (`minimax-h3-director-prompt`, `minimax-h3-instagram-style-director`): a folder with `SKILL.md` at the root (`name`/`description` frontmatter, plain-prose instructions) plus a `references/` folder. No hooks, no subagent frontmatter, no Claude-only extensions — works unmodified across the tools below.

## Claude Code / Claude (Cowork)

- **Personal:** `~/.claude/skills/minimax-h3-commercial-ad-director/`
- **Project-level:** `.claude/skills/minimax-h3-commercial-ad-director/`
- In Cowork, open the packaged `.skill` file directly and install with the **Save skill** button.

## Codex CLI

- **Personal:** `~/.codex/skills/minimax-h3-commercial-ad-director/`
- **Project-level:** `.codex/skills/minimax-h3-commercial-ad-director/`
- **Shared Agent-Skills-standard location** (some Codex builds, Cursor, Gemini CLI): `.agents/skills/minimax-h3-commercial-ad-director/`

If you have the `.skill` zip:

```bash
mkdir -p ~/.codex/skills
unzip minimax-h3-commercial-ad-director.skill -d ~/.codex/skills/
```

Invoke explicitly with `$minimax-h3-commercial-ad-director <request>`, browse via `/skills`, or let it auto-trigger on a matching request. If it doesn't load, check your Codex build's current skills directory (`codex --help`) — this has moved before.

## What's inside

```
minimax-h3-commercial-ad-director/
├── SKILL.md
├── INSTALL.md
└── references/
    ├── VIDEO_PROMPT_WRITING_GUIDE_base_en.md   — MiniMax H3 field syntax (T2VA/I2VA/FL2VA/L2VA)
    ├── VIDEO_PROMPT_WRITING_GUIDE_ref_en.md     — full-reference-mode field syntax
    ├── model_facts.md            — model limits + tested prompting behavior
    ├── commercial_ad_styles.md   — 6 ad structures + universal end-card convention + 7 category playbooks → prompt vocabulary
    ├── timeline_methodology.md   — 0.1s timeline method, tuned for protected hook + CTA/end-card timing
    ├── certification_checklist.md — pre-flight checklist
    └── worked_examples.md        — 4 complete, verified examples at 4 different durations (including a 6s bumper)
```

No scripts, no external dependencies, no network access needed at runtime — the internet research is baked into `commercial_ad_styles.md` already.
