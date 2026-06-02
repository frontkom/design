---
version: alpha
name: Frontkom
description: >
  Design system for Frontkom — a Norwegian digital agency. Confident,
  modern, and brand-forward, with a saturated coral-magenta-violet gradient
  as the recurring signature device. The system supports two equal default
  canvases: deep indigo for brand and advertising, and white for web and
  editorial. Values come from the official Frontkom brand book; usage
  patterns come from active brand collateral (web, ads, posters).
colors:
  # ===== SIGNATURE =====
  brand: "#F86233"             # Frontkom orange. Pantone 1585 C. Brand book p. 7.
  primary: "#F86233"           # Alias of brand for tooling that expects 'primary'.
  # ===== CANVASES (equal defaults) =====
  background: "#FFFFFF"         # Pure white — the editorial / web default.
  background-dark: "#1A0054"   # Deep Indigo. Pantone 2745 C. The brand / ad default.
  background-muted: "#F7F7F8"  # Soft Cloud — alternative section bg on web.
  # ===== FOREGROUND =====
  foreground: "#35323C"         # Charcoal Plum. Pantone 4287 C. Brand book p. 7.
  on-dark: "#FFFFFF"           # Primary text on background-dark.
  on-dark-muted: "#C8B5FF"     # Soft Lavender — secondary text & taglines on indigo.
  # Foreground levels — pre-blended on white for WCAG validation
  foreground-muted: "#5E5C66"  # Body paragraphs (~80% foreground on white).
  foreground-subtle: "#9A98A0" # Quotes & metadata only (~50% foreground on white).
  # ===== LINKS =====
  link: "#4F1BE5"              # Vivid Violet. Pantone 2090 C. Brand book p. 7.
  link-on-dark: "#C8B5FF"      # Soft Lavender. Same value as on-dark-muted but
                                # documented separately because the role differs.
  # ===== STATUS =====
  warning: "#FB1065"            # Hot Pink-Red. Pantone 213 C. Brand book p. 7.
  # ===== BORDERS =====
  border: "#E8E7EC"            # Default 1px divider on light. Brand book p. 7.
  border-strong: "#D4D2DC"     # Stronger borders on light. Brand book p. 7.
  border-on-dark: "#2D1170"    # Subtle divider on indigo (lighter than bg-dark).
  # ===== AD-HOC PRESENTATION ACCENTS =====
  # Pastel fills used in presentation info-card grids. Not locked brand tokens —
  # they're a documented variant set for slide decks where multiple light cards
  # need visual differentiation. Don't use these on web; the web palette is
  # white + background-muted only.
  pastel-lavender: "#F0E9FB"   # Light lavender — pairs with link / gradient-5 text
  pastel-peach: "#FCE7DD"      # Light peach — pairs with brand text
  pastel-pink: "#F8D9E5"       # Light pink — pairs with gradient-3 text
  # ===== BRAND GRADIENT (5-stop) =====
  # The signature gradient. Used as text fill, text-flow, decorative bars,
  # frame accents. Derived from brand book's 7-stop "color harmony" (p. 8),
  # condensed to 5 stops for cleaner rendering on text and small surfaces.
  gradient-1: "#F86233"        # = brand. Gradient start.
  gradient-2: "#DA446E"
  gradient-3: "#BC25A9"        # Middle stop. Brand book color harmony p. 8.
  gradient-4: "#861FCB"
  gradient-5: "#521CE4"        # Gradient terminus, near link color.
typography:
  # Hero uses Red Hat Display 400 — how frontkom.com renders the marketing H1,
  # and the canvas the gradient text-fill sits on. Display has more character
  # at very large sizes than Red Hat Text. (Brand book specifies only Red Hat
  # Text; this is a documented website-led extension.)
  hero:
    fontFamily: Red Hat Display
    fontSize: 80px
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: -0.01em
  # All other headers use Red Hat Text Bold (700) per brand book p. 9. Sizes
  # follow the brand book's 1.333 (4:3) ratio scale.
  h1:
    fontFamily: Red Hat Text
    fontSize: 60px
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: -0.01em
  h2:
    fontFamily: Red Hat Text
    fontSize: 45px
    fontWeight: 700
    lineHeight: 1.2
  h3:
    fontFamily: Red Hat Text
    fontSize: 34px
    fontWeight: 700
    lineHeight: 1.25
  h4:
    fontFamily: Red Hat Text
    fontSize: 25px
    fontWeight: 700
    lineHeight: 1.3
  h5:
    fontFamily: Red Hat Text
    fontSize: 19px
    fontWeight: 700
    lineHeight: 1.4
  # Poster heading — used in advertising and event materials. Larger letter
  # spacing, often set in ALL CAPS. See annonse-eksempelene.
  poster:
    fontFamily: Red Hat Text
    fontSize: 56px
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 0.02em
  lead:
    fontFamily: Red Hat Text
    fontSize: 22px
    fontWeight: 400
    lineHeight: 1.5
  body:
    fontFamily: Red Hat Text
    fontSize: 17px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Red Hat Text
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: Red Hat Text
    fontSize: 14px
    fontWeight: 700
    lineHeight: 1.4
  eyebrow:
    fontFamily: Red Hat Text
    fontSize: 12px
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 0.1em
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  "2xl": 48px
  "3xl": 64px
  "4xl": 96px
  section-y: 96px
  container-x: 16px
  container-x-md: 24px
  container-x-lg: 32px
rounded:
  none: 0px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 20px
  "2xl": 28px
  "3xl": 40px
  full: 9999px
