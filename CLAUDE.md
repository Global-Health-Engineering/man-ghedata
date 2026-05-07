# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Collaborative Quarto manuscript that consumes data from the companion R package `ghedata` (loaded via `library(ghedata)` in `manuscript.qmd`). The single source document is `manuscript.qmd`; supporting prose lives in `docs/` (e.g. `docs/pitch.qmd`).

The `ghedata` package is listed in `renv.lock` with `"Source": "unknown"` — it is not on CRAN and must already be installed in the local R library for `renv::restore()` and rendering to succeed. If `library(ghedata)` fails, ask the user where the package source lives rather than guessing.

## Commands

```r
renv::restore()    # install pinned package versions from renv.lock
renv::snapshot()   # update renv.lock after adding a new package — commit the change
```

```bash
quarto render manuscript.qmd     # render the manuscript to HTML
quarto preview manuscript.qmd    # live preview while editing
```

## Workflow conventions (from CONTRIBUTING.md)

- Branching: work happens on `dev`; PRs target `main`. Only the maintainer (@bonschorno) merges to `main`.
- Commits should reference the issue they address, e.g. `Address #12: Brief description`. PR descriptions use `Closes #<issue>`.
- AI vs human attribution is tracked via commit author: Claude Code commits (with the auto-attribution footer) mark AI-generated/substantially-modified content; standard commits mark human edits. Preserve this split — do not roll human revisions into a Claude-attributed commit, or vice versa.
- Render locally before opening a PR.
