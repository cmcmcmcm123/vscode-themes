# mono-okay

A dark VS Code / Cursor color theme based on Monokai Pro (Filter Machine) colors.

## Install

- **From repo:** Open this folder in VS Code/Cursor, press **F5** to run the extension in a new window, then choose **mono-okay** from the Color Theme picker (`Cmd+K Cmd+T`).
- **From VSIX:** Run `vsce package` in this folder, then **Extensions** → **Install from VSIX...** and select the `.vsix` file.

## Project structure

```
vscode-themes/
├── package.json
├── themes/
│   └── mono-okay-color-theme.json
├── README.md
└── THEME_NEXT_STEPS.md
```

To add more themes later, add another JSON file under `themes/` and another entry in `contributes.themes` in `package.json`.
