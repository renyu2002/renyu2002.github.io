# SoftGS Homepage Asset Production Plan

## Goal
Produce a small set of polished research assets that make the homepage visually credible
without overexposing unstable or unpublished technical details.

## Final asset list

1. `assets/hero_visual.png`
2. `assets/softgs_teaser.png`
3. `assets/dep_transition.png`
4. `assets/adaptive_refinement.png`
5. `assets/deformation_demo.mp4`
6. `assets/deformation_demo_poster.png`
7. `assets/Yu_Ren_CV.pdf`

The HTML currently uses SVG placeholders. When a real asset is ready, either:
- export it with the same basename and update the extension in `index.html`, or
- overwrite the placeholder using the same filename if you export SVG.

---

## Phase 1 — Minimum viable homepage (1 day)

### A. Hero visual
Purpose:
- Make the first screen look like a graphics research homepage.
- It can be a crop of the main teaser instead of a portrait.

Produce:
- One clean 4:3 image.
- Recommended resolution: 1200 × 900 or 1600 × 1200.
- Use one object, one deformation, and minimal text.

Best source:
- A stable SoftGS result you already trust.

Do not include:
- crowded legends,
- debug overlays,
- too many method details.

---

## Phase 2 — Main SoftGS teaser (1–2 days)

### Recommended structure
Four horizontal stages:
1. Initial
2. Peak Load
3. Local Refinement
4. Released / Residual Shape

Optional fifth inset:
- refined region close-up.

Recommended model:
- Bunny compression first if it already gives a visually obvious residual shape.
- Armadillo stretching can become the second example later.

Visual requirements:
- Same camera across all stages.
- Same lighting and background.
- Deformation should be visually obvious.
- Use arrows or a single small force glyph only if necessary.
- Keep the refined region overlay subtle.

Recommended export:
- 2400 × 1050 PNG.
- Keep an editable source in PPT / Illustrator / Figma / Inkscape.

This image becomes:
- homepage featured image,
- project-page header,
- possible paper teaser draft.

---

## Phase 3 — D-EP concept figure (1–2 days)

### Goal
Explain the constitutive idea in a way that a graphics reader can understand in 10 seconds.

### Recommended layout
Left:
- conventional hard elastic/plastic switch.

Right:
- D-EP smooth activation.

Bottom strip:
- Loading → Yield transition → Unloading → Residual state.

Possible plots:
- activation field versus trial stress / yield measure,
- stress-strain or response curve,
- gradient continuity around transition.

Important:
- Keep "strict elastic sub-yield region" visually explicit.
- Separate reversible activation behavior from irreversible plastic history.
- Avoid putting the full derivation on the homepage figure.

Recommended export:
- 1800 × 1100 PNG or SVG.

---

## Phase 4 — Adaptive local refinement figure (1–2 days)

### Goal
Show that refinement is local, physics-aware, and tied to Gaussian representation.

### Recommended 4-panel layout
1. Coarse simulation mesh + Gaussians
2. High-deformation / high-error region highlighted
3. Local mesh subdivision + Gaussian split
4. Refined rendered result

Optional inset:
- parent Gaussian → child Gaussians.

Important visual checks:
- use the same camera and object pose,
- show that unaffected regions stay coarse,
- show that the refined region actually improves shape / rendering / simulation accuracy,
- if possible add a tiny numerical annotation such as local error reduction or element count.

Recommended export:
- 1800 × 1100 PNG.

---

## Phase 5 — Deformation demo video (0.5–1 day)

### Recommended sequence
Duration: 8–15 seconds.

Timeline:
- 0–2 s: Initial
- 2–6 s: Loading
- 6–8 s: Peak deformation
- 8–12 s: Unloading
- 12–15 s: Residual shape

Labels:
- Initial
- Peak Load
- Release
- Residual Shape

Recommended settings:
- 1920 × 1080
- 30 fps
- H.264 MP4
- muted
- loop-friendly
- under ~8–12 MB if possible for fast page loading

Also export:
- a representative poster frame as `deformation_demo_poster.png`.

---

## Phase 6 — CV (0.5 day)

Suggested sections:
- Name / email / homepage / GitHub
- Education
- Research interests
- Research experience
- Projects
- Publications / preprints (only public items)
- Skills / tools
- Awards (if applicable)

File:
- `assets/Yu_Ren_CV.pdf`

Keep:
- 1 page if early-stage,
- 2 pages if you have enough research content.

---

## Recommended production order

1. SoftGS teaser
2. Hero crop from teaser
3. D-EP concept figure
4. Adaptive refinement figure
5. Demo video + poster
6. CV
7. Only then add a Selected Results gallery

This order avoids duplicated work because the teaser can supply both the hero visual
and the video poster style.

---

## Visual consistency rules

Use the same:
- camera style,
- neutral background,
- font family,
- label capitalization,
- arrow style,
- crop ratio,
- deformation-state naming.

Recommended terminology:
- Initial
- Loading
- Peak Load
- Release
- Residual Shape
- Coarse
- Refined
- Local Refinement
- Gaussian Split

Avoid mixing:
- Released / Recovery / Unloaded / Final
unless the paper itself uses those terms consistently.

---

## What to avoid publishing too early

Until the method is stable, avoid putting these on the public homepage:
- complete constitutive derivation,
- all ablation numbers,
- unstable quantitative claims,
- unpublished comparison tables,
- implementation details that you still expect to change.

The homepage should communicate:
1. what problem you study,
2. what the two main ideas are,
3. what the result looks like.

That is enough.
