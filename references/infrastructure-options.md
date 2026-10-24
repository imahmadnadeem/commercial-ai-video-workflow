# Infrastructure & Compute Architecture Guide

Choosing the right technical infrastructure is the highest-leverage decision when building an AI video pipeline for a studio or brand.

---

## 1. Option 1: Local Dedicated Silicon (High CapEx, Zero Token Fees)

### Hardware Specs & Tiers
- **Tier 1 (Creator Workstation):** NVIDIA RTX Spark Arm-based desktop workstations running Windows 11 on Arm with up to 128 GB memory ($4,999 – $5,500 / approx. ₹4.1 – ₹4.5 Lakh). Ideal for individual 3D/video artists.
- **Tier 2 (Dedicated Mini-Studio):** NVIDIA DGX Spark 140W Linux mini-desktops running the GB10 Grace Blackwell unified chip with 128 GB unified memory ($4,699 – $6,950 / approx. ₹3.9 – ₹5.8 Lakh).
- **Tier 3 (Enterprise Multi-Seat Cluster):** High-end multi-GPU racks and towers ($50,000 – $95,000+ / ₹40 Lakh – ₹80 Lakh+). Used by major post houses fine-tuning proprietary LoRAs across 20+ editing bays.

### Operating Models
- Pull models straight from GitHub / Hugging Face (e.g. LTX-Video 2.5, Stable Video Diffusion, ComfyUI nodes, local LLMs).

### Advantages
- **Zero Token Anxiety:** Render all day without meter fees.
- **Client Confidentiality & NDA Compliance:** Footage never leaves the studio's local network.
- **No Cloud Downtime:** Completely insulated from provider outages or queue throttles.

### Risks & Mitigations
- **Requires Systems Engineering:** CUDA driver breakages, out-of-memory (OOM) errors, thermal throttling, and repo dependency conflicts must be handled internally.

---

## 2. Option 2: Unified API Routing (Flexible, Scalable, Low CapEx)

### Architecture
- Connect a unified routing layer (e.g., OpenRouter or direct developer API endpoints) directly into terminal CLI tools like **Claude Code**.
- Orchestrate scripting, asset tagging, and motion prompt builds through code scripts rather than web browser dashboards.

### Cost Structure
- Initial test budget: As low as $100 (~₹8,000 – ₹8,500).
- Example Token Economics:
  - **Frontier Reasoning (Claude 5.5 Opus):** ~$15 / M input tokens, ~$75 / M output tokens.
  - **Fast Execution (Astra / Sonnet):** ~$5 / M input tokens, ~$15 / M output tokens.

### Advantages
- **Zero Hardware Lock-In:** When a new state-of-the-art model releases, simply update a single string parameter in your script instead of swapping GPUs.
- **Scalable Across Remote Teams:** Editors can execute calls globally without requiring heavy hardware on set.

### Risks & Mitigations
- **Uncapped Billing:** Editors running looping generations can spike cloud bills. Mitigate with hard token limits, cost alerting, and rate-limiting wrappers.

---

## 3. Option 3: Stacking Web Subscriptions (The SaaS Stack)

### Typical Monthly Spend
- **Chat & Scripting:** $20/month (ChatGPT Plus) or $20–$25/user/month (Claude Team).
- **Video & Motion:** $30–$60/month (Midjourney) + $30–$95/month (Runway / Luma / Kling / Higgsfield).
- **3D & Audio:** $20–$50/month (Meshy / ElevenLabs).
- **Total recurring cost:** $150 – $300+ / seat / month.

### Advantages
- Zero setup friction. Any non-technical team member can start generating in minutes.

### Disadvantages
- **Fragmented Data Silos:** Files end up stranded across multiple cloud downloads. Editors spend 30% of their day downloading MP4s from one browser tab to re-upload to another.
- **Policy Censorship:** Cloud platforms enforce strict, unpredictable filters that block standard commercial and action scenes without recourse.
