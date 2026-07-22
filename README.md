# Agent OS

> 本地优先的桌面 Agent 工作台 —— 统一管理 AI CLI 会话、原生终端、任务看板、定时执行、对比、记忆搜索、统计与远程 Runtime 节点。

本仓库同时托管：

- **产品官网** (`index.html` + 资源) — 由 GitHub Pages 在 `https://lohasle.github.io/agent-life/` 发布。
- **使用指南** (`guide.html`) — 安装、首次启动、会话、任务、定时执行与远程节点说明。
- **版本发布** — 最新安装包见 [Releases](https://github.com/lohasle/agent-life/releases)。
- **更新记录** — 见 [`CHANGELOG`](https://lohasle.github.io/agent-life/changelog.html) 页。

## 最新版本

当前最新版本：**v0.3.2** · 2026-07-22

本版本优化定时任务执行详情：将 Agent 的流式思考与输出片段按真实语义边界归并，避免一句话因 token 或 stdout chunk 被拆成多个过程节点，同时保留工具、权限、错误和跨回合边界。

最终构建绑定 Agent-OS 源码提交 `87907abec348`；桌面、节点与校验资产只有在远端 exact set 和 SHA-256 全部一致后才会公开。

产品网站与下载链接由发布 workflow 从版本清单同步；截图文件名保留其实际采集版本。

| 平台 | 安装包 | 下载 |
|---|---|---|
| macOS · Apple Silicon | `Agent-Os-0.3.2-mac-arm64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-mac-arm64.dmg) |
| macOS · Intel | `Agent-Os-0.3.2-mac-x64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-mac-x64.dmg) |
| Windows · x64 | `Agent-Os-0.3.2-win-x64-setup.exe` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-win-x64-setup.exe) |
| Linux · x64 (deb) | `Agent-Os-0.3.2-linux-amd64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-linux-amd64.deb) |
| Linux · x64 (AppImage) | `Agent-Os-0.3.2-linux-x86_64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-linux-x86_64.AppImage) |
| Linux · arm64 (deb) | `Agent-Os-0.3.2-linux-arm64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-linux-arm64.deb) |
| Linux · arm64 (AppImage) | `Agent-Os-0.3.2-linux-arm64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-linux-arm64.AppImage) |

> macOS 安装包未做开发者签名（无 Developer ID），首次启动需右键 → 打开。
> Windows / Linux 安装包由对应架构的原生 GitHub-hosted runner 构建。

## 版本检查 API

```
GET https://api.github.com/repos/lohasle/agent-life/releases/latest
```

返回示例字段：

```json
{
  "tag_name": "v0.3.2",
  "name": "v0.3.2 — Agent OS",
  "assets": [
    { "name": "Agent-Os-0.3.2-mac-arm64.dmg", "browser_download_url": "https://github.com/lohasle/agent-life/releases/download/v0.3.2/Agent-Os-0.3.2-mac-arm64.dmg" }
  ]
}
```

## 网站维护

- `index.html` — 单文件产品展示页（含完整实机界面总览、内联样式与 i18n）。
- `guide.html` — 中英文完整使用指南。
- `changelog.html` — 版本更新记录页。
- `agentos-icon.png` — 与桌面应用一致的官网 favicon 与品牌图标。
- `task-board-v0.2.9.png` / `task-schedule-v0.2.9.png` — 完整比例的任务看板与定时任务实机截图。
- `mqoj247*.png` — 落地页配图资源。
- `DESIGN-HANDOFF.md` / `DESIGN-MANIFEST.json` — 设计交付件。

修改后提交至 `main` 分支，GitHub Pages 自动部署。

## License

MIT · 本地优先 · 主权数据 · 所有会话与索引离线可用
