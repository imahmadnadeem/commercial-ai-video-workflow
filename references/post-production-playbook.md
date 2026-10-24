# Post-Production Editorial Playbook

Generative AI produces raw visual plates; it does not produce a finished film. The difference between an amateur "AI demo" and a high-end commercial asset lies entirely in timeline discipline.

---

## 1. Trimming Edge Glitches (The 0.5-Second Cut)

Generative diffusion models almost universally suffer from boundary instability:
- **Head Glitches:** The initial 0.5 seconds often stutters as the latent noise space resolves into coherent geometry.
- **Tail Drift:** The final few frames frequently de-converge, introducing motion smearing, warping hands, or drifting perspectives.

### Standard Operating Procedure:
1. Always generate clips 1 to 2 seconds longer than the target scene duration.
2. In DaVinci Resolve or Premiere Pro, immediately blade off the first 12–15 frames (at 24fps) and the final 12 frames.
3. Use only the rock-solid center portion for edit assembly.

---

## 2. Killing the "Plastic Sheen" (Color & Film Emulation)

Raw AI footage displays an unnatural, overly smooth hyper-digital texture with blown highlights and flat shadows.

### Grade Pipeline:
1. **Color Space Transform (CST):** Map generative sRGB / Rec.709 outputs into an intermediate wide-gamut log space (such as DaVinci Wide Gamut or ARRI LogC3).
2. **Skin Tone Balancing:** Re-balance mids to prevent artificial magenta or hyper-orange tinting.
3. **Print Film Emulation (PFE):** Apply Kodak 2383 or Fuji 3513 print stock LUTs to compress highlight roll-off and restore organic film contrast.
4. **Scanned 35mm Grain Overlay:**
   - Blend real scanned 35mm film grain (fine-to-medium stock) in `Overlay` or `Soft Light` mode at 30%–45% opacity.
   - Grain breaks up repetitive latent pixel clustering and makes the output feel shot on optical cinema lenses.

---

## 3. Sound Design: The Missing 50%

AI video arrives completely silent. Visual suspension of disbelief collapses if the audio track is neglected.

### The 4-Layer Sound Bed:
1. **Layer 1: Room Tone / Atmosphere (The Foundation):** Continuous low-level ambient bed (room hum, city rumble, subtle wind, room reverb). A dry silence immediately tells the brain the scene is fake.
2. **Layer 2: Foley Movement:** Footsteps on hard surfaces, cloth friction, coat rustle, leather creak, prop handling.
3. **Layer 3: Micro-Effects:** Breaths, head turns, eye shifts, glass clinks.
4. **Layer 4: Spatial Reverb:** Match the acoustic room dimensions visible on screen using convolution reverb so dialogue and foley sound bound to the physical geometry.
