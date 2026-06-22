# Agent OS

> 桌面端个人 AI 超级工作台 —— 开箱接入 Claude、Codex、Gemini、Cursor、Pi 等 8 款主流 AI CLI，沉淀你与 AI 协作的记忆、知识与成长。

本仓库同时托管：

- **产品官网** (`index.html` + 资源) — 由 GitHub Pages 在 `https://lohasle.github.io/agent-life/` 发布。
- **版本发布** — 最新安装包见 [Releases](https://github.com/lohasle/agent-life/releases)。

## 最新版本

当前最新版本：**v0.2.3** · 发布日期 2026-06-22

| 平台 | 安装包 | 下载 |
|---|---|---|
| macOS · Apple Silicon | `Agent-Os-0.2.3-mac-arm64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.3/Agent-Os-0.2.3-mac-arm64.dmg) |
| macOS · Intel | `Agent-Os-0.2.3-mac-x64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.3/Agent-Os-0.2.3-mac-x64.dmg) |
| Windows · x64 | 即将发布 | [关注 Releases](https://github.com/lohasle/agent-life/releases/tag/v0.2.3) |
| Linux · AppImage / deb | 即将发布 | [关注 Releases](https://github.com/lohasle/agent-life/releases/tag/v0.2.3) |

## 版本检查 API
| Windows · x64 | `Agent-Os-0.2.2-win-x64-setup.exe` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.2.2/Agent-Os-0.2.2-win-x64-setup.exe) |
更新系统通过 GitHub Releases API 获取最新版本信息：

```
GET https://api.github.com/repos/lohasle/agent-life/releases/latest
```

返回示例字段：

```json
{
  "tag_name": "v0.2.3",
  "name": "v0.2.3 — Agent OS",
  "published_at": "2026-06-22T02:31:06Z",
  "assets": [
    { "name": "Agent-Os-0.2.3-mac-arm64.dmg", "browser_download_url": "https://github.com/lohasle/agent-life/releases/download/v0.2.3/Agent-Os-0.2.3-mac-arm64.dmg" },
    { "name": "Agent-Os-0.2.3-mac-x64.dmg",   "browser_download_url": "https://github.com/lohasle/agent-life/releases/download/v0.2.3/Agent-Os-0.2.3-mac-x64.dmg" }
  ]
}
```

## 网站维护

- `index.html` — 单文件落地页（含内联样式与 i18n）。
- `mqoj247*.png` — 落地页配图资源。
- `DESIGN-HANDOFF.md` / `DESIGN-MANIFEST.json` — 设计交付件。

修改后提交至 `main` 分支，GitHub Pages 自动部署。

## License

MIT · 本地优先 · 主权数据 · 所有会话与索引离线可用
