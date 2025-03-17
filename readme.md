# Sea Otter Localization 🌍

Help us make Sea Otter accessible to everyone! This guide will help you translate and maintain localization files.

## 📥 Getting Started

### 1. Install Tools
- [GitHub Desktop](https://desktop.github.com/) (simplifies Git operations)
- [Visual Studio Code](https://code.visualstudio.com/) (text editor with JSON support)
- *recommended* [Git](https://git-scm.com/download/) (integrates with VS Code)

### 2. Fork & Clone
1. **Fork the repository**  
   Click "Fork" at top-right of [GitHub repository page](https://github.com/sbowoskskk/SeaOtter-Localization)

2. **Clone your fork**  
   In GitHub Desktop:  
   File > Clone Repository > **Your Account** > SeaOtter-Localization  
   Choose a local folder

## 🛠 Contribution Model

We use **fork & pull** workflow:
1. Make changes in **your fork**
2. Push to **your fork's** main branch
3. Create Pull Request (PR) to main repository
4. We'll review and merge your changes

## 📝 Translating Workflow

### 1. Keep in Sync
- Click "Fetch origin" in GitHub Desktop every time before contributing
- If we request changes, pull updates before working

### 2. Edit Files
- Open `[lang_CODE].json` in VSCode  
- **Only modify values** (right side):
```json
"welcome": "Translate this text",
"bienvenue": "❌ the key must stay untouched" 
```

### 3. Submit Changes
1. In GitHub Desktop:  
   - Write clear summary ("Added Italian server messages")  
   - Click "Commit to main"

2. Push to **your fork**:  
   Click "Push origin" 

3. [Create Pull Request](https://docs.github.com/articles/creating-a-pull-request)

## ⚠️ Golden Rules

### Variable Handling
Variables like `{server}` or `{channel}` must:
- Stay **untouched** (don't translate/modify/delete)
- Keep original spacing, inside and outside of the brackets

✅ **Good** (English):  
```json
"nf" : "No {filter}players found",
```

❌ **Bad** (English):  
```json
"nf" : "No {filter} players found",  # Changed variable space
```
❌ **Bad** (English):  
```json
"nf" : "No {filter }players found",  # Changed variable space
```

❌ **Bad** (English):  
```json
"nf" : "No {filteur}players found",  # Changed variable name
```
❌ **Bad** (English):  
```json
"nf" : "No {filter}players found in {server}",  # Added an undefined variable
```

### Special Formatting
| Case          | Example                  | Solution               |
|---------------|--------------------------|------------------------|
| New lines     | `Line1\nLine2`           | Keep `\n` exactly      |
| Real {braces} | Show `{` in text         | Use double braces `{{` |
| JSON symbols  | Quotes `"` in translation| Escape with backslash `\"` |
| Comments      | Temporary notes          | ❌ JSON is data-only. comments can't be added. |

## 💬 Need Help?

Chat with the team in [Sea Otter Support](https://is.gd/SeaOtterSupport)

---

**Thank you for making Sea Otter accessible!** 🦦💚  

*(Last updated: 2025-03-17)*
