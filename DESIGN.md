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
  background-dark-deep: "#12003B" # A shade deeper than background-dark, for the
                                # button-brand hover state. 19.29:1 on white text.
                                # OPEN: the 2021 book says #160046 for a deep indigo,
                                # and the new colour page shows that value. Not
                                # resolved — kept at #12003B until the team decides.
  background-muted: "#F7F7F8"  # Soft Cloud — alternative section bg on web.
  slide-statement-canvas: "#F7F7F8" # Alias of background-muted. Same value,
                                # named so the role is visible at the call site:
                                # the muted-grey canvas reserved for statement
                                # slides (see components.slide-statement).
  # ===== FOREGROUND =====
  foreground: "#35323C"         # Charcoal Plum. Pantone 4287 C. Brand book p. 7.
  on-dark: "#FFFFFF"           # Primary text on background-dark.
  on-dark-muted: "#C8B5FF"     # Soft Lavender — secondary text & taglines on indigo.
  surface-lavender: "#C8B5FF"  # Soft Lavender used as a light interactive surface
                                # (button-on-dark hover). Same value as on-dark-muted,
                                # named separately because the role differs.
  # Foreground levels — pre-blended on white for WCAG validation
  foreground-muted: "#5E5C66"  # Web / long-form body paragraphs (~80% foreground
                                # on white). NOT for pastel info cards or slide
                                # cards — those use full `foreground` charcoal.
  foreground-subtle: "#9A98A0" # Metadata & timestamps only (~50% on white). NOT for
                                # quotes anymore — quotes are indigo (see quote token).
  # ===== LINKS =====
  link: "#4F1BE5"              # Vivid Violet. Pantone 2090 C. Brand book p. 7.
  link-on-dark: "#C8B5FF"      # Soft Lavender. Same value as on-dark-muted but
                                # documented separately because the role differs.
  link-hover: "#3E15B4"        # Darkened Vivid Violet for text-link hover.
                                # Replaces the earlier one-off reuse of gradient-4
                                # in the interaction layer. 10.65:1 on white.
  # ===== ACTION (primary CTA) =====
  action: "#521CE4"            # Primary action / CTA violet. Same hue as the
                                # gradient violet endpoint (gradient-5), promoted
                                # to a named interaction role so buttons don't
                                # reach into the decorative gradient stops.
                                # 7.94:1 against white text — passes WCAG AA.
  action-hover: "#3E15B4"      # Darkened action violet for primary-button hover.
                                # Same value as link-hover; named per role.
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
  # Derived as 78% tints of the four brand gradient colors (gradient-2…5),
  # so the fills share the brand's hue family and step clearly from one to
  # the next. When several cards sit together, ALWAYS stack them light →
  # dark in this gradient order (rose → magenta → purple → blue), never in
  # a random order. Charcoal body text stays ≥8.4:1 on all four.
  pastel-rose: "#F7D6DF"       # 78% tint of gradient-2 (#DA446E). Lightest.
  pastel-magenta: "#F0CFEC"    # 78% tint of gradient-3 (#BC25A9).
  pastel-purple: "#E4CEF4"     # 78% tint of gradient-4 (#861FCB).
  pastel-blue: "#D9CDF9"       # 78% tint of gradient-5 (#521CE4). Darkest.
  # ===== BRAND GRADIENT (5-stop) =====
  # The signature gradient. Used as text fill, text-flow, decorative bars,
  # frame accents. Derived from brand book's 7-stop "color harmony" (p. 8),
  # condensed to 5 stops for cleaner rendering on text and small surfaces.
  # Pantone + CMYK confirmed against the 2021 book (Oct 2026 review).
  # Flag: the library "Gradient" style has only THREE stops. Five (print) vs
  # three (screen) may both be correct, but it isn't documented anywhere.
  gradient-1: "#F86233"        # = brand. Pantone 1585 C. C0 M66 Y99 K0. Start.
  gradient-2: "#DA446E"        # Pantone 198 C.  C0 M85 Y41 K0.
  gradient-3: "#BC25A9"        # Pantone 2395 C. C23 M96 Y0 K0. Middle stop (p. 8).
  gradient-4: "#861FCB"        # Pantone 2592 C. C52 M93 Y0 K0. (#861FC8 in 2021 = typo.)
  gradient-5: "#521CE4"        # Pantone 2090 C. C78 M89 Y0 K0. Terminus, near link.
