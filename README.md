> [!IMPORTANT]
> **Merged into [aiutil/agent-os](https://github.com/aiutil/agent-os). The product site and application source now live in one repository.**
>
> **本产品站已合并至 [aiutil/agent-os](https://github.com/aiutil/agent-os)，产品页与应用源码现由同一仓库维护。**

# Agent OS

> 顶级的本地优先 Agent 工作台：安全托管其他主机上的 Agent，并把飞书等消息渠道变成所有已安装 Agent 的统一入口。

本仓库同时托管：

- **产品官网** (`index.html` + 资源) — 由 GitHub Pages 在 `https://lohasle.github.io/agent-life/` 发布。
- **使用指南** (`guide.html`) — 安装、首次启动、会话、任务、定时执行与远程节点说明。
- **版本发布** — 最新安装包见 [Releases](https://github.com/lohasle/agent-life/releases)。
- **更新记录** — 见 [`CHANGELOG`](https://lohasle.github.io/agent-life/changelog.html) 页。

## 两个核心亮点

### 1. 远程托管 Agent，授权边界由对方设置

受托管设备负责核验配对码和身份指纹，并自行决定开放哪些能力、Agent 与文件目录。控制端只能访问明确授权的资源；越界路径、错误凭证以及暂停或撤销后的请求都会被拒绝。

### 2. 一次接入消息渠道，切换所有 Agent

连接飞书、个人微信、企业微信、Telegram 或 WhatsApp 后，可在同一对话中通过 `/agents` 查看实时可用列表，再使用 `/use codex`、`/use claude` 等命令切换 Agent。每个 Agent 保留独立的持久会话，切回时继续原上下文；统一搜索与长期记忆仍由 Agent OS 管理。

支持的切换命令以本机发现结果为准，当前适配器包括 Claude、Codex、Cursor Agent、Gemini、Hermes、OpenCode、Pi 与 OpenClaw。

## 最新版本

当前最新版本：**v0.3.8** · 2026-07-24

本版本完善统计页的项目分析能力：项目更容易查找和辨认，可按项目比较使用量、查看 Token 趋势，并导出当前统计。

最终构建绑定 Agent-OS 源码提交 `f10bf3ac96d0`；桌面、节点与校验资产只有在远端 exact set 和 SHA-256 全部一致后才会公开。

产品网站与下载链接由发布 workflow 从版本清单同步；截图文件名保留其实际采集版本。

| 平台 | 安装包 | 下载 |
|---|---|---|
| macOS · Apple Silicon | `Agent-Os-0.3.8-mac-arm64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-mac-arm64.dmg) |
| macOS · Intel | `Agent-Os-0.3.8-mac-x64.dmg` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-mac-x64.dmg) |
| Windows · x64 | `Agent-Os-0.3.8-win-x64-setup.exe` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-win-x64-setup.exe) |
| Linux · x64 (deb) | `Agent-Os-0.3.8-linux-amd64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-linux-amd64.deb) |
| Linux · x64 (AppImage) | `Agent-Os-0.3.8-linux-x86_64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-linux-x86_64.AppImage) |
| Linux · arm64 (deb) | `Agent-Os-0.3.8-linux-arm64.deb` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-linux-arm64.deb) |
| Linux · arm64 (AppImage) | `Agent-Os-0.3.8-linux-arm64.AppImage` | [下载](https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-linux-arm64.AppImage) |

> macOS 安装包未做开发者签名（无 Developer ID），首次启动需右键 → 打开。
> Windows / Linux 安装包由对应架构的原生 GitHub-hosted runner 构建。

## 版本检查 API

```
GET https://api.github.com/repos/lohasle/agent-life/releases/latest
```

返回示例字段：

```json
{
  "tag_name": "v0.3.8",
  "name": "v0.3.8 — Agent OS",
  "assets": [
    { "name": "Agent-Os-0.3.8-mac-arm64.dmg", "browser_download_url": "https://github.com/lohasle/agent-life/releases/download/v0.3.8/Agent-Os-0.3.8-mac-arm64.dmg" }
  ]
}
```

## 网站维护

- `index.html` — 单文件产品展示页（含完整实机界面总览、内联样式与 i18n）。
- `guide.html` — 中英文完整使用指南。
- `changelog.html` — 版本更新记录页。
- `agentos-icon.png` — 与桌面应用一致的官网 favicon 与品牌图标。
- `message-channels-agent-switch-v0.3.3.png` — 消息渠道配置与 Agent 回合状态实机截图。
- `remote-hosting-pairing-v0.3.3.png` — 远程 Agent 配对与方向性授权实机截图。
- `mqoj247*.png` — 落地页配图资源。
- `DESIGN-HANDOFF.md` / `DESIGN-MANIFEST.json` — 设计交付件。

修改后提交至 `main` 分支，GitHub Pages 自动部署。

## License

MIT · 本地优先 · 主权数据 · 所有会话与索引离线可用
