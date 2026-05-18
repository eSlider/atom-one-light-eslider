# Atom One Light (eSlider)

Light theme for [Visual Studio Code](https://code.visualstudio.com/) and [Cursor](https://cursor.com/), based on **Atom One Light** with eSlider UI accents. Syntax colors were tuned from the IntelliJ scheme `Atom One Light (Material)` (see `source/`).

## Install

### Marketplace (recommended)

1. Open **Extensions** (`Ctrl+Shift+X` / `Cmd+Shift+X`)
2. Search for **Atom One Light (eSlider)**
3. Install and select **Preferences: Color Theme** → **Atom One Light (eSlider)**

Or:

```bash
code --install-extension eSlider.atom-one-light-eslider
cursor --install-extension eSlider.atom-one-light-eslider
```

### VSIX (manual)

Download the latest `.vsix` from [GitHub Releases](https://github.com/eSlider/atom-one-light-eslider/releases), then:

```bash
code --install-extension atom-one-light-eslider-1.0.0.vsix
cursor --install-extension atom-one-light-eslider-1.0.0.vsix
```

## Activate

```json
"workbench.colorTheme": "Atom One Light (eSlider)"
```

## Highlights

| Element | Color |
|--------|--------|
| Background | `#FAFAFA` |
| Foreground | `#383A42` |
| Keywords | `#A626A4` (italic) |
| Types / structs | `#A626A4` |
| Functions | `#4078F2` |
| Variables / consts / fields | `#C18401` |
| Strings | `#50A14F` |
| Accent (tabs, focus) | `#5D70E7` |

## Optional editor settings (Go)

These are **not** part of the theme; add to your user `settings.json` if you want the same behavior:

```json
"gopls": {
  "ui.navigation.importShortcut": "Definition"
},
"[go]": {
  "editor.links": false
}
```

## Publish (maintainers)

1. Create a [Marketplace publisher](https://marketplace.visualstudio.com/manage) named `eSlider` (must match `package.json`).
2. Create an Azure DevOps [PAT](https://dev.azure.com) with **Marketplace → Manage** scope.
3. Add repository secret `VSCE_PAT`, then create a GitHub Release — the workflow publishes to the Marketplace and attaches the VSIX.

```bash
npx @vscode/vsce login eSlider
npx @vscode/vsce publish --no-dependencies
```

## Development

```bash
npm install -g @vscode/vsce
vsce package
```

## License

MIT — syntax palette derived from [akamud/vscode-theme-onelight](https://github.com/akamud/vscode-theme-onelight) and Atom One Light.
