# Claude at Intuit — Self-Guided Training

A self-contained interactive training module for Intuit employees to learn how to use Claude effectively.

## 🚀 Live URL

After deployment: `https://<your-github-username>.github.io/claude-at-intuit-training/`

---

## What's Included

- **Module 1** — What Is Claude?
- **Module 2** — How Claude Works (prompting, iteration, limitations)
- **Module 3** — Tools & Features (Claude.ai, Claude Code, Cowork, API)
- **Module 4** — Hands-On Activities with copy-ready prompts
- **Module 5** — Best Practices & Data Privacy
- **Module 6** — Interactive Knowledge Check (quiz)

Features: sidebar navigation, progress tracker, copy-to-clipboard prompts, instant quiz feedback.

---

## Deploy to GitHub Pages (Free, ~2 minutes)

### Step 1 — Create a GitHub repo

```bash
# Go to https://github.com/new
# Name it: claude-at-intuit-training
# Set it to Public (required for free GitHub Pages)
# Do NOT initialize with README
```

### Step 2 — Push this repo

```bash
cd claude-at-intuit-training

git init
git add .
git commit -m "Initial commit: Claude at Intuit training"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/claude-at-intuit-training.git
git push -u origin main
```

> Replace `YOUR_USERNAME` with your GitHub username.  
> Use HTTPS if you don't have SSH set up:  
> `git remote add origin https://github.com/YOUR_USERNAME/claude-at-intuit-training.git`

### Step 3 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **GitHub Actions**
4. That's it — the workflow in `.github/workflows/deploy.yml` handles the rest

### Step 4 — Verify

- Go to **Actions** tab in your repo to watch the deploy
- Once green, visit: `https://YOUR_USERNAME.github.io/claude-at-intuit-training/`

---

## Auto-Deploy on Updates

Every time you push to `main`, GitHub Actions automatically redeploys. To update the training:

```bash
# Edit index.html
git add index.html
git commit -m "Update: [describe your change]"
git push
```

The site will be live with your changes in ~30 seconds.

---

## Local Preview

No build step needed — just open the file:

```bash
open index.html
# or
python3 -m http.server 8080
# then visit http://localhost:8080
```

---

## Sharing the Link

Once deployed, share this URL with all Intuit employees:

```
https://YOUR_USERNAME.github.io/claude-at-intuit-training/
```

You can also embed it in Confluence, Slack, or email as a direct link.

---

## Customization

All content lives in `index.html` — it's a single self-contained file. Common edits:

| What to change | Where in the file |
|---|---|
| Module content | Find the section `id="section-*"` divs |
| Prompt examples | Find `id="act1"` through `id="act5"` |
| Quiz questions | Find `class="quiz-card"` blocks |
| Colors/branding | Edit the `:root { }` CSS variables at the top |

---

## Architecture

```
Browser → GitHub Pages CDN → index.html (static, no server needed)
```

No backend, no database, no dependencies. 100% static HTML/CSS/JS.
