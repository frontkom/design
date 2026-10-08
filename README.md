# Frontkom Design

Machine-readable design system for [Frontkom](https://frontkom.com), a technology-driven agency working across Norway, Portugal and Poland. The file follows the open [DESIGN.md spec](https://github.com/google-labs-code/design.md) from Google Labs.

Drop `DESIGN.md` into any AI agent's context (Claude, Cursor, Stitch, Gemini CLI, GitHub Copilot) and it will produce output that matches the Frontkom brand: web, slides, documents and ads.

## One source, three places

The same content lives in three places, and they must say the same thing:

| Place | What it is |
| --- | --- |
| `DESIGN.md` in this repository | The source. YAML tokens and prose rules. |
| The org skill `frontkom-brand-design` | The same text, used by Claude across Frontkom. |
| The Tindre Standard "Frontkom Design System" | The governed version, with owner and revisions. |

If they disagree, this repository decides.

## Files

| File | Use |
| --- | --- |
| `DESIGN.md` | The design system: tokens and rules. |
| `logo-frontkom.svg` | Charcoal logo (`#35323C`) for light backgrounds. `viewBox="0 0 560 107"`. |
| `logo-frontkom-on-dark.svg` | White logo for indigo and other dark backgrounds. |
| `logo-frontkom-symbol-outlined.svg` | Outlined symbol, no wordmark. `viewBox="0 0 110 107"`. Optional decorative use. |
| `RedHatDisplay-VariableFont_wght.ttf` | Red Hat Display, headings. |
| `RedHatDisplay-Italic-VariableFont_wght.ttf` | Red Hat Display italic. |
| `RedHatText-VariableFont_wght.ttf` | Red Hat Text, body and UI. |
| `RedHatText-Italic-VariableFont_wght.ttf` | Red Hat Text italic. |

`DESIGN.md` refers to `assets/` and `assets/fonts/`. Those are the paths inside the project that uses the design system: copy the logos to `assets/` and the fonts to `assets/fonts/` there. In this repository the files sit at the root.

Never redraw or retype the logo. Use the SVG files.

## Validate

```sh
npx @google/design.md lint DESIGN.md
```

Expected result: `errors: 0` and 20 warnings. The warnings are known and accepted:

- 14 sub-tokens the spec does not support yet (`emphasisColor`, `verticalAlign`, `shape`, `textDecoration`)
- 4 watermark components that are low contrast on purpose, since they are texture only
- 2 colour tokens no component references (`foreground-subtle`, `link-hover`)

Any other warning, and every error, needs fixing before the change is merged.

## Export

To a Tailwind theme:

```sh
npx @google/design.md export --format tailwind DESIGN.md > tailwind.theme.json
```

To W3C DTCG `tokens.json`:

```sh
npx @google/design.md export --format dtcg DESIGN.md > tokens.json
```

## Use with an AI agent

Put `DESIGN.md` at the project root, together with the logos and fonts in `assets/`. Most agents pick it up automatically. In Claude Code you can also point to it from `CLAUDE.md`:

```md
## Design system

Always follow the rules in `DESIGN.md`. Run
`npx @google/design.md lint DESIGN.md` after adding new components.
```

Inside Frontkom, Claude already has the rules through the org skill `frontkom-brand-design`.

## Use with Stitch

Generate the file natively in Stitch, or import this one via the Stitch canvas: Design system, then Import DESIGN.md.

## Making a change

1. Edit `DESIGN.md` and run the linter.
2. Commit to this repository.
3. Publish the same text as the org skill `frontkom-brand-design`. The skill keeps `name: frontkom-brand-design` in its frontmatter; this file keeps `name: Frontkom`.
4. Paste the prose, without the YAML token block, into the Tindre Standard "Frontkom Design System" and publish a new revision.

A change that touches a brand book value records the brand book page next to it.

## Owner

Head of design at Frontkom.

## Status

`alpha`. Both the DESIGN.md spec and this file are evolving. When the spec adds gradient and shadow tokens, move to them instead of describing them in prose.
