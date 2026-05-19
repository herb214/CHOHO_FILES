# GitHub Pages (public sample catalog only)

This repo deploys **`public/`** only: entry page, PDF, entry QR. See `README.md` for live URLs.

## First-time setup

1. Create a **public** repo on GitHub (e.g. `CHOHO_FILES`).
2. Push this repo’s `public/`, `.github/workflows/pages.yml`, and `README.md`.
3. **Settings → Pages → Build and deployment → Source:** **GitHub Actions**.
4. After the first green **Deploy GitHub Pages** run, open `https://<user>.github.io/<repo>/`.

## Updates

```powershell
cd C:\Ali_Cloud
git add public/
git commit -m "Update public catalog"
git push
```

## Notes

- `public/qingdao-zhenghe-sample-2026.pdf` is ~20 MB; first load may take a few seconds.
- `deploy/*.pem` stays local (`.gitignore`).
