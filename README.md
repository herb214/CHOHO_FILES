# CHOHO_FILES

Public sample catalog (2026) on **GitHub Pages** — English entry page, PDF, and print QR.

| Item | URL |
|------|-----|
| Entry (scan QR here) | https://herb214.github.io/CHOHO_FILES/ |
| PDF direct link | https://herb214.github.io/CHOHO_FILES/qingdao-zhenghe-sample-2026.pdf |
| Print QR PNG | `public/entry-qr.png` or https://herb214.github.io/CHOHO_FILES/entry-qr.png |

The QR encodes the **entry URL** (not the PDF). The entry offers two actions: **Download from Google Drive** and **Open PDF directly**.

**Google Drive:** paste one share link (`https://drive.google.com/...`) into `public/google-drive-link.txt`, then `git push`.

**Pages:** Settings → Pages → Source → **GitHub Actions**. Pushes under `public/**` trigger deploy (see `.github/workflows/pages.yml`).
