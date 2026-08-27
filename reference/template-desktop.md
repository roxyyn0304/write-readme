# Template: Desktop Application (Detailed)

For GUI applications with windows, menus, and visual interfaces.

```markdown
# 应用名称

> 一句话描述：做什么 + 给谁用 + 解决什么问题

🌐 [English](README_EN.md) | 简体中文

## 📖 简介

2-3 句话说明：
- 项目是什么
- 来源（Fork 自 xxx / 原创项目）
- 核心技术栈（如 Electron、Tauri、Qt 等）

## ✨ 功能特性

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 功能 1 | 简要说明 |
| 功能 2 | 简要说明 |

### 🎨 界面特性
| 特性 | 说明 |
|------|------|
| 响应式布局 | 支持不同窗口大小 |
| 暗黑模式 | 自动/手动切换 |
| 多语言 | 支持中文/英文 |

### 🔧 高级功能
| 功能 | 说明 |
|------|------|
| 快捷键 | 全局快捷键支持 |
| 系统托盘 | 最小化到托盘 |
| 自动更新 | 检查并安装更新 |

## 🚀 快速开始

### 方式一：下载安装（推荐）
1. 前往 [Releases](https://github.com/xxx/xxx/releases) 下载最新版本
2. 运行安装程序
3. 启动应用

### 方式二：源码编译
```bash
git clone https://github.com/xxx/xxx.git
cd xxx
# 安装依赖
npm install  # 或 yarn install
# 启动开发
npm run dev
# 构建生产版本
npm run build
```

### 环境要求
- 操作系统：Windows 10+ / macOS 10.15+ / Linux
- 内存：4GB+
- 磁盘空间：500MB+

## 📖 使用指南

### 首次启动
1. 启动应用
2. 完成初始设置向导
3. 导入配置（可选）

### 基本操作
| 操作 | 说明 |
|------|------|
| 打开文件 | Ctrl+O |
| 保存文件 | Ctrl+S |
| 撤销 | Ctrl+Z |
| 重做 | Ctrl+Y |
| 设置 | Ctrl+, |

### 快捷键
| 快捷键 | 功能 |
|--------|------|
| `Ctrl+N` | 新建文件 |
| `Ctrl+O` | 打开文件 |
| `Ctrl+S` | 保存文件 |
| `Ctrl+Shift+S` | 另存为 |
| `Ctrl+Z` | 撤销 |
| `Ctrl+Y` | 重做 |
| `Ctrl+F` | 查找 |
| `Ctrl+H` | 替换 |
| `F1` | 帮助 |

## ⚙️ 配置

配置文件路径：
- Windows: `%APPDATA%/app-name/config.json`
- macOS: `~/Library/Application Support/app-name/config.json`
- Linux: `~/.config/app-name/config.json`

| 配置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| theme | string | "system" | 主题（light/dark/system） |
| language | string | "zh-CN" | 语言 |
| auto_save | boolean | true | 自动保存 |
| window_width | number | 1200 | 窗口宽度 |
| window_height | number | 800 | 窗口高度 |

### 配置文件示例
```json
{
  "theme": "dark",
  "language": "zh-CN",
  "auto_save": true,
  "window_width": 1200,
  "window_height": 800
}
```

## 🎨 界面预览

### 主界面
（放置主界面截图）

### 设置界面
（放置设置界面截图）

### 深色模式
（放置深色模式截图）

## 📁 项目结构（开发者）

```
src/
├── main/              # 主进程
│   ├── index.ts       # 入口文件
│   ├── window.ts      # 窗口管理
│   └── ipc.ts         # IPC 通信
├── renderer/          # 渲染进程
│   ├── components/    # 组件
│   ├── pages/         # 页面
│   └── App.tsx        # 根组件
├── assets/            # 资源文件
└── styles/            # 样式文件
```

## 🛠️ 开发指南

### 开发环境搭建
```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 运行测试
npm test

# 构建生产版本
npm run build
```

### 构建发布版本
```bash
# Windows
npm run build:win

# macOS
npm run build:mac

# Linux
npm run build:linux
```

## ⚠️ 注意事项

- 注意事项 1
- 注意事项 2
- 注意事项 3

## 🙏 致谢

- [原项目名](链接) — 说明
- [依赖库](链接) — 说明

## 📸 截图

（放置 1-3 张核心界面截图）

## 📄 License

[MIT](LICENSE)
```