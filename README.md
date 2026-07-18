# Agent OS

> 本地优先的桌面 Agent 工作台 —— 统一管理 AI CLI 会话、原生终端、任务看板、定时执行、对比、记忆搜索、统计与远程 Runtime 节点。

本仓库同时托管：

- **产品官网** (`index.html` + 资源) — 由 GitHub Pages 在 `https://lohasle.github.io/agent-life/` 发布。
- **使用指南** (`guide.html`) — 安装、首次启动、会话、任务、定时执行与远程节点说明。
- **版本发布** — 最新安装包见 [Releases](https://github.com/lohasle/agent-life/releases)。
- **更新记录** — 见 [`CHANGELOG`](https://lohasle.github.io/agent-life/changelog.html) 页。

## 最新版本

当前最新版本：**v0.2.8** · 2026-07-18

本版本新增完整的 Agent 任务系统：可在四列看板中派发、跟踪和人工验收任务，也可为指定 Runtime Host 与 Agent CLI 创建一次性或 Cron 定时计划。任务由 Runtime daemon 持有，关闭桌面窗口后仍可按计划运行；重度历史库的旧会话回填改为后台限流执行，不再阻塞桌面窗口启动。

最终构建已基于源码提交 `0368955` 完成发布：19 个 Release 资产均已重新构建或复核，并由 GitHub 提供 SHA-256 digest。

产品网站内容以 v0.2.8 当前界面为准，按“产品展示 → 快速开始/完整指南 → 分平台下载”组织；CLI 可用性、厂商登录、本地数据与模型服务边界均已明确说明。

| 平台 | 安装包 | 下载 |
|---|---|---|
| macOS · Apple Silicon | `Agent-Os-0.2.8-mac-arm64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-mac-arm64.dmg) |
| macOS · Intel | `Agent-Os-0.2.8-mac-x64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-mac-x64.dmg) |
| Windows · x64 | `Agent-Os-0.2.8-win-x64-setup.exe` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-win-x64-setup.exe) |
| Linux · x64 (deb) | `Agent-Os-0.2.8-linux-amd64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-linux-amd64.deb) |
| Linux · x64 (AppImage) | `Agent-Os-0.2.8-linux-x86_64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-linux-x86_64.AppImage) |
| Linux · arm64 (deb) | `Agent-Os-0.2.8-linux-arm64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-linux-arm64.deb) |
| Linux · arm64 (AppImage) | `Agent-Os-0.2.8-linux-arm64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-linux-arm64.AppImage) |

> macOS 安装包未做开发者签名（无 Developer ID），首次启动需右键 → 打开。
> Windows / Linux 为 mac 交叉打包产出。

## 版本检查 API

```
GET https://api.github.com/repos/lohasle/agent-life/releases/latest
```

返回示例字段：

```json
{
  "tag_name": "v0.2.8",
  "name": "v0.2.8 — Agent OS",
  "assets": [
    { "name": "Agent-Os-0.2.8-mac-arm64.dmg", "browser_download_url": "https://github.com/lohasle/agent-life/releases/download/v0.2.8/Agent-Os-0.2.8-mac-arm64.dmg" }
  ]
}
```

## 网站维护

- `index.html` — 单文件落地页（含内联样式与 i18n）。
- `guide.html` — 中英文完整使用指南。
- `changelog.html` — 版本更新记录页。
- `mqoj247*.png` — 落地页配图资源。
- `DESIGN-HANDOFF.md` / `DESIGN-MANIFEST.json` — 设计交付件。

修改后提交至 `main` 分支，GitHub Pages 自动部署。

## License

MIT · 本地优先 · 主权数据 · 所有会话与索引离线可用
