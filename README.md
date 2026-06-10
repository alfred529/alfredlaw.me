# Alfred Law — Portfolio

Black & white editorial portfolio for Senior/Lead Product Designer roles.
Built with vanilla HTML, CSS, and JS. Hosted on GitHub Pages.

---

## File Structure

```
portfolio/
├── index.html              ← Homepage (hero + work grid)
├── about.html              ← About page
├── style.css               ← Global design system
├── script.js               ← Nav, animations, scroll
├── CNAME                   ← Your custom domain (alfredlaw.me)
├── work/
│   ├── souschef.html       ← SousChef case study
│   ├── td-ec.html          ← TD case study
│   ├── bmo.html            ← BMO case study
│   ├── bgis.html           ← BGIS case study
│   └── letseat.html        ← LetsEat case study
└── assets/
    ├── images/
    │   ├── logo.png            ← Your AL logo (export from Squarespace)
    │   ├── alfred-photo.jpg    ← Your headshot
    │   ├── souschef-cover.png
    │   ├── souschef-research.png
    │   ├── souschef-audit.png
    │   ├── souschef-design-system.png
    │   ├── souschef-screens-1.png
    │   ├── souschef-screens-2.png
    │   ├── souschef-outcomes.png
    │   ├── souschef-learnings.png
    │   ├── td-cover.png
    │   ├── bmo-cover.png
    │   ├── bgis-cover.png
    │   └── letseat-cover.png
    └── alfred-law-resume.pdf
```

---

## Setup

### 1. Create GitHub repo

- Go to github.com → New repository
- Name it: `alfredlaw.me` (or `yourusername.github.io`)
- Set to Public
- Don't add README (you'll push your own)

### 2. Push your code

```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio build"
git branch -M main
git remote add origin https://github.com/yourusername/alfredlaw.me.git
git push -u origin main
```

### 3. Enable GitHub Pages

- Go to your repo → Settings → Pages
- Source: Deploy from branch → main → / (root)
- Save. Site will be live at https://yourusername.github.io/alfredlaw.me

### 4. Connect your custom domain

Add a file called `CNAME` (no extension) to your repo root:
```
alfredlaw.me
```

Then in your domain registrar (where you bought alfredlaw.me), update DNS:

**A Records** (point @ to GitHub):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record**:
```
www → yourusername.github.io
```

DNS changes take up to 48 hours. GitHub will auto-provision an SSL certificate.

---

## Adding images

1. Export all images from your Squarespace site (Settings → Advanced → Export, or screenshot the live pages)
2. For case study images: screenshot each section at 2x resolution from your existing site
3. Optimise images with squoosh.app (free, in-browser) — aim for <300kb per image
4. Drop into `/assets/images/` and push

---

## Adding remaining case studies

Use this template for each new case study. Ask Claude:

> "Create a case study HTML page for [Project Name] using the Alfred Law design system (black and white, Playfair Display headlines, DM Sans body). The file lives in /work/ and links back up to / for nav. Here's the content: [paste your case study content]"

---

## Deploying updates

```bash
git add .
git commit -m "Update: [what you changed]"
git push
```

GitHub Pages auto-deploys within ~60 seconds.
