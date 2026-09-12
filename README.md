# DI6 Website — free GitHub Pages setup

This site is static, so it can be hosted on GitHub Pages for free with a custom domain.

## 1) Create GitHub account
Go to github.com and create an account if you do not have one.

## 2) Create a repository
- Click **New repository**
- Name it: `di6-site`
- Set it to **Public**
- Click **Create repository**

## 3) Upload these files
Upload everything in this folder, keeping the `assets` folder intact:
- index.html
- styles.css
- script.js
- CNAME
- assets/di6-logo.png

Commit the files.

## 4) Turn on GitHub Pages
- Repository → **Settings** → **Pages**
- Under **Build and deployment**, choose **Deploy from a branch**
- Branch: `main` / root
- Save

GitHub will give you a temporary free URL first.

## 5) Connect di6.io in Porkbun
In Porkbun → Domain Management → `di6.io` → DNS, add GitHub Pages records.

For the root domain (`di6.io`), add these four **A records**:
- Host: blank / @ → 185.199.108.153
- Host: blank / @ → 185.199.109.153
- Host: blank / @ → 185.199.110.153
- Host: blank / @ → 185.199.111.153

For `www`, add a **CNAME**:
- Host: `www`
- Answer/Value: `<YOUR-GITHUB-USERNAME>.github.io`

Remove conflicting old A/AAAA/CNAME records for @ or www if Porkbun warns about duplicates.

Back in GitHub → Settings → Pages → Custom domain, enter `di6.io` and save. When available, enable **Enforce HTTPS**.

## Before launch
The site currently uses:
- Instagram: https://www.instagram.com/di6.io/
- LinkedIn: https://www.linkedin.com/company/di6/

If your LinkedIn public URL is different, replace that URL in `index.html` before publishing.