components:
  # ===========================================================
  # GRADIENT TREATMENTS (the signature device, three forms)
  # ===========================================================
  # 1. Gradient text fill — the whole heading takes the gradient as its color.
  # Used on H1 / hero headings. Solid brand orange is the fallback for engines
  # without bg-clip-text. CSS:
  #   background: linear-gradient(90deg,#F86233,#DA446E,#BC25A9,#861FCB,#521CE4);
  #   background-clip: text; -webkit-background-clip: text; color: transparent;
  hero-gradient:
    textColor: "{colors.brand}"
    typography: "{typography.hero}"
  # 2. Gradient text flow — the SECOND clause of a sentence flows from orange
  # through magenta to violet across multiple lines, while the FIRST clause
  # stays in solid foreground (white on indigo, charcoal on white). The
  # canonical pattern from the ad campaigns: "Lønnsom vekst FOR AMBISIØSE
  # BEDRIFTER OG ORGANISASJONER" — first two words solid, the rest gradient-
  # flowed. The gradient progresses with the reading order (top-down on
  # multi-line, left-to-right on single-line).
  gradient-flow-emphasis:
    textColor: "{colors.brand}"
    typography: "{typography.h1}"
  # 3. Gradient bar — a thin horizontal stripe of the full 5-stop gradient,
  # used as a decorative top/bottom border or section divider on indigo
  # canvases. See Bakgårdsfest poster top edge.
  gradient-bar:
    backgroundColor: "{colors.brand}"
    height: 6px
  # The decorative orange stripe — solid 4px × 64px pill. Used on web above
  # section openers as a quieter brand flourish (not the gradient bar).
  decorative-stripe:
    backgroundColor: "{colors.primary}"
    rounded: "{rounded.full}"
    height: 4px
    width: 64px

  # ===========================================================
  # BUTTONS
  # ===========================================================
  # Solid orange pill with indigo text. The high-emphasis primary CTA.
  # 5.79:1 contrast — passes WCAG AA, and indigo-on-orange echoes the brand
  # book avatar logic (orange ground, inverted symbol — p. 6).
  button-brand:
    backgroundColor: "{colors.brand}"
    textColor: "{colors.background-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-brand-hover:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
  # Solid violet pill with white text. The alternative primary CTA, used
  # when an orange button would be too loud for the section.
  button-link:
    backgroundColor: "{colors.link}"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-link-hover:
    backgroundColor: "{colors.gradient-4}"
    textColor: "{colors.on-dark}"
  # Charcoal pill with white text. Used in editorial sections where the
  # CTA should sit quietly.
  button-dark:
    backgroundColor: "{colors.foreground}"
    textColor: "{colors.background}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-dark-hover:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.background}"
  # White pill with charcoal text. Standard CTA on indigo sections.
  button-on-dark:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-on-dark-hover:
    backgroundColor: "{colors.background-muted}"
    textColor: "{colors.foreground}"

  # ===========================================================
  # CARDS
  # ===========================================================
  card-light:
    backgroundColor: "{colors.background-muted}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.xl}"
    padding: 32px
  card-light-bordered:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.xl}"
    padding: 32px
  card-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.2xl}"
    padding: 40px

  # ===========================================================
  # EDITORIAL ELEMENTS
  # ===========================================================
  body-paragraph:
    textColor: "{colors.foreground-muted}"
    typography: "{typography.body}"
  body-paragraph-on-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body}"
  caption:
    textColor: "{colors.foreground-subtle}"
    typography: "{typography.body-sm}"
  # Quote block — large grey body text with the opening sentence in
  # foreground. Brand book p. 13 ("the quote should be written in grey
  # color with a text highlighted black").
  quote:
    textColor: "{colors.foreground-subtle}"
    typography: "{typography.h4}"
  quote-emphasis:
    textColor: "{colors.foreground}"
    typography: "{typography.h4}"
  # Tagline on indigo — soft lavender, often paired with white primary text.
  # See "Bevar historien. Skap fremtiden." in Bakgårdsfest poster.
  tagline-on-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark-muted}"
    typography: "{typography.body}"

  # ===========================================================
  # LINKS
  # ===========================================================
  link:
    textColor: "{colors.link}"
    typography: "{typography.body}"
  link-on-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.link-on-dark}"
    typography: "{typography.body}"

  # ===========================================================
  # STATUS
  # ===========================================================
  warning-badge:
    backgroundColor: "{colors.warning}"
    textColor: "{colors.background-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 4px 12px

  # ===========================================================
  # LAYOUT CHROME (web-specific)
  # ===========================================================
  nav:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    height: 60px
  footer:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body-sm}"
    padding: 64px 32px
  footer-divider:
    backgroundColor: "{colors.border-on-dark}"
    height: 1px
  input:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  divider:
    backgroundColor: "{colors.border}"
    height: 1px
  divider-strong:
    backgroundColor: "{colors.border-strong}"
    height: 1px

  # ===========================================================
  # ADVERTISING / POSTER ELEMENTS
  # ===========================================================
  # Logo frame — ONLY for formal display banner advertising where the logo
  # is the hero element of the composition (e.g., 580×500 square banner,
  # 980×300 wide banner, 180×500 vertical banner). For ALL other indigo
  # surfaces — social media, posters, slides, app UI — place the inverted
  # white logo DIRECTLY on the indigo background. Do not add a frame.
  # See "Logo on indigo" in the top-of-file logo-usage section.
  # The frame shape adapts to the banner aspect ratio:
  #   - Square / tall (580×500) → square diamond rotated 45°
  #   - Wide (980×300) → right-pointing arrow / pentagon
  #   - Narrow vertical (180×500) → rounded square (rounded.3xl)
  # In all cases: pure white fill, charcoal logo inside, padding
  # proportional to the banner size.
  logo-frame:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.3xl}"
    padding: 32px 48px
  # Poster title — large bold text, often ALL CAPS, with gradient text fill
  # on indigo backgrounds. The "BAKGÅRDSFEST" treatment.
  poster-title:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.brand}"
    typography: "{typography.poster}"

  # ===========================================================
  # SLIDES & PRESENTATIONS
  # ===========================================================
  # Slides have their own composition rules distinct from web and posters.
  # Standard slide aspect ratio is 16:9 (1920×1080). Two canvas variants:
  # indigo (default) and muted (#F7F7F8, for statement slides only).
  # Logo placement is ALWAYS bottom-right on content slides; cover slides
  # center the logo in the lower third.

  # Cover slide — first slide of a deck. Indigo with gradient bars top and
  # bottom, eyebrow + h1 + logo. See "Master sales slides" cover.
  slide-cover:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.h1}"
    padding: 72px 96px
  # Content slide — the workhorse. Indigo canvas with optional eyebrow,
  # heading, and content area. Logo always bottom-right.
  slide-content:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.body}"
    padding: 64px 96px
  # Chapter divider — marks the start of a new section in the deck.
  # Just the section title in white, no logo, no decoration. Centered or
  # top-left depending on title length.
  slide-chapter-divider:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.h1}"
    padding: 96px
  # Statement slide — large brand-orange phrase on muted grey canvas with
  # the giant outlined Frontkom symbol bottom-right as atmospheric depth.
  # Used for chapter openers like "Vi hjelper ambisiøse bedrifter å vokse",
  # "Hvordan kommer man i gang?", "Fragmenterte løsninger gir fragmenterte
  # kundereiser." See assets/logo-frontkom-symbol-outlined.svg for the
  # outlined element. Text color is foreground for the bulk of the
  # heading; key words can be set in brand orange for emphasis (like
  # "**lønnsom**" and "**bærekraftig**" on s. 19). Pure-orange statement
  # headings exist (s. 17 "Vi hjelper ambisiøse bedrifter å vokse") as a
  # deliberate brand-stylistic choice but fall below WCAG AA large text
  # threshold — use sparingly, never for body copy.
  slide-statement:
    backgroundColor: "{colors.background-muted}"
    textColor: "{colors.foreground}"
    typography: "{typography.h1}"
    padding: 96px
  # Section eyebrow — orange "Master sales slides" / "Om Frontkom" identifier
  # at the top-left of content slides, sitting above the slide heading.
  slide-eyebrow:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.brand}"
    typography: "{typography.eyebrow}"

  # Info-card grid cards — pastel-filled rounded rectangles used in
  # multi-card slide layouts (e.g. "Kort om disse slidene" on slide 2).
  # Three variants by fill, each pairing with a different emphasis color
  # for KEY WORDS within the body text (the bulk of body text is
  # foreground charcoal for legibility). These are deck-level variants,
  # not locked brand tokens.
  slide-card-lavender:
    backgroundColor: "{colors.pastel-lavender}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.2xl}"
    padding: 32px
  slide-card-peach:
    backgroundColor: "{colors.pastel-peach}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.2xl}"
    padding: 32px
  slide-card-pink:
    backgroundColor: "{colors.pastel-pink}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.2xl}"
    padding: 32px

  # Speech bubble — comic-style callout used to highlight a key remark.
  # Indigo bubble with white text (default), or white bubble with charcoal
  # text. The tail/pointer is drawn as part of the SVG/shape, not built
  # from this token.
  slide-bubble-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.2xl}"
    padding: 24px 32px
  slide-bubble-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.2xl}"
    padding: 24px 32px

  # ===========================================================
  # PROCESS STEPS (color harmony in canonical use)
  # ===========================================================
  # Brand book p. 8: the gradient harmony is meant to convey "digital change,
  # process steps, or time." These tokens are 16px circular markers — one per
  # phase of a project lifecycle.
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

  # ===========================================================
  # EDITORIAL MODE (slides, brand book voice)
  # ===========================================================
  # Single phrase in solid brand orange at h2 size. Brand book p. 11: only
  # one highlighted phrase per page. Use in slides and editorial pages
  # where the gradient hero would feel out of place.
  signature-highlight:
    textColor: "{colors.brand}"
    typography: "{typography.h2}"
