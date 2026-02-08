# mono-okay Theme — Next Steps

A custom VSCode/Cursor color theme based on Monokai Pro (Filter Machine) colors.

---

## 1. Project Structure

Your theme extension folder should look like:

```
vscode-themes/
├── package.json
├── themes/
│   └── mono-okay-color-theme.json
├── README.md
└── THEME_NEXT_STEPS.md  (this file)
```

---

## 2. Add Your Theme JSON

1. Create the `themes/` folder if it doesn't exist
2. Create `themes/mono-okay-color-theme.json` (or another name for additional themes)
3. Paste your full theme JSON (with the Monokai Pro Filter Machine colors) into that file

---

## 3. Configure package.json

Open `package.json` and ensure the `contributes.themes` section looks like this:

```json
"contributes": {
  "themes": [
    {
      "label": "mono-okay",
      "uiTheme": "vs-dark",
      "path": "./themes/mono-okay-color-theme.json"
    }
  ]
}
```

- **label**: Name that appears in the Color Theme picker
- **uiTheme**: `"vs-dark"` for dark theme, `"vs"` for light
- **path**: Path to your theme JSON file

To add more themes, add more objects to the `themes` array.

---

## 4. Test the Theme

1. Open your theme project folder in Cursor/VSCode
2. Press **F5** (or Run → Start Debugging)
3. A new "Extension Development Host" window opens
4. In that window: **File → Preferences → Color Theme** (or `Cmd+K Cmd+T` on Mac)
5. Select **mono-okay** from the list
6. Make edits to your theme JSON, save, then press **Ctrl+Shift+F5** (or Run → Restart Extension Host) to see changes

---

## 5. Install for Personal Use (Optional)

To install the theme so it's always available:

1. Install `vsce`: `npm install -g @vscode/vsce`
2. From your theme folder: `vsce package`
3. This creates a `.vsix` file
4. In Cursor: **Extensions** panel → `...` menu → **Install from VSIX...** → select the `.vsix` file

---

## 6. Publish to GitHub (Optional)

```bash
cd your-theme-folder
git init
git add .
git commit -m "Initial mono-okay theme"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/vscode-themes.git
git push -u origin main
```

Then add a README with:
- Theme description
- Screenshot
- Installation instructions (clone repo + install from VSIX, or link to VSIX release)

---

## 7. Publish to VSCode Marketplace (Optional)

1. Create a [Personal Access Token](https://dev.azure.com) (Azure DevOps)
2. Run `vsce login YOUR_PUBLISHER_NAME`
3. Run `vsce publish` to publish the extension

---

## Quick Reference: Key Colors Used

| Element | Hex |
|---------|-----|
| Editor background | `#273136` |
| Editor foreground | `#f2fffc` |
| Comments | `#6b7678` |
| Keywords | `#ff6d7e` |
| Strings | `#ffed72` |
| Functions | `#a2e57b` |
| Types/Classes | `#7cd5f1` |
| Numbers/Constants | `#baa0f8` / `#ffb270` |
| Punctuation | `#8b9798` |
