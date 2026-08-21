# Template: Android / Xposed Module

For system-level Android modules, Xposed/LSPosed modules, HyperOS integrations.

```markdown
# 模块名称

> 一句话描述：为 xxx 设备提供 xxx 功能

🌐 [English](README_EN.md) | 简体中文

## 📖 简介

基于 xxx 改造的 xxx 模块，将 xxx 深度接入 xxx 系统。

- 核心集成点 1
- 核心集成点 2
- 核心集成点 3

## ✨ 功能一览

### 🎧 设备控制
| 功能 | 说明 |
|------|------|
| 功能 1 | 关闭/通透/降噪 |
| 功能 2 | 高/中/低三档 |

### 🏝️ 系统集成
| 功能 | 说明 |
|------|------|
| 超级岛 | 支持官方超级岛 |
| 融合设备中心 | 支持设备卡片控制 |

### 🪟 弹窗与体验
| 功能 | 说明 |
|------|------|
| 连接弹窗 | 底部卡片 + 动画 |
| 电量岛 | 临时电量显示 |

### 🛠️ 模块能力
| 功能 | 说明 |
|------|------|
| 蓝牙日志 | 实时查看协议收发 |
| 调试页面 | HEX 发送测试 |

## 🚀 快速开始

### 环境要求
- 设备：小米/红米手机
- 系统：HyperOS（Android 15+）
- 框架：LSPosed API ≥ 101
- Root：需要

### 安装步骤
1. 从 [Releases](https://github.com/xxx/xxx/releases) 下载 APK
2. 在 LSPosed 中启用模块
3. 勾选推荐作用域：
   - `com.android.bluetooth`
   - `com.milink.service`
   - `com.xiaomi.bluetooth`
   - `com.android.settings`
4. 使用模块右上角「一键重启作用域」
5. 蓝牙连接你的设备

### 开发者构建
```bash
./gradlew assembleDebug
# 产物: app/build/outputs/apk/debug/app-debug.apk
```

## ⚠️ 重要提醒

> 🚫 请使用模块内的界面进行设备控制

系统设置里的设备界面显示的状态是由模块注入的，可能不准确。
请不要在系统设置中更改任何设置 —— 引发的问题不予处理。

一切控制请通过 **模块 App / 模块弹窗** 完成。

## 🙏 致谢

- [原项目](链接) — 原始项目
- [UI 组件库](链接) — 风格组件
- [协议库](链接) — 通信协议

## 📄 License

[GPL-3.0](LICENSE)

Made with ❤️ for xxx users
```