---

# Frontkom Design System

## Logo usage — read this before generating any visual

The Frontkom wordmark is `assets/logo-frontkom.svg`. **Do not reconstruct
it.** Always reference, embed, or copy the actual SVG file from
`assets/logo-frontkom.svg`. AI agents have a strong tendency to redraw
logos from prose descriptions; the result is always wrong. If you cannot
read the SVG file, leave a placeholder and tell the user — do not draw
"two arrows" or "a `<>` shape" or "frontkom in some font."

What the actual logo contains (so you recognize correctness):

- The symbol is two filled, rounded shapes that read as a stylised left
  arrow and a stylised right arrow, constructed on a 45° geometric grid
  (brand book p. 5). It is **not** the `<>` characters or angle brackets.
- The wordmark "frontkom" is set in a **custom-drawn typeface specific
  to the logo** — paths converted from a tweaked Red Hat sibling. The
  letterforms are part of the SVG; they are not live text. Do not retype
  "frontkom" in Red Hat Text and assume that's correct — it is not.
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

### Logo on indigo (`background-dark`) — ALWAYS invert

When the logo sits on `background-dark` or any other dark surface, it
must be rendered in white. **The default is white logo directly on
indigo, not a white frame containing a charcoal logo.** A white pill
or diamond frame is reserved for specific advertising layouts where
the logo is the primary subject (see `logo-frame` component); for
social media, posters, slides, app screens, and most other dark-canvas
uses, place the inverted logo directly on the indigo background.

Three SVG files are provided so agents don't have to manipulate paths:

- `assets/logo-frontkom.svg` — charcoal logo (full lockup) for **light backgrounds**
- `assets/logo-frontkom-on-dark.svg` — white logo (full lockup) for **indigo / dark
  backgrounds**
