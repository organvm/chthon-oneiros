# DISCOVERY — organvm/chthon-oneiros

**Date:** 2026-06-22
**Verdict:** ⭐ VALUE FOUND — promoted to ranked tier (`value-repos.json`)
**Discovered by:** auto-discovery sweep ("no repo stays dark")

---

## Value Thesis

CHTHON-ONEIROS reads, at a glance, like a creative-writing archive: ~340k words of
psychological-horror theory, research, and serialized fiction (Season 1's *Black Book*
omnibus + 8 Season 2 episodes). That framing undersells it. Beneath the prose sits a
genuinely reusable estate asset — **The Director Engine** — a deterministic,
parameter-driven creative-generation capability that has already been proven across two
complete seasons of production. The engine has four parts that already exist in this repo
and only need packaging: (1) a **three-axis dial schema** (`$ARGENTO_GEL` /
`$LYNCH_DRIFT` / `$KON_SPIRAL`, each 0–100) that converts vague aesthetic intent into
concrete generation parameters; (2) a **dial-modulated system prompt**
(`prompts/director_persona.md`) that swaps voice, vocabulary, and narrative logic based on
dial state; (3) a **fixed narrative grammar** — the 4-stage Core Loop
(`bible/core_loop.md`) and the 7 Epistemological Laws (`bible/physics.md`) — that
constrains output to a coherent, repeatable structure; and (4) a working
**post-generation validator** (`tools/giallo_check.py`) plus text-effect tools
(`satiation.py`, `metabolize.sh`). Packaged as a single callable contract, this is exactly
the capability ORGAN II's generative siblings (`example-generative-visual`,
`example-generative-music`, `example-ai-collaboration`, `performance-sdk`) lack: an
opinionated, tested, parameterized content generator *with built-in QA*. The pattern —
"named aesthetic dials → modulated system prompt → structural grammar → automated linter" —
generalizes to any domain (music, visuals, copy), making this repo a reference
implementation for dial-calibrated generation across the estate. **Secondary value:** the
corpus itself is publishable serialized-horror IP with an existing pitch deck
(`docs/pitch/index.html`) and monetization plan (`docs/strategy/`), suitable for a
Substack/web/transmedia ARG release.

This is **not** archival. The capability is live, validated by output, and consumable by
the rest of the estate once extracted.

---

## What This Repo Actually Is

- **Real entrypoints (tools/):** `giallo_check.py` (color-vocabulary linter),
  `satiation.py` (glitch-text generator → museum exhibits), `metabolize.sh` (Unicode
  decay pass), `update_stats.sh` (catalog stats).
- **The latent engine (prompts/ + bible/):** `director_persona.md` is the generator;
  `core_loop.md` + `physics.md` are its grammar and constraints; the dial schema is the
  public interface.
- **Output corpus:** `release/` (Season 1, weeks 01–24), `production/beta/` (Season 2,
  episodes 01–08), `production/alpha/` (calibration fragments), `research/` (34 director
  deep-dives), `museum/` (generated artifacts).
- **CI:** minimal structure/seed/py-compile validation + catalog-existence check. Adding
  this discovery and the engine contract keeps the build green.

## Highest Latent Value (ranked)

1. **The Director Engine** — extractable, reusable generative capability + QA. *(primary)*
2. **Dial-calibration pattern** — a reference architecture for parameterized generation
   that siblings in Organ II can copy. *(estate capability)*
3. **Serialized-horror IP** — finished, publishable content with a pitch deck. *(revenue path)*

## Single Best Concrete First Task

**Extract and package the Director Engine into one versioned, machine-readable contract.**
Create `engine/engine.json` that declares the dial schema (names, ranges, defaults) and a
documented input → output interface, wiring together `prompts/director_persona.md`
(generator), `bible/core_loop.md` + `bible/physics.md` (grammar/constraints), and
`tools/giallo_check.py` (validator) into a single callable module. Deliverable: a sibling
repo can invoke "generate a dial-calibrated fragment, then validate it" deterministically,
without reverse-engineering the convention from scattered Markdown. This converts proven
latent capability into a consumable estate asset.
