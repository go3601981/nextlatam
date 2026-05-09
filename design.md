# Next LATAM — Design System

> **Direction:** top-tier IT consultancy. Stripe / Linear / Vercel product-grade.
> **Posture:** white-first, deep ink, one vivid orange. Confident, technical, unfussy.
> **Voice:** specific, declarative, light on adjectives. We engineer outcomes — we don't decorate them.

Next is a B2B IT consultancy in immersive technology — AR, VR, 3D — for enterprises in LATAM and the US.

---

## Contents

1. [Brand essence](#brand-essence)
2. [Logo](#logo)
3. [Color](#color)
4. [Typography](#typography)
5. [Spacing & radii](#spacing--radii)
6. [Shadows & elevation](#shadows--elevation)
7. [Motion](#motion)
8. [Components](#components)
9. [Voice & tone](#voice--tone)
10. [Applications](#applications)
11. [Files](#files)

---

## Brand essence

| | |
|---|---|
| **Mission** | Help enterprises ship immersive products that move metrics. |
| **Audience** | CMOs, heads of innovation, retail, training, and brand at LATAM + US enterprises. |
| **Position** | A specialist consultancy — not an agency, not a generalist studio. |
| **Personality** | Calm, exact, opinionated. Engineers first; storytellers when it matters. |
| **Pillars** | Outcomes · Craft · Specificity · Partnership |

**We say:** "Old Trafford in six minutes. 94k headsets activated. +38% lift in shop conversion."
**We don't say:** "Cutting-edge synergies in the metaverse."

---

## Logo

The wordmark is **next** in lowercase black ink, with a vivid orange arrow piercing the **x** — pointing up and to the right. The arrow is the only mark of color in the logo.

### Variants

| Variant | File | Use |
|---|---|---|
| Primary | `assets/logo-next.png` | Default. Place on white or `--ink-50`. |
| Inverse | `assets/logo-next-inverse.png` | Place on `--ink-900` / `--ink-1000` only. |

### Construction rules

- **Clearspace:** minimum padding equal to the cap-height of the wordmark on all sides.
- **Minimum size:** 24 px tall on screen, 12 mm tall in print.
- **Always horizontal.** Never stack, rotate, or arch.

### Don'ts

- Don't recolor the wordmark or the arrow. Black ink + `--orange-500` only.
- Don't add gradients, shadows, glow, or outlines.
- Don't place on busy photography without a solid scrim or clearspace card.
- Don't substitute another arrow style. The piercing arrow is part of the mark.

---

## Color

### Brand orange (accent only)

| Token | Hex | Purpose |
|---|---|---|
| `--orange-50`  | `#FFF1EA` | Tints, hover surfaces, badge backgrounds |
| `--orange-200` | `#FFB48A` | Quiet accents on dark surfaces |
| `--orange-400` | `#FF6E2E` | Hover state of `--orange-500` |
| `--orange-500` | `#FF5A1F` | **Primary accent.** The single brand orange. |
| `--orange-600` | `#E64612` | Pressed / focus ring core |
| `--orange-700` | `#B8350B` | `--accent-ink` — orange text that passes AA on white |
| `--orange-900` | `#561705` | Deep tint for headings on cream surfaces |

> Orange is **accent only**. Never use it for body copy, large surfaces, or anything bigger than a CTA, badge, or 1–2 word emphasis. The site is white-first.

### Ink scale (cool-neutral)

| Token | Hex | Purpose |
|---|---|---|
| `--ink-1000` | `#0A0A0B` | Headings, primary buttons, dark sections |
| `--ink-900`  | `#111114` | Anchor sections (Contact, footer) |
| `--ink-700`  | `#2E2E36` | Strong body text on light |
| `--ink-600`  | `#4B4B57` | Default body copy |
| `--ink-500`  | `#6E6E7B` | Muted body, captions |
| `--ink-300`  | `#BFBFC7` | Disabled / quiet borders |
| `--ink-200`  | `#DEDEE3` | Standard borders |
| `--ink-100`  | `#F2F2F5` | Card surfaces, hover backgrounds |
| `--ink-50`   | `#F8F8FA` | Soft section backgrounds, stat strips |
| `--white`    | `#FFFFFF` | Page background |

### Contrast (AA / AAA)

| Pair | Ratio | Status |
|---|---|---|
| `--ink-1000` on `--white` | 19.2 : 1 | AAA |
| `--ink-600` on `--white`  | 7.8 : 1  | AAA |
| `--ink-500` on `--white`  | 5.0 : 1  | AA |
| `--orange-700` on `--white` | 5.6 : 1 | AA (use for orange text) |
| `--orange-500` on `--white` | 3.4 : 1 | UI / large only — never body |
| `--white` on `--ink-1000` | 19.2 : 1 | AAA |

**Rule:** orange copy must be `--orange-700` (`--accent-ink`). `--orange-500` is for fills, indicators, and large display only.

---

## Typography

**Type families.** Geist (sans + display) and Geist Mono (eyebrows, metadata, numerics).

```css
--font-sans:    "Geist", "Inter", system-ui, -apple-system, sans-serif;
--font-display: "Geist", "Inter", system-ui, sans-serif;
--font-mono:    "Geist Mono", ui-monospace, "SF Mono", monospace;
```

### Scale (16 px base)

| Token | Size | Use |
|---|---|---|
| `--fs-display` | 104 px | Editorial display only. Sparingly. |
| `--fs-h1` | 72 px | Hero headline |
| `--fs-h2` | 56 px | Section heads |
| `--fs-h3` | 40 px | Sub-sections |
| `--fs-h4` | 30 px | Card titles |
| `--fs-h5` | 24 px | Inline emphasis |
| `--fs-h6` | 20 px | Small heads |
| `--fs-body-lg` | 18 px | Lead paragraphs |
| `--fs-body` | 16 px | Default body |
| `--fs-body-sm` | 14 px | Dense UI |
| `--fs-caption` | 13 px | Captions |
| `--fs-eyebrow` | 12 px | Mono eyebrows, labels |

### Weight & tracking

- **Display & headings.** Geist 600, line-height 1.05, letter-spacing −0.02 → −0.024em.
- **Body.** Geist 400/500, line-height 1.55–1.65, no tracking.
- **Mono / eyebrows.** Geist Mono 500, line-height 1.4, letter-spacing 0.02em (no `text-transform` — Geist Mono is already calm at small sizes).

### Eyebrow pattern

```html
<span class="eyebrow">selected work</span>
```

Renders a 6 × 6 px `--orange-500` dot followed by 12 px Geist Mono in `--accent-ink`. Use once per section, never two in a row.

---

## Spacing & radii

### Spacing — 4 px base

| Token | Value | Common use |
|---|---|---|
| `--s-1` | 4 px | Icon-to-label gap |
| `--s-2` | 8 px | Tight stacks |
| `--s-3` | 12 px | Form rows |
| `--s-4` | 16 px | Card inner padding (small) |
| `--s-5` | 24 px | Card inner padding (default) |
| `--s-6` | 32 px | Component → component |
| `--s-7` | 48 px | Group → group |
| `--s-8` | 64 px | Block → block |
| `--s-9` | 96 px | Section padding (medium) |
| `--s-10` | 128 px | Section padding (large) |

**Section rhythm.** Hero `64–96 / 96`, content sections `128 / 128`, anchor sections (Contact / footer) `128 / 96`.

### Radii

| Token | Value | Use |
|---|---|---|
| `--r-xs` | 4 px | Inline pills, focus rings |
| `--r-sm` | 6 px | Buttons, inputs |
| `--r-md` | 10 px | Cards, thumbnails |
| `--r-lg` | 14 px | Section panels |
| `--r-xl` | 20 px | Hero media, feature panels |
| `--r-pill` | 999 px | Badges, status indicators |

---

## Shadows & elevation

| Token | Value | Use |
|---|---|---|
| `--sh-xs` | `0 1px 2px rgba(10,10,11,.04)` | Inputs at rest |
| `--sh-sm` | `0 1px 3px rgba(10,10,11,.06), 0 1px 2px rgba(10,10,11,.04)` | Cards at rest |
| `--sh-md` | `0 8px 24px -8px rgba(10,10,11,.10), 0 2px 6px rgba(10,10,11,.05)` | Hover, popovers |
| `--sh-lg` | `0 24px 48px -16px rgba(10,10,11,.18), 0 8px 16px rgba(10,10,11,.06)` | Modals, sheets |
| `--sh-glow` | `0 0 0 1px rgba(255,90,31,.20), 0 8px 24px -8px rgba(255,90,31,.30)` | Focus on accent |

Shadows are **cool-neutral** — they cast deep ink, never warm grey. Elevation steps are subtle; we lean on `border` + `background` contrast more than blur.

---

## Motion

| Token | Value | Use |
|---|---|---|
| `--ease-out`  | `cubic-bezier(0.22, 0.61, 0.36, 1)` | Standard exits |
| `--ease-snap` | `cubic-bezier(0.16, 1, 0.3, 1)` | Default for hovers, reveals |
| `--dur-fast`  | 140 ms | Hover state, focus ring |
| `--dur-base`  | 220 ms | Reveal, color shift |
| `--dur-slow`  | 420 ms | Page transitions, large reveals |

Motion is **functional, not decorative**. Buttons don't bounce. Cards lift 2 px on hover, never 8. Honor `prefers-reduced-motion`.

---

## Components

### Buttons

| Variant | Tokens | Use |
|---|---|---|
| Primary | `--ink-1000` bg, `--white` fg | Lead CTA — "Start a project" |
| Accent | `--orange-500` bg, `--white` fg | Sparingly — single in-page emphasis |
| Ghost | transparent bg, `--border-strong` outline | Secondary CTAs |
| Soft | `--ink-50` bg, `--ink-1000` fg | Tertiary, downloads |
| Link | underlined Geist Mono 11.5 px | Inline "Read the case study" |

Padding `12 / 22 px`, radius `--r-sm`, weight 600, size 14 px. Never two primary buttons side-by-side.

### Form inputs

Inputs are 15 px Geist on `--white`, padded `12 / 14 px`, radius `--r-sm`, with `--border-strong` border. Focus state: 1.5 px `--orange-500` border + 3 px `rgba(255,90,31,.18)` glow. Labels are 11 px Geist Mono `--ink-500` with 0.14 em tracking, uppercase.

### Badges & tags

Pill (`--r-pill`), 12 px Geist 500. Default is outline (`--border-strong` border, `--ink-700` fg). Featured fills with `--ink-1000`. New / status uses `--orange-50` bg + `--orange-700` fg. In-production uses outline + 6 px `--orange-500` dot.

### Project card (horizontal)

Grid `200 px / 1 fr`, 24 px gap. Square thumbnail left (`--r-md`, 1 px border), copy stack right: tag (Geist Mono `--accent-ink`), title (22 px / 600), sub (14 px `--ink-600`), CTA underline. Hover: `--ink-50` background, `--border` outline.

### Stat block

Four-column grid in a `--ink-50` strip, 24 / 22 px padding, `--ink-200` dividers. Number is 36 px / 600, label is 11 px Geist Mono `--ink-500`. Use `<em>` for `+`, `·`, etc. — they get colored `--orange-500` automatically.

### Testimonial

Block quote in display face — Geist 500, 26 px, line-height 1.32, tracking −0.012 em. Avatar 44 px circular, name 14 px / 600, role 12.5 px `--ink-500`. No quote-mark glyphs in the visual — typographic curly quotes only.

### Hero block

`1 fr / 1.1 fr` grid, 40 px gap. Left: 4:5 image-slot (`--r-lg`, 1 px border, `--ink-100` placeholder bg). Right: eyebrow → H1 → lead → CTAs (primary + ghost) → trust row (Geist Mono 12.5 px logo names).

---

## Voice & tone

### Principles

1. **Specific over clever.** Numbers, places, durations. "94k headsets activated," not "massive reach."
2. **Declarative over hedged.** "We ship in eight weeks." Not "We typically aim to ship in around eight weeks."
3. **Engineer-first.** We talk about systems, integrations, and outcomes — not "magic" or "wow."
4. **Short sentences.** Then a longer one for rhythm. Then short again.
5. **No metaverse, no synergy, no journey, no wow.** Ever.

### Eyebrow vocabulary

- `selected work`, `in good company`, `our practice`, `our approach`, `start a project`, `immersive technology consultancy`

### Headline patterns

- "Immersive technology, **engineered** for outcomes."
- "Built with brands that need to **move metrics**."
- "Strategy and craft for the brands **leading their industries.**"

The orange-italicized phrase carries the verb. Everything around it is plain.

---

## Applications

### Marketing site

White background. One dark anchor section (Contact) in `--ink-1000`. Hero: image-slot left, copy right. Stats strip in `--ink-50`. Services as 3-col grid with hairline borders. Work as horizontal cards (image left, copy right). Approach as 2-col with numbered steps. Testimonials as a single rotating quote in display face. Clients as a 6-col grid of image-slots.

### Business card

85 × 55 mm. Front: white card, `logo-next.png` upper-left, name + role lower-left in Geist 500 / 14 px. Back: `--ink-1000` flood, inverse logo centered.

### Email signature

```
[Name] · [Role]
Next  →  immersive technology
[email] · nextlatam.com
```

Three lines, Geist 14 px, name in `--ink-1000` 600, the rest in `--ink-600`.

### Slide deck (16:9)

White slides; one orange divider slide between sections. Title slide: H1 left, image-slot right. Section heads: 72 px Geist 600 with `--orange-500` italicized verb.

---

## Files

| Path | What |
|---|---|
| `tokens.css` | All CSS custom properties — color, type, spacing, radii, shadows, motion. |
| `assets/logo-next.png` | Primary wordmark for light surfaces. |
| `assets/logo-next-inverse.png` | Wordmark for dark surfaces. |
| `branding.html` | This manual, formatted for print/PDF. |
| `ui_kits/marketing-site/` | React + CSS reference build of the homepage. |
| `ui_kits/marketing-site/index.bundled.html` | Single-file standalone homepage. |
| `preview/*.html` | One card per token / component for the Design System tab. |

---

## Colophon

Authored 2026 for the Next LATAM relaunch. Geist by Vercel. All tokens are MIT-spirited internal-use; the brand mark and wordmark are property of Next LATAM.
