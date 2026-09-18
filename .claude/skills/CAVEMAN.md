# Caveman (vendored)

Source: https://github.com/JuliusBrussee/caveman — `skills/caveman`, licensed MIT
(see `LICENSE.caveman`; the engine/proxy/mcp directories of that repo are
BSL-1.1 and are **not** vendored here).

Vendored at upstream commit `542442bab314973709f95b85b1ac0b3f6f5b5dc6`
(2026-09-17).

## What is installed

Only `.claude/skills/caveman/` — the compression mode itself. It works in any
Claude Code session opened on this repo, including Claude Code on the web, where
`/plugin` does not exist.

The upstream pack ships 20 skills; the other 19 were deliberately left out:

- 9 (`caveman-setup`, `-discover`, `-learn`, `-manage`, `-optimize`,
  `-evidence-review`, `-stats`, `-compress`, `-commit`) target Caveman Cloud, the
  author's hosted gateway. Without an account there they are dead text.
- 6 (`investigate-first`, `lean-build`, `migration`, `safe-refactor`,
  `surgical-patch`, `verify-and-stop`) are generic workflow prose.
- the rest (`cavecrew`, `caveman-explore`, `caveman-review`, `caveman-help`)
  duplicate built-in agents and commands.

Each skill's name and description is injected into every session's index, so the
full pack cost ~1.100 tokens per session before any work started. Keeping one
skill cuts that to ~70.

The `caveman@caveman` plugin is **not** enabled in `.claude/settings.json`: it
would load this same skill a second time and add two hooks that run on every
session start. The marketplace stays registered, so `/plugin install
caveman@caveman` is one command away if the hooks and slash commands are ever
wanted.

## Use

Say `caveman mode` or `/caveman`. Levels: `lite`, `full` (default), `ultra`, plus
the `wenyan-*` variants. Turn off with `/caveman off`, `stop caveman` or
`normal mode`.

## Update

Re-copy `skills/caveman` from upstream and bump the commit hash above.
