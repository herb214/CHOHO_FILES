# CHOHO_FILES

本仓库含两类内容，**对外发布范围不同**：

## 对外（GitHub Pages · 海外）

仅发布 **`public/`** 目录：2026 样本 PDF 与扫码页。**不含**内部地图与区域市场报告。

| 内容 | URL |
|------|-----|
| 入口（英文，扫码进入） | https://herb214.github.io/CHOHO_FILES/ |
| PDF 直链 | https://herb214.github.io/CHOHO_FILES/qingdao-zhenghe-sample-2026.pdf |
| **打印用二维码 PNG** | 仓库内 `public/entry-qr.png`，或线上 https://herb214.github.io/CHOHO_FILES/entry-qr.png |

二维码内容 = 入口页 URL（不是 PDF）。入口仅两个按钮：**Download from Google Drive**、**Open PDF directly**。

Google Drive：在 `public/google-drive-link.txt` 粘贴一行分享链接后 `git push`。

Pages 设置：**Settings → Pages → Source → GitHub Actions**。

## 内部（勿上 GitHub Pages）

以下仅用于本机或阿里云，**不会**被 `Deploy GitHub Pages` 工作流发布：

- `index.html` — ACS 海外市场情报库 · 世界地图
- `素材/`
- `Overseas Market Intelligence/`

### 国内访问（内网/阿里云）

http://8.136.202.129/
