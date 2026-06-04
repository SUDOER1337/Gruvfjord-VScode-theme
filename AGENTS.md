# Gruvfjord VS Code Theme — Agent Guide

## Repo structure

- Single-theme VS Code extension. No JS/TS, no tests, no build pipeline.
- Theme definition: `themes/color-theme.json`
- Entrypoint: `package.json` → `contributes.themes[0].path`

## Dev commands

- **Package VSIX:** `vsce package` (uses `.vscodeignore`)
- **Install VSIX (Code):** `code --install-extension gruvfjord-*.vsix`
- **Install VSIX (VSCodium):** `codium --install-extension gruvfjord-*.vsix`
- **Debug:** Open in VS Code, press F5 (uses `.vscode/launch.json`)

## Key facts

- VSIX-only distribution; **not** on the VS Code Marketplace.
- `.vscodeignore` strips `.vscode/**`, `.gitignore`, and `vsc-extension-quickstart.md` from the packaged extension.
- Theme is `"uiTheme": "vs-dark"` — dark theme only.
- The single source of truth for all colors is `themes/color-theme.json`. No generated or compiled theme files.
