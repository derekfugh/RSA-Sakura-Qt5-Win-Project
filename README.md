# RSA-Sakura-Qt5-Win-Project

RSA-Sakura Driver 的 Windows 纯绿色免安装版本（基于 Qt 5.15 构建，兼容 Windows 7 / 8 / 10 / 11）。

Windows out-of-the-box portable version of RSA-Sakura Driver (Built with Qt 5.15, compatible with Windows 7 / 8 / 10 / 11).

---

## 🚀 快速开始 (Quick Start)

本程序**不需要**安装任何 Qt 运行库，所有依赖已打包在内。

**第一步：环境初始化**
1. 启动你的 RSA-Sakura 加密器，打开其命令行窗口。
2. 将本目录下的 `qt-win-setup.bat` 拖入该命令行窗口并回车运行。
   *(这会在后台生成一个 `rsa-sakura-qt-env.ini`，用于告诉 Driver 加密器的核心路径)*

**第二步：运行 Driver**
直接双击 **`RSA-Sakura-Qt.exe`** 即可启动。

*(建议：你可以右键 `RSA-Sakura-Qt.exe`，发送快捷方式到桌面，以后直接双击即可)*

---

## ✨ 功能特性 (Features)

*   **纯绿色免安装**：包含完整的 Qt5 运行库与 MinGW 依赖，解压即用。
*   **完全兼容**：支持 Windows 7、8、10 和 11。
*   **无缝对接**：自动继承加密器的命令行环境，完美支持拖拽加解密。
*   **与 macOS / Linux 版体验一致**：相同的 UI 布局、相同的密钥管理逻辑。

---

## 🛠️ 常见问题 (Troubleshooting)

**1. 双击没有反应，或提示“找不到 xxx.dll”？**
请确保你没有单独把 `exe` 文件拖出来运行。必须保留压缩包的完整目录结构（包括 `platforms` 文件夹、`plugins` 文件夹以及所有的 `.dll` 文件）。

**2. 提示“环境缺失”或找不到加密命令？**
说明你还没有执行第一步的初始化。请回到加密器命令行窗口，运行 `qt-win-setup.bat`。

**3. 窗口太小，或者控件挤在一起？**
这是因为 Windows 系统的高 DPI 缩放导致的。可以右键 `RSA-Sakura-Qt.exe` -> 属性 -> 兼容性 -> 更改高 DPI 设置 -> 勾选“替代高 DPI 缩放行为”，并选择“系统(增强)”。

---

## 💻 源码说明 (Source Code)
本仓库目前仅提供编译后的可直接运行版本。如需查看 Qt 源码，请移步 [RSA-Sakura-Qt (macOS/Linux)](链接到你的源代码仓库)。

---

## 🌸 满血樱花：全平台支持矩阵 (Platform Support)

RSA-Sakura 拥有极其强悍的跨平台能力。底层核心（`xrsaoapp.sw` 等）完全基于纯命令行，无需任何 GUI 环境即可在任意服务器或终端上运行；结合 Driver GUI，我们提供了开箱即用的全平台桌面体验。

| 平台 / 架构 | 核心引擎 (CLI) | 图形界面 (Driver GUI) | 获取方式 / 备注 |
| :--- | :---: | :---: | :--- |
| **macOS (Apple Silicon)** | ✅ | ✅ | **Driver：Xcode 原生版** |
| **macOS (Intel)** | ✅ | ❌ |  |
| **Linux ARM64** | ✅ | ✅ | **Driver：Qt6 版**（需系统安装 Qt6 库） |
| **Linux x64 (Linux 18.04 +)** | ✅ | ✅ | **Driver：Qt5-Linux + 完整依赖包** |
| **Windows x64 (Win7～11)** | ✅ | ✅ | **Driver：Qt5-Win 纯绿色免安装包** |
| **Windows x86 (WinXP)** | ✅ | ❌ |  |
| **Windows ARM64** | ❌ | ❌ |  |
| **任意 Linux 服务器 (无图形界面)** | ✅ | - | 直接在命令行终端中使用樱花🌸加密。 |

*(注：✅ 代表完美支持，❌ 代表不支持，🛠️ 代表需要一定开发基础自行编译)*
