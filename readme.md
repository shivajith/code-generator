
# CodeGemma Assistant VS Code Extension

Generate code using Hugging Face models directly from VS Code!

---

## ✨ Features
- AI-powered code generation using Hugging Face models
- Supports any model available for hosted inference (e.g., Salesforce/codegen-16B-multi)
- Secure API key storage via VS Code settings
- Output appears in a new editor tab

---

## 🛠 Setup

1. **Install dependencies**
   ```sh
   npm install
   ```
2. **Build the extension**
   ```sh
   npm run compile
   ```
3. **Open in VS Code**
   - Open this folder in VS Code.
4. **Set your Hugging Face API key**
   - Open VS Code settings (`Ctrl+,`)
   - Search for `codegemma.apiKey` and enter your Hugging Face API key
   - Or add to your `settings.json`:
     ```json
     {
       "codegemma.apiKey": "hf_YourTokenHere"
     }
     ```

---

## � Usage
1. Select code or a prompt in the editor
2. Run the command: `CodeGemma: Generate Code` (via Command Palette or shortcut)
3. The generated code will open in a new tab

---

## ⚙️ Configuration
| Setting             | Type   | Description                        |
|---------------------|--------|------------------------------------|
| codegemma.apiKey    | string | Your Hugging Face API key (required)|

---

## 🧠 Model Support
- You can use any Hugging Face model that supports hosted inference and text generation.
- Example: `Salesforce/codegen-16B-multi`
- If you get a 404 or error, the model may not be available for public inference.

---

## 🧩 Project Structure
```
codegemma-assistant/
├── src/extension.ts      # Main extension logic
├── package.json          # Extension manifest
├── tsconfig.json         # TypeScript config
├── README.md             # This file
└── ...
```

---

## 📄 License
MIT License

---

## 🙋‍♂️ Author
Made with ❤️ by Shivajith. For questions or contributions, open a GitHub Issue.