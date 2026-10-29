# 澄码 / Clearcode 安装包

这是澄码的安装包发布仓库。通过本仓库的 Releases 下载 Windows、Mac 测试安装包和校验文件。

澄码是独立的 OpenCode V2 客户端，内置 OpenCode；首次启动按引导连接内核、选择项目并登录自己的模型账户。应用数据和模型账户配置保存在自己的电脑上。

## 当前版本：0.1.35

- 修复 Windows 安装包在「安全停止旧版本」检查阶段必定失败的问题：安全检查脚本被放进安装包根目录，运行时却从 `$PLUGINSDIR` 读取。0.1.30、0.1.34 均受影响，换任何 Windows 机器结果相同。
- 安装脚本改为 `File /oname=$PLUGINSDIR\prepare-windows-install.ps1`；安装、覆盖升级和卸载的任务检查、进程归属校验与原生原子删除流程保持不变。
- 功能与 0.1.34 相同：项目自主浏览器、任务检查与自动修复、全项回归。

[查看 0.1.35 更新说明与全部附件](https://github.com/Teddyroll/clearcode-releases/releases/tag/v0.1.35)

| 平台 | 安装包与验证范围 |
| --- | --- |
| Windows 10 / 11 x64，Intel / AMD | 未签名测试 EXE；已核验编译、内嵌代码、依赖、内核与更新配置，并确认成品内安全检查脚本位于 `$PLUGINSDIR`。本轮 Windows 实机安装、首启与覆盖升级未执行。 |
| Mac，Apple 芯片，macOS 26.0+ | ad-hoc 签名测试 DMG，未使用 Developer ID 签名、未经 Apple 公证；已挂载核验版本与内核清单，应用代码与 0.1.34 相同，本次未重跑打包应用的运行验收；手动安装。 |

[下载 Windows 0.1.35](https://github.com/Teddyroll/clearcode-releases/releases/download/v0.1.35/Clearcode-0.1.35-win-x64-UNSIGNED.exe) · [下载 Mac 0.1.35](https://github.com/Teddyroll/clearcode-releases/releases/download/v0.1.35/Clearcode-0.1.35-arm64-LOCAL-TEST.dmg)

下载后可核对同名 `.sha256` 文件。自主浏览器不包含全桌面控制、现有登录浏览器接管、密码填写、上传下载或验证码处理。本次工具链验收使用本地脚本化 provider，没有真实付费模型调用，不代表模型编程能力评分。

## Windows 更新

已安装 0.1.2 或更高版本时，在「设置 → 应用更新」填写下面的固定地址，然后检查更新。每个发布版本同时提供安装器、SHA-256 校验文件、blockmap 和 `latest.yml` 更新清单。

```text
https://github.com/Teddyroll/clearcode-releases/releases/latest/download/
```

关闭澄码后也可以直接运行新版安装包覆盖安装。请先保存草稿和备份资料。Mac 当前通过 DMG 手动更新。

任务台账新增全项回归记录；如需降级，请使用对应版本备份。本仓库只发布可分发的安装包、公开说明和校验信息。
