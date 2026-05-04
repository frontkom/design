# Frontkom Design

Machine-readable design system for [frontkom.com](https://frontkom.com),
following the open [DESIGN.md spec](https://github.com/google-labs-code/design.md)
from Google Labs.

Drop this file into any AI coding agent's context (Claude Code, Cursor,
Stitch, Gemini CLI, GitHub Copilot) and it will generate UI that matches
Frontkom's brand without further prompting.

## Files

- `DESIGN.md` — the design system itself. YAML tokens + prose rationale.
- `assets/logo-frontkom.svg` — the wordmark, single-color, 560×107 viewBox.
  All paths use `#35323C` (`{colors.foreground}`) so the logo inverts cleanly
  on dark surfaces by setting `fill: var(--color-on-dark)`.

## Validate

```sh
npx @google/design.md lint DESIGN.md
```

Should report `errors: 0, warnings: 0`.

## Export to Tailwind

```sh
npx @google/design.md export --format tailwind DESIGN.md > tailwind.theme.json
```

Or to W3C DTCG `tokens.json`:

```sh
npx @google/design.md export --format dtcg DESIGN.md > tokens.json
```

## Use with Claude Code / Cursor

Put `DESIGN.md` at the project root. The agent will pick it up automatically.
For Claude Code, you can also reference it explicitly from `CLAUDE.md`:

```md
## Design system

Always follow the rules in `DESIGN.md`. Run
`npx @google/design.md lint DESIGN.md` after introducing new components to
verify WCAG AA compliance.
```

## Use with Stitch

Generate the file natively in Stitch, or import this one via the Stitch
canvas → Design system → Import DESIGN.md.

## Status

`alpha` — both the DESIGN.md spec and this file are evolving. When the spec
adds gradient and shadow tokens, this file should be updated to use them
natively rather than documenting them in prose.