- `assets/logo-frontkom-symbol-outlined.svg` — outlined version of the symbol
  only (no wordmark), in soft grey strokes. Used as a giant decorative
  element on statement slides (see Slides & presentations / Statement
  slide). `viewBox="0 0 110 107"`.

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
("[Frontkom logo]") — not to attempt a freehand SVG.

## Font loading — set this up before generating any visual

Frontkom uses two Red Hat sibling families: **Red Hat Text** for body and
all headers (per brandbook), and **Red Hat Display** for the marketing
hero H1 only (web extension). Both are open-source via Google Fonts and
SIL Open Font License.

The font files are provided in `assets/fonts/` as variable TTFs:

- `RedHatText-VariableFont_wght.ttf`
- `RedHatText-Italic-VariableFont_wght.ttf`
- `RedHatDisplay-VariableFont_wght.ttf`
- `RedHatDisplay-Italic-VariableFont_wght.ttf`

### Loading strategy by context

**For web (HTML/CSS/React) — Google Fonts CDN is preferred.** It's
fastest, cached across the internet, and works in every AI rendering
environment that has network access:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;1,400&family=Red+Hat+Text:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
```

Or via CSS `@import`:

```css
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;1,400&family=Red+Hat+Text:ital,wght@0,400;0,700;1,400;1,700&display=swap');
```

The URL above includes only the weights and styles the system uses:
Display 400 regular & italic; Text 400 regular & italic, 700 regular &
italic. Don't load other weights — the system uses 400 and 700 only.

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

For the hero family:

```css
font-family: 'Red Hat Display', 'Red Hat Text', system-ui, -apple-system, sans-serif;
```

Always include `system-ui` in the stack so unstyled output still looks
deliberate, not broken.

### What AI agents should NOT do

- Don't substitute a different font (Inter, Roboto, Helvetica) and
  claim it's "close enough." It isn't — Red Hat's character markers
  (the open `a`, the angled `t` terminal, the geometric `o`) are part
  of the brand.
- Don't load all weights. The system uses 400 and 700 only. Loading
  300, 500, 600, 800, 900 wastes bandwidth and tempts mixing.
- Don't use the variable font's full weight axis to invent new weights
  (e.g. 500 for "soft headers"). Stick to 400 and 700.

## Overview

Frontkom is a Norwegian digital agency. The brand reads as **confident,
modern, and brand-forward**, with a saturated coral-magenta-violet gradient
as the recurring signature device.

The system supports **two equal default canvases**, chosen by context:

- **Indigo (`#1A0054`)** is the canonical brand canvas. Use it for
  advertising, posters, social media, presentations, and any communication
  *about* Frontkom. Indigo carries the brand most loudly — gradient text,
  bright orange accents, and lavender taglines all sing on it.
- **White (`#FFFFFF`)** is the editorial and web canvas. Use it for the
  website, blog posts, case studies, and any communication *from*
  Frontkom about its work. White provides the airy, editorial calm where
  long-form content can breathe.

Don't think of one as default and the other as exception — they're peers.
The wrong canvas for the context is more wrong than the wrong color
within the right canvas.

The defining brand device is **the five-stop gradient** — Frontkom orange
(`#F86233`) through pink, magenta, and violet to indigo-violet
(`#521CE4`). The gradient appears in three distinct forms (see Components
/ Gradient treatments) and is the single strongest signal that something
is Frontkom.

The audience is enterprise buyers, editorial readers, and event audiences
in Norwegian and English. NO and EN are first-class equals; the language
toggle is a component, not an afterthought.

## Colors

The palette is the brand book palette, organized around two canvases and
the signature gradient.

### Signature

- **`brand` `#F86233` (Pantone 1585 C)** — Frontkom orange. The single
  defining accent. Used as the gradient start, primary CTA fill, and
  decorative stripe color.

### Canvases

- **`background-dark` `#1A0054` (Pantone 2745 C)** — deep indigo. The
  brand canvas. White primary text, lavender secondary text, gradient
  accents.
- **`background` `#FFFFFF`** — pure white. The editorial canvas. Charcoal
  primary text, muted charcoal body text, violet links.
- **`background-muted` `#F7F7F8`** — soft cloud grey. Section background
  on web that pairs with white for rhythm.

### Foreground

All text on white uses `foreground` (`#35323C`) — never pure
`#000000`. Brand book is explicit: "almost black but not quite; it's our
text color."

Three text-color tiers on white, achieved by varying alpha. Pre-computed
values are provided for WCAG validation:

- **`foreground` `#35323C`** — headlines and high-priority text. WCAG AA
  passes 12.6:1 on white.
- **`foreground-muted` `#5E5C66`** (≈80%) — body paragraphs. AA passes
  6.4:1.
- **`foreground-subtle` `#9A98A0`** (≈50%) — quotes and metadata only.
  Below AA for paragraph text, by design.

On indigo, `on-dark` (`#FFFFFF`) is the primary text color and
`on-dark-muted` (`#C8B5FF`, soft lavender) is the secondary — used for
taglines, supporting text, and link hover states.

### Links

`link` (`#4F1BE5`, vivid violet) on light surfaces; `link-on-dark`
(`#C8B5FF`, soft lavender — same value as `on-dark-muted` but distinct
role) on indigo.

### Status

`warning` (`#FB1065`) is the only status color and is used exclusively
for warning states. Don't reuse it as accent or emphasis — that's
`brand`'s job.

### Borders

`border` (`#E8E7EC`) is the default 1px divider on light surfaces;
`border-strong` (`#D4D2DC`) is the higher-contrast variant. On indigo,
`border-on-dark` (`#2D1170`, slightly lighter than the canvas) creates
subtle hierarchy.

### The brand gradient

