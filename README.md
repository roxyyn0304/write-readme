# 📝 Write README Skill

> 通用 README 写作技能，支持 Claude、GitHub Copilot、DeepSeek Harness 等 AI Agent。

🌐 [English](README_EN.md) | 简体中文

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 智能分析 | 自动检测项目类型（Rust/Node/Python/Android/Web/C++/Java/C#） |
| 模板匹配 | 根据项目类型选择最佳 README 结构 |
| 中英双语 | 自动生成 README.md + README_EN.md |
| 质量评分 | 自动评估 README 质量（满分40分） |
| 自动化检查 | 结构、内容、格式全面检查 |

**支持的项目类型：** 应用工具 · 库包 · Android 模块 · Web 应用 · CLI 工具 · API 服务 · 桌面应用

## 🚀 安装

复制下面的命令，粘贴给你的 AI Agent 即可自动安装：

```
请帮我安装 write-readme 技能：git clone https://github.com/roxyyn0304/dsh-write-readme.git 到你的 skills 目录
```

## 📖 使用

安装后直接说：

```
帮我写 README
```

或

```
帮我优化 README
```

## 📁 文件结构

```
├── SKILL.md              # 主技能文件
├── reference/
│   ├── template-app.md   # 应用/工具模板
│   ├── template-lib.md   # 库/包模板
│   ├── template-module.md # Android 模块模板
│   ├── template-web.md   # Web 应用模板
│   ├── template-cli.md   # CLI 工具模板（新增）
│   ├── template-desktop.md # 桌面应用模板（新增）
│   ├── template-api.md   # API 服务模板（新增）
│   ├── examples.md       # 好坏示例对比
│   ├── prompt-template.md # Prompt 模板集
│   └── checklist.md      # 质量检查清单（新增）
```

## 🔧 自定义

- **添加模板：** 在 `reference/` 创建 `template-xxx.md`，并在 `SKILL.md` Phase 2 表格中注册
- **修改规则：** 编辑 `SKILL.md` 中的 Writing rules 表格
- **自定义检查：** 编辑 `reference/checklist.md` 中的检查项

## ✅ 质量评分系统

### 评分标准（满分40分）
1. **结构完整性**（10分）
2. **内容质量**（10分）
3. **格式规范**（10分）
4. **用户体验**（10分）

### 评分结果
- **40分**：优秀，无需修改
- **30-39分**：良好，可选优化
- **20-29分**：一般，建议优化
- **<20分**：较差，需要重写

## 📋 自动化检查

使用 `reference/checklist.md` 进行自动化检查：

```bash
# 检查 README 质量
# 结构检查：文件存在、语言切换、章节完整性
# 内容检查：一句话描述、功能展示、快速开始
# 格式检查：标题格式、代码块、表格
# 链接检查：外部链接、内部链接
```

## 📄 License

[MIT](LICENSE)

---

Made with ❤️ by [米萌 (MiMeng)](https://github.com/roxyyn0304)