# Michael George — Portfolio

Personal portfolio site. Live at: **https://mycoola.github.io**

---

## 🚀 Publish to GitHub Pages (one time, ~5 minutes)

### Step 1 — Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name the repo **exactly**: `mycoola.github.io`
3. Set it to **Public**
4. Click **Create repository**

### Step 2 — Push this folder to GitHub

Open a terminal in this `portfolio/` folder and run:

```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/Mycoola/mycoola.github.io.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source", select **Deploy from a branch**
4. Choose branch: `main`, folder: `/ (root)`
5. Click **Save**

Your site will be live at `https://mycoola.github.io` within ~2 minutes.

---

## 📄 Add Your Resume PDF

1. Export your resume as a PDF (open `resume.html` in Chrome → Print → Save as PDF)
2. Create an `assets/` folder inside `portfolio/`
3. Save the PDF as `assets/michael-george-resume.pdf`
4. Push to GitHub — the "Download CV" button will then work

---

## ✏️ How to Update Your Portfolio

### Change any text / content

- Open `index.html` in VS Code (or any text editor)
- Find the section you want to edit (search for section headings like `<!-- PROJECTS -->`)
- Make your changes
- Save and push:
  ```bash
  git add .
  git commit -m "Update projects section"
  git push
  ```
- GitHub Pages rebuilds automatically in ~1 minute

### Add a new project

Find the `<!-- PROJECTS -->` section in `index.html` and copy one project card block:

```html
<div class="project-card fade-in">
  <div class="project-industry">Industry Name</div>
  <div class="project-name">Project Name</div>
  <div class="project-desc">
    Description of what you built and the impact.
  </div>
  <div class="project-tags">
    <span class="project-tag">Technology</span>
  </div>
</div>
```

### Add a blog article

1. Copy `blog/template.html` → rename it (e.g. `blog/my-article.html`)
2. Fill in the title, date, and content
3. In `index.html`, find the `<!-- BLOG -->` section and add a card:
   ```html
   <div class="blog-card">
     <div class="blog-date">June 2026</div>
     <div class="blog-title">Your Article Title</div>
     <div class="blog-excerpt">One or two sentence summary.</div>
     <a href="blog/my-article.html" class="blog-read-more">Read more →</a>
   </div>
   ```
4. Also delete the `<div class="blog-empty">` placeholder once you have your first article
5. Push to GitHub

### Update your availability badge

In `index.html`, find:

```html
<div class="hero-badge">Available for Opportunities</div>
```

Change it to `Currently Employed` or `Open to Consulting` etc. as needed.

---

## 📁 Folder Structure

```
portfolio/
├── index.html              ← Main portfolio (edit this)
├── README.md               ← This file
├── assets/
│   └── michael-george-resume.pdf   ← Add your PDF here
└── blog/
    ├── template.html       ← Copy this to create new articles
    └── my-article.html     ← Your actual articles go here
```

---

## 🌐 Custom Domain (optional, free)

If you want `www.michaelgeorge.dev` instead of `mycoola.github.io`:

1. Buy a domain from [Namecheap](https://namecheap.com) or [Cloudflare](https://cloudflare.com) (~$10/year)
2. In GitHub repo → Settings → Pages → Custom domain: enter your domain
3. In your domain registrar, add a CNAME record pointing to `mycoola.github.io`

---

## Tips

- **Mobile-friendly** — the site is fully responsive, looks great on phones
- **No server needed** — pure HTML, nothing to install or maintain
- **Fast** — no frameworks, loads instantly
- **Free forever** — GitHub Pages is free for public repos
