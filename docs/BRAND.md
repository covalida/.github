<!--
  Corporate identity reference for Covalida. The authoritative brand guide,
  with the full asset library, downloads and detailed guidance, lives at
  https://brand-guide.covalida.com. This file mirrors its essentials for the
  organization repository. When a brand value changes, change it in the brand
  guide first, then mirror it here and in RESOURCES.md.
-->

# Covalida — Brand & Corporate Identity

Essential reference for the Covalida visual identity: logo, color palette,
typography, and usage. The complete, authoritative brand guide — construction
grids, clear-space math, accessibility ratios, component specs and the full
downloadable asset library — lives at **[brand-guide.covalida.com](https://brand-guide.covalida.com)**.

> Tagline: **"Securing the Core."**

---

## Logo

The mark is the **Core-Shield** — a shield shaped as an open **"C"** (for
*Covalida*) with an inner mini-shield, drawn in clean faceted geometry and
filled with a teal diagonal gradient. The open "C" is the protective embrace;
the inner shield is the core being protected. It reads as a digital
force-field around the business — modern and reassuring, never a medieval
coat-of-arms or an authority stamp.

The wordmark **COVALIDA** is set in **Montserrat ExtraBold (800)** — Deep Slate
Gray (`#2F4F4F`) on light surfaces, white on dark. It ships as a finished
vector; never re-typeset it by hand.

### Variants

| Variant | Where | File |
| --- | --- | --- |
| **Horizontal** (primary) | Default — headers, footers, docs, this profile | `covalida-logo-horizontal.svg` · `…-dark.svg` |
| **Vertical** (stacked) | Square or narrow spaces, avatars, cover slides | brand guide → [Downloads](https://brand-guide.covalida.com/downloads/) |
| **Symbol** (gradient) | App icons, avatars, favicons, watermarks | `covalida-icon.svg` |
| **Flat mono** (single color) | Where a gradient can't render — tiny favicons, single-color tools | `covalida-icon-flat.svg` |

### Approved backgrounds

| Background | Logo treatment |
| --- | --- |
| Light (white / Light Mint `#CDE9E6`) | Gradient symbol, slate (`#2F4F4F`) wordmark — the positive logo |
| Dark (Deep Petrol `#155D5B`, Deep Slate, black) | Gradient symbol, white wordmark — the dark variant |

On busy or low-contrast backgrounds, place the logo on a calm solid panel first.

---

## Color Palette

Five core colors carry the entire brand. Restraint is the point: a
whitespace-rich canvas with one confident teal reads as sovereign and premium.

| Token | Hex | RGB | Role |
| --- | --- | --- | --- |
| Deep Teal | `#008080` | `0, 128, 128` | Primary — brand color, key surfaces, primary emphasis |
| Light Teal | `#20B2AA` | `32, 178, 170` | Accent — lines, highlights, data-viz (not small text on white) |
| Deep Petrol | `#155D5B` | `21, 93, 91` | Deep — button backgrounds, icon circles, gradient end |
| Deep Slate Gray | `#2F4F4F` | `47, 79, 79` | Text — body copy, headings, and the wordmark |
| Light Mint | `#CDE9E6` | `205, 233, 230` | Surface — section backgrounds, calm fills (never text) |

### Signature gradient

The Core-Shield symbol is filled with a single diagonal teal gradient — a
bright mint-teal down to Deep Petrol. Use it only on the symbol, hero accents
and large graphic shapes; never behind body text, and never recolor it.

```css
background: linear-gradient(135deg, #2db3a4 0%, #25a699 38%, #1a847f 68%, #155d5b 100%);
```

### Non-brand, regulatory accent (EC-REP badge only)

The EU-flag colors below signal the EU Authorized Representative role on the
EC-REP badge. They are **not** brand colors and are used nowhere else.

| Token | Hex | Usage |
| --- | --- | --- |
| EU Blue | `#003399` | EU-flag blue — EC-REP "EU Authorized Representative" badge |
| EU Gold | `#FFCC00` | EU-flag gold — paired with EU Blue |

### Design tokens (CSS)

Copy-paste custom properties for building on-brand surfaces. This is the core
set; the full teal scale (50–900), OKLCH variants and semantic tokens live on
the brand guide's **[Design Tokens](https://brand-guide.covalida.com/downloads/tokens)** page.

```css
:root {
  /* Core brand colors */
  --cv-primary: #008080; /* Deep Teal */
  --cv-accent:  #20b2aa; /* Light Teal */
  --cv-petrol:  #155d5b; /* Deep Petrol */
  --cv-slate:   #2f4f4f; /* Deep Slate Gray — text */
  --cv-mint:    #cde9e6; /* Light Mint — surfaces */

  /* Signature gradient */
  --cv-gradient: linear-gradient(135deg, #2db3a4 0%, #25a699 38%, #1a847f 68%, #155d5b 100%);

  /* Typography */
  --cv-font-family: "Montserrat", system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
}
```

---

## Typography

Covalida uses **one** typeface everywhere: **Montserrat** — a geometric
sans-serif that reads as engineered and trustworthy yet warm and human. It is
published under the SIL Open Font License and self-hosted (via
`@fontsource/montserrat`, no Google Fonts CDN) so no visitor data leaves the
site — modeling the compliance posture the brand sells.

| Weight | Value | Role |
| --- | --- | --- |
| Regular | 400 | Body copy, long-form text, table cells |
| Medium | 500 | Emphasized body, captions, labels, kickers |
| SemiBold | 600 | Sub-headings, button labels |
| Bold | 700 | Headings (H1–H3), section titles |
| ExtraBold | 800 | Wordmark, display type, hero headlines, big numbers |

Fallback stack: `system-ui, -apple-system, "Segoe UI", Roboto, sans-serif`.

---

## Usage Rules

- Always place the supplied SVG (or a high-resolution PNG from the brand
  guide's Downloads). Never redraw, re-type, or re-color the logo.
- Match the background: positive logo on light and mint; the dark variant on
  dark. Keep contrast high and the backdrop quiet.
- Give it room. Keep clear space around the logo equal to at least the height
  of the shield's inner "C".
- Do **not** recolor the symbol outside the teal palette, stretch it, rotate
  it, or add effects (shadows, outlines, extra strokes).
- Keep the wordmark in uppercase Montserrat ExtraBold; never re-space it or
  substitute another face.

---

## Asset Files

Vector logo assets shipped in this repository live under
[`assets/logo/`](assets/logo/):

| File | Use |
| --- | --- |
| [covalida-logo-horizontal.svg](assets/logo/covalida-logo-horizontal.svg) | Primary horizontal lockup — light backgrounds (slate wordmark) |
| [covalida-logo-horizontal-dark.svg](assets/logo/covalida-logo-horizontal-dark.svg) | Horizontal lockup — dark backgrounds (white wordmark) |
| [covalida-icon.svg](assets/logo/covalida-icon.svg) | Gradient symbol — favicons, app icons, avatars |
| [covalida-icon-flat.svg](assets/logo/covalida-icon-flat.svg) | Flat mono symbol (Deep Teal) — single-color / tiny contexts |

> The full asset library — vertical lockups, high-resolution PNGs, favicons,
> the Open Graph image and design tokens — is on the brand guide:
> **[brand-guide.covalida.com/downloads](https://brand-guide.covalida.com/downloads/)**.

---

## Maintenance

- **Owner:** `@covalida/core`
- **Source of truth:** the brand guide at
  [brand-guide.covalida.com](https://brand-guide.covalida.com). The palette in
  [RESOURCES.md](RESOURCES.md) mirrors the colors above. Change a value in the
  brand guide first, then mirror it here and in RESOURCES.md.
