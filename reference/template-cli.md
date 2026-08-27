# Template: CLI Tool (Detailed)

For command-line tools with arguments, options, and complex usage patterns.

```markdown
# 工具名称

> 一句话描述：做什么 + 给谁用 + 解决什么问题

🌐 [English](README_EN.md) | 简体中文

## 📖 简介

2-3 句话说明：
- 项目是什么
- 来源（Fork 自 xxx / 原创项目）
- 核心技术栈

## ✨ 功能特性

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 功能 1 | 简要说明 |
| 功能 2 | 简要说明 |

### 🔧 高级特性
| 功能 | 说明 |
|------|------|
| 配置文件 | 支持 JSON/YAML 配置 |
| 插件系统 | 支持自定义插件 |

## 🚀 快速开始

### 方式一：下载安装（推荐）
1. 前往 [Releases](https://github.com/xxx/xxx/releases) 下载最新版本
2. 解压到任意目录
3. 添加到 PATH 环境变量

### 方式二：源码编译
```bash
git clone https://github.com/xxx/xxx.git
cd xxx
# 编译命令
cargo build --release  # 或 go build 等
```

### 环境要求
- 操作系统：Windows / macOS / Linux
- 版本要求：xxx
- 其他依赖：xxx

## 📖 使用指南

### 基本用法
```bash
# 最简单的使用方式
tool-name [options] [arguments]
```

### 命令行参数
| 参数 | 短参数 | 说明 | 默认值 |
|------|--------|------|--------|
| `--config` | `-c` | 配置文件路径 | `./config.json` |
| `--output` | `-o` | 输出目录 | `./output` |
| `--verbose` | `-v` | 详细输出 | `false` |
| `--help` | `-h` | 显示帮助 | - |
| `--version` | `-V` | 显示版本 | - |

### 子命令（如有）
```bash
# 子命令用法
tool-name <command> [options]

# 可用命令：
#   init      初始化项目
#   build     构建项目
#   test      运行测试
#   deploy    部署项目
```

### 使用示例
```bash
# 示例 1：基本使用
tool-name --config ./my-config.json

# 示例 2：批量处理
tool-name --input ./data --output ./results

# 示例 3：使用配置文件
tool-name init --name my-project --template react
```

## ⚙️ 配置

配置文件路径：`~/.tool-name/config.json`

| 配置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| theme | string | "dark" | 界面主题 |
| auto_save | boolean | true | 自动保存 |
| max_retries | number | 3 | 最大重试次数 |
| timeout | number | 30 | 超时时间（秒） |

### 配置文件示例
```json
{
  "theme": "dark",
  "auto_save": true,
  "max_retries": 3,
  "timeout": 30
}
```

## 🔌 API 参考（如有）

| 方法 | 路径 | 说明 |
|------|------|------|
| GET | `/api/status` | 获取状态 |
| POST | `/api/process` | 处理数据 |
| GET | `/api/results` | 获取结果 |

## 📁 项目结构（开发者）

```
src/
├── main.rs        # 入口文件
├── cli.rs         # 命令行解析
├── config.rs      # 配置管理
├── core/          # 核心逻辑
├── utils/         # 工具函数
└── tests/         # 测试文件
```

## ⚠️ 注意事项

- 注意事项 1
- 注意事项 2
- 注意事项 3

## 🙏 致谢

- [原项目名](链接) — 说明
- [依赖库](链接) — 说明

## 📄 License

[MIT](LICENSE)
```