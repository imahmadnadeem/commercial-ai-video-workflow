# Commercial AI Video Workflow (`ai-video-workflow`)

[![skills.sh](https://img.shields.io/badge/skills.sh-ai--video--workflow-blue)](https://skills.sh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> A battle-tested hybrid AI video production workflow for creative directors, producers, and agencies. Developed by **Nadeem Ahmad** ([ahmadnadeem.in](https://ahmadnadeem.in)).

---

## Overview

Most generative AI discussions in commercial video fall into two extreme traps:
1. Believing text prompts typed into a browser will replace human production crews.
2. Dismissing generative media completely as unpredictable, plastic slop.

This skill equips AI agents (Antigravity, Claude Code, Cursor, Codex) with the exact technical and operational rules required to build **commercial-grade, hybrid video pipelines** combining physical cinema cameras (Sony FX3), Blender 3D pre-visualization, model-tier API routing, and traditional DaVinci Resolve / Premiere Pro post-production.

---

## Installation via `skills.sh`

Install this skill directly into your AI coding assistant or agent environment:

```bash
# Using skills.sh CLI
npx skills add imahmadnadeem/ai-video-workflow
```

Or clone manually into your local agent skills directory:
```bash
git clone https://github.com/imahmadnadeem/ai-video-workflow.git ~/.gemini/config/skills/ai-video-workflow
```

---

## Repository Structure

```
ai-video-workflow/
├── README.md                      # Public documentation & installation guide
├── SKILL.md                       # Core Agent Skill specification with YAML frontmatter
├── references/
│   ├── infrastructure-options.md  # Detailed hardware (DGX/RTX) vs API vs SaaS breakdown
│   └── post-production-playbook.md# DaVinci/Premiere grading, grain overlay, and foley rules
└── templates/
    └── commercial-shot-brief.md   # Practical shot breakdown and 3-Generation log sheet
```

---

## Core Production Rules

1. **Physical Motion Grounding:** Never beg text prompts to render human movement. Shoot physical blocking on optical full-frame cameras (Sony FX3), pull clean neural mattes (Corridor Keyer), and feed keyed footage as motion guidance.
2. **Compute Allocation:** Use fast models for beat outlines, reasoning models for continuity briefs, and generative diffusion strictly after scene beats are locked.
3. **Blender 3D Bridge:** Lock focal lengths and camera moves with low-poly 3D pre-vis before rendering draft 720p passes and final 4K upscales.
4. **The 3-Generation Rule:** Take 1 (Base character lock) $\rightarrow$ Take 2 (Camera drift & handheld parallax) $\rightarrow$ Take 3 (Atmospheric dust, haze, lens flares).
5. **Timeline Discipline:** Trim the 0.5s head/tail glitch, apply 35mm scanned grain and print emulation LUTs to kill the plastic sheen, and build a rich multi-track foley bed.

---

## Author & Attribution

- **Nadeem Ahmad** — Creative Director & Systems Builder
- Website: [ahmadnadeem.in](https://ahmadnadeem.in)
- Inquiries: [info.ahmadnadeem@gmail.com](mailto:info.ahmadnadeem@gmail.com)
- LinkedIn: [linkedin.com/in/imahmadnadeem](https://www.linkedin.com/in/imahmadnadeem/)
- IMDb Pro: [pro.imdb.com/name/nm18357923](https://pro.imdb.com/name/nm18357923/public/?rf=cons_nm_more_allow_mypg&ref_=cons_nm_more_allow_mypg)

## License

MIT License. Free to use, adapt, and build upon.
