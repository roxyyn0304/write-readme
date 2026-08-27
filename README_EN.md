# 📝 Write README Skill

> Universal README writing skill for AI Agents like Claude, GitHub Copilot, DeepSeek Harness.

🌐 English | [简体中文](README.md)

## ✨ Features

| Feature | Description |
|---------|-------------|
| Smart Analysis | Auto-detect project type (Rust/Node/Python/Android/Web/C++/Java/C#) |
| Template Matching | Select best README structure based on project type |
| Bilingual | Generate both README.md (Chinese) and README_EN.md (English) |
| Quality Scoring | Auto-evaluate README quality (max 40 points) |
| Auto Check | Comprehensive structure, content, and format checks |

**Supported Project Types:** Applications · Libraries · Android Modules · Web Apps · CLI Tools · API Services · Desktop Apps

## 🚀 Installation

Copy the command below and paste it to your AI Agent:

```
Please install write-readme skill: git clone https://github.com/roxyyn0304/dsh-write-readme.git to your skills directory
```

## 📖 Usage

After installation, simply say:

```
Write README for my project
```

or

```
Improve my README
```

## 📁 File Structure

```
├── SKILL.md              # Main skill file
├── reference/
│   ├── template-app.md   # Application/Tool template
│   ├── template-lib.md   # Library/Package template
│   ├── template-module.md # Android module template
│   ├── template-web.md   # Web application template
│   ├── template-cli.md   # CLI tool template (new)
│   ├── template-desktop.md # Desktop application template (new)
│   ├── template-api.md   # API service template (new)
│   ├── examples.md       # Good vs Bad examples
│   ├── prompt-template.md # Prompt templates
│   └── checklist.md      # Quality checklist (new)
```

## 🔧 Customization

- **Add Templates:** Create `template-xxx.md` in `reference/` and register in `SKILL.md` Phase 2 table
- **Modify Rules:** Edit Writing rules table in `SKILL.md`
- **Custom Checks:** Edit checklist items in `reference/checklist.md`

## ✅ Quality Scoring System

### Scoring Criteria (Max 40 points)
1. **Structure Completeness** (10 points)
2. **Content Quality** (10 points)
3. **Format Standards** (10 points)
4. **User Experience** (10 points)

### Score Results
- **40 points:** Excellent, no changes needed
- **30-39 points:** Good, optional optimization
- **20-29 points:** Average, recommended optimization
- **<20 points:** Poor, needs rewrite

## 📋 Automated Checks

Use `reference/checklist.md` for automated checks:

```bash
# Check README quality
# Structure: File existence, language switching, section completeness
# Content: One-line description, feature display, quick start
# Format: Heading format, code blocks, tables
# Links: External links, internal links
```

## 📄 License

[MIT](LICENSE)

---

Made with ❤️ by [MiMeng](https://github.com/roxyyn0304)