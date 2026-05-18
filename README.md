# LRU Tab Limiter

LRU Tab Limiter is an Obsidian plugin that keeps the number of open Markdown tabs under a configurable limit.

When opening a new Markdown tab would exceed the limit, the plugin closes the least recently used Markdown tab instead of blocking the new tab. Switching to a tab marks it as recently used, so older inactive tabs are replaced first.

This project is based on the original Tab Limiter plugin and was modified in May 2026 to change the limit behavior from rejection to LRU replacement.

## Settings

Use the plugin settings tab to choose the global maximum number of Markdown tabs. The default limit is 5.

Do not enable this plugin together with the original Tab Limiter plugin. They manage the same workspace behavior and will conflict with each other.

## Manual installation

1. Build the plugin with the commands below.
2. Create a folder named `tab-limit-lru` under your vault's `.obsidian/plugins/` directory.
3. Copy `main.js` and `manifest.json` into that folder.
4. Reload Obsidian and enable **LRU Tab Limiter** in community plugins.

## Development

Install dependencies and build the plugin:

```bash
npm ci
npm run build
```

The build outputs `main.js`, which can be installed with `manifest.json` in an Obsidian vault plugin directory.
