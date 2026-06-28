<!--
  Corporate identity reference for Covalida. The color values here are the
  single source of truth for brand colors; the short palette table in
  RESOURCES.md mirrors them. Update colors HERE first, then propagate.
-->

# Covalida — Brand & Corporate Identity

Authoritative reference for the Covalida visual identity: logo, color palette,
typography, scalability, and logo lockups.

> Tagline: **"Securing the Core."**

---

## Logo

The mark is a **shield** with a negative-space **"C"** (for *Covalida*) that
reads as a keyhole — signalling security, protection, and trust. It is rendered
with a teal gradient and a subtle 3D fold for depth.

Variants:

- **Icon** — the shield mark on its own (favicons, app icons, avatars).
- **Horizontal lockup** — icon + `COVALIDA` wordmark, set side by side.

Backgrounds the logo is approved on:

| Background | Logo treatment |
| --- | --- |
| Light (`#F5F5F0` / white) | Full-color teal icon, slate (`#2F4F4F`) wordmark |
| Deep Slate (`#2F4F4F`) | Full-color teal icon, white wordmark |
| Black (`#000000`) | Full-color teal icon, white wordmark |

---

## Color Palette

Three brand colors. (The EU-flag colors below are used **only** on the EC-REP
badge to signal the EU Authorized Representative role — they are not brand
colors.)

| Token | Hex | RGB | Usage |
| --- | --- | --- | --- |
| Deep Teal | `#008080` | `0, 128, 128` | Primary brand color — logo mark, primary accents, CTAs |
| Light Teal | `#20B2AA` | `32, 178, 170` | Secondary accent — highlights, gradients, status |
| Deep Slate Gray | `#2F4F4F` | `47, 79, 79` | Dark neutral — backgrounds, wordmark on light, body text |

Non-brand, regulatory-context accent (EC-REP badge only):

| Token | Hex | Usage |
| --- | --- | --- |
| EU Blue | `#003399` | EU-flag blue — EC-REP "EU Authorized Representative" badge |
| EU Gold | `#FFCC00` | EU-flag gold — paired with EU Blue |

---

## Typography

The wordmark and headings use a **geometric sans-serif**, set in **uppercase**
for the wordmark (`COVALIDA`).

| Weight | Use |
| --- | --- |
| Bold | Wordmark, primary headings |
| Semibold | Sub-headings, emphasis |
| Regular | Body text, captions |

---

## Scalability

The icon must remain legible across sizes. Three reference tiers:

| Tier | Context |
| --- | --- |
| Large | Signage, hero graphics, print |
| Medium | Web headers, documents |
| Tiny | App icons, favicons — simplified detail |

---

## Logo Lockups

| Lockup | Where |
| --- | --- |
| Icon + wordmark on light | Primary lockup — light surfaces |
| Icon + wordmark on Deep Slate | Dark-neutral surfaces |
| Icon + wordmark on black | Maximum-contrast / monochrome contexts |

---

## Asset Files

Official, production-ready assets are not yet committed. Place them under
`docs/assets/` once available, preferably as **SVG** (scales losslessly):

```text
docs/assets/
├── logo/
│   ├── covalida-icon.svg
│   ├── covalida-icon-mono.svg
│   ├── covalida-lockup-light.svg
│   ├── covalida-lockup-dark.svg
│   └── covalida-lockup-black.svg
└── favicon/
    ├── favicon.svg
    └── apple-touch-icon.png
```

> **Source files needed.** The brand sheet shared so far is a raster preview;
> cropping it would yield low-quality marks. Provide the original vector
> (SVG/AI) or high-resolution PNG exports to populate `docs/assets/`.

---

## Usage Rules

- Keep clear space around the logo equal to at least the height of the shield's
  inner "C".
- Do **not** recolor the icon outside the teal palette, stretch it, rotate it,
  or add effects (shadows beyond the built-in fold, outlines).
- On busy backgrounds, place the logo on a solid slate or white panel.
- Maintain the wordmark in uppercase; never letter-space it tighter than the
  approved lockups.

---

## Maintenance

- **Owner:** `@covalida/core`
- Brand colors here are the single source of truth; the palette table in
  [RESOURCES.md](RESOURCES.md) mirrors them. Change a value here first.
