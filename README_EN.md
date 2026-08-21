# 📝 Write README Skill

> A universal README writing skill for Claude, GitHub Copilot, DeepSeek Harness, and other AI Agents.

🌐 English | [简体中文](README.md)

## ✨ Features

### 🎯 Core Features
| Feature | Description |
|---------|-------------|
| Smart Analysis | Auto-detect project type (Rust/Node/Python/Android/Web) |
| Template Matching | Select best README structure based on project type |
| Bilingual | Generate README.md + README_EN.md automatically |
| Good vs Bad Examples | 8 comparison examples showing best practices |

### 📦 Supported Project Types
| Type | Template | Use Case |
|------|----------|----------|
| Application/Tool | `template-app.md` | CLI tools, desktop apps, system tray |
| Library/Package | `template-lib.md` | npm/pip/cargo packages |
| Android Module | `template-module.md` | Xposed/LSPosed modules |
| Web Application | `template-web.md` | Frontend projects, dashboards |

## 🚀 Quick Start

### Installation

Copy the command below and paste it to your AI Agent, it will install automatically:

**Claude Code:**
```
Please install write-readme skill:
git clone https://github.com/roxyyn0304/dsh-write-readme.git ~/.claude/skills/write-readme
```

**GitHub Copilot:**
```
Please install write-readme skill:
git clone https://github.com/roxyyn0304/dsh-write-readme.git .github/skills/write-readme
```

**DeepSeek Harness:**
```
Please install write-readme skill:
git clone https://github.com/roxyyn0304/dsh-write-readme.git ~/.dsh/.agent-presets/mimeng/skills/write-readme
```

**Other Agents:**
```
Please install write-readme skill:
git clone https://github.com/roxyyn0304/dsh-write-readme.git to your skills directory
```

### Usage

After installation, simply say to your AI:

```
Help me write a README
```

or

```
Use the write-readme skill to write this project's README
```

AI will automatically load this skill and follow this workflow:

1. **Analyze Project** — Read config files, detect tech stack
2. **Select Template** — Match best structure based on project type
3. **Generate Draft** — Write README.md (Chinese) following template
4. **Quality Check** — 10-item checklist verification
5. **Deliver** — Generate README.md + README_EN.md

## 📁 File Structure

```
dsh-write-readme/
├── SKILL.md                    # Main skill file
├── README.md                   # This file (Chinese)
├── README_EN.md                # This file (English)
├── LICENSE                     # MIT License
└── reference/
    ├── template-app.md         # Application/Tool template
    ├── template-lib.md         # Library/Package template
    ├── template-module.md      # Android/Module template
    ├── template-web.md         # Web Application template
    ├── examples.md             # Good vs Bad examples
    └── prompt-template.md      # Prompt template collection
```

## 📖 Template Examples

### Application/Tool Template

```markdown
# Project Name

> One-line description: what it does + who it's for + problem it solves

🌐 English | 简体中文

## 📖 Introduction
...

## ✨ Features
### 🎯 Core Features
| Feature | Description |
|---------|-------------|
| ... | ... |

## 🚀 Quick Start
### Option 1: Download (Recommended)
### Option 2: Build from Source
...
```

### Library/Package Template

```markdown
# Package Name

> One-line description

## 📦 Installation
\```bash
npm install package-name
\```

## 🚀 Quick Start
\```javascript
import { something } from 'package-name'
\```

## 📖 API Reference
...
```

## 🔧 Customization

### Adding New Templates

1. Create `template-xxx.md` in `reference/` directory
2. Add corresponding row in Phase 2 table of `SKILL.md`
3. Follow existing template format

### Modifying Writing Rules

Edit the Writing rules table in `SKILL.md` to add or modify Do/Don't rules.

## 📝 Prompt Templates

### Basic (Fill-in-the-blank)

```
Please write README.md + README_EN.md for my project:

Project Name:
Description:
Tech Stack:
Fork Origin:
Core Features:
Installation Method:
Requirements:
Target Audience:
```

### Detailed

```
Please generate professional README documentation for the following project:

[Project Info]
- Name: [project name]
- Type: [CLI tool/Library/Android Module/Web App/Other]
- Language: [Rust/TypeScript/Python/Java/Kotlin/Other]
...

[Core Features]
1. [Feature 1]: [brief description]
...
```

More templates in `reference/prompt-template.md`.

## ✅ Quality Checklist

Auto-check after writing README:

- [ ] One-line description is clear and specific
- [ ] Language toggle links work correctly
- [ ] Features grouped by category, displayed in tables
- [ ] Quick start can be "copy-pasted and run"
- [ ] All commands in code blocks
- [ ] Config/API items use tables
- [ ] Fork projects credit the original
- [ ] GUI projects include screenshots
- [ ] License matches LICENSE file
- [ ] No placeholder text, TODOs, or empty sections

## 🤝 Contributing

Contributions welcome! Please submit Issues or Pull Requests.

## 📄 License

[MIT](LICENSE)

## 🔗 Related Resources

- [Agent Skills Specification](https://agentskills.io) — Agent Skills standard
- [Claude Skills Documentation](https://code.claude.com/docs/en/skills) — Claude official docs
- [GitHub Copilot Skills](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) — GitHub official docs

---

Made with ❤️ by [MiMeng](https://github.com/roxyyn0304)
