# README 好坏示例对比

## 1. 一句话描述

**❌ Bad — 太模糊：**
```markdown
# Heart Rate Monitor
A heart rate monitoring tool.
```

**✅ Good — 具体清晰：**
```markdown
# Band Heart Rate

> OBS 以及其他支持通过网页源显示手环、手表「心率广播」的实时心率监测工具
```

**✅ Good — 说明技术栈：**
```markdown
# Band Heart Rate

> 基于 Rust 的轻量级系统托盘心率监测应用，支持 BLE 实时数据推送
```

---

## 2. 功能展示

**❌ Bad — 长段落：**
```markdown
## 功能
这个项目有很多功能，包括心率监测、系统托盘运行、Windows通知、实时心率显示、OBS覆盖层、HTTP API、自动重连等等。使用起来非常方便，只需要在手环设置中开启心率广播，然后运行程序就可以了。
```

**❌ Bad — 平铺列表：**
```markdown
## 功能
- 系统托盘运行
- Windows 通知
- 实时心率显示
- OBS 覆盖层
- HTTP API
- 自动重连
- 配置文件
- 多设备支持
```

**✅ Good — 分组表格：**
```markdown
## ✨ 功能特性

### 🎯 核心功能
| 功能 | 说明 |
|------|------|
| 系统托盘运行 | 静默启动，资源占用极低 |
| 实时心率显示 | Web 界面大数字刷新，心形动画 |
| 自动重连 | 断开后自动扫描重连，指数退避 |

### 🔗 集成能力
| 功能 | 说明 |
|------|------|
| OBS 覆盖层 | 透明背景心率叠加层 |
| HTTP API | REST + SSE 实时推送 |
| 配置接口 | 读写配置的 REST 接口 |
```

---

## 3. 快速开始

**❌ Bad — 一上来就编译：**
```markdown
## 快速开始
1. 安装 Rust 工具链（推荐 rustup）
2. git clone https://github.com/xxx/xxx.git
3. cd xxx
4. cargo build --release
5. 找到 target/release/xxx.exe 运行
```

**✅ Good — 从最简方式开始：**
```markdown
## 🚀 快速开始

### 方式一：下载安装（推荐）
前往 [GitHub Releases](https://github.com/xxx/xxx/releases) 下载最新版本，直接运行即可。

### 方式二：源码编译
\```bash
git clone https://github.com/xxx/xxx.git
cd xxx
cargo build --release
\```

### 环境要求
- Windows 10+（macOS/Linux 需自行添加平台依赖）
- Rust 工具链（推荐 rustup）
```

---

## 4. 配置说明

**❌ Bad — 没有默认值：**
```markdown
## 配置
可以在配置文件中修改以下选项：
- max_heart_rate：最大心率
- server_port：HTTP 端口
- auto_start：开机自启
```

**✅ Good — 表格 + 默认值：**
```markdown
## ⚙️ 配置

配置保存在 `%APPDATA%/band-heart-rate/settings.json`，也可通过 HTTP API 修改。

| 配置项 | 说明 | 默认值 |
|--------|------|--------|
| max_heart_rate | 最大心率（影响区间划分） | 190 |
| server_port | HTTP 服务端口 | 3030 |
| auto_start | 开机自启动 | false |
| minimize_to_tray | 关闭时最小化到托盘 | true |
```

---

## 5. API 文档

**❌ Bad — 没有方法说明：**
```markdown
## API
- /heart-rate
- /heart-rate-stream
- /settings
- /health
```

**✅ Good — 表格 + 方法 + 说明：**
```markdown
## 🔌 HTTP API

| 方法 | 路径 | 说明 |
|------|------|------|
| GET | `/` | Web UI 页面 |
| GET | `/heart-rate` | 当前心率 JSON |
| GET | `/heart-rate-stream` | SSE 实时心率数据流 |
| GET | `/settings` | 获取当前配置 |
| PUT | `/settings` | 更新配置（JSON body） |
| GET | `/health` | 健康检查 |

默认地址 `http://127.0.0.1:3030`，端口冲突时自动使用随机端口。
```

---

## 6. 致谢

**❌ Bad — 没有说明：**
```markdown
## 致谢
- OppoPods
- Miuix
- moondrop-gaia-protocol
```

**✅ Good — 有链接和说明：**
```markdown
## 🙏 致谢

| 项目 | 说明 |
|------|------|
| [OppoPods](https://github.com/1812z/OppoPods) | 原始项目 |
| [Miuix](https://github.com/Miuix-Kotori/Miuix) | HyperOS 风格 Compose UI 组件 |
| [moondrop-gaia-protocol](https://github.com/xxx) | MOONDROP 协议库 |
```

---

## 7. 标题格式

**❌ Bad — 纯英文：**
```markdown
## Features
## Getting Started
## Configuration
```

**✅ Good — emoji + 中文：**
```markdown
## ✨ 功能特性
## 🚀 快速开始
## ⚙️ 配置
## 📖 使用指南
## 📄 License
```

---

## 8. 截图位置

**❌ Bad — 截图放在最前面：**
```markdown
# 项目名称

> 一句话描述

![截图1](screenshot1.png)
![截图2](screenshot2.png)

## 功能
...
```

**✅ Good — 截图放在最后或功能后面：**
```markdown
# 项目名称

> 一句话描述

## ✨ 功能特性
...

## 📸 截图

![控制面板](screenshot1.png)
![终端日志](screenshot2.png)
```
