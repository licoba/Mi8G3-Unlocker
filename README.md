# Mi8G3-Unlocker

<p align="center">
  <b>Snapdragon 8 Gen 3 小米设备高版本 HyperOS 全自动 BL 解锁辅助工具</b>
</p>

<p align="center">
  <a href="https://t.me/Kernix_dev">
    <img src="https://img.shields.io/badge/Telegram-Kernix_dev-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/SoC-Snapdragon%208%20Gen%203-red?style=for-the-badge" alt="Snapdragon 8 Gen 3">
  <img src="https://img.shields.io/badge/System-HyperOS%202%2B-orange?style=for-the-badge" alt="HyperOS 2+">
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status">
</p>

---

## 📌 项目简介

**Mi8G3-Unlocker** 是一款面向 **Snapdragon 8 Gen 3 平台小米设备** 的 Windows 全自动 BL 解锁辅助工具。

本项目针对高版本 HyperOS 环境进行适配，集成了解锁脚本、机型适配资源、ADB/Fastboot 工具、状态检测工具与调试入口，旨在简化 BL 解锁流程，降低手动操作复杂度，并提升多机型环境下的执行效率。

目前项目已支持多款 Xiaomi / Redmi / MIX 系列 Snapdragon 8 Gen 3 设备，可通过脚本自动完成机型选择、环境检查、流程执行与状态检测。

> 如需帮助或交流，欢迎加入频道：  
> **https://t.me/Kernix_dev**

---

## 🚀 项目亮点

- **高版本 HyperOS 支持**  
  面向 HyperOS 2.0 及以上系统环境适配。

- **Windows 全自动流程**  
  通过 `toUnlock.bat` 启动，一键进入自动化解锁流程。

- **多机型资源适配**  
  内置 Xiaomi / Redmi / MIX 多款机型所需资源文件。

- **内置 ADB / Fastboot**  
  无需用户额外安装 Android Platform Tools。

- **BL 状态检测**  
  提供 `check-unlock.bat` 用于检测 BL 锁与工程状态。

- **调试工具入口**  
  提供 `adb-tool.bat`，方便执行 ADB / Fastboot 相关调试命令。

- **中文交互提示**  
  内置清晰流程提示，方便用户按步骤操作。

---

## 📱 支持机型

当前项目已适配以下 **7 款 Snapdragon 8 Gen 3 平台设备**：

| 系列 | 机型 |
|---|---|
| Xiaomi | Xiaomi 14 |
| Xiaomi | Xiaomi 14 Pro |
| Xiaomi | Xiaomi 14 Ultra |
| Redmi | Redmi K70 Pro |
| Redmi | Redmi K80 |
| MIX | Xiaomi MIX Fold 4 |
| MIX | Xiaomi MIX Flip |

---

## 🧩 系统要求

| 项目 | 要求 |
|---|---|
| 电脑系统 | Windows 10 / Windows 11 |
| 手机系统 | HyperOS 2.0 及以上 |
| 设备平台 | Qualcomm Snapdragon 8 Gen 3 |
| 连接方式 | USB 数据线 |
| 调试状态 | USB 调试已开启 |

### 不支持

- HyperOS 1.0 及更早版本
- 非 Snapdragon 8 Gen 3 平台设备
- 未列入支持列表的设备
- 无法被 ADB / Fastboot 正常识别的设备

---

## 📦 Release 包结构

```text
Mi8g3-unlock-highversion-windows-auto-release.zip
├── 8650-Ennea.img
├── 8g3-unlock.bat
├── toUnlock.bat
├── check-unlock.bat
├── adb-tool.bat
├── adb.exe
├── fastboot.exe
├── AdbWinApi.dll
├── AdbWinUsbApi.dll
├── 赞助一下谢谢喵.png
└── unlockFolder/
    ├── bin/
    │   ├── Redmik80/
    │   │   ├── exploit
    │   │   └── su
    │   └── Xiaomi14/
    │       ├── exploit
    │       └── su
    ├── factoryImages/
    │   ├── Redmik70pro/
    │   ├── Redmik80/
    │   ├── Xiaomi14/
    │   ├── Xiaomi14pro/
    │   ├── Xiaomi14ultra/
    │   ├── Xiaomimixflip/
    │   └── Xiaomimixfold4/
    └── unlockGPT/
        ├── Redmik70pro/
        ├── Redmik80/
        ├── Xiaomi14/
        ├── Xiaomi14pro/
        ├── Xiaomi14ultra/
        ├── Xiaomimixflip/
        └── Xiaomimixfold4/
```

