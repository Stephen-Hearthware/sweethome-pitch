# Sweethome pitch page

A single self-contained `index.html` — a gentle, scrollable explainer to send her.
No build step, no dependencies. Edit the copy directly in `index.html`.

## Preview locally
Just open the file:
```
open index.html
```

## Deploy to GitHub Pages

**Option A — gh CLI (fastest):**
```bash
cd sweethome-pitch
git init -b main
git add .
git commit -m "Sweethome pitch page"
gh repo create sweethome-pitch --public --source=. --push
gh api -X POST repos/{owner}/sweethome-pitch/pages -f "source[branch]=main" -f "source[path]=/"
```
Live in ~1 min at: `https://<your-username>.github.io/sweethome-pitch/`

**Option B — web UI:**
1. Create a new public repo named `sweethome-pitch` on github.com.
2. Upload `index.html`.
3. Repo → Settings → Pages → Source: `main` branch, `/ (root)` → Save.
4. URL appears at the top of the Pages settings.

## Notes
- The page is set to `noindex` so it won't show up in search — it's just for her.
- Want a friendlier URL? Point a custom domain (or use a link shortener) when you text her.
- The before/after example uses her real "volunteer-community" voice memo. Swap the draft text in the `.card.after` block anytime.
