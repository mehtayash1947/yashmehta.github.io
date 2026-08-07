# Yash Mehta — Personal Website

A clean multi-page static site for GitHub Pages. Minimal homepage with your photo; each nav tab opens its own page. Burgundy accent, light theme with a dark-mode toggle (choice is remembered across pages).

## Files

```
index.html         Home — photo, name, tagline, contact links
education.html     Education
research.html      Research & Teaching
publications.html  Publications & Patents
experience.html    Professional Experience + Selected Projects
misc.html          Achievements, Skills, Coursework, Beyond Work
style.css          Shared styling for every page
assets/photo.jpg   Your profile photo (you add this — see below)
```

Keep all files together in the repo root (with `photo.jpg` inside an `assets/` folder). The links between pages are relative, so it all works once uploaded.

## 1. Add your photo

Create a folder named `assets` and put your picture in it named exactly **`photo.jpg`** (a square image works best — it's shown in a circle at ~170px). Until you add it, the homepage shows a burgundy "YM" circle automatically, so the site never looks broken. To use a `.png` instead, change `assets/photo.jpg` to `assets/photo.png` in `index.html`.

## 2. Fill in 3 links

In the files, replace these placeholders (search for the quoted text):

1. **Blog** — replace every `#BLOG_URL` with your WordPress trekking/running blog URL (in `index.html` and `misc.html`).
2. **Google Scholar** — replace `https://scholar.google.com/` in `index.html` with your Scholar profile, or delete that button.
3. **GitHub** — replace `https://github.com/` in `index.html` with `https://github.com/YOUR_USERNAME`, or delete that button.

LinkedIn (`linkedin.com/in/yashmehta`) and email are already set.

## 3. Publish to GitHub Pages (username.github.io)

1. Create a free GitHub account. Your username becomes your web address: `https://USERNAME.github.io`.
2. Create a new **public** repository named exactly `USERNAME.github.io` (e.g. `yashmehta.github.io`).
3. Upload all the files: on the repo page click **Add file → Upload files**, drag in every `.html` file, `style.css`, and the `assets` folder, then **Commit**. (Or use Git: clone, copy files in, `git add .`, `git commit -m "site"`, `git push`.)
4. Go to **Settings → Pages**. Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)**, Save.
5. Wait ~1 minute, then open `https://USERNAME.github.io`.

To update later, edit the file in the repo and commit — the live site refreshes automatically.

## 4. Optional: custom domain (e.g. yashmehta.com)

1. Buy the domain (~€10/yr) from any registrar.
2. Repo **Settings → Pages → Custom domain** → enter the domain → Save.
3. At the registrar's DNS, add four `A` records for the apex pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, and a `CNAME` for `www` → `USERNAME.github.io`.
4. Tick **Enforce HTTPS** once available.

## Notes

- No build step, no frameworks. Fonts load from Google Fonts; the only local file dependency is `style.css` and your photo.
- Edit shared look-and-feel once in `style.css` and it applies to every page.
- The theme toggle uses `localStorage` (works on GitHub Pages; only restricted preview sandboxes block it).
