// File: package.json
{ ... }

// File: tsconfig.json
{ ... }

// File: .vscode/launch.json
{ ... }

// File: src/extension.ts
/**
 * @file extension.ts
 * @description VS Code extension entry point for CodeGemma Assistant.
 */

import * as vscode from 'vscode';
import axios from 'axios';

export function activate(context: vscode.ExtensionContext) {
  ...
}

export function deactivate() {}

// File: .vscodeignore
node_modules
.vscode
out
dist/**/*.map

// File: README.md
# CodeGemma Assistant VS Code Extension

Run Google’s CodeGemma model hosted on Hugging Face directly in your editor.

## 💡 What is This?
This is a [VS Code Extension](https://code.visualstudio.com/api/get-started/your-first-extension) that allows you to use the **CodeGemma** language model from Hugging Face to interact with and generate code directly inside VS Code.

---

## 🧱 Project Structure & Workflow

```
codegemma-assistant/
├── src/              # TypeScript source code
│   └── extension.ts  # Extension's main logic
├── dist/             # Compiled JavaScript output (auto-generated)
├── .vscode/          # VS Code debug configs
├── package.json      # Project config, dependencies, commands
├── tsconfig.json     # TypeScript compiler settings
├── README.md         # This documentation
└── .vscodeignore     # Files to ignore when packaging
```

---

## 🔄 How It Works

1. **You write code in TypeScript** (`.ts` files) under the `src/` folder.
2. You compile it to **JavaScript** using the TypeScript compiler (`tsc`).
3. The compiled output goes into `dist/`.
4. VS Code runs `dist/extension.js` when the extension is launched.

---

## 🧰 Requirements
- [Node.js](https://nodejs.org) (includes `npm`) ✅
- [VS Code](https://code.visualstudio.com/) (v1.70 or later)
- [Hugging Face API Key](https://huggingface.co/settings/tokens)

---

## ⚙️ Setup Instructions

### 1. Install Node.js and npm
- Download and install from: https://nodejs.org (LTS version)

### 2. Install dependencies
```bash
npm install

 It reads the package.json file in your project folder and installs all dependencies listed under:

  "dependencies" (for production)

  "devDependencies" (for development)

These get installed into a node_modules/ folder.

 Files Affected
 node_modules/: where packages are installed.

 package-lock.json: created or updated to lock the exact version of installed packages.

 package.json: updated if you install a package manually.

```

### 3. Set Hugging Face API key
- In VS Code: `File → Preferences → Settings → Extensions → CodeGemma Assistant`
- Set `codegemma.apiKey` with your Hugging Face token

### 4. Compile TypeScript to JavaScript
```bash
npm run compile
```
- Compiles `src/extension.ts` → `dist/extension.js`

### 5. Run the Extension
- Press `F5` (runs via `.vscode/launch.json`)
- A new VS Code window will open (Extension Development Host)
- Open a file, **select some code**, and run `Run CodeGemma` from the Command Palette

---

## 📦 Package the Extension
```bash
npm install -g vsce
vsce package
```
This creates a `.vsix` file for distribution.

---

## ❓Common Errors
| Error | Fix |
|-------|-----|
| `npm: not recognized` | Install Node.js and restart terminal |
| `Execution policy error` | Use Command Prompt or allow scripts in PowerShell |
| `No active editor` | Open a code file before running the command |
| `API key missing` | Set `codegemma.apiKey` in settings |

---

## 🧠 Summary
- TypeScript → JavaScript with `tsc`
- VS Code runs `dist/extension.js`
- You interact with CodeGemma by selecting code and running a command

## License
MIT