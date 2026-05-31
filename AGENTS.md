# Repository Guidelines

Global policy: /Users/4jp/AGENTS.md applies and cannot be overridden.

## Project Structure & Module Organization
`chthon-oneiros` is a Markdown-first corpus with light scripting support. Use these top-level directories consistently:
- `bible/`: canonical world laws and narrative constraints.
- `research/`: deep-dive studies and cluster/world synthesis docs.
- `production/alpha/` and `production/beta/`: draft fragments and canonical episode content.
- `release/week_XX/`: published weekly drops.
- `docs/`: catalog, theory, integration, and strategy artifacts (`docs/CATALOG.md` is the index anchor).
- `tools/`: project automation scripts (`update_stats.sh`, `giallo_check.py`, `metabolize.sh`, `satiation.py`).

## Build, Test, and Development Commands
There is no compile/build pipeline; contribution flow is script-based:
- `./tools/update_stats.sh`: recompute Markdown file/word totals and update `docs/CATALOG.md`.
- `python3 ./tools/giallo_check.py path/to/file.md`: lint color vocabulary in changed narrative files.
- `python3 ./tools/satiation.py <seed_word> [count]`: generate museum-style semantic-satiation artifacts.
- `./tools/metabolize.sh`: apply substrate "decay" transformations to `production/beta/` (use intentionally).

## Coding Style & Naming Conventions
- Prefer Markdown for content work; keep headings descriptive and section order logical.
- Follow existing filename patterns: `episode_08_pandemonium.md`, `cluster_14_literary_shadow.md`, `week_24/...`.
- Keep root clean; place new material in the correct domain folder (`docs/theory/`, `research/`, `production/beta/`).
- Python in `tools/` should follow PEP 8 (4-space indentation, clear function names). Shell scripts should be executable with a shebang.

## Testing Guidelines
No formal unit-test suite exists. Minimum validation before PR:
- Run `python3 ./tools/giallo_check.py` on each modified production file.
- Run `./tools/update_stats.sh` after adding/removing/editing Markdown content.
- If you change automation scripts, run the touched script once with a safe sample input and verify no errors.
- Ensure catalog-related paths remain aligned with `.github/workflows/catalog-validator.yml`.

## Commit & Pull Request Guidelines
- Use Conventional Commits seen in history: `feat: ...`, `docs: ...`, `chore: ...`.
- Keep commits scoped to one logical change (research batch, episode update, tooling fix).
- PRs should include: intent summary, key directories touched, and any catalog/script updates performed.
- Link related issues when available; include short before/after excerpts when changing production narrative tone or structure.

## Security & Configuration Tips
- Never commit secrets or private keys; this repo is content-oriented but still public-facing.
- When changing automation behavior, update `.config/ai-agents/seed.yaml` and relevant `tools/` paths together.

<!-- ORGANVM:AUTO:START -->
## Agent Context (auto-generated — do not edit)

This repo participates in the **ORGAN-II (Art)** swarm.

### Active Subscriptions
- *No active event subscriptions*

### Production Responsibilities
- *No production responsibilities*

### External Dependencies
- *No external dependencies*

### Governance Constraints
- Adhere to unidirectional flow: I→II→III
- Never commit secrets or credentials

*Last synced: 2026-05-23T00:26:31Z*
<!-- ORGANVM:AUTO:END -->
