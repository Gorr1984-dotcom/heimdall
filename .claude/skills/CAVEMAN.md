# Caveman skills (vendored)

Source: https://github.com/JuliusBrussee/caveman — `skills/`, licensed MIT
(see `LICENSE.caveman`; the engine/proxy/mcp directories of that repo are
BSL-1.1 and are **not** vendored here).

Vendored at upstream commit `542442bab314973709f95b85b1ac0b3f6f5b5dc6`
(2026-09-17).

## What is installed

- `.claude/skills/caveman*`, `cavecrew`, `investigate-first`, `lean-build`,
  `migration`, `safe-refactor`, `surgical-patch`, `verify-and-stop` — the MIT
  skill pack. Works in any Claude Code session opened on this repo, including
  Claude Code on the web (no `/plugin` needed).
- `.claude/settings.json` — registers the upstream marketplace and enables the
  `caveman@caveman` plugin, so a local Claude Code CLI also gets the plugin's
  hooks and slash commands (`/caveman`, `/caveman-init`, `/caveman-review`,
  `/caveman-stats`, `/caveman-commit`).

## Use

Say `caveman mode` or run `/caveman`. Levels: `lite`, `full` (default),
`ultra`, plus the `wenyan-*` variants. Turn off with `/caveman off`,
`stop caveman`, or `normal mode`.

## Update

Re-copy `skills/` from upstream and bump the commit hash above.
