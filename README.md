# 📝 Write README Skill

> 通用 README 写作技能，支持 Claude、GitHub Copilot、DeepSeek Harness 等 AI Agent。

🌐 [English](README_EN.md) | 简体中文

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 智能分析 | 自动检测项目类型（Rust/Node/Python/Android/Web） |
| 模板匹配 | 根据项目类型选择最佳 README 结构 |
| 中英双语 | 自动生成 README.md + README_EN.md |
| 好坏对比 | 8 组示例展示最佳实践 |

**支持的项目类型：** 应用工具 · 库包 · Android 模块 · Web 应用

## 🚀 安装

复制下面的命令，粘贴给你的 AI Agent 即可自动安装：

```
请帮我安装 write-readme 技能：
git clone https://github.com/roxyyn0304/dsh-write-readme.git 到你的 skills 目录
```

| Agent | 安装路径 |
|-------|----------|
| Claude Code | `~/.claude/skills/write-readme` |
| GitHub Copilot | `.github/skills/write-readme` |
| DeepSeek Harness | `~/.dsh/.agent-presets/<preset>/skills/write-readme` |

## 📖 使用

安装后直接说：

```
帮我写 README
```

## 📁 文件结构

```
├── SKILL.md              # 主技能文件
├── reference/
│   ├── template-app.md   # 应用/工具模板
│   ├── template-lib.md   # 库/包模板
│   ├── template-module.md # Android 模块模板
│   ├── template-web.md   # Web 应用模板
│   ├── examples.md       # 好坏示例对比
│   └── prompt-template.md # Prompt 模板集
```

## 🔧 自定义

- **添加模板：** 在 `reference/` 创建 `template-xxx.md`，并在 `SKILL.md` Phase 2 表格中注册
- **修改规则：** 编辑 `SKILL.md` 中的 Writing rules 表格

## ✅ 质量清单

- [ ] 一句话描述清晰具体
- [ ] 功能按类别分组，用表格展示
- [ ] 快速开始能「复制粘贴就能跑」
- [ ] Fork 项目注明来源
- [ ] 无占位符、TODO

## 📄 License

[MIT](LICENSE)

---

Made with ❤️ by [米萌 (MiMeng)](https://github.com/roxyyn0304)
