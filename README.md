# Linar

**基于 QML + Rust 的 Material 3 Linux 桌面环境与显示管理器**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Material Design 3](https://img.shields.io/badge/Material%20Design-3-green.svg)](https://m3.material.io/)
[![Qt 6](https://img.shields.io/badge/Qt-6.8+-yellow.svg)](https://www.qt.io/)
[![Rust](https://img.shields.io/badge/Rust-stable-orange.svg)](https://www.rust-lang.org/)
[![Platform: Linux](https://img.shields.io/badge/Platform-Linux-lightgrey.svg)](https://www.linux.org/)

---

## 📖 项目简介

Linar 是一个面向 Linux 与 Cyanite (未来可期) 平台的**桌面环境（DE）**与**显示管理器（DM）**，采用 **QML + Rust** 作为核心技术栈，严格遵循 Google **Material Design 3** 设计语言，提供流畅、简洁的操作体验。

### 🎯 项目目标

| 目标 | 描述 |
|------|------|
| **统一桌面体验** | 整合窗口管理器、桌面面板、文件管理器、应用启动器等核心组件 |
| **显示管理器** | 提供美观的登录界面（Display Manager），支持多用户切换、生物识别 |
| **Material Design 3** | 严格遵循 MD3 设计规范，提供动态主题、色彩系统与排版系统 |
| **Rust 后端** | 用 Rust 编写高性能后端，确保系统安全、稳定、低资源占用 |

---

## 🏗️ 技术架构

```
┌─────────────────────────────────────────────────────────┐
│                     Linar Desktop                        │
├─────────────────────────────────────────────────────────┤
│  Presentation Layer (QML)                               │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌───────────┐  │
│  │ Display  │ │ Desktop  │ │ Settings │ │ File Mgr  │  │
│  │ Manager  │ │ Shell    │ │ Center   │ │           │  │
│  └────┬─────┘ └────┬─────┘ └────┬─────┘ └─────┬─────┘  │
│       │             │            │              │        │
│  ┌────┴─────────────┴────────────┴──────────────┴────┐  │
│  │           Material Design 3 Component Layer        │  │
│  │  NavigationBar │ TopAppBar │ Cards │ Dialogs │ …   │  │
│  │  Theme (Dynamic Colors, Typography, Shape)        │  │
│  └────────────────────────┬──────────────────────────┘  │
├────────────────────────────┴────────────────────────────┤
│  Core Layer (Rust)                                      │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌───────────┐  │
│  │ Window   │ │ System   │ │ User     │ │ IPC       │  │
│  │ Manager  │ │ Services │ │ Session  │ │ (D-Bus)   │  │
│  └──────────┘ └──────────┘ └──────────┘ └───────────┘  │
├─────────────────────────────────────────────────────────┤
│  Linux Kernel / Wayland / X11                           │
└─────────────────────────────────────────────────────────┘
```

---

## 🧩 核心组件

### 🖥️ 显示管理器（Display Manager）

提供系统登录界面，是用户与系统交互的第一个接触点。

- 多用户头像与切换
- 密码输入 / 生物识别（指纹、面部）
- 会话选择（X11 / Wayland / 其他桌面环境）
- 时钟与日期显示
- 壁纸动态主题同步
- 安全锁定与超时保护

### 🏠 桌面 Shell（Desktop Shell）

核心桌面环境，提供日常操作界面。

- **底栏任务栏（Shelf）**：常驻底部，类 ChromeOS 的应用启动栏 + 系统托盘
- **应用网格（App Grid）**：全屏应用启动器，支持文件夹分组与搜索
- **窗口管理**：平铺/堆叠布局，支持 Snap 窗口吸附
- **通知中心**：系统通知聚合、快捷操作面板
- **桌面小部件**：时钟、天气、搜索栏等可拖拽小部件
- **多虚拟桌面**：工作区切换与管理

### ⚙️ 设置中心（Settings）

统一的系统设置界面。

- 网络、蓝牙、显示、声音
- 外观与主题（动态壁纸配色、字体、深色模式）
- 用户账户与权限管理
- 应用管理与存储

### 📁 文件管理器

Material Design 3 风格的文件管理器。

- 列表视图 / 网格视图切换
- 侧边栏快速导航
- 标签页浏览
- 文件预览与搜索

---

## 🎨 设计系统

Linar 严格遵循 [Material Design 3](https://m3.material.io/) 设计规范，通过 `material-color-utilities` 实现动态配色、排版、形状、高度与动效的完整 Token 体系。所有令牌均为默认值，支持用户自定义覆盖。

> 📄 完整设计令牌定义见 [`docs/default-design-tokens.md`](docs/default-design-tokens.md)

---

## 📁 项目结构

```
Linar/
├── CMakeLists.txt                  # 顶层 CMake 构建配置
├── main.cpp                        # 应用入口
├── Main.qml                        # QML 主界面
├── LICENSE                         # MIT 许可证
│
├── src/                            # 核心源码
│   ├── core/                       # Rust 核心模块
│   │   ├── window-manager/         # 窗口管理
│   │   ├── session-manager/        # 用户会话管理
│   │   ├── system-services/        # 系统服务接口
│   │   └── ipc/                    # D-Bus / IPC 通信
│   │
│   ├── shell/                      # 桌面 Shell
│   │   ├── shelf/                  # 底栏任务栏
│   │   ├── app-launcher/           # 应用网格启动器
│   │   ├── notification-center/    # 通知中心
│   │   ├── workspace/              # 虚拟桌面管理
│   │   └── widgets/                # 桌面小部件
│   │
│   ├── lndm/                       # 显示管理器
│   │   ├── login/                  # 登录界面
│   │   ├── session-selector/       # 会话选择器
│   │   └── auth/                   # 认证模块
│   │
│   ├── settings/                   # 设置中心
│   └── components/                 # 通用 UI 组件
│
├── design-system/                  # Material Design 3 设计系统
│   ├── theme/                      # 主题定义
│   ├── tokens/                     # Design Tokens
│   └── icons/                      # 图标资源
│
├── design-example/                 # 参考组件库
│   ├── material-components-qml/    # QML MD3 组件参考实现
│   └── creeper-qt/                 # C++ Widgets MD3 封装参考
│
├── docs/                           # 项目文档
└── tests/                          # 测试代码
```

---

## 🛠️ 技术栈

| 层级 | 技术 | 说明 |
|------|------|------|
| **UI 框架** | Qt 6.8+ / QML | 声明式 UI 构建 |
| **核心语言** | Rust | 系统级后端、性能关键路径 |
| **构建系统** | CMake 3.16+ | 跨平台构建 |
| **设计语言** | Material Design 3 | Google 设计规范 |
| **颜色系统** | material-color-utilities | 动态配色算法 |
| **显示协议** | Wayland / X11 | Linux 显示服务器 |
| **系统通信** | D-Bus | 进程间通信 |
| **包管理** | Cargo (Rust) + CMake FetchContent | 依赖管理 |

---

## 🚀 快速开始

### 环境要求

- **操作系统**：Linux（推荐 Arch Linux / Ubuntu 22.04+）
- **Qt**：6.8 或更高版本
- **Rust**：stable 工具链
- **CMake**：3.16 或更高版本
- **编译器**：GCC 14+ / Clang 16+（支持 C++17）

### 构建步骤

```bash
# 克隆仓库
git clone https://github.com/CyaniAgent/Linar.git
cd Linar

# 安装依赖（以 Arch Linux 为例）
sudo pacman -S qt6-base qt6-declarative qt6-svg cmake gcc

# 创建构建目录
cmake -B build -DCMAKE_BUILD_TYPE=Release

# 编译
cmake --build build -j$(nproc)

# 运行（开发模式）
./build/appLinar
```

### 设置为系统显示管理器

```bash
# 安装到系统
sudo cmake --install build

# 配置显示管理器
sudo systemctl enable lndm.service
sudo systemctl set-default graphical.target

# 重启
sudo reboot
```

---

## 📐 设计规范

Linar 的设计令牌（Design Tokens）定义在 [`docs/default-design-tokens.md`](docs/default-design-tokens.md)，涵盖颜色、排版、形状、高度、状态层、动效与图标系统。所有令牌均为默认值，可通过用户设置或配置文件覆盖。

---

## 🗺️ 路线图

详见 [`docs/roadmap.md`](docs/roadmap.md)。

---

## 🤝 致谢

Linar 的设计系统参考了以下优秀开源项目：

- [**material-components-qml**](https://github.com/sudoevolve/material-components-qml) — QML Material Design 3 完整组件库（LGPL v3）
- [**creeper-qt**](https://github.com/creeper5820/creeper-qt) — C++ Widgets 声明式 MD3 封装（MIT）
- [**material-color-utilities**](https://github.com/nicolo-ribaudo/material-color-utilities) — Google 动态颜色算法库

---

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

```
MIT License — Copyright (c) 2026 CyaniAgent
```

> **注意**：`design-example/` 中引用的第三方组件库遵循各自的开源许可证（MIT / LGPL v3）。

---

<p align="center">
  <strong>Linar</strong> — 用 Material Design 3 重新定义 Linux 桌面体验
</p>
