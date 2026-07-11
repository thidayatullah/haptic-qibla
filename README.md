# Haptic Qibla — public website

Static pages for App Store Connect (Privacy Policy, Support, Marketing).

**This folder is published to a separate public GitHub repo.** The iOS app source stays in the private `QiblaLens` repo.

## Live URLs (after setup)

| Page | URL |
|------|-----|
| Home | https://thidayatullah.github.io/haptic-qibla/ |
| Privacy | https://thidayatullah.github.io/haptic-qibla/privacy.html |
| Support | https://thidayatullah.github.io/haptic-qibla/support.html |

## One-time setup

### 1. Create a new **public** repo on GitHub

- Name: `haptic-qibla`
- Visibility: **Public**
- Do **not** add a README (keep it empty)

### 2. Push this folder to the public repo

From the **QiblaFinder** project root:

```bash
cd website
git init
git add index.html privacy.html support.html style.css
git commit -m "Initial Haptic Qibla website"
git branch -M main
git remote add origin git@github.com:thidayatullah/haptic-qibla.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Open https://github.com/thidayatullah/haptic-qibla
2. **Settings → Pages**
3. **Source:** Deploy from a branch
4. **Branch:** `main` → **`/ (root)`**
5. Save

Wait 1–3 minutes, then open the Privacy URL above.

### 4. Replace placeholder email

Edit `privacy.html` and `support.html` — replace `REPLACE_WITH_YOUR_EMAIL` with your support address, then push again from the `website/` folder.

## Updating later

Edit files in `website/` inside the private app repo, then publish:

```bash
cd website
git add .
git commit -m "Update privacy policy"
git push
```

## Why two repos?

GitHub Pages on the **free plan** only works for **public** repos. Keeping `QiblaLens` private protects your Swift source while this tiny public repo exposes only HTML pages.
