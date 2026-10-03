# site/

This folder is published as a GitHub Pages site at:
`https://YOUR-GITHUB-USERNAME.github.io/rope-untangle/`

It hosts the privacy policy and the version check file the app downloads on launch.

## Publishing with GitHub Pages

1. Push this repo to GitHub (if not already there).
2. In your GitHub repo, go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**.
4. Set the branch to `main` (or `master`) and the folder to `/site`.
5. Click **Save**. GitHub will publish the site in a minute or two.
6. Visit `https://YOUR-GITHUB-USERNAME.github.io/rope-untangle/` to confirm it's live.
7. Replace `YOUR-GITHUB-USERNAME` with your actual username in:
   - `www/index.html` — the `VERSION_CHECK_URL` constant near the top of the game section.
   - `site/README.md` (this file) — optional, for your own reference.

## Updating the minimum version

When you want to force players onto a new version, edit `site/version.json`:

```json
{ "minVersionCode": 2, "latestVersionCode": 2,
  "message": "A new version of Rope Untangle is ready." }
```

- `minVersionCode` — anyone below this sees a non-dismissible Update screen.
- `latestVersionCode` — anyone below this (but at or above min) sees a one-per-day toast.
- `message` — shown on the forced-update screen.

Commit and push; the change goes live within seconds. No app update needed.

## Before publishing

Fill in the placeholders in `privacy-policy.html`:
- `[DATE]` — today's date, e.g. 2026-10-03
- `[YOUR NAME OR COMPANY]` — your name or studio name
- `[YOUR EMAIL]` — a contact email