```css
background: linear-gradient(90deg,
  #F86233 0%,    /* gradient-1 (= brand) */
  #DA446E 25%,   /* gradient-2 */
  #BC25A9 50%,   /* gradient-3 — middle stop */
  #861FCB 75%,   /* gradient-4 */
  #521CE4 100%   /* gradient-5 (near link) */
);
```

The gradient is derived from the brand book's seven-stop "color harmony"
(p. 8), condensed to five stops for cleaner rendering at typography
sizes. The brand book describes the harmony as conveying "digital
change, process steps, or time" — that meaning carries through. The
gradient *moves*; it doesn't sit still. See Components / Gradient
treatments for the three canonical applications.

## Typography

The brand book is unambiguous: **Red Hat Text Bold (700)** for headers,
**Red Hat Text Regular (400)** for body. Sizes follow a 1.333 (4:3)
ratio scale.

The website extends this with one exception: **Red Hat Display 400** is
used on the marketing hero H1 only, providing the canvas for the
gradient text fill. This is a documented website-led deviation.

Posters and advertising add a third extension: the **`poster`** size
(56px / `letterSpacing: 0.02em`), used for short event titles like
"BAKGÅRDSFEST". Posters can be set in ALL CAPS — the only place in the
system where ALL CAPS is permitted for headings (the eyebrow uses
uppercase but is not a heading).

### Roles

- **`hero`** — Red Hat Display 400, ~80px. The marketing H1 with
  gradient text fill.
- **`h1`** — Red Hat Text 700, ~60px. Article H1, secondary marketing
  hero, page titles in editorial mode, and the ad text-flow size.
- **`h2`** — Red Hat Text 700, ~45px. Major section headings.
- **`h3`** — Red Hat Text 700, ~34px. Article H2.
- **`h4`** — Red Hat Text 700, ~25px. Subsection headings, quote blocks.
- **`h5`** — Red Hat Text 700, ~19px. Card titles.
- **`poster`** — Red Hat Text 700, ~56px, slightly increased letter-
  spacing. Event posters and short ad headlines (often ALL CAPS).
- **`lead`** — Red Hat Text 400, 22px. The "eye-catching intro" (brand
  book p. 9). Use once, at the start of a text block.
- **`body`** — Red Hat Text 400, 17px / 1.6. Workhorse paragraph text.
- **`body-sm`** — Red Hat Text 400, 14px. Image subtitles, fine print.
- **`label`** — Red Hat Text 700, 14px. Buttons, UI labels.
- **`eyebrow`** — Red Hat Text 700, 12px, uppercase, `tracking: 0.1em`.

### Fluid sizing

Token values are desktop maximums. Scale fluidly with `clamp()` for
mobile — e.g. `clamp(40px, 6vw, 80px)` for hero. Don't use abrupt
breakpoints.

### Casing

Sentence case for headings and body text by default. ALL CAPS is
permitted only on the `poster` size for event titles, and on the
`eyebrow` token. Title Case is not used.

## Layout

### Alignment

> Brand book principle (p. 10): *"Text should always be left-aligned."*

Strict rule on web and editorial. Centered alignment is permitted in
advertising and poster contexts where a single short phrase is the
entire composition (the Bakgårdsfest poster centers the title block
under the photo).

### Container widths (web)

- **`max-w-7xl` (≈1280px)** — marketing rows, nav, footer.
- **`max-w-4xl` (≈896px)** — featured-image article header.
- **`max-w-3xl` (≈768px)** — long-form article body. The editorial
  canvas. Every piece of running prose belongs here.

### Horizontal padding (web)

`container-x` → `container-x-md` → `container-x-lg`
(16/24/32px → `px-4 sm:px-6 lg:px-8`).

### Section alternation (web)

Marketing pages rotate through three surfaces — `background` (white),
`background-muted` (cloud grey), and `background-dark` (indigo) — to
create rhythm. Two adjacent sections must never share the same surface.
A typical landing page:
white (hero) → indigo (stats) → muted (services) → white (editorial) →
indigo (CTA) → footer.

### Asymmetrical balance

Brand book guidance (p. 10): asymmetrical layouts are encouraged — but
balance the visual weight, don't collide it.

### Bilingual layout

Norwegian copy runs ~10–15% longer than English. Design with this slack
built in.

### Advertising layout

Indigo canvas is the default. Compositions are typically split between
a content area (text, image) and a logo area (with the white logo frame
— see Components). Aspect ratios common in the system: 320×250, 580×500,
180×500, 980×300, 320×400. The white logo frame adapts its shape to
the ad's proportions: square diamond for tall formats, right-pointing
arrow for wide formats, rounded square for narrow vertical formats.

## Elevation & Depth

The system is **flat**. No drop shadows. Depth comes from:

1. **Surface contrast** — alternating
   `background` / `background-muted` / `background-dark` on web.
2. **Border accents** — `border` outlines on light cards;
   `border-on-dark` for subtle indigo hierarchy.
3. **Corner radius** — `rounded.xl` and `rounded.2xl` create softness
   without shadow.
4. **Outlined symbol elements** (brand book p. 17) — outlined versions
   of the Frontkom symbol can be placed partially off-canvas as
   atmospheric depth devices.

If `box-shadow` feels needed, increase contrast or radius instead.

## Shapes

- **Actions** — always `rounded.full` (pill). Buttons, tags, language
  toggle. No square corners on interactive elements.
- **Cards** — `rounded.xl` (20px) standard, `rounded.2xl` (28px) for
  hero cards.
- **Inputs** — `rounded.sm` (8px). The only place where shape softens
  but doesn't go fully round.
- **Logo frame (advertising only)** — `rounded.3xl` (40px) when
  rendered as a rounded square; full diamond / arrow shapes are SVG-
  drawn paths matching the symbol geometry.
