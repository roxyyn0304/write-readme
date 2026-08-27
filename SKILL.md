---
name: write-readme
description: Use when the user wants to write, rewrite, or improve a README.md for a project. Covers analyzing existing code, summarizing features, structuring documentation, generating bilingual content, and following best practices for open-source project documentation.
---

# Write README

When the user asks to write a README, follow this workflow: **Analyze → Classify → Draft → Polish → Deliver**.

## Phase 1: Analyze (gather facts)

1. **Detect project type** by reading config files:

   | Config file | Project type |
   |-------------|--------------|
   | `package.json` | Node.js / Web |
   | `Cargo.toml` | Rust |
   | `build.gradle*` / `AndroidManifest.xml` | Android |
   | `go.mod` | Go |
   | `pyproject.toml` / `setup.py` | Python |
   | `pubspec.yaml` | Flutter/Dart |
   | `CMakeLists.txt` | C/C++ |
   | `pom.xml` | Java |
   | `*.csproj` | C# |

2. **Read existing README** (if any) — understand what's documented, what's missing.

3. **Extract key facts**:
   ```
   □ Project name
   □ One-line description (what + who + why)
   □ Tech stack (language, framework, key dependencies)
   □ Fork origin (if any, credit the original)
   □ Core features (3-5 main ones)
   □ Installation method (download / build / package manager)
   □ Target audience
   ```

4. **Ask user** only for missing critical info — don't guess project purpose.

## Phase 2: Classify (pick a template)

Load the matching template from `reference/`:

| Project type | Template | When to use |
|--------------|----------|-------------|
| CLI tool / Desktop app | `template-app.md` | User runs it directly |
| Library / Package | `template-lib.md` | Others import/use it |
| Android module / Xposed | `template-module.md` | System-level integration |
| Web app / Frontend | `template-web.md` | Browser-based interface |
| CLI tool (detailed) | `template-cli.md` | Command-line tools with args |
| API service | `template-api.md` | REST/GraphQL APIs |
| Desktop app (detailed) | `template-desktop.md` | GUI applications |

**If none match**, use the generic structure in Phase 3.

## Phase 3: Draft (write README.md in Chinese)

### Generic structure:

```markdown
# 项目名称

> 一句话描述：做什么 + 给谁用 + 解决什么问题

🌐 English | 简体中文

## 📖 简介
2-3 句话说明项目定位、来源（Fork/原创）、核心技术栈。

## ✨ 功能特性
按类别分组，**必须用表格**：

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 功能 1 | 简要说明 |

## 🚀 快速开始
### 环境要求
### 下载安装（最简单的方式优先）
### 源码编译（可选）

## 📖 使用指南
操作步骤，关键步骤配截图或表格。

## ⚙️ 配置（如有）
配置文件路径 + 配置项表格。

## 🔌 API 参考（如有）
接口表格：方法 | 路径 | 说明

## ⚠️ 注意事项
已知限制、使用禁忌、常见问题。

## 🙏 致谢（如有）
Fork 项目、依赖库、灵感来源，附链接。

## 📸 截图（如有）
1-3 张核心界面截图。

## 📄 License
```

### Writing rules (严格遵守):

| Rule | ✅ Do | ❌ Don't |
|------|-------|---------|
| 语言 | README.md 中文，README_EN.md 英文 | 只写一个语言版本 |
| 语言切换 | 标题下方加 `🌐 English \| 简体中文` | 忘记加切换链接 |
| 功能展示 | 用表格，按类别分组 | 用长段落或平铺列表 |
| 命令 | 用 ``` 代码块包裹 | 裸写命令 |
| 标题 | emoji + 中文（如 `## ✨ 功能特性`） | 纯英文标题 |
| 简洁性 | 每句话都提供信息 | 写废话、套话 |
| Fork | 注明来源并致谢 | 抄袭不署名 |
| 快速开始 | 从最简单方式开始（下载 > 编译） | 一上来就让用户 clone 编译 |

## Phase 4: Polish (质量评分 + 自检)

### 自动评分系统（每项10分，满分40分）：

1. **结构完整性**（10分）
   - [ ] 包含所有必要章节
   - [ ] 章节顺序合理

2. **内容质量**（10分）
   - [ ] 一句话描述清晰具体
   - [ ] 功能描述具体明确

3. **格式规范**（10分）
   - [ ] 功能用表格展示
   - [ ] 命令在代码块内

4. **用户体验**（10分）
   - [ ] 快速开始简单易懂
   - [ ] 有截图展示（GUI项目）

**总分低于30分需要重新优化。**

### 自检清单：
- [ ] 一句话描述清晰具体（不是「一个项目」）
- [ ] 语言切换链接正确
- [ ] 功能按类别分组，用表格展示
- [ ] 快速开始能「复制粘贴就能跑」
- [ ] 所有命令在代码块内
- [ ] 配置/API 用表格
- [ ] Fork 项目注明来源
- [ ] GUI 项目有截图
- [ ] License 与 LICENSE 文件一致
- [ ] 无占位符、TODO、空白章节

## Phase 5: Deliver

Always deliver both files:

1. `README.md` — 中文版（主版本）
2. `README_EN.md` — 英文版

**中译英要点**：
- 保留 emoji 和格式
- 表格列名翻译
- 技术术语保持原文或加注（如「心率广播 (Heart Rate Broadcast)」）
- 链接保持不变

## AI Installation

### 安装方式（给AI Agent用）

复制下面的命令，粘贴给你的 AI Agent 即可自动安装：

```
请帮我安装 write-readme 技能：git clone https://github.com/roxyyn0304/write-readme.git 到你的 skills 目录
```

## Prompt template (给其他 AI 用)

```markdown
请为以下项目写 README.md + README_EN.md：

项目名称：[名称]
项目简介：[一句话描述]
技术栈：[语言/框架/关键依赖]
Fork 来源：[原项目链接，没有写「原创项目」]
核心功能：[列出 3-5 个]
安装方式：[下载安装 / 源码编译 / 包管理器]
目标用户：[谁会用这个]

格式要求：
- 功能特性用分组表格
- 命令用代码块
- 标题用 emoji + 中文
- 快速开始从最简单方式写起
- 中文 README.md + 英文 README_EN.md
```