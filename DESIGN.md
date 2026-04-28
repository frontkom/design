---
title: Design System  Frontkom
source_urls:
  - https://frontkom.com/
  - https://frontkom.com/blog/ki-i-skyggene
captured: 2026-04-28
stack: Next.js + Tailwind v4 (utility-first, design tokens via CSS vars)
---

# Design System: Frontkom

**Project:** frontkom.com — corporate site + blog
**Source:** Live site analysis

## 1. Visual Theme & Atmosphere

Confident, modern, and unmistakably Norwegian-tech. The site reads as a **deep-night marketing site with editorial calm** — hero sections sit on near-black indigo (`#160046`), while content sections breathe on warm-white (`#F7F7F8`). The mood alternates between two registers:

- **Bold marketing surfaces** — saturated violet-to-coral gradients power H1s, primary buttons, and emphasis text. These gradients are the brand signature.
- **Quiet editorial surfaces** — long-form content (blog posts, case studies) is generous in whitespace, narrow in column width (`max-w-3xl`), and uses a desaturated charcoal (`#35323c`) for text rather than pure black. This produces a softer, more readable rhythm than typical SaaS sites.

The aesthetic is **airy, geometric, and slightly playful** — pill-shaped buttons, rounded card corners, no heavy shadows, no skeuomorphism. Density is moderate: enough whitespace to feel premium, not so sparse that the page feels empty. Animations are restrained (color/transform transitions at 150–200ms).

## 2. Color Palette & Roles

### Brand / Action

| Name | Hex | Role |
|---|---|---|
| **Vivid Electric Violet** | `#521CE4` | Primary brand accent; gradient terminus; hover-state link color; CTA gradient endpoint |
| **Royal Indigo** | `#4F1BE5` | Secondary violet (near-twin of `#521CE4`, used in subtle variants) |
| **Midnight Indigo** | `#160046` | Hero backgrounds, dark sections, footer; the site's "negative-space" canvas |
| **Deep Plum** | `#1E0060` / `#1A0054` | Slightly lighter indigo variants for layered backgrounds |
| **Magenta Burst** | `#BC25A9` | Mid-stop in primary brand gradient; standalone accent for tags/eyebrows |
| **Hot Coral-Pink** | `#FB1065` | High-energy accent (notifications, badges) |
| **Sunset Coral** | `#ED5E3F` / `#F86233` / `#F07040` | Gradient start; warm accent for editorial flourishes |
| **Soft Lavender** | `#C8B5FF` | Tinted highlight on dark backgrounds |

### Brand Gradient (signature)

```
linear-gradient(90deg, #ED5E3F → #BC25A9 → #521CE4)
```

Used for: H1 text fills (`bg-clip-text`), eyebrow labels, decorative bars, primary CTA backgrounds. A two-stop variant `#BC25A9 → #521CE4` is used for header contact buttons.

### Surface / Neutral

| Name | Hex | Role |
|---|---|---|
| **Soft Cloud Grey** | `#F7F7F8` | Primary section background (alternates with white and indigo) |
| **Hover Cloud Grey** | `#F0F0F2` | Hover state for grey card surfaces |
| **Border Mist** | `#E8E7EC` | Subtle dividers and card borders |
| **Quiet Lilac-Grey** | `#D4D2DC` | Soft contrast borders |
| **Pure White** | `#FFFFFF` | Card surfaces, button surfaces on dark, text on dark |

### Text / Foreground

| Name | Hex | Role |
|---|---|---|
| **Charcoal Plum (foreground)** | `#35323C` | All body text and headings on light backgrounds — chosen instead of pure black for warmth |
| Foreground at 80% opacity | `#35323CCC` | Body paragraphs (`text-foreground/80`) — primary reading color in articles |
| Foreground at 50% opacity | `#35323C80` | Captions, metadata |
| Foreground at 30% / 20% | `#35323C4D` / `#35323C33` | Disabled / tertiary text |
| White at 30% opacity | `#FFFFFF4D` | Body text on indigo backgrounds |

### Status

| Name | Hex | Role |
|---|---|---|
| **Forest Confirmation Green** | `#0B874B` | Success state |

## 3. Typography Rules

**Font system:** Two complementary Red Hat sibling families, loaded as Next.js font variables.

- **Display family:** `Red Hat Display` (`var(--font-red-hat-display)`) — used for `<h1>` only, set in `font-normal` (400) at very large sizes (`clamp(36px, 5.5vw, 80px)`) with tight `line-height: 1.15`. Often filled with the brand gradient via `bg-clip-text text-transparent` so the heading itself becomes the brand mark.
- **Sans family:** `Red Hat Text` (`var(--font-red-hat-text)`) — everything else: H2–H4, body, UI, buttons, captions.

**Weight scale:** Only three weights are used.
- `400` (normal) — body text, the H1 display
- `500` (medium) — H2/H3, button labels, link text
- `600` (semibold) — sparingly, for emphasis

**Headings.**
- **H1 (hero):** Display family, weight 400, `clamp(36px, 5.5vw, 80px)`, line-height `1.15`, gradient-filled.
- **H1 (article):** Sans family, weight 500, `clamp(28px, 4vw, 48px)`, line-height tight, foreground charcoal.
- **H2 (marketing):** `clamp(28px, 3.5vw, 52px)`, weight 500, leading-tight.
- **H2 (article):** `clamp(22px, 2.5vw, 32px)`, weight 500, with `mt-12 mb-4` rhythm.

