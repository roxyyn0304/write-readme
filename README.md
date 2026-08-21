# 📝 Write README Skill

> 通用 README 写作技能，支持 Claude、GitHub Copilot、DeepSeek Harness 等 AI Agent。

🌐 [English](README_EN.md) | 简体中文

## ✨ 功能特性

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 智能分析 | 自动检测项目类型（Rust/Node/Python/Android/Web） |
| 模板匹配 | 根据项目类型选择最佳 README 结构 |
| 中英双语 | 自动生成 README.md + README_EN.md |
| 好坏对比 | 8 组示例展示最佳实践 |

### 📦 支持的项目类型
| 类型 | 模板 | 适用场景 |
|------|------|----------|
| 应用/工具 | `template-app.md` | CLI 工具、桌面应用、系统托盘 |
| 库/包 | `template-lib.md` | npm/pip/cargo 包 |
| Android 模块 | `template-module.md` | Xposed/LSPosed 模块 |
| Web 应用 | `template-web.md` | 前端项目、Dashboard |

## 🚀 快速开始

### 安装

直接复制下面的命令，粘贴给你的 AI Agent，它会自动帮你安装：

**Claude Code:**
```
请帮我安装 write-readme 技能：
git clone https://github.com/roxyyn0304/dsh-write-readme.git ~/.claude/skills/write-readme
```

**GitHub Copilot:**
```
请帮我安装 write-readme 技能：
git clone https://github.com/roxyyn0304/dsh-write-readme.git .github/skills/write-readme
```

**DeepSeek Harness:**
```
请帮我安装 write-readme 技能：
git clone https://github.com/roxyyn0304/dsh-write-readme.git ~/.dsh/.agent-presets/mimeng/skills/write-readme
```

**其他 Agent：**
```
请帮我安装 write-readme 技能：
git clone https://github.com/roxyyn0304/dsh-write-readme.git 到你的 skills 目录
```

### 使用

安装后，直接对 AI 说：

```
帮我写 README
```

或

```
用 write-readme 技能帮我写这个项目的 README
```

AI 会自动加载这个技能，按照以下流程生成文档：

1. **分析项目** — 读取配置文件，检测技术栈
2. **选择模板** — 根据项目类型匹配最佳结构
3. **生成初稿** — 按模板写 README.md（中文）
4. **质量检查** — 10 项自检清单
5. **交付** — 生成 README.md + README_EN.md

## 📁 文件结构

```
dsh-write-readme/
├── SKILL.md                    # 主技能文件
├── README.md                   # 本文件
├── README_EN.md                # 英文版说明
├── LICENSE                     # MIT 协议
└── reference/
    ├── template-app.md         # 应用/工具模板
    ├── template-lib.md         # 库/包模板
    ├── template-module.md      # Android/模块模板
    ├── template-web.md         # Web 应用模板
    ├── examples.md             # 好坏示例对比
    └── prompt-template.md      # Prompt 模板集
```

## 📖 模板示例

### 应用/工具模板

```markdown
# 项目名称

> 一句话描述：做什么 + 给谁用 + 解决什么问题

🌐 English | 简体中文

## 📖 简介
...

## ✨ 功能特性
### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| ... | ... |

## 🚀 快速开始
### 方式一：下载安装（推荐）
### 方式二：源码编译
...
```

### 库/包模板

```markdown
# 包名称

> 一句话描述

## 📦 安装
\```bash
npm install package-name
\```

## 🚀 快速开始
\```javascript
import { something } from 'package-name'
\```

## 📖 API 参考
...
```

## 🔧 自定义

### 添加新模板

1. 在 `reference/` 目录创建 `template-xxx.md`
2. 在 `SKILL.md` 的 Phase 2 表格中添加对应行
3. 按照现有模板格式编写

### 修改写作规则

编辑 `SKILL.md` 中的 Writing rules 表格，添加或修改 Do/Don't 规则。

## 📝 Prompt 模板

### 基础版（填空式）

```
请为我的项目写 README.md + README_EN.md：

项目名称：
项目简介：
技术栈：
Fork 来源：
核心功能：
安装方式：
环境要求：
目标用户：
```

### 详细版

```
请为以下项目生成专业的 README 文档：

【项目信息】
- 名称：[项目名]
- 类型：[CLI工具/库/Android模块/Web应用/其他]
- 语言：[Rust/TypeScript/Python/Java/Kotlin/其他]
...

【核心功能】
1. [功能1]：[简要说明]
...
```

更多模板见 `reference/prompt-template.md`。

## ✅ 质量清单

写完 README 后自动检查：

- [ ] 一句话描述清晰具体
- [ ] 语言切换链接正确
- [ ] 功能按类别分组，用表格展示
- [ ] 快速开始能「复制粘贴就能跑」
- [ ] 所有命令在代码块内
- [ ] 配置/API 用表格
- [ ] Fork 项目注明来源
- [ ] GUI 项目有截图
- [ ] License 与 LICENSE 文件一致
- [ ] 无占位符、TODO、空白章节

## 🤝 Contributing

欢迎贡献！请提交 Issue 或 Pull Request。

## 📄 License

[MIT](LICENSE)

## 🔗 相关资源

- [Agent Skills 规范](https://agentskills.io) — Agent Skills 标准
- [Claude Skills 文档](https://code.claude.com/docs/en/skills) — Claude 官方文档
- [GitHub Copilot Skills](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) — GitHub 官方文档

---

Made with ❤️ by [米萌 (MiMeng)](https://github.com/roxyyn0304)
