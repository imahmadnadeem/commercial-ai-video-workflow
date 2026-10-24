# Commercial Shot Brief & 3-Generation Tracker

Use this template to plan, direct, and log every hybrid shot before burning compute tokens.

---

## Shot Overview
- **Project Name:** 
- **Scene / Shot Number:** Scene ___ / Shot ___
- **Target Timeline Duration:** ____ seconds (Shoot / Generate: target + 1.5s buffer)
- **Primary Visual Goal:** 

---

## 1. Physical Plate Specifications (If Live-Action Guided)
- **Camera Package:** Sony FX3 (Full Frame) / Other: ___________
- **Lens Focal Length:** [ ] 24mm  [ ] 35mm  [ ] 50mm  [ ] 85mm
- **Aperture / Depth of Field:** f/______ (Deep / Shallow)
- **Physical Actor Action:** 
- **Keying Setup:** [ ] Green Screen  [ ] Neural Depth Matte  [ ] Practical Plate
- **Clean Plate File Name:** `plate_sc___sh___take___.mov`

---

## 2. 3D Pre-Visualization Pass (If Blender Guided)
- **3D Asset / Environment:** 
- **Camera Move Type:** [ ] Static  [ ] Dolly-In  [ ] Orbit  [ ] Handheld Parallax
- **Viewport Draft Render File:** `previz_sc___sh___720p.mov`

---

## 3. The 3-Generation Rule Log

| Pass | Purpose | Prompt / Seed Tweaks | Status / Notes |
|---|---|---|---|
| **Take 1 (Base Lock)** | Character stability, bone anatomy, strict frame hold | Motion scale: Low (0.2 – 0.4) | [ ] Pass  [ ] Reroll |
| **Take 2 (Drift & Depth)** | Subtle handheld camera drift, parallax shift | Motion scale: Mid (0.5 – 0.65) | [ ] Pass  [ ] Reroll |
| **Take 3 (Atmosphere)** | Environmental texture (haze, dust, flares, rain) | Target atmospheric elements | [ ] Pass  [ ] Reroll |

---

## 4. Post-Production Finishing Checklist
- [ ] **Head / Tail Trim:** Trimmed initial 12–15 frames (0.5s) and trailing drift.
- [ ] **Color Management:** Applied CST and Film Emulation LUT (Kodak 2383 / Fuji).
- [ ] **Film Grain:** Scanned 35mm grain overlaid (30–40% opacity, Overlay mode).
- [ ] **Sound Design Bed:**
  - [ ] Ambient room tone layer
  - [ ] Diegetic foley footsteps / movement
  - [ ] Micro-sound effects
  - [ ] Acoustic convolution reverb match
- [ ] **Master Export:** 1080p / 4K ProRes 422HQ or DNxHR HQX.