typography:
  # Hero uses Red Hat Display 500 (Medium) — how frontkom.com renders the H1,
  # and the canvas the gradient text-fill sits on. Display has more character
  # at very large sizes than Red Hat Text. (Brand book specifies only Red Hat
  # Text; this is a documented website-led extension.)
  hero:
    fontFamily: Red Hat Display
    fontSize: 80px
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: -0.01em
  # All other headers use Red Hat Text Medium (500) per brandbook 3.0's
  # typography page. Sizes follow the 1.333 (4:3) ratio scale.
  h1:
    fontFamily: Red Hat Text
    fontSize: 60px
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: -0.01em
  h2:
    fontFamily: Red Hat Text
    fontSize: 45px
    fontWeight: 500
    lineHeight: 1.2
  h3:
    fontFamily: Red Hat Text
    fontSize: 34px
    fontWeight: 500
    lineHeight: 1.25
  h4:
    fontFamily: Red Hat Text
    fontSize: 25px
    fontWeight: 500        # Red Hat Text Medium — all headers Medium (brandbook 3.0)
    lineHeight: 1.3
  h5:
    fontFamily: Red Hat Text
    fontSize: 19px
    fontWeight: 500        # Red Hat Text Medium (brandbook 3.0)
    lineHeight: 1.4
  # Poster heading — used in advertising and event materials. Larger letter
  # spacing, often set in ALL CAPS. See annonse-eksempelene.
  poster:
    fontFamily: Red Hat Text
    fontSize: 56px
    fontWeight: 500
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
    fontWeight: 500
    lineHeight: 1.4
  eyebrow:
    fontFamily: Red Hat Text
    fontSize: 12px
    fontWeight: 500
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
  spacing-section-y: 96px      # Semantic layout value (vertical section rhythm),
                               # not a primitive step on the xs–4xl scale.
  container-x: 16px
  container-x-md: 24px
  container-x-lg: 32px
# Corner radius. NOTE: the brand book does not define corner treatment —
# there is no rule for it there. Rounded (not sharp) corners are chosen
# because active material — presentations and the website — has used them
# consistently over time, giving a soft expression that matches the soft,
# organic forms in the logo symbol. Keep the rounding restrained: enough
# to read as soft, never so much that it looks naive or unserious. This is
# read-from-practice, not a brand-book value (cf. the colors, which cite
# brand-book pages).
rounded:
  sm: 8px      # input fields
  md: 12px     # small elements: colour swatches, tags, chips, thumbnails. Also
               # any element nested inside a card — one step down from the card's
               # 20px so the two surfaces read as separate, not merged into one.
  lg: 20px     # cards, panels, image frames
  full: 9999px # buttons, pills, badges. Nothing else
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
  # used as a decorative border along the TOP edge of a slide/section only
  # (never the bottom). See Bakgårdsfest poster top edge. It is a SMOOTH
  # continuous blend, not hard-edged color segments — see the CSS in
  # Components / gradient-bar.
  gradient-bar:
    # FALLBACK ONLY — a single color field can't express the 5-stop gradient.
    # Render the smooth linear-gradient from the CSS below, not this solid.
    backgroundColor: "{colors.brand}"  # fallback; gradientStart=gradient-1, gradientEnd=gradient-5
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
  # PRIMARY — solid violet pill with white text. The high-emphasis primary
  # CTA across web and slides. 7.94:1 — passes WCAG AA for normal text, so no
  # compromise on text color (unlike orange, which forced dark text). Hover
  # darkens. Replaces the former orange primary.
  button-primary:
    backgroundColor: "{colors.action}"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-primary-hover:
    backgroundColor: "{colors.action-hover}"
    textColor: "{colors.on-dark}"
    textDecoration: underline    # underline the label on hover
  # SECONDARY — solid deep-indigo pill with white text. NOTE: the token is
  # still named `button-brand` for continuity, but it no longer uses the
  # brand orange — the orange button was retired from the set. Default is
  # indigo (17.92:1); hover goes a shade deeper and underlines the label.
  button-brand:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-brand-hover:
    backgroundColor: "{colors.background-dark-deep}"
    textColor: "{colors.on-dark}"
    textDecoration: underline
  # White pill with charcoal text. Standard CTA on indigo sections.
  button-on-dark:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: 14px 24px
  button-on-dark-hover:
    backgroundColor: "{colors.surface-lavender}"
    textColor: "{colors.foreground}"
    textDecoration: underline

  # ===========================================================
  # CARDS
  # ===========================================================
  card-light:
    backgroundColor: "{colors.background-muted}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: 32px
  card-light-bordered:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: 32px
  card-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.lg}"
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
  # Quote block — indigo body (NOT the old light grey, which measured
  # 2.85:1 and failed AA — and a quote should be foregrounded, not receded).
  # Opening sentence in brand orange bold. Orange measures 3.09:1 and clears
  # AA only as Large Text, so the opening NEVER goes below 25px (h3 size).
  # Oct 2026 review, replaces brand book p. 13 grey treatment.
  quote:
    textColor: "{colors.background-dark}"   # #1A0054 indigo
    typography: "{typography.h3}"           # 34/46
  quote-emphasis:
    textColor: "{colors.brand}"             # #F86233 orange opening sentence
    typography: "{typography.h3}"
    fontWeight: 500   # emphasis carried by colour (orange vs indigo), not weight
  quote-name:
    textColor: "{colors.foreground}"
    typography: "{typography.h4}"           # 25/33
    fontWeight: 500
  quote-role:
    textColor: "{colors.foreground}"
    typography: "{typography.lead}"         # 22/33
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
  # The frame is a pure-white shape holding the charcoal logo, padding
  # proportional to the banner. Which SHAPE depends on the banner aspect
  # ratio — so there are three sibling tokens, one per shape. Pick the one
  # that matches the format; don't reshape a single token. Only the rounded
  # variant uses a CSS `rounded` value — diamond and arrow are SVG paths.
  logo-frame-diamond:      # Square / tall banners (e.g. 580×500)
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: diamond         # a square rotated 45°; drawn as an SVG path, not a radius
    padding: 32px 48px
  logo-frame-arrow:        # Wide banners (e.g. 980×300)
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: arrow           # right-pointing arrow / pentagon; SVG path, not a radius
    padding: 32px 48px
  logo-frame-rounded:      # Narrow vertical banners (e.g. 180×500)
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    shape: rounded-square
    rounded: "{rounded.lg}"
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
  # Logo placement is ALWAYS bottom-right on content slides; on the cover
  # the logo sits in the lower third, aligned with the title — left if the
  # title is left-aligned, centered only when the whole composition is.

  # Cover slide — first slide of a deck. Indigo with a gradient bar on the
  # top edge only, eyebrow + h1 + logo. See "Master sales slides" cover.
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
  # outlined element. Text color is background-dark (deep indigo #1A0054)
  # for the bulk of the heading — NOT charcoal foreground; the indigo ties
  # the light slide to the brand's dark canvas. Key words can be set in
  # brand orange for emphasis (like
  # "**lønnsom**" and "**bærekraftig**" on s. 19). Pure-orange statement
  # headings exist (s. 17 "Vi hjelper ambisiøse bedrifter å vokse") as a
  # deliberate brand-stylistic choice but fall below WCAG AA large text
  # threshold — use sparingly, never for body copy.
  slide-statement:
    backgroundColor: "{colors.slide-statement-canvas}"
    textColor: "{colors.background-dark}"
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
  # Four fills, derived from the brand gradient (gradient-2…5). When
  # several sit together, stack them light → dark in gradient order:
  # rose → magenta → purple → blue. Body text is full-strength foreground
  # charcoal — NEVER foreground-muted grey. The card HEADING and any
  # key-word emphasis take the card's own `emphasisColor` (its parent
  # gradient hue) — NOT charcoal. Content is TOP-aligned (verticalAlign:
  # top), never vertically centered. Deck-level variants, not locked tokens.
  slide-card-rose:
    backgroundColor: "{colors.pastel-rose}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-2}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  slide-card-magenta:
    backgroundColor: "{colors.pastel-magenta}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-3}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  slide-card-purple:
    backgroundColor: "{colors.pastel-purple}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-4}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top
  slide-card-blue:
    backgroundColor: "{colors.pastel-blue}"
    textColor: "{colors.foreground}"
    emphasisColor: "{colors.gradient-5}"
    rounded: "{rounded.lg}"
    padding: 32px
    verticalAlign: top

  # Speech bubble — comic-style callout used to highlight a key remark.
  # Indigo bubble with white text (default), or white bubble with charcoal
  # text. The tail/pointer is drawn as part of the SVG/shape, not built
  # from this token.
  slide-bubble-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.lg}"
    padding: 24px 32px
  slide-bubble-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
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
    fontFamily: Red Hat Display   # Display 400 — the one editorial use of Display
    fontWeight: 400
