# Democracy Defender Mod Manager 中文版

这是 [Democracy Defender Mod Manager](https://github.com/katsyk/DemocracyDefenderModManager) 的**非官方简体中文本地化版本**，基于原项目源码构建。

> 本项目由社区维护，不代表原作者，也未获得原作者官方背书。

- 原项目：https://github.com/katsyk/DemocracyDefenderModManager
- 原项目文档：https://katsyk.github.io/DemocracyDefenderModManager/
- 本项目 Releases：https://github.com/Kevinnnooobb/DemocracyDefenderModManager-zhcn/releases

## 中文本地化

主程序支持在“设置 → 语言”中选择 `English` 或 `简体中文`，语言选择会保存在本地并在下次启动时恢复。默认语言仍为 English。

## 自动同步与构建

本仓库通过 GitHub Actions 定期检查上游仓库：

1. 每六小时检查 `katsyk/DemocracyDefenderModManager` 的 `main` 分支和最新 `v*` Release 标签。
2. 将上游更新合并到本仓库的 `main` 分支。
3. 把新的上游版本标签推送到本仓库。
4. 触发现有构建流程，运行测试、i18n 检查和 Linux smoke test。
5. 自动构建 Windows、Linux 和浏览器扩展，并发布到本仓库的 GitHub Releases。

也可以在 **Actions → Sync upstream releases → Run workflow** 中手动触发同步。

如果上游修改与本地中文修改发生 Git 冲突，同步 workflow 会失败而不会强行覆盖本地修改；解决冲突并推送后，再手动运行 workflow 即可继续。

## 原项目说明

*Your mods. Your democracy. Defended.*

**Works with:** AyakaMods · Nexus Mods · ModWorkshop · GameBanana · GitHub · any direct link

DDMM is a source-neutral mod manager for Helldivers 2: install mods from any site, a direct download link, an archive, or a plain folder — no site is privileged, and no account with any mod site is ever required.

## The DDMM Promise

- **Every mod is welcome.** DDMM will never block, blacklist, or rank mods or mod sites.
- **No account, anywhere.** No mod site's login or credentials are ever asked for.
- **Your files, your choice.** Your mods live in a folder you control.
- **Open source, forever.** Apache-2.0, today and always.
- **Updates on your terms.** Update checks never run unless you ask.

## Installing / building

Prerequisites: [pnpm](https://pnpm.io/), a stable [Rust toolchain](https://rustup.rs/), and (Linux only) the Tauri system dependencies:

```sh
sudo apt install -y libwebkit2gtk-4.1-dev build-essential curl wget file libxdo-dev libssl-dev libayatana-appindicator3-dev librsvg2-dev
```

Then:

```sh
pnpm install
pnpm tauri build
```

For local development, `pnpm tauri dev` runs the app with hot reload. The built binary is named `ddmm` (`ddmm.exe` on Windows).

## Credits & license

DDMM is derived from Helldivers 2 Mod Manager by teutinsa (https://github.com/teutinsa/Helldivers2ModManager), licensed under Apache-2.0.

Original project: https://teutinsa.github.io/hd2mm-site · support the original author: https://ko-fi.com/teutinsa

This repository retains the original `LICENSE.txt` and `NOTICE` files. Changes in this fork include Simplified Chinese localization and automation for community builds. The original project name, copyright notices, and license terms remain unchanged.
