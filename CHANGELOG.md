# Changelog

All notable changes to **PixelForge BMP Conversion Suite** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

> Changes that are in development and not yet released will appear here.

---

## [1.0.0] — 2026-11-19

### 🎉 Initial Release

> First stable public release of the PixelForge BMP Conversion Suite by **SPManchester Private Limited**.

### Added

- **7 BMP Conversion Tools** — dedicated, single-purpose converters for every major output format:
  - `BMP → PNG` — lossless conversion with transparency support
  - `BMP → JPG` — lossy conversion with adjustable quality slider
  - `BMP → WebP` — modern format with superior compression
  - `BMP → PDF` — printable single-page PDF export via Canvas API
  - `BMP → SVG` — raster-embedded SVG wrapper output
  - `BMP → ICO` — multi-resolution Windows icon generator (16×16 up to 256×256)
  - `BMP → Base64` — inline data URI encoder for embedding in HTML/CSS

- **Batch Processing** — queue multiple BMP files and convert them all in one operation with live progress tracking

- **Aspect-Ratio-Safe Resizing** — preset scale options (Original, 75%, 50%, 25%) and custom width/height input that preserves the original aspect ratio

- **One-Click ZIP Download** — download all batch-converted outputs as a single `.zip` archive (powered by JSZip, bundled client-side)

- **100% Client-Side Processing** — all conversions happen in the browser using the HTML5 Canvas API and FileReader API; no files are ever uploaded to any server

- **Responsive Mobile-First UI** — fully functional on desktop, tablet, and mobile with a clean, modern interface

- **Main Suite Hub** (`index.html`) — central landing page linking to all 7 conversion tools with descriptions and direct navigation

- **GitHub Pages Deployment** — automated CI/CD workflow (`.github/workflows/pages.yml`) for zero-config static hosting via GitHub Pages

- **MIT License** — open-sourced under the MIT License, Copyright © 2026 SPManchester Private Limited

---

## Links

- [Repository](https://github.com/spmanchester/pixelforge-bmp-suite)
- [GitHub Pages Live Demo](https://spmanchester.github.io/pixelforge-bmp-suite/)
- [Issue Tracker](https://github.com/spmanchester/pixelforge-bmp-suite/issues)
- [SPManchester Private Limited](https://www.spmanchester.com)

---

> _"Keep a Changelog so your contributors — and future you — know what has changed."_
