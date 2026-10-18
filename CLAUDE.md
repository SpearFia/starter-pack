# starter-pack

Free, license-clean starter transitions, SFX, music and presets for Spear Fia, with descriptors.

## Layout

- `transitions/`, `sfx/`, `music/`, `templates/`: one folder per asset with the file,
  `<id>.asset.json` and a preview.
- `presets/`: vision presets (`vision` schema).
- `LICENSES.md`: per-asset license table. Every asset needs a row.

## Commands

```powershell
# with spearfia-spec next to this repo
node ..\spearfia-spec\scripts\check.mjs vision presets\cinematic.yaml presets\chaotic-gaming-comedy.yaml presets\motorsport-news-react.yaml
```

Only add assets that are free and license-clean, with the license and source recorded.

## Naming

| Context | Form |
| --- | --- |
| Prose, UI, README titles | Spear Fia |
| GitHub org, URLs, crates, packages, IDs | `spearfia` |
| Rust crates | `spearfia-<name>` |
| npm packages | `@spearfia/<name>` |
| Asset and plugin IDs | `spearfia/<asset>@<semver>`, e.g. `spearfia/focus-loupe@0.1.0` |
| Schema IDs | `https://spearfia.dev/schemas/<name>/v1.json` |

Never write the second word of the name in all capitals.

## Rules

- Never commit media. Media lives on the external drive, not under `C:\dev`.
- The schemas in `spearfia/spearfia-spec` are the source of truth for every format.
  Change the schema there first, then the code or data that uses it.
- `main` is protected: work on `feat/`, `fix/` or `exp/` branches and open a PR.
- New files are dual licensed MIT OR Apache-2.0.
