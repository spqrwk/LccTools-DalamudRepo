# LCC Tools Dalamud Repository

LCC Tools 的 Dalamud 自定义插件仓库，仅发布编译并混淆后的插件产物，不包含源代码。

## 添加仓库

在 Dalamud 设置的“自定义插件仓库”中添加：

```text
https://raw.githubusercontent.com/spqrwk/LccTools-DalamudRepo/main/pluginmaster.json
```

然后在插件安装器中搜索 `LCC Tools`。

## 直接下载

- [latest.zip](plugins/lccTools/latest.zip)

## 命令

- `/lcc`、`/lcctools`：打开工具箱。
- `/lcctp`：MagicCode 激活后传送至鼠标指向位置。

## 维护者更新流程

1. 在插件项目 `lccTools.csproj` 中提高 `<Version>`，完成普通版、混淆版构建和功能回归。
2. 运行 `D:\weiyue\lccTools\prepare-release.ps1 -Changelog '本次更新内容'`；更新日志为必填项。
3. 检查本仓库中 `pluginmaster.json` 和 `plugins/lccTools/latest.zip` 的改动。
4. 使用 GitHub Desktop 提交并推送 `main`。
5. 验证仓库主页、`pluginmaster.json`、图标和 ZIP 均可公网访问，并核对远程 ZIP 与本地 SHA-256 一致。