---

# Frontkom Design System

## Logo usage — read this before generating any visual

The Frontkom wordmark is `assets/logo-frontkom.svg`
(canonical source: https://github.com/frontkom/design/blob/main/logo-frontkom.svg).
**Do not reconstruct it, and never create variants of the logo.** Always
reference, embed, or copy the actual SVG file from
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
the logo is the primary subject (see the `logo-frame-*` components); for
social media, posters, slides, app screens, and most other dark-canvas
uses, place the inverted logo directly on the indigo background.

Three SVG files are the single source of truth — link to, embed, or copy
these exact files. Never recreate the logo or make variants of it:

- `assets/logo-frontkom.svg` — charcoal logo (full lockup) for **light backgrounds**.
  Source: https://github.com/frontkom/design/blob/main/logo-frontkom.svg
- `assets/logo-frontkom-on-dark.svg` — white logo (full lockup) for **indigo / dark
  backgrounds**.
  Source: https://github.com/frontkom/design/blob/main/logo-frontkom-on-dark.svg
- `assets/logo-frontkom-symbol-outlined.svg` — outlined version of the symbol
  only (no wordmark), in soft grey strokes. **Use very sparingly** — only as a
  giant decorative element on statement slides (see Slides & presentations /
  Statement slide). `viewBox="0 0 110 107"`.
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
("[Frontkom logo]") — not to attempt a freehand SVG.

### Clear space & spacing

Clear space is measured on the lowercase **r**, NOT on the symbol height
(the old "clear space = symbol height" rule is wrong). Measured on the
2021 lockup (the orange plate is 560×165 with the 476×81 logo area
inside — exactly 42px of air on all four sides; the `r` is 29×42):

- **Clear space** around the lockup = the **height of the `r`** (the
  x-height of the logotype) = **8.82% of the lockup width**. Keep at
  least this much empty space on all four sides.
- **Space between symbol and logotype** = the **width of the `r`** =
  **6.1% of the lockup width**. ("Space between symbol and logotype
  equals the width of r" is verbatim from the 2021 file, on a page that
  never made the PDF export.)

The symbol's own height is ~82 at the same scale — nearly double the
clear space — so never use the symbol height as the clear-space measure.

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
<link href="https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;0,500;1,400;1,500&family=Red+Hat+Text:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
```

Or via CSS `@import`:

```css
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Display:ital,wght@0,400;0,500;1,400;1,500&family=Red+Hat+Text:ital,wght@0,400;0,500;1,400;1,500&display=swap');
```

The URL above includes only the weights and styles the system uses:
Display 400 regular & italic; Text 400 regular & italic, 700 regular &
italic. The system uses just two weights: 400 (Regular) for paragraphs
and 500 (Medium) for everything else — don't load weights beyond these.

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
- Don't load every weight. The system uses 400 and 500 only. Loading
  300, 500, 600, 800, 900 wastes bandwidth and tempts mixing.
- Don't use the variable font's full weight axis to invent new weights
  the full variable axis is wasteful. Stick to 400 and 500.

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

Don't think of one as default and the other as exception — they're peers,
chosen by context. Presentations lean on the dark canvas; the website
stays light, with the occasional dark section as a break in the rhythm.
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
  passes 12.6:1 on white. Exception: on pastel info cards the heading and
  key-word emphasis take the card's `emphasisColor` (its gradient hue),
  not charcoal.
- **`foreground-muted` `#5E5C66`** (≈80%) — web / long-form body
  paragraphs. AA passes 6.4:1. Not for pastel info cards or slide cards —
  those keep body text in full `foreground` charcoal.
- **`foreground-subtle` `#9A98A0`** (≈50%) — metadata and timestamps only
  (quotes are now indigo, not grey).
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

Per brandbook 3.0's typography page: **Red Hat Text Medium (500)** for all
headers, **Red Hat Text Regular (400)** for paragraphs. Sizes follow a
1.333 (4:3) ratio scale. (This restores the 2021 book's Medium header
weight — an earlier draft of this file had used Bold 700 with h4/h5 in
regular; brandbook 3.0 settles on a single Medium weight across the header
ramp.)

The website adds a documented exception: **Red Hat Display** is used on
the marketing hero H1 (the canvas for the gradient text fill; Display 500
to match the header weight) **and on the signature highlighted phrase**
(`signature-highlight`). The 2021 file uses Display in both places; the
original typography page never listed them, which was a gap, not a doubt.
Everywhere else is Red Hat Text (400 / 500).

Posters and advertising add a third extension: the **`poster`** size
(56px / `letterSpacing: 0.02em`), used for short event titles like
"BAKGÅRDSFEST". Posters can be set in ALL CAPS — the only place in the
system where ALL CAPS is permitted for headings (the eyebrow uses
uppercase but is not a heading).

### Roles

- **`hero`** — Red Hat Display 500, ~80px. The marketing H1 with
  gradient text fill.
- **`h1`** — Red Hat Text 500, ~60px. Article H1, secondary marketing
  hero, page titles in editorial mode, and the ad text-flow size.
- **`h2`** — Red Hat Text 500, ~45px. Major section headings.
- **`h3`** — Red Hat Text 500, ~34px. Article H2.
- **`h4`** — Red Hat Text 500, ~25px. Subsection headings, quote blocks.
- **`h5`** — Red Hat Text 500, ~19px. Card titles. Sits close to `body`,
  so lean on size and placement to keep it reading as a heading.
- **`poster`** — Red Hat Text 500, ~56px, slightly increased letter-
  spacing. Event posters and short ad headlines (often ALL CAPS).
- **`lead`** — Red Hat Text 400, 22px. The "eye-catching intro" (brand
  book p. 9). Use once, at the start of a text block.
- **`body`** — Red Hat Text 400, 17px / 1.6. Workhorse paragraph text.
- **`body-sm`** — Red Hat Text 400, 14px. Image subtitles, fine print.
- **`label`** — Red Hat Text 500, 14px. Buttons, UI labels.
- **`eyebrow`** — Red Hat Text 500, 12px, uppercase, `tracking: 0.1em`.

### Fluid sizing

Token values are desktop maximums. On web, scale fluidly with `clamp()`
for mobile — e.g. `clamp(40px, 6vw, 80px)` for hero. Don't use abrupt
breakpoints.

On fixed canvases (ads, posters, slides — e.g. a 1:1 social ad) there is
no fluid range, so the headline must be **scaled down to fit the frame,
and text must never be clipped or run off the edge.** Shrink the heading
size (and re-wrap) until the longest line fits with margin to spare.
Budget width for the longest word before locking a size — remember
Norwegian runs ~10–15% longer than English, and ALL CAPS is wider than
sentence case (e.g. "ORGANISASJONER"). If it still won't fit, reduce the
size further or shorten the copy — never crop.

### Casing

Sentence case for headings and body text by default. ALL CAPS is
permitted only on the `poster` size for standalone event titles, and on
the `eyebrow` token. Title Case is not used. Never mix cases within a
single heading — in particular, a `gradient-flow-emphasis` headline is
sentence case throughout; the gradient clause is NOT set in ALL CAPS.

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
3. **Corner radius** — `rounded.lg` (cards, panels, and the logo frame)
   creates softness without shadow.
4. **Outlined symbol elements** (brand book p. 17) — outlined versions
   of the Frontkom symbol can be placed partially off-canvas as
   atmospheric depth devices.
5. **Filled symbol as a tint** — the mark scaled far beyond the frame
   and cropped by the edge, in a tone so close to the surface it reads
   as texture, not as a logo. On light grey: white symbol (1.05:1 vs
   `#F7F7F8`). On indigo: `#22006C` (1.10:1 vs `#1A0054`).

Indigo tints are made by **lightening along the hue, not by mixing in a
neutral.** `#1A0054` has green at zero; `#2D1170` adds green and turns
muddy, while `#22006C` keeps green at zero and reads cleaner even though
it measures weaker.

If `box-shadow` feels needed, increase contrast or radius instead.

## Shapes

- **Actions** — always `rounded.full` (pill). Buttons, tags, language
  toggle. No square corners on interactive elements.
- **Cards** — `rounded.lg` (20px), the same on web and slides. Kept
  deliberately restrained — soft, never so round it looks naive.
- **Inputs** — `rounded.sm` (8px). The only place where shape softens
  but doesn't go fully round.
- **Small & nested elements** — `rounded.md` (12px). Colour swatches,
  tags, chips, thumbnails, and anything sitting *inside* a card. Radius
  steps down as surfaces nest: an element inside a card takes 12px, never
  the card's own 20px, so the two surfaces read as separate rather than
  merging into one.
- **Logo frame (advertising only)** — `rounded.lg` (20px) when
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
headings on **both white and indigo canvases** — the 2021 cover and the
EU-law ad both run full gradient text on indigo. Size floor: **never
below `h3`.** Solid `brand` orange is the fallback for engines without
`background-clip: text` support.

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
phrase in gradient.

**It is ONE continuous heading, not two stacked elements.** The solid
clause and the gradient clause share the same size, weight, and case —
only the color changes between them. Set the whole thing in **sentence
case**; never put the gradient clause (or any part of it) in ALL CAPS,
and never enlarge one clause relative to the other. ALL CAPS belongs to
`poster` event titles only (see Casing and `poster-title`), never to
gradient-flow headlines.

Geometry (corrected, Oct 2026 review — the old "top-down on multi-line"
rule was wrong): the ramp runs **horizontally and restarts on every
line**. Each line opens in orange; how far along the ramp it gets depends
on the line length, so short lines stop at magenta — that is correct, not
a bug.

Technique: put the gradient on the **whole heading** and paint the setup
phrase back in **solid** color on top. Never fill the emphasis phrase as
its own element — that restarts the ramp on each line *of the phrase*.
Break the line so the emphasis phrase **starts at the left margin**; that
is what makes it open in orange.

```css
.flow        { display: inline-block;
               background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
               background-clip: text; -webkit-background-clip: text;
               color: transparent; }
.flow .solid { color: #FFFFFF; }   /* setup phrase painted back solid (charcoal on white) */
```

This is the strongest brand moment in advertising and works equally
well on indigo and white. Use it when the message has a primary clause
("we offer X") and an emphasis clause ("for the kinds of people we want
to reach"). The gradient does the work of italics and underline at
once.

#### 3. `gradient-bar` — gradient stripe

A thin horizontal stripe of the full 5-stop gradient, used as a
decorative border along the **top edge only** of a slide or poster.
Never place it at the bottom of a slide, and never on both edges — it is
a top accent. See the top edge of the Bakgårdsfest poster — a single 6px
stripe spanning the full width does the work of a frame.

It must be a **smooth, continuous blend** — the colors flow into one
another with no hard stops. Do NOT render it as five equal solid blocks
or a segmented / banded stripe. Use the CSS below verbatim (even 90°
distribution, no explicit stop percentages):

```css
background: linear-gradient(90deg, #F86233, #DA446E, #BC25A9, #861FCB, #521CE4);
height: 6px;
```

### Buttons

All buttons are pills (`rounded.full`) with `label` typography and flat
color transitions at 150–200ms. No transforms.

- **`button-primary`** — solid violet pill (`action`, #521CE4) with white
  text. The high-emphasis primary CTA across web and slides. White text
  clears WCAG AA at 7.94:1, so no dark-text compromise. Hover darkens to
  `action-hover` and underlines the label.
- **`button-brand`** — solid deep-indigo pill with white text. The
  secondary CTA. (Name kept for continuity; the orange button was retired,
  so despite the name this no longer uses the brand orange.) Hover goes a
  shade deeper (`background-dark-deep`) and underlines the label.
- **`button-on-dark`** — white pill with charcoal text. Standard CTA on
  indigo sections. Hover fills with Soft Lavender (`surface-lavender`) and
  underlines the label.

### Cards

- **`card-light`** — `background-muted` fill on white sections.
  Workhorse. `rounded.lg`, 32px padding.
- **`card-light-bordered`** — white fill with 1px `border`, for cards
  on `background-muted` sections where contrast is needed.
- **`card-dark`** — `background-dark` fill, white text, `rounded.lg`,
  40px padding.

### Editorial

- **`body-paragraph`** — `body` typography in `foreground-muted` on
  light. The reading style for long-form prose.
- **`body-paragraph-on-dark`** — `body` in `on-dark` (white) on indigo.
- **`caption`** — `body-sm` in `foreground-subtle`. Image subtitles,
  metadata, fine print. Never body copy.
- **`quote`** + **`quote-emphasis`** (+ `quote-name`, `quote-role`) —
  large quote blocks. Quote body in `background-dark` indigo at `h3`
  (34/46); the opening sentence in `brand` orange bold. This replaces the
  old light-grey treatment, which measured 2.85:1 and failed AA — and a
  quote should be foregrounded, not receded. The orange opening measures
  3.09:1, so it clears AA only as Large Text: it never drops below 25px.
  Attribution: `quote-name` charcoal 25/33 bold, `quote-role` charcoal
  22/33. (Open conflict: the "one orange phrase per page" signature rule —
  an orange quote opening is one such highlight. Either the opening is
  exempt, or a quote counts as the page's one highlight. Not yet resolved.)
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
  `button-primary` CTA on the right. Includes the NO/EN language toggle.
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

- **`logo-frame-diamond` / `logo-frame-arrow` / `logo-frame-rounded`** —
  the white shape that holds the wordmark in **formal display banner ads
  only** (banner formats like 580×500, 980×300, 180×500 where the logo is
  the hero element). For social media, posters, slides, app UI, and any
  other indigo surface, place the inverted white logo directly on the
  indigo background — do NOT use a frame. One token per shape; pick by
  banner aspect ratio:
  - `logo-frame-diamond` — square / tall (e.g. 580×500). Square rotated
    45°, drawn as an SVG path.
  - `logo-frame-arrow` — wide (e.g. 980×300). Right-pointing arrow /
    pentagon, drawn as an SVG path.
  - `logo-frame-rounded` — narrow vertical (e.g. 180×500). Rounded
    square at `rounded.lg` (20px) — the only variant with a CSS radius.
  - In all cases: pure white fill, charcoal logo inside, padding
    proportional to the banner size.
- **`poster-title`** — large bold title on indigo for **event posters
  and short standalone event titles** (e.g. "BAKGÅRDSFEST"), using the
  `poster` typography. This is the one place ALL CAPS is allowed on a
  title, and it may take a gradient fill. Do NOT use `poster-title` for
  sentence-style ad headlines like "Lønnsom vekst for ambisiøse
  bedrifter …" — those are `gradient-flow-emphasis`, in sentence case.

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

### Slide layouts in the .pptx theme

The three canonical slide types must exist as **real layouts in the
deck's theme** (slide masters), not as formatting applied to individual
slides. A deck where indigo is painted per-slide breaks the moment
someone inserts a new slide or copies one into another file: they get a
white canvas and have to rebuild the brand by hand.

| Layout name | Maps to component | Canvas | Fixed elements |
|---|---|---|---|
| `Frontkom forside` | `slide-cover` | `background-dark` | Gradient bar, top edge; white logo in lower third, aligned with the title |
| `Frontkom mørk side` | `slide-content` | `background-dark` | White logo bottom-right |
| `Frontkom lys side` | `slide-statement` | `background-muted` | Charcoal logo bottom-right |

The two remaining slide types are variants on the dark layout: chapter
dividers and closing / CTA slides both build on `Frontkom mørk side`, so
these three theme layouts cover all five slide types.

**Background and logo live on the layout, never on the slide.** This is
what makes duplication and insertion safe, and it's the only way the
logo stays in its non-negotiable position without relying on discipline.

Placeholders per layout:

- `Frontkom forside` — eyebrow, title, subtitle
- `Frontkom mørk side` — eyebrow, title
- `Frontkom lys side` — title

#### Two rules that are easy to get wrong

**Every placeholder a layout declares must be filled by the slides using
it.** PowerPoint draws the prompt text ("Klikk for å legge til tekst")
for any placeholder a slide leaves empty, and it lands on top of
whatever the slide already contains. Slide text must be written *into*
the placeholder, not into a separate text box positioned over it. If a
layout needs a slot that most slides won't use, leave it out — the
content slide is a free canvas below the title, not a body-text
template.

**Title placeholders must set left alignment explicitly.** PowerPoint's
built-in title placeholder centers by default, and a title inherits that
unless the layout overrides it. Every heading in this system is
left-aligned.

#### Copying slides between decks

A slide pasted into another presentation adopts the destination theme
unless the person chooses *Keep source formatting* — the branded canvas
reverts to white. This is PowerPoint behaviour and cannot be designed
around; note it when handing a deck over.

### Slide types

Five canonical slide types cover almost every deck:

#### 1. Cover slide

The first slide. Indigo canvas with **a gradient bar on the top edge**
(the cover is the one slide that carries the gradient bar). Centered
or left-aligned composition with:

- An eyebrow in `brand` orange (e.g. "A part of the Frontkom Value
  Layer")
- The slide title in `h1`, white (`on-dark`)
- The Frontkom logo in white in the lower third, **aligned with the
  title** — left-aligned when the title is left-aligned, centered only
  when the whole composition is centered. Don't center the logo under a
  left-aligned title; the logo floating mid-slide while the text sits
  left looks off.

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
- Heading text color: **`background-dark` deep indigo (`#1A0054`)** for
  the bulk of the heading — not charcoal `foreground`. On a light slide
  canvas the dark heading text is always indigo: it ties the slide to the
  brand's dark canvas and reads more branded than a neutral grey (and it's
  higher contrast — 16.74:1 on the muted canvas). Emphasis words in
  **bold** `brand` orange ("Hva mener vi med **lønnsom** og
  **bærekraftig** vekst?"). This is the canonical pattern.
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
  beyond the canvas right edge. Render it in **soft lavender
  (`on-dark-muted`, #C8B5FF) at low opacity on a dark / indigo canvas** —
  that is where this device belongs. Avoid the grey-outline-on-light
  treatment: on a pale background the stray wireframe reads as an
  unfinished artifact, not a brand device. If the slide is light, either
  drop the symbol or keep it extremely faint.
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

A grid of pastel-filled cards. Two firm colour rules, both easy to get
wrong by falling back on the generic "dark heading + grey body" pattern:

- **Card heading and any key-word emphasis take the card's `emphasisColor`
  — its parent gradient hue — never charcoal.** That colour is what ties
  each card to its fill.
- **Body text is full-strength `foreground` charcoal — never
  `foreground-muted` grey**, which looks washed and muddy on the pastel
  fills.

**Top-align the content in every card — never vertically center it.**
Each card sets `verticalAlign: top`: the heading starts at the top padding
and text flows down from there, so the headings line up across the row.
Vertical centering is the most common mistake here — cards hold different
amounts of copy, so centering pushes each heading to a different height
and the row looks ragged. Equal card heights are fine; the content still
starts at the top, not the middle.

The four fills are 78% tints of the brand gradient (gradient-2…5). When
several cards sit together, **always stack them light → dark in gradient
order** — rose, magenta, purple, blue — never a random arrangement. Each
pairs with its parent hue as the emphasis color:

- `slide-card-rose` — `pastel-rose` (`#F7D6DF`) bg; emphasis in
  `gradient-2` rose (`#DA446E`). Lightest.
- `slide-card-magenta` — `pastel-magenta` (`#F0CFEC`) bg; emphasis in
  `gradient-3` magenta (`#BC25A9`).
- `slide-card-purple` — `pastel-purple` (`#E4CEF4`) bg; emphasis in
  `gradient-4` purple (`#861FCB`).
- `slide-card-blue` — `pastel-blue` (`#D9CDF9`) bg; emphasis in
  `gradient-5` blue-violet (`#521CE4`). Darkest.

Mix in 1–2 photo cards (rounded `rounded.lg`) at the same dimensions
to break the monotony.

Note on contrast (emphasis = parent hue, measured on each fill):

- `slide-card-blue` — `gradient-5` on `pastel-blue` is **5.3:1**. Passes
  AA for normal text; the strongest pairing.
- `slide-card-purple` — `gradient-4` on `pastel-purple` is **4.7:1**.
  Passes AA for normal text.
- `slide-card-magenta` — `gradient-3` on `pastel-magenta` is **3.7:1**.
  Large Text only — keep the emphasis to bold headings (`h5`+), not body.
- `slide-card-rose` — `gradient-2` on `pastel-rose` is **3.1:1**. The
  weakest — only clears Large Text; keep the rose emphasis to short bold
  headings, or darken it (e.g. to `gradient-4` purple) if you need more.

Because each emphasis sits on its own hue's tint, the two warm fills
(rose, magenta) have modest contrast — fine for a bold card heading, not
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
  card variants (`slide-card-rose` / `magenta` / `purple` / `blue`) instead.

## Photography

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

### Text over photo

Three treatments:

1. **None** — only where the image is quiet behind the text. Check at the
   smallest size the layout ever renders.
2. **Darken the whole image** — indigo at ~55%. When text sits in the
   middle of the frame, or when the crop may change.
3. **A scrim behind the text** — indigo fading to nothing. When the image
   carries the message and only part of it should go quiet.

Aim for the ratio, not the look: measure white against the lightest pixel
the text actually crosses, not the average. 4.5:1, or 3:1 for large text.
**The overlay is always indigo, never black** — black flattens the image
and pulls the composition out of the palette.

## Iconography

```
Source:  Aksel, designsystemet.no (open source)
Variant: Stroke
Grid:    24px
Use:     instances of the published components, so they update at source
```

Icons inherit the text colour beside them. An icon is never the only
carrier of meaning: it sits with a label, or it has an accessible name.

**The symbol is not an icon.** The Frontkom mark, the bracket bullet, and
the outlined shapes are brand elements. They never enter the icon set,
and an icon never stands in for the logo.

**The bullet is a bracket.** The bullet-point marker is the component
`shape/fill/bracket`, 8×16px, taken from the right-hand part of the
symbol. It is NOT a square rotated 45°.

## Avatars

Sharp corners, no rounding, no indigo variant. Four combinations only:

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

**No dash as a pause marker** — neither em dash nor en dash. Use a full
stop, comma, colon, or parentheses instead. Number ranges like 64–72px
are not pause markers and keep the dash.

## Archived

Retired, kept here so no one re-introduces them:

- **The anniversary logos.** (See open question below — Figma has a
  25-year version.)
- **The Frontkom Experience lockup.** Discontinued, no successor.
- **The outline display lettering** from the 2021 cover. Heading type
  takes the solid gradient fill instead. Note there is still a
  documented text style for it in the library, `Desktop/Background text
  outlined`; it should be retired there too.

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
- **Don't** mix Red Hat Display into anything other than `hero` and
  `signature-highlight`. Those are its only two uses; everything else is
  Red Hat Text.
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
- **Do** keep the brand orange tightly constrained on web. It fails WCAG
  AA as normal text on white and is not a web button color, so reserve it
  for large display headings, the gradient, and accents — not body text or
  UI. White text on an orange button is permitted on slides only, where
  WCAG AA doesn't apply (see Slide-specific).
- **Don't** use the `logo-frame-*`, `poster-title`, or `gradient-bar`
  components on web. They're for advertising contexts.

### Advertising-specific

- **Do** default to indigo canvas.
- **Do** use `gradient-flow-emphasis` to split a message into "the
  setup" (solid foreground) and "the punch" (gradient).
- **Do** use a white `logo-frame-*` to anchor the wordmark on indigo
  banner ads — pick the token whose shape matches the aspect ratio:
  `logo-frame-diamond`, `logo-frame-arrow`, or `logo-frame-rounded`.
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
- **Do** allow white text on an orange button in presentations. WCAG AA
  is not required on slides the way it is on web, so this pairing is
  permitted — even though white-on-orange (`#F86233`) sits at 3.09:1,
  below the web contrast bar. This is a deliberate slide-only exception.
  Orange otherwise stays sparing on slides; this is its one button use.
- **Do** use the muted grey canvas (`background-muted`) only for
  statement slides, paired with the giant outlined Frontkom symbol
  (`logo-frontkom-symbol-outlined.svg`) bottom-right.
- **Do** use the canonical quote treatment in slides too: indigo body,
  brand-orange bold opening sentence (min 25px).
- **Do** use the gradient harmony as the fill of stages or steps when
  showing progression — pyramid, journey, timeline. The gradient
  *means* "process / time / change" (brand book p. 8).
- **Do** include an orange eyebrow at the top-left of content slides
  to identify the deck section ("Master sales slides", "Om Frontkom").
- **Don't** set pastel card headings in charcoal. The heading takes the
  card's `emphasisColor` (its parent gradient hue) — that colour is the
  whole point of the card.
- **Don't** style pastel card body with the web editorial grey
  (`foreground-muted`). Inside a pastel card, body text is full
  `foreground` charcoal — the grey reads as washed and muddy on the fill.
- **Don't** vertically center the content inside info cards or columns.
  Top-align it (`verticalAlign: top`) so headings line up across the row;
  centering makes the tops sit at different heights and looks ragged.
- **Don't** use `hero-gradient` text fill on ordinary content-slide
  headings — prefer `signature-highlight` there. (Full gradient text fill
  is allowed on hero-scale headings and covers, on white or indigo, at
  `h3`+; it just isn't the treatment for a regular slide heading.)
- **Don't** put the logo anywhere except bottom-right on content
  slides. Cover slides are the only exception — the logo sits in the
  lower third there, aligned with the title (not centered under a
  left-aligned title).
- **Don't** use `decorative-stripe` (web) or `gradient-bar` (poster)
  inside content slides. The cover slide is the only place a gradient
  bar appears in a deck — on the **top edge only**, never the bottom.
- **Don't** use Red Hat Display on slides except for the
  `signature-highlight` phrase (Display 400). Everything else on slides
  is Red Hat Text.
- **Don't** use the pastel slide cards (`pastel-rose`, `pastel-magenta`,
  `pastel-purple`, `pastel-blue`) on web. They're for slide info-card
  grids only.
- **Don't** combine `hero-gradient` with `signature-highlight` on the
  same surface. Pick one register.