---

## 🛠️ 使用方法

### 1. 下载工具包

前往 **Releases** 页面下载最新版本：

```text
Mi8g3-unlock-highversion-windows-auto-release.zip
```

### 2. 解压文件

请完整解压到本地目录，建议使用英文路径，例如：

```text
C:\Mi8G3-Unlocker\
```

不要直接在压缩包内运行脚本。

### 3. 开启 USB 调试

手机端开启：

```text
设置 → 关于手机 → 连续点击版本号开启开发者选项
设置 → 更多设置 → 开发者选项 → USB 调试
```

连接电脑后，请在手机弹窗中允许 USB 调试授权。

### 4. 运行解锁脚本

双击运行：

```text
toUnlock.bat
```

然后按照脚本提示选择机型并执行流程。

### 5. 检查解锁状态

解锁完成后，可运行：

```text
check-unlock.bat
```

用于检测 BL 锁状态与工程状态。

### 6. ADB / Fastboot 调试

如需调试，可运行：

```text
adb-tool.bat
```

---

## 📁 主要文件说明

| 文件 / 目录 | 说明 |
|---|---|
| `toUnlock.bat` | 一键解锁入口 |
| `8g3-unlock.bat` | 主解锁流程脚本 |
| `check-unlock.bat` | BL / 工程状态检测脚本 |
| `adb-tool.bat` | ADB / Fastboot 调试工具 |
| `8650-Ennea.img` | 解锁流程相关镜像 |
| `unlockFolder/bin/` | 机型相关执行组件 |
| `unlockFolder/factoryImages/` | 各机型 factory images 资源 |
| `unlockFolder/unlockGPT/` | 各机型 unlock GPT 文件 |
| `adb.exe` / `fastboot.exe` | Android 调试与 Fastboot 工具 |

---

## ⚠️ 注意事项

- 解锁 BL 会清除用户数据，请务必提前备份。
- 请使用原装或质量稳定的数据线。
- 建议连接电脑后置 USB 2.0 接口。
- 请完整解压工具包后再运行脚本。
- 请勿删除或移动工具包内的文件。
- 建议使用 Windows 10 / 11 运行。
- 不建议在虚拟机或不稳定 USB 环境中操作。
- 不保证所有系统版本、区域版本或设备状态均可正常使用。

---

## ❓ 常见问题

### 设备无法识别怎么办？

请检查：

- 是否开启 USB 调试
- 是否点击允许 USB 调试授权
- 数据线是否支持数据传输
- Windows 驱动是否正常
- 是否被其他手机助手占用 ADB
- 是否完整解压工具包

### HyperOS 1.0 可以使用吗？

不支持。  
本工具面向 HyperOS 2.0 及以上系统环境。

### 解锁会清除数据吗？

会。  
BL 解锁流程会清除用户数据，请务必提前备份。

### 脚本运行失败怎么办？

请保留报错截图，并反馈以下信息：

- 设备型号
- 系统版本
- 当前模式：系统 / Fastboot
- 脚本报错截图
- 执行到哪一步失败

---

## 💬 反馈与交流

如果你遇到设备未识别、脚本报错、状态检测异常等问题，请提交 Issue，或前往频道交流：

> **https://t.me/Kernix_dev**

---

## 👥 贡献者

感谢来自 [@Littlenine](https://github.com/LittlenineEnnea) 的核心技术支持。

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LittlenineEnnea">
        <img src="https://github.com/LittlenineEnnea.png" width="100px;" alt="LittlenineEnnea"/><br />
        <sub><b>Littlenine</b></sub>
      </a><br />
      <sub>核心技术支持 / 解锁相关研究</sub>
    </td>
  </tr>
</table>

---

## ⚖️ 免责声明

本项目仅供技术交流、自有设备维护与授权测试使用。

使用本工具可能导致数据清除、设备异常、系统损坏、保修状态变化或其他不可预期后果。  
请在使用前确认设备属于你本人或已获得明确授权，并自行承担全部风险。

开发者不对任何滥用行为、设备损坏、数据丢失、保修失效或法律后果承担责任。

请勿将本项目用于未授权设备、非法用途或任何侵犯他人权益的行为。