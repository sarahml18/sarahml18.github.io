# Sarah Livingston — Portfolio Website

Two-page portfolio site built with plain HTML and CSS. No frameworks, no build tools, no subscriptions.

---

## Files in this folder

| File | What it is |
|------|-----------|
| `index.html` | Homepage (hero, values, featured work, about, contact) |
| `work.html` | Full case studies page |
| `README.md` | This file |

**Files you'll add:**
| File | What it is |
|------|-----------|
| `sarah-hero.jpg` | Your main hero photo (tall portrait, min 800px wide) |
| `sarah-about.jpg` | Your secondary about photo |
| `sarah-livingston-resume.pdf` | Your resume (rename to match exactly) |
| `images/` | Folder for case study screenshots and project images |

---

## How to edit copy

Open `index.html` or `work.html` in any text editor (even Notepad works).

Look for the ALL-CAPS HTML comments — they mark every editable spot:
- `<!-- YOUR NAME -->` → your name
- `<!-- HERO HEADLINE -->` → main homepage headline
- `<!-- PROJECT TITLE -->` → case study title
- etc.

Change the text between the HTML tags, save the file, and push to GitHub.

---

## How to add your photos

1. Save your hero photo as `sarah-hero.jpg` in the same folder as `index.html`
2. Save your about photo as `sarah-about.jpg` in the same folder
3. The CSS already points to these filenames — no code changes needed
4. Once photos are added, delete the `<span class="hero-image-placeholder">` line inside each image div

For case study images:
1. Create an `images/` folder
2. Save images there (e.g. `images/voyage-cover.jpg`)
3. In `work.html`, find the placeholder div for that case study and replace it with:
   ```html
   <img src="images/voyage-cover.jpg" alt="Brief description of image" />
   ```

---

## How to add a new case study

**On work.html:**
1. Copy one of the `<article class="case-study">` blocks
2. Paste it before the `<!-- ADD MORE CASE STUDIES HERE -->` comment
3. Change the `id` to something unique (e.g. `id="new-project"`)
4. Update all the content inside

**On work.html (jump links):**
Add a new pill in the `<nav class="work-index">`:
```html
<a href="#new-project" class="index-pill">New Project Name</a>
```

**On index.html (featured work):**
Add a new card in the `.work-grid` section:
```html
<a href="work.html#new-project" class="work-card">
  <span class="work-tag">Your Tag</span>
  <div class="work-title">Your Project Title</div>
  <div class="work-desc">Short description of the project.</div>
  <span class="work-link">Read case study</span>
</a>
```
If you want only 4 featured on the homepage, remove one of the existing cards.

---

## How to change colours

All colours are CSS variables at the top of each file inside the `:root {}` block.
Change a hex value there and it updates everywhere on that page.

```css
:root {
  --cream:       #F5F7F2;  /* page background */
  --green-deep:  #3B6D11;  /* accent colour */
  --forest:      #1E2A1F;  /* dark sections + footer */
  /* etc. */
}
```

---

## GitHub Pages setup (how your site goes live)

1. Go to [github.com](https://github.com) and create a free account
2. Click **New repository** (top right, green button)
3. Name it exactly: `your-username.github.io` (replace with your actual GitHub username)
4. Set it to **Public**, then click **Create repository**
5. On the next screen, click **uploading an existing file**
6. Drag all files from this folder into the upload area
7. Click **Commit changes**
8. Go to **Settings → Pages** → under Source, select **Deploy from branch → main → / (root)**
9. Wait 2–3 minutes, then visit `https://your-username.github.io`

Your site is live. Every time you upload updated files, it republishes automatically.

---

## Custom domain (optional, ~$15/year)

1. Buy a domain from [Namecheap](https://namecheap.com) or [Squarespace Domains](https://domains.squarespace.com)
2. In GitHub → Settings → Pages → Custom domain, type your domain and save
3. In your domain registrar's DNS settings, add these A records:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
4. Wait up to 24 hours for DNS to propagate — then your domain points to GitHub Pages
