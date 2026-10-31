# blainekyle.github.io (`▲▼▲▼▲▼`)

[![Live Site](https://img.shields.io/badge/Live-blainekyle.github.io-050507?style=flat-square&logo=github)](https://blainekyle.github.io/)

Personal interactive homepage and live-synced featured project dock for **[@blainekyle](https://github.com/blainekyle)**.

Visit live: **[blainekyle.github.io](https://blainekyle.github.io/)**

---

## Architecture

- **Interactive Bioluminescent Canvas**: High-DPI HTML5 `<canvas>` particle field with pointer trail interpolation, click/touch radial bursts, and idle geometric constellation formation (`triangle`, `square`, `circle`, `cross`, `star`) that spins and disintegrates on wake.
- **Live-Synced Featured Project Dock**:
  - Automatically populates the floating obsidian dock in exact profile pin order from **[github.com/blainekyle](https://github.com/blainekyle)** on page load.
  - **Stale-While-Revalidate (`localStorage`)** renders immediately at frame zero without layout shift while refreshing pinned selections and official GitHub REST API metadata (`has_pages`, `homepage`, `description`) in parallel.
  - **Multi-Tier Resilience**: Queries a real-time CORS JSON pinned-repos endpoint first, falls back to direct `DOMParser` extraction of `github.com/blainekyle`, and maintains a self-hosted [`assets/pinned.json`](assets/pinned.json) snapshot automatically updated by [`.github/workflows/sync-pinned.yml`](.github/workflows/sync-pinned.yml).
  - **Zero-Config Future Repo Support**: Preserves handcrafted vector glyphs and accent palettes for known repositories while automatically routing (`LIVE` GitHub Pages URL vs. `APP` repository URL), summarizing captions, and discovering/generating vector icons for any newly pinned repository.
