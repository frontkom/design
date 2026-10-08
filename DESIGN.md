---
version: alpha
name: Frontkom
description: >
  Design system for Frontkom, a technology-driven agency working across
  Norway, Portugal and Poland. Confident, modern, and brand-forward, with a
  saturated coral-magenta-violet gradient as the recurring signature device.
  The system supports two equal default canvases: deep indigo for brand and
  advertising, and white for web and editorial. Values come from the official
  Frontkom brand book; usage patterns come from active brand collateral (web,
  ads, posters).
colors:
  brand: "#F86233"
  primary: "#F86233"
  background: "#FFFFFF"
  indigo: "#1A0054"
  background-dark: "#160046"
  muted: "#F7F7F8"
  foreground: "#35323C"
  on-dark: "#FFFFFF"
  foreground-subtle: "#9A98A0"
  link: "#4F1BE5"
  link-on-dark: "#C8B5FF"
  link-hover: "#3E15B4"
  action: "#521CE4"
  action-hover: "#3E15B4"
  warning: "#FB1065"
  grey-light: "#E8E7EC"
  grey: "#D4D2DC"
  watermark-on-indigo: "#22006C"
  pastel-rose: "#F7D6DF"
  pastel-magenta: "#F0CFEC"
  pastel-purple: "#E4CEF4"
  pastel-blue: "#D9CDF9"
  gradient-1: "#F86233"
  gradient-2: "#DA446E"
  gradient-3: "#BC25A9"
  gradient-4: "#861FCB"
  gradient-5: "#521CE4"
typography:
  hero:
    fontFamily: Red Hat Display
    fontSize: 80px
    fontWeight: 500
    lineHeight: 92px
    letterSpacing: -0.01em
  h1:
    fontFamily: Red Hat Display
    fontSize: 60px
    fontWeight: 500
    lineHeight: 69px
    letterSpacing: -0.01em
  h2:
    fontFamily: Red Hat Display
    fontSize: 45px
    fontWeight: 500
    lineHeight: 52px
  h3:
    fontFamily: Red Hat Display
    fontSize: 34px
    fontWeight: 500
    lineHeight: 39px
  h4:
    fontFamily: Red Hat Display
    fontSize: 25px
    fontWeight: 500
    lineHeight: 29px
  h5:
    fontFamily: Red Hat Display
    fontSize: 19px
    fontWeight: 500
    lineHeight: 22px
  poster:
    fontFamily: Red Hat Display
    fontSize: 107px
    fontWeight: 500
    lineHeight: 123px
    letterSpacing: 0.02em
  lead:
    fontFamily: Red Hat Text
    fontSize: 22px
    fontWeight: 400
    lineHeight: 32px
  body:
    fontFamily: Red Hat Text
    fontSize: 17px
    fontWeight: 400
    lineHeight: 27px
  body-sm:
    fontFamily: Red Hat Text
    fontSize: 14px
    fontWeight: 400
    lineHeight: 22px
  quote:
    fontFamily: Red Hat Text
    fontSize: 25px
    fontWeight: 400
    lineHeight: 34px
  label:
    fontFamily: Red Hat Text
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
  spec:
    fontFamily: Red Hat Text
    fontSize: 13px
    fontWeight: 400
    lineHeight: 20px
  eyebrow:
    fontFamily: Red Hat Text
    fontSize: 12px
    fontWeight: 500
    lineHeight: 16px
    letterSpacing: 0.1em
  ad-headline:
    fontFamily: Red Hat Display
    fontSize: 80px
    fontWeight: 500
    lineHeight: 92px
  ad-body:
    fontFamily: Red Hat Text
    fontSize: 34px
    fontWeight: 400
    lineHeight: 46px
  ad-detail:
    fontFamily: Red Hat Text
    fontSize: 25px
    fontWeight: 400
    lineHeight: 34px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  "2xl": 48px
  "3xl": 64px
  "4xl": 96px
  spacing-section-y: 96px
  container-x: 16px
  container-x-md: 24px
  container-x-lg: 32px
rounded:
  sm: 8px
  md: 12px
  lg: 20px
  full: 9999px
components:
  hero-gradient:
    textColor: "{colors.brand}"
    typography: "{typography.hero}"
  gradient-flow-emphasis:
    textColor: "{colors.brand}"
    typography: "{typography.h1}"
  gradient-bar:
    backgroundColor: "{colors.brand}"
    height: 8px
  watermark-positive:
    backgroundColor: "{colors.muted}"
    textColor: "{colors.grey-light}"
  watermark-on-white:
    backgroundColor: "{colors.background}"
    textColor: "{colors.grey-light}"
  watermark-negative:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.watermark-on-indigo}"
  watermark-on-gradient:
    backgroundColor: "{colors.brand}"
    textColor: "{colors.on-dark}"
  decorative-stripe:
    backgroundColor: "{colors.primary}"
    rounded: "{rounded.md}"
    height: 4px
    width: 64px
  button-primary:
    backgroundColor: "{colors.action}"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-primary-hover:
    backgroundColor: "{colors.action-hover}"
    textColor: "{colors.on-dark}"
    textDecoration: underline
  button-brand:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-brand-hover:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    textDecoration: underline
  button-on-dark:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-on-dark-hover:
    backgroundColor: "{colors.link-on-dark}"
    textColor: "{colors.foreground}"
    textDecoration: underline
  card-light:
    backgroundColor: "{colors.muted}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: 32px
  card-light-bordered:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: 32px
  card-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.lg}"
    padding: 40px
  body-paragraph:
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
  body-paragraph-on-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body}"
  caption:
    textColor: "{colors.foreground}"
    typography: "{typography.body-sm}"
  quote:
    textColor: "{colors.indigo}"
    typography: "{typography.quote}"
  quote-on-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.quote}"
  quote-emphasis:
    textColor: "{colors.brand}"
    typography: "{typography.quote}"
  quote-name:
    textColor: "{colors.foreground}"
    typography: "{typography.h5}"
  quote-role:
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
  quote-name-on-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.h5}"
  quote-role-on-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body}"
  link:
    textColor: "{colors.link}"
    typography: "{typography.body}"
  link-on-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.link-on-dark}"
    typography: "{typography.body}"
  warning-badge:
    backgroundColor: "{colors.warning}"
    textColor: "{colors.indigo}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    padding: 4px 12px
  nav:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    height: 60px
  footer:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body-sm}"
    padding: 64px 32px
  input:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  divider:
    backgroundColor: "{colors.grey-light}"
    height: 1px
  divider-strong:
    backgroundColor: "{colors.grey}"
    height: 1px
  logo-frame-diamond:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: diamond
    padding: 32px 48px
  logo-frame-arrow:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: arrow
    padding: 32px 48px
  logo-frame-rounded:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: rounded-square
    rounded: "{rounded.lg}"
    padding: 32px 48px
  poster-title:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.brand}"
    typography: "{typography.poster}"
  slide-cover:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.h1}"
    padding: 72px 96px
  slide-content:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body}"
    padding: 64px 96px
  slide-heading-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.indigo}"
    typography: "{typography.h2}"
  slide-content-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
    padding: 64px 96px
  slide-chapter-divider:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    typography: "{typography.h1}"
    padding: 96px
  slide-statement:
    backgroundColor: "{colors.background}"
    textColor: "{colors.indigo}"
    typography: "{typography.h1}"
    padding: 96px
  card-rose:
    backgroundColor: "{colors.pastel-rose}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-2}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  card-magenta:
    backgroundColor: "{colors.pastel-magenta}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-3}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  card-purple:
    backgroundColor: "{colors.pastel-purple}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-4}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  card-blue:
    backgroundColor: "{colors.pastel-blue}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-5}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  slide-bubble-dark:
    backgroundColor: "{colors.indigo}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.lg}"
    padding: 24px 32px
  slide-bubble-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: 24px 32px
  process-step-1:
    backgroundColor: "{colors.gradient-1}"
    rounded: "{rounded.full}"
    size: 16px
  process-step-2:
    backgroundColor: "{colors.gradient-2}"
    rounded: "{rounded.full}"
    size: 16px
  process-step-3:
    backgroundColor: "{colors.gradient-3}"
    rounded: "{rounded.full}"
    size: 16px
  process-step-4:
    backgroundColor: "{colors.gradient-4}"
    rounded: "{rounded.full}"
    size: 16px
  process-step-5:
    backgroundColor: "{colors.gradient-5}"
    rounded: "{rounded.full}"
    size: 16px
  signature-highlight:
    textColor: "{colors.brand}"
    typography: "{typography.h1}"
