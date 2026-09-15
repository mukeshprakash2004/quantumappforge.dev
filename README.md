# quantumappforge.dev

The Quantum App Forge website. Served by GitHub Pages at
<https://quantumappforge.dev>.

## Why this repo exists separately

There are two other Pages sites on this account, and neither could take this
domain safely while Brainfloss is mid-launch:

- `mukeshprakash2004.github.io` (user site) serves `/app-ads.txt`, which AdMob
  is waiting to crawl. A custom domain on a **user** site moves every project
  site under it, so `app-ads.txt` would relocate and its current URL would only
  work via redirect.
- `Brainfloss` (project site) serves the landing page and the privacy policy.
  That privacy URL is **hardcoded in the shipped app**, and the project-site URL
  is the developer website declared on the Play listing. A custom domain there
  would start redirecting both.

A dedicated repo takes the domain without touching either, so nothing that
currently works starts depending on a redirect.

## Contents

| File | Purpose |
|---|---|
| `index.html` | Landing page |
| `app-ads.txt` | Matches the file on the user site, ready for the eventual migration. Inert until this domain is declared as the developer website on Google Play. |
| `CNAME` | Binds the Pages site to `quantumappforge.dev` |

## Not here yet

The **privacy policy** deliberately still lives at
`https://mukeshprakash2004.github.io/Brainfloss/privacy`. It is hardcoded in the
app at `app/src/main/res/values/strings.xml`, so moving it needs a new app
release rather than a DNS change. Keeping one copy avoids two that drift.
