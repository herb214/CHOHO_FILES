# GitHub Pages 部署（海外 · 仅 PDF / 扫码）

**GitHub Pages 只发布 `public/`（样本 PDF + 扫码页）。**  
内部地图 `index.html`、`素材/`、`Overseas Market Intelligence/` **不会**上 GitHub，仅走阿里云等内网部署。

## 一、首次创建仓库并发布

1. 在 GitHub 新建仓库（建议 **Public**，否则免费版 Pages 受限），例如：`acs-omi`。
2. 在 GitHub 网站新建空仓库（**Public**），不要勾选 “Add README”（避免首次 push 冲突）。
3. 在本机 `Ali_Cloud` 目录执行（需已安装 [Git](https://git-scm.com/)）：

```powershell
cd C:\Ali_Cloud
git init
git branch -M main
git add index.html 素材 "Overseas Market Intelligence" public .github .gitignore
git add deploy/github-pages-setup.md deploy/omi-aliyun-deploy.txt
git commit -m "Add overseas market intelligence site for GitHub Pages"
git remote add origin https://github.com/herb214/CHOHO_FILES.git
git push -u origin main
```

当前账号：**herb214**，仓库：**CHOHO_FILES**。

3. **在 push 之前或之后立刻做（不做会 404）：**  
   打开 https://github.com/herb214/CHOHO_FILES/settings/pages  
   **Build and deployment → Source** 选 **GitHub Actions**（不要选 Deploy from a branch）。
4. 若 Actions 里 `deploy`  job 曾失败并提示 *Ensure GitHub Pages has been enabled*：完成上一步后，打开 [Actions](https://github.com/herb214/CHOHO_FILES/actions) → 点进失败的那次运行 → **Re-run all jobs**。
5. 等 **Deploy GitHub Pages** 全部变绿（约 1～3 分钟），再打开 Pages 链接。

## 二、访问地址

| 内容 | URL |
|------|-----|
| 入口 | https://herb214.github.io/CHOHO_FILES/ |
| PDF 直链 | https://herb214.github.io/CHOHO_FILES/qingdao-zhenghe-sample-2026.pdf |
| 扫码页 | https://herb214.github.io/CHOHO_FILES/sample-qr.html |

Actions 会自动按仓库名生成二维码 PNG（指向 GitHub 上的 PDF）。

## 三、以后更新

改完 `index.html` 或报告后：

```powershell
git add -A
git commit -m "Update dashboards"
git push
```

推送后会自动重新部署 Pages。

## 四、与阿里云 ECS 的关系

- **ECS**：可继续给国内同事用 `http://8.136.202.129/`。
- **GitHub Pages**：推荐给海外；无需改 ECS。
- 若希望扫码页只指向 GitHub，用 Pages 上的 `sample-qr.html` 即可。

## 五、注意

- PDF 约 20MB，首次从 GitHub 打开可能仍要几秒，但通常比跨国访问国内 ECS 更稳。
- 仓库需包含 `public/qingdao-zhenghe-sample-2026.pdf`（已在 `.gitignore` 中对该文件放行）。
- 私钥 `deploy/*.pem` 不会入库。
