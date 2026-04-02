# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML project — a single-page website displaying the last 10 results of the Brazilian national soccer team (Seleção Brasileira).

## Running the Project

Open the file directly in the default browser:

```bash
start selecao_brasileira.html
```

## Architecture

The entire project is a single self-contained file: `selecao_brasileira.html`

- **Layout**: CSS Grid cards, one per match, ordered most-recent-first.
- **Flag images**: Loaded at runtime from `https://flagcdn.com/w40/{country-code}.png` — requires internet access.
- **Styling**: All CSS is inline in a `<style>` block within the file. Color scheme uses dark blue tones (`#0a2a4a` background) with yellow (`#FFDF00`) accents.
- **Result coloring**: Each `.game-card` receives a class (`win`, `draw`, or `loss`) that controls the left border color and the `.result-badge` appearance.
- **Stats bar**: Hardcoded aggregate totals (wins/draws/losses/GF/GA) in the `.stats-bar` section — must be updated manually when match data changes.
