# Buzzword website

Public homepage, privacy policy and support page for the Buzzword Chrome extension.
Plain HTML and CSS, no build step. Deployed on Vercel.

| Page | URL | Used by |
| --- | --- | --- |
| Home | `/` | Web Store "Homepage URL", OAuth branding homepage |
| Privacy policy | `/privacy` | Web Store privacy field, OAuth branding, `PRIVACY.md` |
| Support | `/support` | Web Store "Support URL" |

**Don't rename or move `privacy.html`.** The Web Store and Google's OAuth consent screen link to `/privacy`.
`vercel.json` sets `cleanUrls`, so `privacy.html` is served at `/privacy`.

## Deploy
1. Push this repo to GitHub.
2. In Vercel: Add New → Project → import the repo. Framework preset: **Other**. No build command, output directory is the repo root.
3. After it's live, update the Web Store listing, the OAuth Branding page and `PRIVACY.md` in the Buzzword repo with the new URLs.

## Preview locally
```
python3 -m http.server 4321
```
(Locally, open `/privacy.html`. The extensionless `/privacy` only works on Vercel.)

## Rules for edits
- The privacy facts must match the extension code and the Web Store Privacy tab.
- No analytics. If any are ever added, the privacy policy has to say so.
- Made-up names only. Don't quote the AP Stylebook or link to AP pages.
