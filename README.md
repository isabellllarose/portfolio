# Isabella Heath — Portfolio Site
## Advanced Diploma of Building Design (Architectural) — 22627VIC · Holmesglen

---

## File structure

```
portfolio-site/
├── index.html          ← Main portfolio (hero, about, all projects, contact)
├── qualifications.html ← Course page with unit codes + academic project detail
├── style.css           ← Shared styles — colours, fonts, layout all live here
└── README.md           ← This file
```

All three files need to be in the same folder for the links between them to work.

---

## Things still to personalise

### index.html
- LinkedIn URL — find `linkedin.com/in/yourname` and replace with your real URL
- The "Interested in" and "Open to" panels in the hero right column — update if you want
- The About section paragraphs — currently written in a general voice, rewrite in your own words

### qualifications.html
- The image placeholder divs — replace with your actual drawings, renders or photos (see below)

### style.css
- No changes needed unless you want to adjust colours (see colour reference at the bottom of this file)

---

## How to add a project to the main page (index.html)

Find `<!-- PLACEHOLDER -->` near the bottom of the projects grid and paste a new card directly above it:

```html
<a class="project-card"
   href="qualifications.html#proj-your-anchor"
   data-category="residential academic">
  <div class="card-top">
    <div class="card-badges">
      <span class="badge badge-type">Residential</span>
      <span class="badge badge-academic">Academic</span>
    </div>
    <span class="card-year">2025</span>
  </div>
  <h3 class="card-title">Project Name</h3>
  <p class="card-desc">Short description — two sentences max.</p>
  <div class="card-tags">
    <span class="tag">Tag 1</span>
    <span class="tag">Tag 2</span>
  </div>
  <span class="card-arrow">↗</span>
</a>
```

**data-category options** (combine with a space): `residential` `commercial` `documentation` `analysis` `academic`

**Badge colour options:**
- `badge-academic` → blue (course work)
- `badge-personal` → green (self-initiated)
- `badge-professional` → amber (paid / work experience)
- `badge-type` → neutral grey (the project type label)

---

## How to add the matching project detail to qualifications.html

Find the last project section and paste this block after it (before the closing `</div>` of the section-wrap):

```html
<hr class="proj-divider">

<div class="proj-section" id="proj-your-anchor">
  <a href="index.html#work" class="back-link">← Back to all work</a>
  <div class="proj-intro-header">
    <span class="badge badge-type">Residential</span>
    <span class="badge badge-academic">Academic</span>
  </div>
  <h2 class="proj-section-title">Project Name</h2>
  <div class="proj-detail">
    <div class="proj-body">
      <div class="img-placeholder">
        <div class="img-placeholder-text">Add your drawings or renders here</div>
      </div>
      <p>First paragraph about the project.</p>
      <p>Second paragraph — process, thinking, what you learnt.</p>
      <h4 style="font-family:'DM Serif Display',serif; font-size:1.1rem; margin: 1.75rem 0 0.75rem;">Key outcomes</h4>
      <ul class="outcomes-list">
        <li>Outcome one</li>
        <li>Outcome two</li>
      </ul>
    </div>
    <div class="proj-sidebar">
      <div class="proj-sidebar-row">
        <div class="proj-sidebar-label">Year</div>
        <div class="proj-sidebar-value">2025</div>
      </div>
      <div class="proj-sidebar-row">
        <div class="proj-sidebar-label">Type</div>
        <div class="proj-sidebar-value">Residential — Class 1</div>
      </div>
      <div class="proj-sidebar-row">
        <div class="proj-sidebar-label">Deliverables</div>
        <div class="proj-sidebar-value">Floor plan · Elevations · Sections</div>
      </div>
      <div class="proj-sidebar-row">
        <div class="proj-sidebar-label">Tags</div>
        <div class="proj-tags-row">
          <span class="tag">Tag 1</span>
          <span class="tag">Tag 2</span>
        </div>
      </div>
    </div>
  </div>
</div>
```

The `id="proj-your-anchor"` must match the `href` in the index card exactly.

---

## How to add real images

Replace any `<div class="img-placeholder">` block with a standard image tag:

```html
<img src="images/beach-house-floorplan.jpg"
     alt="Beach House floor plan"
     style="width:100%; display:block; margin-bottom:1.5rem;">
```

Create an `images/` folder inside your portfolio-site folder and put your image files in there. JPG or PNG both work fine. Keep file names lowercase with hyphens, no spaces.

---

## How to host for free on GitHub Pages

1. Go to github.com — create a free account
2. Click the + icon → New repository → name it `portfolio` → set to Public → Create
3. Click "uploading an existing file" and drag in all four files (index.html, qualifications.html, style.css, README.md) plus your images folder if you have one
4. Click Commit changes
5. Go to Settings → Pages → under Source, select "Deploy from a branch" → Branch: main → Save
6. Wait 1–2 minutes → your site is live at `isabellaheath.github.io/portfolio`

To update the site later: go to your repository on GitHub, click the file you want to edit or re-upload, make the change, commit. Live within a minute.

---

## Colour reference

Edit these values in `style.css` to change the look of the whole site:

| Variable | Current value | Used for |
|---|---|---|
| `--bg` | #F6F5F2 | Page background |
| `--bg-card` | #FFFFFF | Cards and panels |
| `--bg-dark` | #181816 | Contact section |
| `--text-primary` | #1A1A18 | Headings, main text |
| `--text-secondary` | #555550 | Body paragraphs |
| `--text-muted` | #9A9A94 | Labels, captions |
| `--accent` | #3B5B8C | Blue — links, badges, hover states |
| `--accent-light` | #EBF0F7 | Light blue fills |
| `--accent-warm` | #B85C2A | Terracotta — available for future use |

To change the accent colour sitewide, update `--accent` and `--accent-light` in `style.css`.
