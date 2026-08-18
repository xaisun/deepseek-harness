# DeepSeek Harness 桌面版 (DSH Desktop)

> 中英文说明 · Bilingual README（中文 / English）

DeepSeek Harness（简称 **DSH**）的 Windows 桌面版，开箱即用的本地 AI 助手客户端。
A ready-to-run Windows desktop client for DeepSeek Harness (aka **DSH**), a local AI assistant.

---

## 下载 / Download

> 桌面版为预编译二进制（约 256MB），请到 **[Releases](https://github.com/xaisun/deepseek-harness/releases)** 页面下载对应版本的压缩包。
> The desktop build is a precompiled binary (~256MB). Download the archive for your version from the **[Releases](https://github.com/xaisun/deepseek-harness/releases)** page.

- **v1.0.2**：[DeepSeek Harness v1.0.2.zip](https://github.com/xaisun/deepseek-harness/releases/tag/v1.0.2)（新增「重启前端」入口，修复改 UI 后窗口消失问题）

---

## 使用教程 / Getting Started

### 1. 安装 / Install

**中文**
1. 从 Releases 下载 `DeepSeek Harness v1.0.2.zip`。
2. 将压缩包解压到任意目录（建议路径**不要包含中文或空格**，如 `D:\DSH\`）。
3. 解压后无需安装额外依赖，运行时已随包内置。

**English**
1. Download `dsh-v1.0.1.zip` from the Releases page.
2. Extract it to any folder (avoid paths with **spaces or non-ASCII characters**, e.g. `D:\DSH\`).
3. No extra dependencies required — the runtime is bundled in the package.

### 2. 启动 / Launch

**中文**
1. 进入解压目录，双击 `DeepSeek Harness.exe`。
2. 首次启动会加载内置运行时（含 Node.js），可能需要等待数秒。
3. 启动后会出现客户端窗口；按界面提示完成初始化或配置即可使用。
   > 注：具体功能与配置项以客户端实际界面为准。

**English**
1. Open the extracted folder and double-click `DeepSeek Harness.exe`.
2. On first launch the bundled runtime (including Node.js) loads — allow a few seconds.
3. A client window appears; follow the on-screen prompts to finish setup.
   > Note: Actual features and settings depend on the client UI.

### 3. 数据与配置 / Data & Config

**中文**
- 用户数据默认存放在解压目录下的 `dsh-data/`，可整体备份/迁移。
- 运行时与组件位于 `harness-runtime/`，一般无需手动改动。
- 如需重置，关闭程序后删除 `dsh-data/` 即可（会清空本地数据）。

**English**
- User data lives in `dsh-data/` under the extracted folder — back it up or move it as needed.
- Runtime and components are in `harness-runtime/` — usually no manual changes needed.
- To reset, quit the app and delete `dsh-data/` (this clears local data).

### 4. 更新 / Update

**中文**
- 前往 Releases 下载新版本压缩包，解压覆盖原目录（建议先备份 `dsh-data/`）。
- 本仓库不通过 git 提交二进制，版本以 Release 标签为准。

**English**
- Download a newer archive from Releases and extract it over the old folder (back up `dsh-data/` first).
- Binaries are not committed to git; the version is the Release tag.

---

## 目录结构 / Package Structure

```
DeepSeek Harness.exe     # 主程序 / Main executable
harness-runtime/         # 运行时（含 node 运行时与 dsh 组件）/ Runtime (Node.js + dsh components)
dsh-data/                # 用户数据目录 / User data
dsh.ico                  # 图标 / Icon
```

---

## 常见问题 / FAQ

**Q：启动时被 Windows 拦截 / SmartScreen 提示？**
A（中文）：未签名的 exe 可能被 SmartScreen 或杀毒软件误报。确认来源可信后，点击"仍要运行"或将其加入白名单。
A（English）：Unsigned executables may trigger SmartScreen or antivirus warnings. If you trust the source, choose "Run anyway" or whitelist it.

**Q：解压后双击无反应？**
A（中文）：请确认已完整解压（含 `harness-runtime/`），且路径不含中文/空格；尝试以管理员身份运行。
A（English）：Make sure extraction completed (including `harness-runtime/`) and the path has no spaces/non-ASCII chars; try running as administrator.

**Q：数据存在哪里、怎么备份？**
A（中文）：见上方"数据与配置"，直接复制 `dsh-data/` 目录即可。
A（English）：See "Data & Config" above — just copy the `dsh-data/` folder.

**Q：让 Harness 改完对话窗口（放大、TOKEN 一行、会话费用）后窗口就不见了？**
A（中文）：这是正常现象——web 服务在启动时一次性读入界面文件，UI 改动需重启服务才生效。点 **☰ 菜单 → 重启前端**（或托盘右键 → 重启前端）即可让改动生效，不必彻底退出重开。
A（English）：Expected behavior — the web service loads the UI file only at startup, so UI changes need a service restart. Click **☰ Menu → Restart Frontend** (or right-click the tray icon → Restart Frontend) to apply changes without fully quitting.

---

## 免责声明 / Disclaimer

**中文**
1. 本仓库仅托管 DeepSeek Harness 桌面版的**预编译发布包**，由 `xaisun` 整理与分发，与 DeepSeek 官方无隶属关系。
2. 软件按"现状"提供，**不提供任何明示或暗示的担保**（包括但不限于适用性、可靠性、安全性）。使用风险由使用者自行承担。
3. 使用者应遵守所在国家/地区的法律法规，不得将本软件用于任何违法、侵权或损害他人权益的用途。
4. 因使用本软件导致的任何数据丢失、系统故障或其他损失，作者与维护者不承担责任。
5. 如本软件涉及第三方组件，其权利归各自权利人所有，请遵守对应许可证。

**English**
1. This repository only hosts the **precompiled release package** of the DeepSeek Harness desktop app, curated and distributed by `xaisun`. It is **not affiliated with or endorsed by DeepSeek**.
2. The software is provided **"as is"**, without any express or implied warranty (including, without limitation, fitness, reliability, or security). Use it at your own risk.
3. Users must comply with all applicable laws and regulations and must not use the software for any unlawful, infringing, or harmful purpose.
4. The author and maintainers are not liable for any data loss, system failure, or other damages arising from the use of this software.
5. Third-party components, if any, are owned by their respective rights holders and are subject to their own licenses.

---

## 许可证 / License

本仓库仅分发预编译二进制；各组件的许可证以压缩包内 `harness-runtime/LICENSE` 及对应文件为准。
This repo distributes precompiled binaries only. Component licenses follow `harness-runtime/LICENSE` inside the archive and respective files.

---

## 维护者 / Maintainer

- GitHub: [@xaisun](https://github.com/xaisun)
- 用途：仅供学习与交流 / For learning and communication only.