- **The symbol** — the Frontkom logo symbol uses a stylised geometric
  construction at 45° (brand book p. 5). When using it as a decorative
  element, respect the original geometry — don't stretch, recolor, or
  recompose it.

## Components

### Gradient treatments

The signature device. Three forms — pick by context.

#### 1. `hero-gradient` — gradient text fill

The whole heading takes the gradient as its color. Used on H1 / hero
headings on **white canvases**. Solid `brand` orange is the fallback
for engines without `background-clip: text` support.

```css
background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
background-clip: text;
-webkit-background-clip: text;
color: transparent;
```

#### 2. `gradient-flow-emphasis` — gradient text flow

The canonical pattern from the ad campaigns. The first part of a
sentence stays in solid foreground (white on indigo, charcoal on
white); the rest flows from orange through magenta to violet across
multiple lines.

The original example: *"Lønnsom vekst **for ambisiøse bedrifter og
organisasjoner**"* — first two words in solid white, the remaining
phrase in gradient. The gradient progresses with reading order:
top-down on multi-line, left-to-right on single-line.

This is the strongest brand moment in advertising and works equally
well on indigo and white. Use it when the message has a primary clause
("we offer X") and an emphasis clause ("for the kinds of people we want
to reach"). The gradient does the work of italics and underline at
once.

#### 3. `gradient-bar` — gradient stripe

A thin horizontal stripe of the full 5-stop gradient, used as a
decorative top edge or section divider, primarily on indigo. See the
top edge of the Bakgårdsfest poster — a single 6px stripe spanning
the full width does the work of a frame.

```css
background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
height: 6px;
```

### Buttons

All buttons are pills (`rounded.full`) with `label` typography and flat
color transitions at 150–200ms. No transforms.

- **`button-brand`** — solid orange pill with indigo text. The high-
  emphasis primary CTA. Hover shifts to indigo with white text — a
  dramatic flip that mirrors the brand's two canvases.
- **`button-link`** — solid violet pill with white text. The
  alternative primary CTA, used when an orange button would be too loud.
- **`button-dark`** — charcoal pill with white text. Used in editorial
  sections where the CTA should sit quietly.
- **`button-on-dark`** — white pill with charcoal text. Standard CTA on
  indigo sections.

### Cards

- **`card-light`** — `background-muted` fill on white sections.
  Workhorse. `rounded.xl`, 32px padding.
- **`card-light-bordered`** — white fill with 1px `border`, for cards
  on `background-muted` sections where contrast is needed.
- **`card-dark`** — `background-dark` fill, white text, `rounded.2xl`,
  40px padding.

### Editorial

- **`body-paragraph`** — `body` typography in `foreground-muted` on
  light. The reading style for long-form prose.
- **`body-paragraph-on-dark`** — `body` in `on-dark` (white) on indigo.
- **`caption`** — `body-sm` in `foreground-subtle`. Image subtitles,
  metadata, fine print. Never body copy.
- **`quote`** + **`quote-emphasis`** — large quote blocks (h4-sized).
  Brand book p. 13: quote body in `foreground-subtle` (grey), opening
  sentence in `foreground` (near-black) for emphasis. The canonical
  Frontkom quote treatment.
- **`tagline-on-dark`** — body text in `on-dark-muted` (soft lavender)
  on indigo. Used for closing taglines like "Bevar historien. Skap
  fremtiden." The lavender tagline is one of the most identifiable
  brand moments on indigo.

### Links

- **`link`** — `link` color (vivid violet) on light surfaces.
- **`link-on-dark`** — `link-on-dark` (soft lavender) on indigo.

### Status

- **`warning-badge`** — pink pill with indigo text. The only place
  `warning` color appears.

### Layout chrome (web)

- **`nav`** — white, 60px tall, `max-w-7xl`. Plain links plus a single
  `button-brand` CTA on the right. Includes the NO/EN language toggle.
- **`footer`** — `background-dark` with `on-dark` text. Four-column
  desktop grid. Includes the Miljøfyrtårn certification badge — a
  real-world trust signal that's part of the brand.
- **`footer-divider`** — 1px line in `border-on-dark` for subtle
  separation within the indigo footer.
- **`input`** — `border` outlines, `rounded.sm` corners.
- **`divider`** / **`divider-strong`** — 1px lines.
- **`decorative-stripe`** — solid orange 4px × 64px pill above section
  openers. The web equivalent of a section flourish (quieter than the
  gradient bar — use the bar in advertising, the stripe on web).

### Advertising / poster

These components are for advertising contexts only — banners, social
media, posters, event materials. Don't use them on the website.

- **`logo-frame`** — the white shape that holds the wordmark in
  **formal display banner ads only** (banner formats like 580×500,
  980×300, 180×500 where the logo is the hero element). For social
  media, posters, slides, app UI, and any other indigo surface, place
  the inverted white logo directly on the indigo background — do NOT
  use a frame. The frame shape adapts to the banner aspect ratio:
  - Square / tall (e.g. 580×500) — full square diamond rotated 45°.
  - Wide (e.g. 980×300) — right-pointing arrow / pentagon.
  - Narrow vertical (e.g. 180×500) — `rounded.3xl` rounded square.
  - In all cases: pure white fill, charcoal logo inside, padding
    proportional to the banner size.
- **`poster-title`** — large bold title on indigo, often in ALL CAPS,
  using the `poster` typography. Fills with `gradient-flow-emphasis`
  for the brand moment ("BAKGÅRDSFEST").

### Process steps

`process-step-1` through `process-step-5` are 16px circular markers in
the five gradient colors. The brand book describes the color harmony
as conveying "digital change, process steps, or time" (p. 8) — these
tokens are the canonical use: small dots in a process diagram, with
each color representing one phase of a project lifecycle.

### Editorial mode (slides, brand book voice)

- **`signature-highlight`** — single phrase in solid `brand` orange at
  `h2` size. Brand book p. 11: one highlighted phrase per page. Use in
  slide decks and editorial documents where the gradient hero would
  feel out of place.

## Slides & presentations

Slides are a core deliverable for Frontkom (sales decks, client
workshops, strategy presentations). They have their own composition
rules distinct from web and advertising. The standard format is 16:9
(1920×1080).

### Canvas

Indigo (`background-dark`) is the default canvas for almost all slide
types — covers, content slides, chapter dividers, CTA slides. The muted
grey canvas (`background-muted`) is reserved for **statement slides**
(see below) and rare editorial moments. White is used sparingly inside
slides — for embedded screenshots, mockups, and the occasional info
card — but is not a standalone slide background.

### Slide types

Five canonical slide types cover almost every deck:

#### 1. Cover slide

The first slide. Indigo canvas with **a gradient bar at the top edge
and a matching one at the bottom edge**, framing the canvas. Centered
or left-aligned composition with:

- An eyebrow in `brand` orange (e.g. "A part of the Frontkom Value
  Layer")
- The slide title in `h1`, white (`on-dark`)
- The Frontkom logo in white centered in the lower third (this is
  the only slide where the logo is centered)

Use `slide-cover` and add the gradient bars manually with CSS or SVG.

#### 2. Content slide

The workhorse. Indigo canvas, padding `64px 96px`, with:

- An optional `slide-eyebrow` in orange at the top-left ("Master sales
  slides", "Om Frontkom") — page identifier
- A heading in white, typically `h2` or `h3`
- Content area: text, cards, illustrations, charts
- The Frontkom logo bottom-right, always (`logo-frontkom-on-dark.svg`)

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
strong message — typically a question or claim — between content
clusters. See "Vi hjelper ambisiøse bedrifter å vokse", "Hva mener vi
med lønnsom og bærekraftig vekst?", "Hvordan kommer man i gang?",
"Fragmenterte løsninger gir fragmenterte kundereiser".

Composition rules:

- Canvas: `background-muted` (`#F7F7F8`)
- Heading: `h1`-sized, **left-aligned in the middle-left of the
  slide** (not top, not centered)
- Heading text color: `foreground` for the bulk of the heading;
  emphasis words in **bold** `brand` orange ("Hva mener vi med
  **lønnsom** og **bærekraftig** vekst?"). This is the canonical
  pattern.
- Pure-orange statement headings exist in the deck (s. 17 "Vi hjelper
  ambisiøse bedrifter å vokse", s. 21 "Synes du det er lett å være en
  god innkjøper...", s. 37 "Fragmenterte løsninger gir fragmenterte
  kundereiser") as a deliberate brand-stylistic choice. They fall
  below WCAG AA Large Text contrast (2.89:1) — use this variant
  sparingly and only for short standalone statements, never paired
  with body text.
- Atmospheric depth: a giant outlined Frontkom symbol fills the
  bottom-right area, partially clipped off the canvas edge. Use
  `assets/logo-frontkom-symbol-outlined.svg` scaled to roughly 60–70%
  of the slide height, positioned with its right edge extending
  beyond the canvas right edge.
- Charcoal Frontkom wordmark logo bottom-right (small, sitting on top
  of or near the outlined symbol)

Use `slide-statement` and combine with the outlined symbol asset.

#### 5. Closing / CTA slide

A final slide with a call to action ("Let's talk", "Reach out today").
Indigo canvas, large heading in white, supporting text in
`on-dark-muted` (lavender), and a single `button-on-dark` CTA. Logo
bottom-right.

Use `slide-content` with CTA composition.

### Layout patterns

#### Info-card grid (slide 2–3 of master deck)

A 3×2 or 2×3 grid of pastel-filled cards. Each card holds 2–4 lines of
body text in `foreground` charcoal for legibility, with key phrases
set in **bold** in the card's *emphasis color*. The three pastel fills
each have a paired emphasis color:

- `slide-card-lavender` — `pastel-lavender` (`#F0E9FB`) bg; emphasis
  in `link` violet (`#4F1BE5`)
- `slide-card-peach` — `pastel-peach` (`#FCE7DD`) bg; emphasis in
  `brand` orange (`#F86233`)
- `slide-card-pink` — `pastel-pink` (`#F8D9E5`) bg; emphasis in
  `gradient-3` magenta (`#BC25A9`)

Mix in 1–2 photo cards (rounded `rounded.2xl`) at the same dimensions
to break the monotony.

Note on contrast: the emphasis colors don't pass WCAG AA against the
pastel fills as full body copy, which is why bulk body text uses
`foreground`. Emphasis is reserved for **bold key phrases at h5 size
or larger** — at that size and weight they qualify as Large Text under
WCAG AA, and visually they read as accents, not paragraphs.

These pastels are deck-level variants, not locked brand tokens. A
specific deck may use a different palette of three pastels if it suits
the topic — but always three colors, always paired with a matching
emphasis color, never used solo.

#### Speech bubbles

Comic-style callouts used to highlight a remark or supplementary
thought. Indigo bubble with white text (`slide-bubble-dark`) for
emphasis on light slides; white bubble with charcoal text
(`slide-bubble-light`) for emphasis on indigo slides. Draw the tail
as part of the SVG shape, not as a separate element.

Use sparingly — at most one or two bubbles per slide.

#### Competence cloud

The "we can do many things" layout used on slides like "Å lykkes i
2026 krever spisskompetanse innen mange fagfelt". Words/phrases laid
out in soft organic clusters across the slide, each in a small rounded
indigo or pastel pill. Visually communicates breadth without listing
formally. Use sparingly (once per deck) as it's a high-impact device.

#### Pyramid / harmony progression

When showing hierarchy or stages, use the gradient harmony as the
fill colors of the steps — orange at the top, violet at the base
(or reverse, depending on what's being conveyed). See the decision
pyramid on "Hvor tas beslutningen når noe skal endres?". This makes
the gradient harmony do real work: representing progression, not
just decorating.

### Typography on slides

- Slide H1: `h1` (60px) — covers, statement slides, chapter dividers
- Slide H2: `h2` (45px) — content slide headings
- Slide H3: `h3` (34px) — sub-headings within a slide
- Card title: `h5` (19px) — info-card titles
- Slide body: `body` (17px) — slide body text
- Slide eyebrow: `eyebrow` — page identifier at top-left of content
  slides

Don't use `hero` typography on slides — it's web-only (Red Hat Display
is reserved for the marketing hero H1).

### What slides do NOT do

- They don't use `hero-gradient` text fill — gradient text fill is for
  web hero only. Use `signature-highlight` (single orange phrase) for
  emphasis instead.
- They don't use the `decorative-stripe` (web flourish) or `gradient-bar`
  (poster device) inside content slides — except on the cover slide,
  where gradient bars frame the canvas.
- They don't use `card-light` or `card-dark` web cards — use the slide
  card variants (`slide-card-lavender` / `peach` / `pink`) instead.

## Do's and Don'ts

### General

- **Do** treat indigo and white as equal default canvases. Pick by
  context: brand / advertising / posters use indigo; web / editorial
  use white.
- **Do** lead brand moments with the gradient — text fill on web hero,
  text flow in advertising, gradient bar on posters.
- **Do** scale headings fluidly with `clamp()` rather than abrupt
  breakpoints.
- **Do** use `foreground` (`#35323C`) for text on white — never pure
  `#000000`.
- **Do** verify any new component combination against WCAG AA by
  running `npx @google/design.md lint DESIGN.md`.
- **Don't** add drop shadows. Depth is contrast, radius, and outlined
  off-canvas symbol elements.
- **Don't** use square corners on buttons or interactive elements.
- **Don't** mix Red Hat Display into anything other than `hero`. Display
  is reserved for the marketing H1.
- **Don't** apply the gradient to body copy or small text — at sizes
  below `h3`, the gradient turns muddy and contrast drops below WCAG
  AA. Reserve it for hero, h1, h2, poster, and decorative bars.
- **Don't** use `foreground-subtle` (`#9A98A0`) for body copy on white
  — it fails WCAG AA. Quotes and metadata only.
- **Don't** use `warning` (`#FB1065`) as an accent or emphasis color.
- **Don't** stretch, recolor, or recompose the Frontkom symbol.
- **Do** place the white inverted Frontkom logo directly on indigo
  surfaces — no frame, no pill, no white box around it. The frame is
  reserved for formal banner ads where the logo is the hero element.
- **Don't** wrap the logo in a white pill or rounded rectangle on
  social media posts, posters, or slides. It crowds the composition
  and weakens the brand.

### Web-specific

- **Do** rotate sections through `background` / `background-muted` /
  `background-dark` for rhythm. Two adjacent sections must never share
  the same surface.
- **Do** keep long-form prose in `max-w-3xl`. Wider columns hurt
  readability.
- **Do** left-align all paragraph text. Center alignment is for short
  standalone elements only.
- **Don't** use the `logo-frame`, `poster-title`, or `gradient-bar`
  components on web. They're for advertising contexts.

### Advertising-specific

- **Do** default to indigo canvas.
- **Do** use `gradient-flow-emphasis` to split a message into "the
  setup" (solid foreground) and "the punch" (gradient).
- **Do** use the white `logo-frame` to anchor the wordmark on indigo
  backgrounds — adapt the shape (diamond, arrow, rounded square) to the
  ad aspect ratio.
- **Do** use ALL CAPS for short event titles in `poster` typography.
  This is the only place ALL CAPS is permitted for headings.
- **Don't** reuse web layout patterns (alternating sections, max-w-3xl)
  in advertising. Advertising is poster composition, not scrolling page.

### Slide-specific

- **Do** use indigo (`background-dark`) as the default canvas for
  almost every slide — covers, content, chapter dividers, CTA.
- **Do** place the Frontkom logo bottom-right on every content slide.
  The position is non-negotiable.
- **Do** use `signature-highlight` (single orange phrase) for emphasis
  on slides — brand book p. 11: one highlighted phrase per page.
- **Do** use the muted grey canvas (`background-muted`) only for
  statement slides, paired with the giant outlined Frontkom symbol
  (`logo-frontkom-symbol-outlined.svg`) bottom-right.
- **Do** use the canonical quote treatment in slides too (grey body,
  foreground emphasis on the opening sentence).
- **Do** use the gradient harmony as the fill of stages or steps when
  showing progression — pyramid, journey, timeline. The gradient
  *means* "process / time / change" (brand book p. 8).
- **Do** include an orange eyebrow at the top-left of content slides
  to identify the deck section ("Master sales slides", "Om Frontkom").
- **Don't** use `hero-gradient` text fill on slide headings — gradient
  text fill is web-only. Use `signature-highlight` instead.
- **Don't** put the logo anywhere except bottom-right on content
  slides. Cover slides are the only exception (logo centered in the
  lower third).
- **Don't** use `decorative-stripe` (web) or `gradient-bar` (poster)
  inside content slides. The cover slide is the only place gradient
  bars appear in a deck — framing the canvas top and bottom.
- **Don't** use Red Hat Display on slides. Display is reserved for
  the marketing hero H1 on web.
- **Don't** use the pastel slide cards (`pastel-lavender`,
  `pastel-peach`, `pastel-pink`) on web. They're for slide info-card
  grids only.
- **Don't** combine `hero-gradient` with `signature-highlight` on the
  same surface. Pick one register.
