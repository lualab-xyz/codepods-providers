# Decisions

- **Provider folder structure:** one folder per provider under `providers/`, containing `manifest.yml` plus light/dark SVGs.
- **English only:** all manifest `description` text is written in English.
- **Free-tier transparency:** every description states whether the provider has a free tier, promo/initial credits, or is strictly pay-per-use.
- **Icons:** lightweight placeholder SVGs (rounded square with the provider wordmark) are provided so the manifest icon fields always resolve. Brand-accurate icons can be swapped later.
- **Git:** the environment's git proxy shim is non-functional; work is performed directly on files and git operations are skipped until the proxy is available.
