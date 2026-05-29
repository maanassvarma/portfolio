# Personal portfolio

Minimal static site for a policy researcher portfolio. Host it on GitHub Pages and put the URL on your resume.

## Publish (GitHub Pages)

1. Create a new repository on GitHub (e.g. `yourname.github.io` for a clean URL, or any name like `portfolio`).
2. In this folder, initialize git and push:

```powershell
cd c:\Users\maana\Projects\portfolio_website
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

3. On GitHub: **Settings → Pages → Build and deployment → Source** → choose **GitHub Actions**.
4. After the workflow runs (about one minute), your site is live.

**Resume URL**

| Repository name | Public URL |
|-----------------|------------|
| `yourname.github.io` | `https://yourname.github.io` |
| Any other name (e.g. `portfolio`) | `https://yourname.github.io/portfolio/` |

Use the first option if you want the shortest link on your resume.

Updates: edit `index.html`, commit, and push — the site redeploys automatically.

## Customize content

Edit the block at the top of the `<script>` in `index.html`:

- `name`, `tagline`, `bio` (array of paragraphs)
- `email`
- `pieces` — each entry needs `title`, `description`, and `pdf` (path from site root)

Place PDFs in `papers/` (e.g. `papers/my-paper.pdf`).

## Preview locally

Open `index.html` in a browser, or:

```powershell
npx serve .
```
