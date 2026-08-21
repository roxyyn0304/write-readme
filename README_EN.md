# 📝 Write README Skill

> A universal README writing skill for Claude, GitHub Copilot, DeepSeek Harness, and other AI Agents.

🌐 English | [简体中文](README.md)

## ✨ Features

| Feature | Description |
|---------|-------------|
| Smart Analysis | Auto-detect project type (Rust/Node/Python/Android/Web) |
| Template Matching | Select best README structure based on project type |
| Bilingual | Generate README.md + README_EN.md automatically |
| Good vs Bad Examples | 8 comparison examples showing best practices |

**Supported types:** Application/Tool · Library/Package · Android Module · Web App

## 🚀 Installation

Copy the command below and paste it to your AI Agent:

```
Please install write-readme skill:
git clone https://github.com/roxyyn0304/dsh-write-readme.git to your skills directory
```

| Agent | Install Path |
|-------|--------------|
| Claude Code | `~/.claude/skills/write-readme` |
| GitHub Copilot | `.github/skills/write-readme` |
| DeepSeek Harness | `~/.dsh/.agent-presets/<preset>/skills/write-readme` |

## 📖 Usage

After installation, simply say:

```
Help me write a README
```

## 📁 File Structure

```
├── SKILL.md              # Main skill file
├── reference/
│   ├── template-app.md   # Application/Tool template
│   ├── template-lib.md   # Library/Package template
│   ├── template-module.md # Android Module template
│   ├── template-web.md   # Web Application template
│   ├── examples.md       # Good vs Bad examples
│   └── prompt-template.md # Prompt template collection
```

## 🔧 Customization

- **Add templates:** Create `template-xxx.md` in `reference/`, register in SKILL.md Phase 2
- **Modify rules:** Edit the Writing rules table in SKILL.md

## ✅ Quality Checklist

- [ ] One-line description is clear and specific
- [ ] Features grouped by category in tables
- [ ] Quick start can be "copy-pasted and run"
- [ ] Fork projects credit the original
- [ ] No placeholder text or TODOs

## 📄 License

[MIT](LICENSE)

---

Made with ❤️ by [MiMeng](https://github.com/roxyyn0304)
