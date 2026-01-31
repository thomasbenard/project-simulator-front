# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A browser-based Monte Carlo project simulator that estimates actual project duration based on probability distributions. Single-page application with no build process.

## Development

**Run locally:** Open `index.html` directly in a browser.

**Deployment:** Automatically deploys to GitHub Pages on push to master via `.github/workflows/deploy.yml`.

**Live site:** https://thomasbenard.github.io/project-simulator-front/

## Architecture

Single `index.html` file containing:
- **HTML**: Input controls, results display, two chart canvases
- **CSS**: Inline styles in `<style>` block
- **JavaScript**: Inline in `<script>` block

### Key Components

1. **Distribution Editor**: Two-way synchronized editable table and interactive bar chart (uses chartjs-plugin-dragdata for drag-to-edit)
2. **ProjectSimulator class**: Core Monte Carlo simulation engine with weighted random selection
3. **Results visualization**: Histogram chart showing distribution of simulation outcomes

### External Dependencies (CDN)
- Chart.js
- chartjs-plugin-dragdata

### Simulation Parameters
- Number of tasks
- Number of simulation runs
- Rejection rate (% chance task needs rework)
- Probability distribution (preset or custom)
