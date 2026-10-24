---
name: commercial-ai-video-workflow
description: Commercial AI video and hybrid production workflow system. Use when designing, directing, or executing brand video pipelines combining physical cameras (Sony FX3), 3D pre-viz (Blender), generative motion guidance, model tier routing, and timeline finishing.
---

# Commercial AI Video & Hybrid Production Workflow

A battle-tested production framework for creative directors, producers, and agencies building hybrid AI video pipelines. Developed by Nadeem Ahmad ([ahmadnadeem.in](https://ahmadnadeem.in)).

---

## Core Philosophy

1. **Never outsource creative taste, pacing, or physical blocking to text prompts.**
2. **Text-to-video prompts always fail commercial standards:** Pure text prompting produces chaotic motion, morphing limbs, and plastic skin textures.
3. **Automate the repetitive; ground the narrative:** Use AI for boring mechanical tasks (rotoscoping assistance, rapid animatics, surface texture rendering), but anchor all human performance in physical cameras and optical glass.
4. **Treat generative AI as a specialized camera department and post-production layer, not a replacement for cinema discipline.**

---

## When to Activate This Skill

Activate this skill when the user or project asks to:
- Plan, budget, or direct an AI-powered or hybrid commercial video.
- Design an agency or studio AI video production pipeline.
- Resolve camera motion, character continuity, or prompt-guardrail failures.
- Build pre-visualization workflows bridging 3D animation (Blender) and generative video.
- Establish post-production finishing standards for generative media (DaVinci Resolve / Premiere Pro).

---

## The 7-Step Hybrid Production Protocol

### Step 1: The Live Motion Formula (Bypassing Text-Prompt Failures)
When human movement, action, or character interaction is required:
1. **The Physical Take:** Perform or direct the physical blocking on camera against a green screen or clean backdrop. Shoot on a cinema camera with full-frame optical depth (e.g., Sony FX3).
2. **Clean Neural Extraction:** Pull the actor using neural keying tools (Corridor Keyer or local depth mattes). Keep edge integrity, hair detail, and natural motion blur intact.
3. **Motion Guidance Input:** Feed the keyed plate into the generative video engine as a video-to-video or motion-control reference guide.
4. **Result:** The AI renders environmental lighting, wardrobe, and world styling, while the physical posture, timing, and bone geometry remain 100% human.
5. **The Fail-Forward Rule:** If a model fights the plates or hits strict policy filters, do not spend hours wrestling prompts—switch models immediately and keep moving.

### Step 2: Infrastructure Selection Matrix
Before spinning up seats, evaluate the studio's technical profile:

| Tier | Setup | Best For | Tradeoffs |
|---|---|---|---|
| **Option 1: Local Silicon** | NVIDIA RTX Spark / DGX Spark (Grace Blackwell 128GB) / Enterprise multi-GPU racks | Strict client NDAs, offline heavy rendering, zero token fees | High initial CapEx ($5k - $95k+), requires local systems engineering & CUDA maintenance |
| **Option 2: Unified API Routing** | OpenRouter / Direct API endpoints orchestrated via CLI developer tools (e.g., Claude Code) | Fast-moving agencies, scalable multi-model access | Pay-as-you-go token costs; requires token usage limits and monitoring |
| **Option 3: SaaS Stack** | ChatGPT Plus + Claude Team + Runway / Luma / Kling + ElevenLabs | Quick prototyping and individual experimentation | High recurring OpEx per seat, fragmented files, cloud lock-in |

*Recommendation:* Start with Option 2 (Unified APIs) to train the creative team. Transition heavy repetitive rendering to Option 1 once monthly cash flow justifies hardware CapEx.

### Step 3: Compute Allocation Hierarchy (Stop Burning Tokens)
Do not use expensive frontier reasoning models for rough ideation:
- **Fast Tier (Lightweight / Sonnet-tier):** Use for rapid scene outlines, rough beat sheets, and quick brainstorm iterations.
- **Reasoning Tier (Heavy Frontier LLMs):** Reserve exclusively for script continuity, resolving story contradictions, and drafting technical production specs.
- **Generative Media Tier (Midjourney, Luma, Runway, Kling, LTX-Video):** Trigger ONLY after the script and scene beats are locked. Generating video before the script is approved is wasted capital.

### Step 4: Asset Retrieval via Local Semantic Search (RAG)
Avoid lost footage across disorganized hard drives:
- Index visual assets, 3D elements, and B-roll plates locally using semantic vector embeddings.
- Enable natural language discovery: searching *"car driving through neon rain at night"* immediately surfaces matching takes without relying on manual file naming.

### Step 5: Pre-Visualization (3D Animation Meets AI Generation)
To maintain spatial accuracy without random camera warping:
1. **Rough 3D Blocking:** Block the scene in Blender with low-poly geometry. Lock camera lens focal length (e.g. 35mm / 50mm), camera path, and parallax speed.
2. **Draft Generative Passes:** Run viewport renders through generative diffusion at low draft resolution (720p) to test surface textures, lighting mood, and color palette.
3. **Final Upscaling:** Once camera moves and lighting are locked, upscale the final pass to clean 1080p or 4K.

### Step 6: The 3-Generation Rule
AI video is inherently stochastic. Follow the studio 3-generation discipline:
- **Take 1 (The Stable Base):** Low motion intensity, strict adherence to frame reference. Locks character anatomy.
- **Take 2 (Camera Drift):** Slightly elevated motion to introduce realistic handheld camera micro-shake and parallax depth.
- **Take 3 (Atmospheric Texture):** Render pass tuned for organic environmental particles (haze, dust motes, volumetric light, anamorphic flares).
- *Rule:* If a shot misses, do not rewrite the whole prompt. Diagnose the specific variable (framing, seed, matte, or motion scale) like tweaking lights on set.

### Step 7: Timeline Finishing (Kill the Plastic Look)
Raw generative video is never a finished commercial. It must pass through traditional editorial finishing in DaVinci Resolve or Premiere Pro:
1. **Trim Edge Glitches:** Cut off the first 0.5s stutter and trailing frame drift. Keep only the rock-solid center.
2. **Color Grade & Film Emulation:** Apply custom print emulation LUTs to balance skin tones and remove digital saturation sheen.
3. **Overlay 35mm Grain:** Add subtle, scanned 35mm film grain to break up smooth neural textures and match real optical lens diffusion.
4. **Sound Design (The Missing 50%):** AI video outputs silent frames. Realism is won in the audio track. Layer rich room tone, footsteps, clothing rustle, and diegetic foley beds so the audience intuitively accepts the visual.

---

## Detailed References

- For in-depth hardware setups and API endpoints, review `references/infrastructure-options.md`.
- For color grading, grain blending, and foley guidelines, review `references/post-production-playbook.md`.
- For the production shot breakdown worksheet, review `templates/commercial-shot-brief.md`.