**Body.** `17px` with `line-height: 1.75` (`leading-[1.75]`) at 80% foreground opacity — generous, readable, slightly looser than Tailwind's default prose.

**Eyebrow / metadata.** `11–13px`, `tracking-widest`, `uppercase`, often filled with the brand gradient. This is a strong recurring motif — small uppercase labels with rainbow fill above section titles.

**Letter-spacing.** Default for most copy; `tracking-wide` (.04em) and `tracking-widest` (.1em) reserved for uppercase eyebrows and small UI labels.

## 4. Component Stylings

### Buttons
- **Shape:** Pill-shaped (`rounded-full`, i.e. fully rounded). Sharp corners are not used for actions.
- **Primary CTA on dark surfaces:** White fill, charcoal text, `px-6 py-3.5`, weight 500. Hover dims fill to 90% opacity.
- **Primary CTA in nav:** Linear-gradient fill `#BC25A9 → #521CE4`, white text, smaller `px-4 py-2`, weight 400.
- **Decorative gradient hover sweep:** Some buttons layer a coral-to-violet gradient (`#ED5E3F → … → #521CE4`) at `opacity:0` underneath, presumably revealed on hover for a sweep effect.
- **Transition:** `transition-colors duration-150` is the standard interaction rhythm.

### Cards / Containers
- **Corner radius:** Uses Tailwind's radius scale plus literal pixel values. Common values: `0.5rem` (`md`), `0.75rem` (`xl`), `1rem` (`2xl`), and bespoke `20px / 24px / 28px` for hero cards. **Pill** (`999px` / fully-round) for actions and tags.
- **Background:** `#F7F7F8` for the default light card; `#160046` for dark hero cards.
- **Hover:** Light cards shift to `#F0F0F2`. No transform-on-hover; only color.
- **Shadow:** **Effectively flat.** The stylesheet exposes Tailwind's shadow ring scaffolding but no custom drop shadows. Depth comes from color contrast, not elevation.
- **Padding:** Cards use generous `p-8` to `p-10` and minimum heights (`min-h-64 → min-h-80`).

### Inputs / Forms
Forms are minimal on the public marketing site (the contact CTA links to a separate page). Where present, inputs follow Tailwind's neutral defaults with the `#E8E7EC` border treatment and rounded corners matching the local card radius.

### Eyebrow / Label Pattern
A defining repeated component:
```
<p class="text-sm font-medium tracking-widest uppercase
         text-transparent bg-clip-text
         bg-linear-to-r from-[#ED5E3F] via-[#BC25A9] to-[#521CE4]">
```
Used above section titles and as category tags. Appears on most major sections — treat as a first-class component.

### Header / Nav
- Fixed-height row, `h-[60px]`, `max-w-7xl mx-auto`, horizontal padding `px-4 sm:px-6`.
- Plain text links + a single gradient pill CTA on the right.
- Norwegian/English language toggle (`NO/EN`) sits in nav.

### Footer
- Dark indigo (`#160046`) with white text at varying opacities (40%, 30%, 20%) to create hierarchy.
- 4-column grid on desktop (`grid-cols-2 lg:grid-cols-4`), generous gap (`gap-8 lg:gap-20`).
- Includes Miljøfyrtårn (eco) certification badge — a real-world trust signal that's part of the brand.

## 5. Layout Principles

- **Container widths:** Three tiers.
  - `max-w-7xl` (≈1280px) — marketing rows, nav, footer.
  - `max-w-4xl` — featured-image article header.
  - `max-w-3xl` (≈768px) — long-form article body. **This is the editorial canvas.**
- **Horizontal padding:** Always `px-4 sm:px-6 lg:px-8` — consistent across every container.
- **Vertical rhythm:** Sections breathe with `py-14`, `py-16`, `py-20 sm:py-24 lg:py-28`. Hero sections claim `min-h-dvh` — full viewport height on every device.
- **Section alternation:** Sections alternate background between three surfaces — white, `#F7F7F8` cloud-grey, and `#160046` midnight-indigo — to create visual rhythm without dividers.
- **Heading-to-body spacing:** `mb-5` to `mb-10` after headings; `mt-12` before secondary headings in articles.
- **Grid usage:** Logo carousels and case-study grids use `grid grid-cols-2 lg:grid-cols-4`. Cards align to a coarse, visible grid rather than overlap or asymmetric collage.
- **Responsive type:** Almost every text size uses `clamp()` (e.g. `clamp(15px, 1.3vw, 20px)`) so type scales fluidly with viewport — no abrupt breakpoints in headings.

## 6. Motion & Interaction

- Transitions are universally `transition-colors duration-150` or `duration-200`.
- No spring/bounce, no large transforms — interactions are flat color shifts only.
- Decorative gradient overlays on buttons sit at `opacity:0` and presumably fade in on hover.

## 7. Recurring Brand Motifs (use these to keep new screens on-brand)

1. **Gradient-filled headlines** — H1 hero text rendered as `bg-clip-text text-transparent` with the coral-magenta-violet gradient.
2. **Uppercase, wide-tracked, gradient-filled eyebrows** above section titles.
3. **Three-surface alternation** — white → cloud-grey → midnight-indigo.
4. **Pill buttons only**, never square corners on actions.
5. **Charcoal-plum (`#35323C`) instead of black** for all foreground text.
6. **Generous reading column** at `max-w-3xl` for any long-form text.
7. **Flat cards, no shadows** — depth comes from background contrast and corner radius, not elevation.