---

# Frontkom Design System

## Logo usage: read this before generating any visual

The Frontkom wordmark is `assets/logo-frontkom.svg`
(canonical source: https://github.com/frontkom/design/blob/main/logo-frontkom.svg).
**Do not reconstruct it, and never create variants of the logo.** Always
reference, embed, or copy the actual SVG file from
`assets/logo-frontkom.svg`. AI agents have a strong tendency to redraw
logos from prose descriptions; the result is always wrong. If you cannot
read the SVG file, leave a placeholder and tell the user. Do not draw
"two arrows" or "a `<>` shape" or "frontkom in some font."

What the actual logo contains (so you recognize correctness):

- The symbol is two filled, rounded shapes that read as a stylised left
  arrow and a stylised right arrow, constructed on a 45° geometric grid
  (brand book 3.0 p. 7). It is **not** the `<>` characters or angle brackets.
- The wordmark "frontkom" is set in a **custom-drawn typeface specific
  to the logo**: paths converted from a tweaked Red Hat sibling. The
  letterforms are part of the SVG; they are not live text. Do not retype
  "frontkom" in Red Hat Text and assume that's correct. It is not.
- The full lockup has `viewBox="0 0 560 107"`. All paths fill
  `{colors.foreground}` (`#35323C`) so the logo inverts cleanly to
  `{colors.on-dark}` on indigo by setting `fill="#FFFFFF"` on the paths
  (or by applying a CSS filter).

How to use it:

- **HTML / web:** `<img src="/assets/logo-frontkom.svg" alt="Frontkom">`
  or inline `<svg>...</svg>` with the path data copied verbatim from the
  asset file.
- **React / JSX:** import the SVG as a component and render it. Do not
  hand-write paths.
- **Slides / PDFs / PowerPoint:** insert the SVG file. Do not recreate.

### Logo on indigo (`indigo`): ALWAYS invert

When the logo sits on `indigo` or any other dark surface, it
must be rendered in white. **The default is white logo directly on
indigo, not a white frame containing a charcoal logo.** A white logo
frame (diamond, arrow or rounded square) is reserved for specific advertising layouts where
the logo is the primary subject (see the `logo-frame-*` components); for
social media, posters, slides, app screens, and most other dark-canvas
uses, place the inverted logo directly on the indigo background.

Three SVG files are the single source of truth. Link to, embed, or copy
these exact files. Never recreate the logo or make variants of it:

- `assets/logo-frontkom.svg`: charcoal logo (full lockup) for **light backgrounds**.
  Source: https://github.com/frontkom/design/blob/main/logo-frontkom.svg
- `assets/logo-frontkom-on-dark.svg`: white logo (full lockup) for **indigo / dark
  backgrounds**.
  Source: https://github.com/frontkom/design/blob/main/logo-frontkom-on-dark.svg
- `assets/logo-frontkom-symbol-outlined.svg`: outlined version of the symbol
  only (no wordmark). Use it to close a space at the edge of a composition
  (brand book 3.0 p. 23). `viewBox="0 0 110 107"`.
  Source: https://github.com/frontkom/design/blob/main/logo-frontkom-symbol-outlined.svg

Pick the file that matches the background and use case; do not invert at runtime.

Decision shortcut for AI agents:

- Dark/indigo background + logo present → use `logo-frontkom-on-dark.svg`,
  no frame (default)
- Light/white background + logo present → use `logo-frontkom.svg` as-is
- Frame around logo → only when the brief explicitly calls for a
  formal advertising lockup (e.g., display banner ad with logo as
  hero element, like the 580×500 and 980×300 banner formats)

If the agent does not have access to either SVG, the correct response is
to ask the user to provide it or to use a text placeholder
("[Frontkom logo]"), not to attempt a freehand SVG.

### Clear space & spacing

Clear space is measured on the lowercase **r**, NOT on the symbol height
(the old "clear space = symbol height" rule is wrong). Measured on the
2021 lockup (the orange plate is 560×165 with the 476×81 logo area
inside, exactly 42px of air on all four sides; the `r` is 29×42):

- **Clear space** around the lockup = the **height of the `r`** (the
  x-height of the logotype) = **8.82% of the lockup width**. Keep at
  least this much empty space on all four sides.
- **Space between symbol and logotype** = the **width of the `r`** =
  **6.1% of the lockup width**. ("Space between symbol and logotype
  equals the width of r" is verbatim from the 2021 file, on a page that
  never made the PDF export.)

The symbol's own height is ~82 at the same scale, nearly double the
clear space, so never use the symbol height as the clear-space measure.

## Font loading: set this up before generating any visual

Frontkom uses two Red Hat sibling families: **Red Hat Display** for all
headings and **Red Hat Text** for everything else (brand book 3.0 p. 16). Both are open-source via Google Fonts and
SIL Open Font License.

The font files are provided in `assets/fonts/` as variable TTFs:

- `RedHatText-VariableFont_wght.ttf`
- `RedHatText-Italic-VariableFont_wght.ttf`
- `RedHatDisplay-VariableFont_wght.ttf`
- `RedHatDisplay-Italic-VariableFont_wght.ttf`

### Loading strategy by context

**For web (HTML/CSS/React), Google Fonts CDN is preferred.** It's
fastest, cached across the internet, and works in every AI rendering
environment that has network access:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;0,500;1,400;1,500&family=Red+Hat+Text:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
```

Or via CSS `@import`:

```css
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;0,500;1,400;1,500&family=Red+Hat+Text:ital,wght@0,400;0,500;1,400;1,500&display=swap');
```

The URL above includes only the weights and styles the system uses:
400 and 500, regular and italic, in both families. Display is used in
500 for headings. Text is used in 400 for paragraphs and 500 for labels
and eyebrows. Don't load other weights.

**For local development or when the CDN isn't reachable**, use the
provided TTF files via `@font-face`:

```css
@font-face {
  font-family: 'Red Hat Text';
  src: url('/assets/fonts/RedHatText-VariableFont_wght.ttf') format('truetype-variations');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Red Hat Text';
  src: url('/assets/fonts/RedHatText-Italic-VariableFont_wght.ttf') format('truetype-variations');
  font-weight: 100 900;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Red Hat Display';
  src: url('/assets/fonts/RedHatDisplay-VariableFont_wght.ttf') format('truetype-variations');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Red Hat Display';
  src: url('/assets/fonts/RedHatDisplay-Italic-VariableFont_wght.ttf') format('truetype-variations');
  font-weight: 100 900;
  font-style: italic;
  font-display: swap;
}
```

Then reference normally: `font-family: 'Red Hat Text', sans-serif;`.

**For slides, presentations, and desktop documents** (Keynote, Google
Slides, PowerPoint, Word, Figma): install the TTF files locally on the
operating system. Drag the `.ttf` files to the system font book on
macOS, or right-click → Install on Windows. Once installed, the
families show up by name in any application's font picker.

### Fallback stack

If neither Google Fonts nor local TTFs load, the fallback should be a
generic sans that approximates Red Hat's geometric humanist character:

```css
font-family: 'Red Hat Text', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
```

For headings:

```css
font-family: 'Red Hat Display', 'Red Hat Text', system-ui, -apple-system, sans-serif;
```

Always include `system-ui` in the stack so unstyled output still looks
deliberate, not broken.

### What AI agents should NOT do

- Don't substitute a different font (Inter, Roboto, Helvetica) and
  claim it's "close enough." It isn't. Red Hat's character markers
  (the open `a`, the angled `t` terminal, the geometric `o`) are part
  of the brand.
- Don't load every weight. The system uses 400 and 500 only. Don't
  load 300, 600, 700, 800 or 900. Never set headings or labels in bold
  (700): headings are Red Hat Display Medium (500). Emphasis inside a
  sentence follows the same rule (see Typography / Emphasis in running
  text).
- Don't use the variable font's weight axis to invent weights between
  or beyond 400 and 500.

## Overview

Frontkom is a technology-driven agency working across Norway, Portugal
and Poland. The brand reads as **confident,
modern, and brand-forward**, with a saturated coral-magenta-violet gradient
as the recurring signature device.

The system supports **two equal default canvases**, chosen by context:

- **Indigo (`#1A0054`)** is the canonical brand canvas. Use it for
  advertising, posters, social media, and any communication
  *about* Frontkom. Gradient text (website hero, covers and ads) and orange
  accents have the most impact on indigo.
- **White (`#FFFFFF`)** is the editorial and web canvas. Use it for the
  website, blog posts, case studies, and any communication *from*
  Frontkom about its work. White gives long-form content room.

Neither canvas is the overall default. Indigo is the default for ads,
white for the web. Presentations mix the two (see Slides / Canvas). The website
stays light, with the occasional dark section as a break in the rhythm.
The wrong canvas for the context is more wrong than the wrong color
within the right canvas.

The defining brand device is **the five-stop gradient**: Frontkom orange
(`#F86233`) through pink, magenta, and violet to indigo-violet
(`#521CE4`). The gradient appears in three distinct forms (see Components
/ Gradient treatments) and is the single strongest signal that something
is Frontkom.

The audience is enterprise buyers, editorial readers, and event audiences
in Norwegian and English. NO and EN are first-class equals; the language
toggle is a component, not an afterthought.

## Colors

Brand book 3.0 p. 11. Orange, indigo and the gradient are the main
colours. The rest are secondary and supporting colours.

### Main colours

- **`brand` `#F86233`** (Pantone 1585 C, C0 M66 Y99 K0): Frontkom
  orange. The accent. Gradient start, highlighted phrase, quote opening.
- **`indigo` `#1A0054`** (Pantone 2745 C, C100 M98 Y0 K22): the brand
  canvas. White text, gradient accents.
- **Brand gradient** `gradient-1` to `gradient-5`, `#F86233` to
  `#521CE4`. See below.

### Canvases

- **`indigo` `#1A0054`**: the brand canvas. Default for advertising,
  and for cover, chapter and closing slides.
- **`background` `#FFFFFF`**: the editorial canvas. Default for the web.
- **`muted` `#F7F7F8`**: section background on web that pairs with
  white for rhythm.
- **`background-dark` `#160046`**: a shade deeper than indigo. Hover
  state on indigo buttons.

### Text

All text on white uses `foreground` (`#35323C`), never pure `#000000`.

One text colour for headings and paragraphs (brand book 3.0 p. 20).
Build hierarchy with size, not with lighter greys. One exception: in
presentations, headings on white slides are `indigo` (see Slides).

- **`foreground` `#35323C`**: all headings, body text and captions on
  white and light backgrounds. 12.55:1 on white. Exception: on card
  colours the card title takes the card's `emphasisColor`.
- **`brand` `#F86233`** as text: one highlighted phrase, the opening of a
  quote, and headings at 24px or larger. Never body copy: 3.09:1 on
  white passes for large text only. 5.79:1 on indigo.
- **`foreground-subtle` `#9A98A0`**: page numbers, token names and
  metadata only. Fails AA for running text.

On indigo, all text is `on-dark` (`#FFFFFF`), 17.92:1.

### Links

`link` (`#4F1BE5`) on light surfaces, 8.01:1 on white. `link-on-dark`
(`#C8B5FF`) on indigo, 9.82:1.

### Status

`warning` (`#FB1065`) is the only status colour and is used only for
warning states. Don't reuse it as accent or emphasis; that is
`brand`'s job. Text on warning is indigo (4.58:1).

### Greys

`grey-light` (`#E8E7EC`) for card borders and table lines on light
surfaces, and the watermark on white. `grey` (`#D4D2DC`) for stronger
lines. `muted` (`#F7F7F8`) for backgrounds.

### Watermark

`watermark-on-indigo` (`#22006C`) is the filled symbol as texture on
indigo, 1.10:1. Texture only, never for content.

### Contrast

Brand book 3.0 p. 14. Check these ratios before you pair two colours.
Ratios follow WCAG 2.2: 4.5:1 for normal text, 3:1 for large text and
for non-text elements that carry meaning.

| Pairing | Ratio | Verdict |
|---|---|---|
| foreground on white | 12.55:1 | AAA |
| link on white | 8.01:1 | AA |
| white on gradient-5 | 7.94:1 | AA |
| brand on white | 3.09:1 | Large only |
| white on indigo | 17.92:1 | AAA |
| link-on-dark on indigo | 9.82:1 | AAA |
| brand on indigo | 5.79:1 | AA |
| indigo on warning | 4.58:1 | AA |
| watermark-on-indigo on indigo | 1.10:1 | Texture only |

Beyond contrast:

- Don't use colour alone to show meaning. Pair it with text, an icon or
  a shape.
- Keep a visible focus ring at 3:1 or better against its surroundings.
- Interactive targets are at least 24px, and 44px on touch.

### The brand gradient

```css
background: linear-gradient(90deg,
  #F86233 0%,    /* gradient-1 (= brand) */
  #DA446E 25%,   /* gradient-2 */
  #BC25A9 50%,   /* gradient-3, middle stop */
  #861FCB 75%,   /* gradient-4 */
  #521CE4 100%   /* gradient-5 */
);
```

Brand book 3.0 p. 12. Five stops, from the 2021 book's seven-stop
colour harmony. Use the gradient for digital change, process steps or
time, always with orange first and violet last. Use it as a fill or a
stripe along the top edge. Set a heading in the gradient only for the
website hero, the title on any cover, and in ads. Keep the blend smooth.
Never use it as a button fill, and never on small text: below heading
size it looks muddy and the contrast is too low. See Components /
Gradient treatments for the three canonical applications.

## Typography

Per brand book 3.0 p. 16 and 17: **Red Hat Display Medium (500)** for all
headings, **Red Hat Text Regular (400)** for paragraphs. Each heading size
is a third larger than the one below it: 19, 25, 34, 45, 60 and 80px.
Line heights follow the same steps.

Ads add one size at the top of the scale: **`poster`** (107px, the next
step after 80, `letterSpacing: 0.02em`), used for short event titles
like "BAKGÅRDSFEST". Posters can be set in ALL CAPS, the only place in
the system where ALL CAPS is permitted for headings (the eyebrow uses
uppercase but is not a heading).

### Roles

- **`hero`**: Display 500, 80/92. The marketing H1, also with gradient
  text fill.
- **`h1`**: Display 500, 60/69. Page titles, slide titles, and the
  `signature-highlight` size.
- **`h2`**: Display 500, 45/52. Major section headings.
- **`h3`**: Display 500, 34/39. Sub-headings.
- **`h4`**: Display 500, 25/29. Subsection headings.
- **`h5`**: Display 500, 19/22. Card titles and small headings. Sits
  close to `body`, so lean on size and placement to keep it reading as
  a heading.
- **`poster`**: Display 500, 107/123, slightly increased letter spacing.
  Event posters and short ad headlines (often ALL CAPS).
- **`lead`**: Text 400, 22/32. For the most prominent paragraph at the
  start of a text block. Use it once.
- **`body`**: Text 400, 17/27. Workhorse paragraph text. Keep paragraphs
  to four to eight lines, one thought each, with vertical space between.
- **`body-sm`**: Text 400, 14/22. Image captions, chart details, fine
  print. Use sparingly.
- **`quote`**: Text 400, 25/34. Quote blocks.
- **`label`**: Text 500, 14/20. Buttons, UI labels.
- **`spec`**: Text 400, 13/20. Token names, values, page numbers.
- **`eyebrow`**: Text 500, 12/16, uppercase, `tracking: 0.1em`. Only for
  the chapter label and page number in long documents like the brand
  book. Never above a heading on web, slides or ads.

Text is always left-aligned (brand book 3.0 p. 18). Balance a
composition by distributing weight, not by centring it.

### Fluid sizing

Token values are desktop maximums. On web, scale fluidly with `clamp()`
for mobile, e.g. `clamp(40px, 6vw, 80px)` for hero. Don't use abrupt
breakpoints.

On fixed canvases (ads, posters, slides, e.g. a 1:1 social ad) there is
no fluid range, so the headline must be **scaled down to fit the frame,
and text must never be clipped or run off the edge.** Shrink the heading
size (and re-wrap) until the longest line fits with margin to spare.
Budget width for the longest word before locking a size. Remember
Norwegian runs ~10 to 15% longer than English, and ALL CAPS is wider than
sentence case (e.g. "ORGANISASJONER"). If it still won't fit, reduce the
size further or shorten the copy. Never crop.

### Casing

Sentence case for headings and body text by default. ALL CAPS is
permitted only on the `poster` size for standalone event titles, and on
the `eyebrow` token. Title Case is not used. Never mix cases within a
single heading. In particular, a `gradient-flow-emphasis` headline is
sentence case throughout; the gradient clause is NOT set in ALL CAPS.

### Emphasis in running text

The system has no weight above 500, and that includes emphasis inside a
sentence (a key phrase in a callout, a paragraph or a card).

- Set the emphasised phrase in Red Hat Text Medium (500), never Bold
  (700).
- On white and light surfaces the phrase also takes `indigo`
  (`#1A0054`), so the step from 400 to 500 is visible against
  `foreground` body text. On indigo it stays white, 500.
- At most one emphasised phrase per paragraph or callout. If most of
  the text needs emphasis, rewrite it instead.
- Don't use `brand` orange for emphasis in body text: it measures
  3.09:1 on white and fails AA below 24px. Orange belongs to the one
  highlighted heading phrase per page (`signature-highlight`).
- Don't use italics or underline for emphasis. Underline means link.

## Layout

### Alignment

> Brand book principle (3.0 p. 18): *"Text should always be left-aligned."*

This applies everywhere: web, documents, presentations and ads. Balance
a composition by distributing weight, not by centring it.

### Container widths (web)

- **`max-w-7xl` (≈1280px)**: marketing rows, nav, footer.
- **`max-w-4xl` (≈896px)**: featured-image article header.
- **`max-w-3xl` (≈768px)**: long-form article body. The editorial
  canvas. Every piece of running prose belongs here.

### Horizontal padding (web)

`container-x` → `container-x-md` → `container-x-lg`
(16/24/32px → `px-4 sm:px-6 lg:px-8`).

### Section alternation (web)

Marketing pages rotate through three surfaces, `background` (white),
`muted` (cloud grey) and `indigo`, to create rhythm. Two adjacent sections must never share the same surface.
A typical landing page:
white (hero) → indigo (stats) → muted (services) → white (editorial) →
indigo (CTA) → footer.

### Asymmetrical balance

Brand book guidance (3.0 p. 18): asymmetrical layouts are encouraged, but
balance the visual weight, don't collide it.

### Bilingual layout

Norwegian copy runs ~10 to 15% longer than English. Design with this slack
built in.

### Advertising layout

Indigo canvas is the default. Compositions are typically split between
a content area (text, image) and a logo area (with the white logo frame,
see Components). Aspect ratios common in the system: 320×250, 580×500,
180×500, 980×300, 320×400. The white logo frame adapts its shape to
the ad's proportions: square diamond for tall formats, right-pointing
arrow for wide formats, rounded square for narrow vertical formats.

## Elevation & Depth

The system is **flat**. No drop shadows. Depth comes from:

1. **Surface contrast**: alternating
   `background` / `muted` / `indigo` on web.
2. **Outlines**: a 1px `grey-light` outline on all four sides of a
   light card. Never a coloured edge on one side (see Shapes / Card and
   box edges).
3. **Corner radius**: `rounded.lg` (cards, panels, and the logo frame)
   creates softness without shadow.
4. **Symbol as watermark** (brand book 3.0 p. 23). The filled symbol
   scaled to roughly 90% of the frame width and pushed past two edges,
   so no complete shape is visible. Keep its proportions. Place it on
   the side opposite the text, normally the right, and let it run past
   the edges nearest to it, with most of the shape inside the frame.
   Keep it out of the logo's clear space (brand book 3.0 p. 5): when the
   logo sits bottom right, the mark ends above that clear space; when the
   logo is on the other side, as on a cover, the mark can also run past
   the bottom edge. On wide formats such as 16:9 slides, scale it to
   about the frame height instead (around 1120 px wide on 1920 × 1080).
   Four variants:
   - **Positive**: `grey-light` `#E8E7EC` on `muted` `#F7F7F8`, 1.15:1.
     Light web sections and documents on `muted`.
   - **On white**: `grey-light` `#E8E7EC` on `background`, 1.23:1.
     Statement slides and light content slides (`watermark-on-white`).
   - **Negative**: `watermark-on-indigo` `#22006C` on `indigo`, 1.10:1.
     Chapter openers and closing slides.
   - **On the gradient**: white at 50% opacity, 1.74:1 to 2.95:1 across
     the ramp. Social banners and ads on a gradient surface.
   Keep the mark below 3:1 against its background. Never place text
   inside it, and never use it in place of the logo.
5. **Outlined symbol** (brand book 3.0 p. 23). The symbol can also be
   used as an outline, to close a space at the edge of a composition.
   It is an option, never a required element: no page type, cover
   included, has to carry it.

Indigo tints are made by **lightening along the hue, not by mixing in a
neutral.** `#22006C` keeps green at zero like `#1A0054`, so it stays
clean. Use only `watermark-on-indigo`, never a mixed indigo tint.

If `box-shadow` feels needed, increase contrast or radius instead.

## Shapes

Brand book 3.0 p. 24. Round the corners to soften the expression.

- **Buttons**: `rounded.full` (pill). Buttons only, so the pill shape
  always signals an action.
- **Cards**: `rounded.lg` (20px). Cards, panels, image frames and
  anything that holds content on a page. The same on web and slides.
- **Inputs**: `rounded.sm` (8px), so they are not mistaken for buttons.
- **Small and nested elements**: `rounded.md` (12px). Colour swatches,
  tags, chips, badges, the language toggle, thumbnails, and anything
  inside a card. An element inside a card takes 12px, never the card's
  own 20px, so the two surfaces stay separate.
- **Logo frame (advertising only)**: `rounded.lg` (20px) when rendered
  as a rounded square; full diamond / arrow shapes are SVG-drawn paths
  matching the symbol geometry.
- **The symbol**: built on a 45° grid (brand book 3.0 p. 7). Every
  angle in the mark is a multiple of 45 degrees. Don't stretch or
  recompose it.

### Card and box edges

A card or box has one colour: its fill. This applies to cards, info
boxes, callouts, notes and text blocks on web, slides and documents.

- Never add a coloured border on one edge only: no top stripe, no left
  stripe, no accent bar along any side. This is a common AI default;
  leave it out even when an existing design or a reference has it.
- The only permitted edge is a 1px `grey-light` outline on all four
  sides (`card-light-bordered`), used when a white card sits on
  `muted`. It is a full outline, never a single side.
- A callout or note is a `muted` or white box, or a card colour.
  Emphasis comes from the text (see Typography / Emphasis in running
  text), not from a stripe beside it.
- To show sequence or category, use the card colours or the process
  step markers, not coloured edges.
- Lines that are content stay: table lines (`divider`), a timeline axis
  and the `gradient-bar` on the top edge of covers, chapter and closing
  slides. They are not edges on a box.

## Components

### Gradient treatments

The signature device. Three forms. Pick by context.

#### 1. `hero-gradient`: gradient text fill

The whole heading takes the gradient as its color. **Only for the
website hero, in ads, and for the title on any cover** (brand book 3.0
p. 12, and the cover of the brand book itself), on white or indigo.

**Every cover may take it**, whatever the format: presentations,
documents, reports, proposals, PDFs, brochures, case studies and the
brand book. A cover is the first page or frame of a standalone piece.
On a cover the title is set at `h1` size or larger (on slides, the
doubled `h1`, see Slides / Typography on slides). The gradient is an
option on covers, not a requirement: a white title on indigo or an
`indigo` title on white is equally correct.

Nowhere else in presentations or documents; use `signature-highlight`
there. On indigo the violet end measures 2.26:1 (`gradient-5`) and
2.62:1 (`gradient-4`), below 3:1; this is accepted for cover titles
only, as on the brand book cover.
Size floor: **never below `h3`.** Solid `brand` orange is the fallback for engines without
`background-clip: text` support.

```css
background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
background-clip: text;
-webkit-background-clip: text;
color: transparent;
```

#### 2. `gradient-flow-emphasis`: gradient text flow

The canonical pattern from the ad campaigns. The first part of a
sentence stays in solid foreground (white on indigo, charcoal on
white); the rest flows from orange through magenta to violet across
multiple lines.

The original example: *"Lønnsom vekst **for ambisiøse bedrifter og
organisasjoner**"*: first two words in solid white, the remaining
phrase in gradient.

**It is ONE continuous heading, not two stacked elements.** The solid
clause and the gradient clause share the same size, weight, and case.
Only the color changes between them. Set the whole thing in **sentence
case**; never put the gradient clause (or any part of it) in ALL CAPS,
and never enlarge one clause relative to the other. ALL CAPS belongs to
`poster` event titles only (see Casing and `poster-title`), never to
gradient-flow headlines.

Geometry: the ramp runs **horizontally and restarts on every
line**. Each line opens in orange; how far along the ramp it gets depends
on the line length, so short lines stop at magenta. That is correct, not
a bug.

Technique: put the gradient on the **whole heading** and paint the setup
phrase back in **solid** color on top. Never fill the emphasis phrase as
its own element: the ramp then starts where the phrase starts, not at
the left margin.
Break the line so the emphasis phrase **starts at the left margin**; that
is what makes it open in orange.

```css
.flow        { display: inline-block;
               background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
               background-clip: text; -webkit-background-clip: text;
               color: transparent; }
.flow .solid { color: #FFFFFF; }   /* setup phrase painted back solid on indigo */
.on-light .flow .solid { color: #35323C; }   /* on white */
```

This is the strongest brand moment in advertising and works equally
well on indigo and white. Use it when the message has a primary clause
("we offer X") and an emphasis clause ("for the kinds of people we want
to reach"). The gradient replaces italics and underline as emphasis.

#### 3. `gradient-bar`: gradient stripe

A thin horizontal stripe of the full 5-stop gradient, used as a
decorative border along the **top edge only** of every cover, and of
chapter and closing slides, posters and ads. Not on web sections.

**Every cover takes the bar**, whatever the format: presentations,
documents, reports, proposals, PDFs, brochures, case studies and the
brand book itself. A cover is the first page or frame of a standalone
piece. The bar spans the full width of the cover, 8px on a 1920px wide
frame and the same proportion on other formats (about 0.4% of the
width, never thinner than 4px). It works on indigo and on white covers
alike.

Never place it at the bottom of a page or slide, and never on both
edges. It is a top accent. Brand book 3.0 uses a single 8px stripe
spanning the full width on the cover, chapter pages and closing page.

It must be a **smooth, continuous blend**, with no hard stops
between the colors. Do NOT render it as five equal solid blocks
or a segmented / banded stripe. Use the CSS below verbatim (even 90°
distribution, no explicit stop percentages):

```css
background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
height: 8px;
```

### Buttons

All buttons are pills (`rounded.full`) with `label` typography and flat
color transitions at 150 to 200ms. No transforms.

- **`button-primary`**: solid violet pill (`action`, #521CE4) with white
  text. The high-emphasis primary CTA across web and slides. White text
  clears WCAG AA at 7.94:1, so no dark-text compromise. Hover darkens to
  `action-hover` and underlines the label.
- **`button-brand`**: solid deep-indigo pill with white text. The
  secondary CTA. (Name kept for continuity; the orange button was retired,
  so despite the name this no longer uses the brand orange.) Hover goes a
  shade deeper (`background-dark`, #160046) and underlines the label.
- **`button-on-dark`**: white pill with charcoal text. Standard CTA on
  indigo sections. Hover fills with Soft Lavender (`link-on-dark`) and
  underlines the label.

### Cards

- **`card-light`**: `muted` fill on white sections.
  Workhorse. `rounded.lg`, 32px padding.
- **`card-light-bordered`**: white fill with 1px `grey-light`, for cards
  on `muted` sections where contrast is needed.
- **`card-dark`**: `indigo` fill, white text, `rounded.lg`,
  40px padding.

### Editorial

- **`body-paragraph`**: `body` typography in `foreground` on light.
  The reading style for long-form prose.
- **`body-paragraph-on-dark`**: `body` in `on-dark` (white) on indigo.
- **`caption`**: `body-sm` in `foreground`. Image captions, chart
  details, fine print.
- **`quote`** + **`quote-emphasis`** (+ `quote-on-dark`, `quote-name`,
  `quote-role`): quote blocks, brand book 3.0 p. 21. `quote` typography
  (25/34, Regular). The opening sentence in `brand` orange, the rest in
  `indigo` on white and white on indigo. Light means white, not `muted`:
  the orange opening is 2.89:1 on `#F7F7F8` and fails.
  Emphasis is carried by colour, not weight. Attribution: name in `h5`,
  role in `body`, both in the text colour. The orange opening is one of
  the permitted orange text uses and does not count against the one
  highlighted phrase per page.

### Links

- **`link`**: `link` color (vivid violet) on light surfaces.
- **`link-on-dark`**: `link-on-dark` (soft lavender) on indigo.

### Status

- **`warning-badge`**: pink badge (`rounded.md`) with indigo text. The only place
  `warning` color appears.

### Layout chrome (web)

- **`nav`**: white, 60px tall, `max-w-7xl`. Plain links plus a single
  `button-primary` CTA on the right. Includes the NO/EN language toggle.
- **`footer`**: `indigo` with `on-dark` text. Four-column
  desktop grid. Includes the Miljøfyrtårn certification badge, a
  real-world trust signal that is part of the brand.
- **`input`**: 1px border in `foreground` (#35323C), `rounded.sm`
  (8px) corners. Brand book 3.0 p. 24.
- **`divider`** / **`divider-strong`**: 1px lines, for tables only.
  Don't use thin divider lines between sections or under headings;
  separate with space.
- **`decorative-stripe`**: solid orange 4px × 64px stripe above section
  openers. The web equivalent of a section flourish (quieter than the
  gradient bar; use the bar in advertising, the stripe on web).

### Advertising / poster

These components are for advertising contexts only: banners, social
media, posters, event materials. Don't use them on the website.

- **`logo-frame-diamond` / `logo-frame-arrow` / `logo-frame-rounded`**:
  the white shape that holds the wordmark in **formal display banner ads
  only** (banner formats like 580×500, 980×300, 180×500 where the logo is
  the hero element). For social media, posters, slides, app UI, and any
  other indigo surface, place the inverted white logo directly on the
  indigo background. Do NOT use a frame. One token per shape; pick by
  banner aspect ratio:
  - `logo-frame-diamond`: square / tall (e.g. 580×500). Square rotated
    45°, drawn as an SVG path.
  - `logo-frame-arrow`: wide (e.g. 980×300). Right-pointing arrow /
    pentagon, drawn as an SVG path.
  - `logo-frame-rounded`: narrow vertical (e.g. 180×500). Rounded
    square at `rounded.lg` (20px), the only variant with a CSS radius.
  - In all cases: pure white fill, charcoal logo inside, padding
    proportional to the banner size.
- **`poster-title`**: large title on indigo for **event posters
  and short standalone event titles** (e.g. "BAKGÅRDSFEST"), using the
  `poster` typography. This is the one place ALL CAPS is allowed on a
  title, and it may take a gradient fill. Do NOT use `poster-title` for
  sentence-style ad headlines. Headlines like "Lønnsom vekst for
  ambisiøse bedrifter …" use `gradient-flow-emphasis`, in sentence case.

### Process steps

`process-step-1` through `process-step-5` are 16px circular markers in
the five gradient colors. The brand book describes the color harmony
as conveying "digital change, process steps, or time" (brand book 3.0 p. 12). These
tokens are the canonical use: small dots in a process diagram, with
each color representing one phase of a project lifecycle.

### Editorial mode (slides, brand book voice)

- **`signature-highlight`**: single phrase in solid `brand` orange at
  `h1` size, Display 500. Brand book 3.0 p. 19: one highlighted phrase
  per page (one website sub-page, one catalogue page, one slide). Use in
  slide decks and editorial documents, where gradient headings are not
  used.

## Slides & presentations

Slides are a core deliverable for Frontkom (sales decks, client
workshops, strategy presentations). They have their own composition
rules distinct from web and advertising. The standard format is 16:9
(1920×1080).

### Canvas

Before making a presentation, ask whether the person prefers mostly
dark slides, mostly light slides, or a mix. Without an answer, mix:
cover, chapter dividers and the closing slide are indigo (`indigo`),
and content slides alternate between indigo and white (`background`),
so the deck is neither all indigo nor all white.

- **Indigo:** text in white.
- **White:** headings in `indigo`, body text in `foreground` #35323C.

### Slide layouts in the .pptx theme

The three canonical layouts must exist as **real layouts in the
deck's theme** (slide masters), not as formatting applied to individual
slides. A deck where indigo is painted per-slide breaks the moment
someone inserts a new slide or copies one into another file: they get a
white canvas and have to rebuild the brand by hand.

| Layout name | Maps to component | Canvas | Fixed elements |
|---|---|---|---|
| `Frontkom forside` | `slide-cover` | `indigo` | Gradient bar, top edge; watermark on the right (optional); white logo in lower third, aligned with the title |
| `Frontkom mørk side` | `slide-content` | `indigo` | White logo bottom-right |
| `Frontkom lys side` | `slide-content-light` | `background` (white) | Charcoal logo bottom-right |
| `Frontkom utsagn` | `slide-statement` | `background` (white) | Watermark in `grey-light`; charcoal logo bottom-right; title placeholder at `h1` size |
| `Frontkom kapittel` | `slide-chapter-divider` | `indigo` | Gradient bar, top edge; no logo |

Closing / CTA slides build on `Frontkom mørk side`. Chapter dividers and
statement slides need their own layouts: a chapter divider has no logo,
and a statement title is larger than the title placeholder on a content
slide.

**Background and logo live on the layout, never on the slide.** This is
what makes duplication and insertion safe, and it's the only way the
logo stays in its non-negotiable position without relying on discipline.

Placeholders per layout:

- `Frontkom forside`: title, subtitle
- `Frontkom mørk side`: title
- `Frontkom lys side`: title
- `Frontkom utsagn`: title
- `Frontkom kapittel`: title

#### Two rules that are easy to get wrong

**Every placeholder a layout declares must be filled by the slides using
it.** PowerPoint draws the prompt text ("Klikk for å legge til tekst")
for any placeholder a slide leaves empty, and it lands on top of
whatever the slide already contains. Slide text must be written *into*
the placeholder, not into a separate text box positioned over it. If a
layout needs a slot that most slides won't use, leave it out, the
content slide is a free canvas below the title, not a body-text
template.

**Title placeholders must set left alignment explicitly.** PowerPoint's
built-in title placeholder centers by default, and a title inherits that
unless the layout overrides it. Every heading in this system is
left-aligned.

#### Copying slides between decks

A slide pasted into another presentation adopts the destination theme
unless the person chooses *Keep source formatting*, the branded canvas
reverts to white. This is PowerPoint behaviour and cannot be designed
around; note it when handing a deck over.

### Slide types

Five canonical slide types cover almost every deck:

#### 1. Cover slide

The first slide. Indigo canvas with **a gradient bar on the top edge**
(also used on chapter and closing slides). Centered or left-aligned
composition with:

- The slide title in `h1`, white (`on-dark`), or in `hero-gradient` at
  `h1` size or larger
- A subtitle directly below the title. A short colophon line (audience,
  part, duration) can follow below the subtitle in body size, separated
  by about one line height of space, not pushed down to the logo
- Optionally, the watermark (`watermark-negative`, the filled symbol in
  `watermark-on-indigo`) on the right, bleeding off the top, right and
  bottom edges, clear of the title. A cover without it, with only the
  gradient bar, title and logo (as on the design manual cover), is
  equally correct. The cover is the only dark slide that can take the
  watermark; chapter dividers have none.
- The Frontkom logo in white in the lower third, **aligned with the
  title**: left-aligned when the title is left-aligned, centered only
  when the whole composition is centered. Don't center the logo under a
  left-aligned title; the logo floating mid-slide while the text sits
  left looks off.

Use `slide-cover` and add the gradient bars manually with CSS or SVG.

#### 2. Content slide

The workhorse. Indigo or white canvas (see Canvas), padding `64px 96px`,
with:

- A heading, typically `h2` or `h3`: white on indigo, `indigo` on white
- Content area: text, cards, illustrations, charts
- The Frontkom logo bottom-right, always (`logo-frontkom-on-dark.svg` on
  indigo, `logo-frontkom.svg` on white)

Logo position is non-negotiable on content slides: bottom-right, never
elsewhere.

#### 3. Chapter divider

A minimalist slide marking the start of a new section
("Om Frontkom", "Vekst og lønnsomhet (forretningsutvikling)",
"NGO spesifikke slides"). Just the section title in white on indigo,
left-aligned with generous padding. **No logo, no eyebrow, no
decoration.** Use `slide-chapter-divider`.

#### 4. Statement slide

The most distinctive slide type in the system. Used to deliver a single
strong message, typically a question or claim, between content
clusters. See "Vi hjelper ambisiøse bedrifter å vokse", "Hva mener vi
med lønnsom og bærekraftig vekst?", "Hvordan kommer man i gang?",
"Fragmenterte løsninger gir fragmenterte kundereiser".

Composition rules:

- Canvas: `background` (`#FFFFFF`). Not `muted`: orange on `#F7F7F8`
  measures 2.89:1.
- Heading: `h1`-sized, **left-aligned in the middle-left of the
  slide** (not top, not centered)
- Heading text color: **`indigo` (`#1A0054`)** for
  the bulk of the heading, not charcoal `foreground`. On a light slide
  canvas the dark heading text is always indigo: it ties the slide to the
  brand's dark canvas and reads more branded than a neutral grey (17.92:1
  on white). One phrase in `brand` orange, same weight as the rest
  ("Hva mener vi med **lønnsom og bærekraftig** vekst?"). This is the
  canonical pattern.
- Watermark: the filled symbol in `grey-light` (`#E8E7EC`)
  (`watermark-on-white`), anchored top right: about 1120 px wide, left
  edge around x = 1060, top 180 px above the slide, so it runs past the
  top and right edges and ends around y = 880, above the logo's clear
  space. Clear of the heading.
- Charcoal Frontkom wordmark logo bottom-right (small, sitting on top
  of or near the outlined symbol)

Use `slide-statement` and combine with the outlined symbol asset.

#### 5. Closing / CTA slide

A final slide with a call to action ("Let's talk", "Reach out today").
Indigo canvas, large heading and supporting text in white, and a single
`button-on-dark` CTA. Logo bottom-right.

Use `slide-content` with CTA composition.

### Layout patterns

#### Card colours (brand book 3.0 p. 13)

A grid of pastel-filled cards. Two firm colour rules, both easy to get
wrong by falling back on the generic "dark heading + grey body" pattern:

- **The card heading takes the card's `emphasisColor`, its parent
  gradient hue, never charcoal.** That colour is what ties each card to
  its fill. Keywords in the body text stay in `foreground`.
- **Body text is `foreground` charcoal**, never a lighter grey.

**Top-align the content in every card, never vertically center it.**
Each card sets `verticalAlign: top`: the heading starts at the top padding
and text flows down from there, so the headings line up across the row.
Vertical centering is the most common mistake here: cards hold different
amounts of copy, so centering pushes each heading to a different height
and the row looks ragged. Equal card heights are fine; the content still
starts at the top, not the middle.

The four fills are 78% tints of the brand gradient (gradient-2…5). When
several cards sit together, **always stack them light → dark in gradient
order**: rose, magenta, purple, blue, never a random arrangement. Each
pairs with its parent hue as the emphasis color:

- `card-rose`: `pastel-rose` (`#F7D6DF`) bg; emphasis in
  `gradient-2` rose (`#DA446E`). Lightest.
- `card-magenta`: `pastel-magenta` (`#F0CFEC`) bg; emphasis in
  `gradient-3` magenta (`#BC25A9`).
- `card-purple`: `pastel-purple` (`#E4CEF4`) bg; emphasis in
  `gradient-4` purple (`#861FCB`).
- `card-blue`: `pastel-blue` (`#D9CDF9`) bg; emphasis in
  `gradient-5` blue-violet (`#521CE4`). Darkest.

Mix in 1 or 2 photo cards (rounded `rounded.lg`) at the same dimensions
to break the monotony.

Note on contrast (emphasis = parent hue, measured on each fill):

- `card-blue`: `gradient-5` on `pastel-blue` is **5.3:1**. Passes
  AA for normal text; the strongest pairing.
- `card-purple`: `gradient-4` on `pastel-purple` is **4.7:1**.
  Passes AA for normal text.
- `card-magenta`: `gradient-3` on `pastel-magenta` is **3.7:1**.
  Large Text only, keep the emphasis to headings (`h5`+), not body.
- `card-rose`: `gradient-2` on `pastel-rose` is **3.1:1**. The
  weakest, only clears Large Text; keep the rose emphasis to short
  headings, or darken it (e.g. to `gradient-4` purple) if you need more.

Because each emphasis sits on its own hue's tint, the two warm fills
(rose, magenta) have modest contrast, fine for a card heading, not
for running text. Body copy is always `foreground` charcoal (≥8.4:1 on
all four), which is what keeps every card legible.

These pastels are deck-level variants, not locked brand tokens, but they
now derive straight from the brand gradient, so prefer them as given. Use
three or four per layout, always stacked light → dark in gradient order
(rose → magenta → purple → blue), always paired with a matching emphasis
color, never used solo.

#### Speech bubbles

Comic-style callouts used to highlight a remark or supplementary
thought. Indigo bubble with white text (`slide-bubble-dark`) for
emphasis on light slides; white bubble with charcoal text
(`slide-bubble-light`) for emphasis on indigo slides. Draw the tail
as part of the SVG shape, not as a separate element.

Use sparingly: at most one or two bubbles per slide.

#### Callouts

A single line or short paragraph set apart from the content, such as a
takeaway or a rule. A `muted` box on white slides, `rounded.lg`, text
in `foreground` with one emphasised phrase (see Typography / Emphasis
in running text). No coloured stripe on its left or top edge, and no
icon bar. On indigo slides, use a white box (`slide-bubble-light`
colours) without the tail.

#### Competence cloud

The "we can do many things" layout used on slides like "Å lykkes i
2026 krever spisskompetanse innen mange fagfelt". Words/phrases laid
out in soft organic clusters across the slide, each in a small rounded
indigo or pastel pill. Visually communicates breadth without listing
formally. Use sparingly (once per deck) as it's a high-impact device.

#### Pyramid / harmony progression

When showing hierarchy or stages, use the gradient harmony as the
fill colors of the steps, orange at the top, violet at the base
(or reverse, depending on what's being conveyed). See the decision
pyramid on "Hvor tas beslutningen når noe skal endres?". This makes
the gradient harmony do real work: representing progression, not
just decorating.

### Typography on slides

The sizes below are the web sizes. On slides they are doubled relative
to the canvas: in a .pptx (960 pt wide) use the numbers as pt, so body
17 becomes 17 pt; in HTML on a 1920 × 1080 canvas, double them, so body
17 becomes 34 px. Both give the same size on screen.

- Slide H1: `h1` (60px) for covers, statement slides, chapter dividers
- Slide H2: `h2` (45px) for content slide headings
- Slide H3: `h3` (34px) for sub-headings within a slide
- Card title: `h5` (19px) for info-card titles
- Slide body: `body` (17px) for slide body text

Don't use `hero` typography on slides; it's web-only. All headings are
Red Hat Display Medium (500), as on the web.

### What slides do NOT do

- They don't use `hero-gradient` text fill, except for the title on the
  cover slide (at `h1` size or larger). Use `signature-highlight` (single orange phrase) for
  emphasis elsewhere. A cover title in the gradient has no orange
  phrase.
- They don't use the `decorative-stripe` (web flourish). The
  `gradient-bar` appears on the top edge of cover, chapter and closing
  slides only, never on content slides.
- They don't use `card-light` or `card-dark` web cards. Use the card
  colours (`card-rose`, `card-magenta`, `card-purple`, `card-blue`), white
  or `muted` instead.

## Photography

Brand book 3.0 p. 27. Show warm, professional people in real
situations, exchanging ideas at work. Modern technologists with warmth,
and real people at the centre. Technology is a tool, never the subject.

Read from the actual photo library, not aspirational. The manner:

- **Available light.** Daylight from a window, or sun outdoors. No flash,
  no studio rig. Shadows fall where they fall.
- **Caught, not posed.** People look at each other, at a screen, at the
  work. Eye contact with the camera is the exception.
- **The real workplace.** Our own rooms, whiteboards, sticky notes,
  printouts, the brick wall in Gamlebyen. No stock interiors.
- **Colour comes from the room.** A photo's palette belongs to the room
  and its materials. Never tone or filter images toward the brand colours.
- **Depth is a tool.** A shoulder or a plant out of focus in the
  foreground places the viewer in the room.
- **People appear together.** One person alone at a desk reads as a
  portrait; two or more read as the way we work.

### No text on photos

Text never sits on top of a photo (brand book 3.0 p. 27). Place text
beside or below the picture, on white or on indigo. No overlays, no
scrims, no darkened images to carry text.

## Iconography

```
Source:  Aksel, designsystemet.no (open source)
Variant: Stroke
Grid:    24px
Use:     instances of the published components, so they update at source
```

Icons inherit the text colour beside them (`foreground` `#35323C` on
light). An icon is never the only carrier of meaning: pair every icon
that means something with a label, or give it an accessible name.
Interactive targets are at least 24px, and 44px on touch (brand book
3.0 p. 25).

**The symbol is not an icon.** The Frontkom mark and the outlined
symbol are brand elements. They never enter the icon set,
and an icon never stands in for the logo.

## Avatars

Brand book 3.0 p. 8. The symbol in a square, for profile pictures and
icons where the full logo is too small to read. Avatars come in positive
and negative, in orange or in the text colour. Sharp corners, no
rounding, no indigo variant. Four combinations only:

```
white background     / charcoal symbol
white background     / orange symbol
charcoal background  / white symbol
orange background    / white symbol
```

Padding is 14.3% of the tile (38 of 265 in the original). The symbol's
proportion is 189×177.

## Prose & punctuation

Running prose in materials follows the text/voice rules (a separate tone
skill owns full voice). One rule belongs here because people write
straight from this file:

**No dash as a pause marker**, neither em dash nor en dash. Use a full
stop, comma, colon, or parentheses instead. Write number ranges with
"to" (64 to 72px, 0:10 to 0:25).

**No middle dot (U+00B7) as a separator**, in labels, headings, lists or
spec lines. Rewrite the line, or split it into two lines.

## Archived

Retired, kept here so no one re-introduces them:

- **The anniversary logos.** The 25-year logo is archived for later use.
- **The Frontkom Experience lockup.** Discontinued, no successor.
- **The bracket bullet** (`shape/fill/bracket`) from the 2021 book.
  Bullets are plain.
- **Text over photo** treatments (overlay, scrim). Replaced by "No text
  on photos".
- **The outline display lettering** from the 2021 cover. Replaced by
  gradient text on the website hero, cover titles and in ads; elsewhere, solid
  heading type. Note there is still a
  documented text style for it in the library, `Desktop/Background text
  outlined`; it should be retired there too.

## Do's and Don'ts

### General

- **Do** treat indigo and white as equal default canvases. Pick by
  context: advertising and posters use indigo; web and editorial use
  white; presentations mix the two (ask first, see Slides / Canvas).
- **Do** lead brand moments with the gradient: text fill on web hero,
  text flow in advertising, gradient bar on every cover and on posters.
- **Do** scale headings fluidly with `clamp()` rather than abrupt
  breakpoints.
- **Do** use `foreground` (`#35323C`) for text on white, never pure
  `#000000`.
- **Do** verify any new component combination against WCAG AA by
  running `npx @google/design.md lint` on this file.
- **Don't** add drop shadows. Depth is contrast, radius, and outlined
  off-canvas symbol elements.
- **Don't** give a card, box, callout or note a coloured edge on one
  side (top stripe, left stripe). A box has one colour, its fill. See
  Shapes / Card and box edges.
- **Don't** set emphasis in running text in Bold (700). Use Medium
  (500), in `indigo` on light surfaces, at most one phrase per
  paragraph.
- **Don't** use square corners on buttons or interactive elements.
- **Don't** use the pill shape for anything but buttons. Tags, badges
  and toggles take `rounded.md`, inputs `rounded.sm`.
- **Don't** set headings in Red Hat Text or paragraphs in Red Hat
  Display. Display is for headings, Text for everything else.
- **Do** left-align all text everywhere: web, documents, slides and
  ads. Never centre.
- **Don't** apply the gradient to body copy or small text. At sizes
  below `h3`, the gradient turns muddy and contrast drops below WCAG
  AA. Reserve gradient text for hero, h1, h2, h3 and poster.
- **Don't** use `foreground-subtle` (`#9A98A0`) for body copy or
  captions. It fails WCAG AA. Page numbers, token names and metadata
  only.
- **Don't** use lighter greys to build text hierarchy. Use size.
- **Don't** use `warning` (`#FB1065`) as an accent or emphasis color.
- **Don't** stretch, recolor, or recompose the Frontkom symbol. The
  watermark colours on p. 23 are the only exception.
- **Don't** place the logo on a busy photo.
- **Do** place the white inverted Frontkom logo directly on indigo
  surfaces, with no frame, pill or white box around it. The frame is
  reserved for formal banner ads where the logo is the hero element.
- **Don't** wrap the logo in a white pill or rounded rectangle on
  social media posts, posters, or slides. It crowds the composition
  and weakens the brand.

### Web-specific

- **Do** rotate sections through `background` / `muted` /
  `indigo` for rhythm. Two adjacent sections must never share
  the same surface.
- **Do** keep long-form prose in `max-w-3xl`. Wider columns hurt
  readability.
- **Do** keep the brand orange tightly constrained on web. It fails WCAG
  AA as normal text on white and is not a web button color, so reserve it
  for large display headings, the gradient, and accents, not body text or
  UI. Never as a button fill, on web or slides.
- **Don't** use the `logo-frame-*`, `poster-title`, or `gradient-bar`
  components on web. `gradient-bar` is for covers of every kind,
  chapter and closing slides, posters and ads; the others are for
  advertising.

### Advertising-specific

- **Do** default to indigo canvas.
- **Do** use `gradient-flow-emphasis` to split a message into "the
  setup" (solid foreground) and "the punch" (gradient).
- **Do** use a white `logo-frame-*` to anchor the wordmark on indigo
  banner ads. Pick the token whose shape matches the aspect ratio:
  `logo-frame-diamond`, `logo-frame-arrow`, or `logo-frame-rounded`.
- **Do** use ALL CAPS for short event titles in `poster` typography.
  This is the only place ALL CAPS is permitted for headings.
- **Don't** reuse web layout patterns (alternating sections, max-w-3xl)
  in advertising. Advertising is poster composition, not scrolling page.

### Slide-specific

- **Do** ask whether the person prefers mostly dark, mostly light or a
  mix of slides. Without an answer, mix: indigo cover, chapter dividers
  and closing, content slides alternating indigo and white.
- **Do** place the Frontkom logo bottom-right on every content slide.
  The position is non-negotiable.
- **Do** use `signature-highlight` (single orange phrase) for emphasis
  on slides: brand book p. 11: one highlighted phrase per page.
- **Do** set statement slides on white with the watermark in
  `grey-light` (`watermark-on-white`).
- **Do** use the canonical quote treatment in slides too: opening
  sentence in brand orange, the rest in indigo on white and white on
  indigo (min 25px).
- **Do** use the gradient harmony as the fill of stages or steps when
  showing progression: pyramid, journey, timeline. The gradient
  *means* "process / time / change" (brand book p. 8).
- **Don't** put an eyebrow (small uppercase label) above headings.
- **Don't** set text in lavender (`link-on-dark` #C8B5FF). Text on indigo
  is white; text on white is `foreground`, headings `indigo`.
- **Don't** set pastel card headings in charcoal. The heading takes the
  card's `emphasisColor` (its parent gradient hue): that colour is the
  whole point of the card.
- **Don't** style pastel card body in a lighter grey. Inside a pastel
  card, body text is `foreground` charcoal.
- **Don't** vertically center the content inside info cards or columns.
  Top-align it (`verticalAlign: top`) so headings line up across the row;
  centering makes the tops sit at different heights and looks ragged.
- **Don't** use `hero-gradient` text fill on ordinary content-slide
  headings, prefer `signature-highlight` there. Full gradient text fill
  is for the cover title only, at `h1` size or larger.
- **Don't** put the logo anywhere except bottom-right on content
  slides. Cover slides are the only exception: the logo sits in the
  lower third there, aligned with the title (not centered under a
  left-aligned title).
- **Don't** use `decorative-stripe` (web) on slides, or `gradient-bar`
  on content slides. The gradient bar appears on cover, chapter and
  closing slides, on the **top edge only**, never the bottom.
- **Don't** use the card colours (`pastel-rose`, `pastel-magenta`,
  `pastel-purple`, `pastel-blue`) on web. They're for presentations and
  documents only.
- **Don't** combine `hero-gradient` with `signature-highlight` on the
  same surface. Pick one register.
