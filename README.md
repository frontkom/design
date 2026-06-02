# Brand Design Repository

Machine-readable design systems for multiple brands, following the open
[DESIGN.md spec](https://github.com/google-labs-code/design.md) from Google Labs.

## Structure

- `Frontkom/DESIGN.md` — Frontkom design system.
- `Frontkom/assets/` — Frontkom logos, fonts, images, exports.
- `Tindre/DESIGN.md` — Tindre design system.
- `Tindre/assets/` — Tindre logos, fonts, images, exports.

## Validate a brand file

Run from repo root with the target file path:

```sh
npx @google/design.md lint Frontkom/DESIGN.md
npx @google/design.md lint Tindre/DESIGN.md
```

Should report `errors: 0, warnings: 0`.

## Export tokens

Example for Frontkom:

```sh
npx @google/design.md export --format tailwind Frontkom/DESIGN.md > Frontkom/tailwind.theme.json
npx @google/design.md export --format dtcg Frontkom/DESIGN.md > Frontkom/tokens.json
```

Example for Tindre:

```sh
npx @google/design.md export --format tailwind Tindre/DESIGN.md > Tindre/tailwind.theme.json
npx @google/design.md export --format dtcg Tindre/DESIGN.md > Tindre/tokens.json
```

## Use with Claude Code / Cursor

Reference the brand-specific file in your project instructions:

```md
## Design system

Always follow the rules in `Frontkom/DESIGN.md`.
Run `npx @google/design.md lint Frontkom/DESIGN.md` after introducing
new components to verify WCAG AA compliance.
```

Use `Tindre/DESIGN.md` similarly when working on Tindre surfaces.

## Use with Stitch

Generate files natively in Stitch, or import the relevant brand file via
Stitch canvas → Design system → Import DESIGN.md.

## Status

`alpha` — both the DESIGN.md spec and these brand files are evolving.
