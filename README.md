# 澄码 / Clearcode 安装包

这是澄码的安装包发布仓库。当前整合版本为 **0.1.30**，提供 macOS Apple Silicon 和 Windows x64 安装包。完整更新内容见 [0.1.30 更新说明](releases/0.1.30.md)。

澄码是独立的 OpenCode V2 客户端。Windows 安装包适用于普通 Intel / AMD 的 Windows 10 / 11 64 位电脑，内置 OpenCode；首次启动按引导连接内核、选择项目并登录自己的模型账户。

## 下载和安装

- [下载最新版本](https://github.com/Teddyroll/clearcode-releases/releases/latest)
- macOS：选择 `arm64-LOCAL-TEST.dmg`，适用于 Apple Silicon、macOS 26 或更高版本。退出澄码后，将应用拖到「应用程序」目录覆盖安装。
- Windows：选择 `win-x64-UNSIGNED.exe`，适用于 Intel / AMD 的 Windows 10 / 11 64 位电脑。退出澄码后运行新版安装器覆盖安装。

升级前请保存草稿并备份本机资料。安装包不包含使用者的聊天记录、模型账户或个人设置；这些内容保存在本机。请勿为了升级先卸载或删除资料目录。

## Windows 应用内更新

已安装 0.1.2 或更高版本时，在「设置 → 应用更新」填写本仓库的最新版下载目录地址，然后检查更新。每个发布版本同时提供安装器、SHA-256 校验文件、blockmap 和 latest.yml 更新清单。

关闭澄码后也可以直接运行新版安装包覆盖安装；无需先卸载。应用数据和模型账户配置保存在自己的电脑上。

## 当前发布状态

当前安装包是测试版：macOS 使用本地 ad-hoc 签名，尚未通过 Developer ID 签名和 Apple 公证；Windows 尚未通过 Authenticode 签名，系统可能提示未知发布者。下载后可核对同名 `.sha256` 文件。Windows 构建和内嵌内容已验证，Windows 实机安装与首次启动仍需在目标电脑确认。

本仓库只发布可分发的安装包、公开说明和校验信息。

## 固定地址

Windows 更新地址：

```text
https://github.com/Teddyroll/clearcode-releases/releases/latest/download/
```

[下载最新安装包及校验文件](https://github.com/Teddyroll/clearcode-releases/releases/latest)
