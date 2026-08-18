# DeepSeek Harness 桌面版 (DSH Desktop)

DeepSeek Harness（简称 **DSH**）的 Windows 桌面版，开箱即用的本地 AI 助手客户端。

## 下载

> 桌面版为预编译二进制（约 256MB），请到 **[Releases](https://github.com/xaisun/deepseek-harness/releases)** 页面下载对应版本的压缩包。

- **v1.0.1**：[DeepSeek Harness v1.0.1.zip](https://github.com/xaisun/deepseek-harness/releases/tag/v1.0.1)

## 使用说明

1. 从 Releases 下载 `DeepSeek Harness v1.0.1.zip` 并解压到任意目录。
2. 双击 `DeepSeek Harness.exe` 启动桌面客户端。
3. 运行时依赖已打包在 `harness-runtime/` 内，无需额外安装 Node.js。

## 目录结构（压缩包内）

```
DeepSeek Harness.exe     # 主程序
harness-runtime/         # 运行时（含 node 运行时与 dsh 组件）
dsh-data/                # 用户数据目录
dsh.ico                  # 图标
```

## 说明

本仓库仅托管桌面版的预编译发布包（通过 GitHub Releases 分发）。如需源码，请参考压缩包内 `harness-runtime/` 中的组件与配置。

---
*由 xaisun 维护 · 仅供学习与交流使用*
