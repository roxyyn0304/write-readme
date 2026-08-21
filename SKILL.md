---
name: write-readme
description: Use when the user wants to write, rewrite, or improve a README.md for a project. Covers analyzing existing code, summarizing features, structuring documentation, generating bilingual content, and following best practices for open-source project documentation.
---

# Write README

When the user asks to write a README, follow this workflow: **Analyze → Classify → Draft → Polish → Deliver**.

## Phase 1: Analyze (gather facts, don't write yet)

1. **Detect project type** by reading config files:

   | Config file | Project type |
   |-------------|--------------|
   | `package.json` | Node.js / Web |
   | `Cargo.toml` | Rust |
   | `build.gradle*` / `AndroidManifest.xml` | Android |
   | `go.mod` | Go |
   | `pyproject.toml` / `setup.py` | Python |
   | `pubspec.yaml` | Flutter/Dart |

2. **Read existing README** (if any) — understand what's documented, what's missing.

3. **Extract key facts** into a mental checklist:

   ```
   □ Project name
   □ One-line description (what + who + why)
   □ Tech stack (language, framework, key dependencies)
   □ Fork origin (if any, credit the original)
   □ Core features (3-5 main ones)
   □ Installation method (download / build / package manager)
   □ Usage environment (OS, versions, prerequisites)
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

**If none match**, use the generic structure in Phase 3.

## Phase 3: Draft (write README.md in Chinese)

### Generic structure (all project types):

```markdown
# 项目名称

> 一句话描述：做什么 + 给谁用 + 解决什么问题

🌐 English | 简体中文

## 📖 简介
2-3 句话说明项目定位、来源（Fork/原创）、核心技术栈。

## ✨ 功能特性
按类别分组，**必须用表格**：
| 功能 | 说明 |
|------|------|
| ... | ... |

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

## 📱 兼容性（如有）
支持的设备/系统版本。

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
| 截图 | 放在最后或功能特性附近 | 放在最前面 |
| 快速开始 | 从最简单方式开始（下载 > 编译） | 一上来就让用户 clone 编译 |

### Good vs Bad examples:

**❌ Bad — 功能用长段落：**
```markdown
## 功能
这个项目有很多功能，包括心率监测、系统托盘运行、Windows通知、
实时心率显示、OBS覆盖层、HTTP API、自动重连等等。
```

**✅ Good — 功能用分组表格：**
```markdown
## ✨ 功能特性

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 系统托盘运行 | 静默启动，资源占用极低 |
| 实时心率显示 | Web 界面大数字刷新，心形动画 |

### 🔗 集成能力
| 功能 | 说明 |
|------|------|
| OBS 覆盖层 | 透明背景心率叠加层 |
| HTTP API | REST + SSE 实时推送 |
```

**❌ Bad — 快速开始太复杂：**
```markdown
## 快速开始
1. 安装 Rust 工具链
2. git clone https://github.com/xxx/xxx.git
3. cd xxx
4. cargo build --release
5. 找到 target/release/xxx.exe 运行
```

**✅ Good — 快速开始从最简方式：**
```markdown
## 🚀 快速开始

### 方式一：下载安装（推荐）
1. 前往 [Releases](https://github.com/xxx/xxx/releases) 下载最新版本
2. 直接运行，无需安装

### 方式二：源码编译
\```bash
git clone https://github.com/xxx/xxx.git
cd xxx
cargo build --release
\```
```

## Phase 4: Polish (自检清单)

写完后逐项检查：

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

## Prompt template (给其他 AI 用)

When delegating, use this flexible template — fill in the brackets:

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
