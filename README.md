# NueWave-CSS

A lightweight, semantic CSS framework for [Nue](https://nuejs.org/), built with a modified version Tailwind’s Preflight reset. NueWave is split into modular reset, base, and components layers, imported by a main `nuewave.css` file, for clean styling of Nue templates and islands.

## Features

- **Tailwind’s Preflight Inspired**: Modern CSS normalise/reset for cross-browser consistency.
- **Modular Design**: Separate `reset.css`, `base.css`, and `components.css` files.
- **Theming**: CSS variables for colors, spacing, and typography customization.
- **Components**: Semantic classes like `.nw-button`, `.nw-card`, `.nw-input`, `.nw-grid`.
- **Lightweight**: ~8KB total uncompressed, optimized for Nue’s single-request rendering.
- **No Utilities**: Promotes clean, maintainable markup per Nue’s CSS-first ethos.

## Installation

Install via npm or Bun:

```bash
bun add nuewave-css
```
