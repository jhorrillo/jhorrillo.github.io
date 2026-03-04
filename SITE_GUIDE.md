# jhorrillo.github.io — Site Guide

## Overview
Personal academic website for Jordan Horrillo, hosted via GitHub Pages.

- **Live URL**: https://jhorrillo.github.io/
- **GitHub repo**: https://github.com/jhorrillo/jhorrillo.github.io
- **Local directory**: `~/jhorrillo.github.io/`
- **Technology**: Static HTML + CSS (no frameworks, no build step)

## File Structure

```
~/jhorrillo.github.io/
├── index.html          # Landing page (bio, affiliation, contact)
├── research.html       # Research page (books, papers, maps)
├── cv.html             # CV page (PDF embed + download link)
├── style.css           # All styling for the site
├── cv_Jordan_Horrillo.pdf  # CV PDF file
└── SITE_GUIDE.md       # This file
```

## How to Make Changes

### 1. Edit files locally
All files are in `~/jhorrillo.github.io/`. Edit the HTML/CSS directly.

### 2. Preview locally
```bash
open ~/jhorrillo.github.io/index.html
```

### 3. Push to GitHub
```bash
cd ~/jhorrillo.github.io
git add <changed files>
git commit -m "Description of change"
git push
```
Changes go live within 1-2 minutes after pushing.

## Common Tasks

### Add an SSRN link to the Labor Day Fires paper
In `research.html`, find the Labor Day Fires entry (currently has a comment placeholder) and add:
```html
<p class="links">
    <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=XXXXXXX">SSRN</a>
</p>
```

### Add a new working paper
In `research.html`, add a new `<div class="paper">` block inside the Working Papers section:
```html
<div class="paper">
    <h3>Paper Title Here</h3>
    <p class="authors">Author Names</p>
    <p class="links">
        <a href="URL">SSRN</a>
    </p>
</div>
```

### Add a new publication
Same as above but inside the Publications `<div class="section">`, and include a venue line:
```html
<div class="paper">
    <h3>Paper Title</h3>
    <p class="authors">Author Names</p>
    <p class="venue">Journal Name, Volume(Issue): Pages, Year</p>
    <p class="links">
        <a href="https://doi.org/DOI_HERE">Paper</a>
    </p>
</div>
```

### Add a new interactive map or GitHub Pages project
Add inside the Interactive Maps section in `research.html`:
```html
<div class="paper">
    <h3>Map Title</h3>
    <p class="links">
        <a href="https://jhorrillo.github.io/repo-name/">View Map</a>
    </p>
</div>
```

### Add a new page to the site
1. Create `newpage.html` using the same structure as the other pages (copy `cv.html` as a template — it has the nav and footer)
2. Add a nav link in ALL html files:
```html
<li><a href="newpage.html">Page Name</a></li>
```
3. Set `class="active"` on the nav link in the new page itself

### Update the CV
1. Replace `cv_Jordan_Horrillo.pdf` with the new version (same filename)
2. Push to GitHub

### Update the bio
Edit the `<div class="bio">` section in `index.html`.

## Design Notes

- **Accent color**: Stanford cardinal `#8c1515` (used for links, heading underlines, CV download button)
- **Font**: Georgia / Times New Roman serif stack
- **Layout**: Max-width 780px, centered
- **Nav**: Sticky top bar with site name left, page links right
- **Research page**: Papers grouped by section (Book Manuscripts, Working Papers, Publications, Interactive Maps) with condensed spacing
- **Responsive**: Mobile-friendly at 600px breakpoint

## Related Resources

- **CV source file**: Located in Dropbox at `/Users/jordanhorrillo/Haber Research Group Dropbox/Haber Research/fires/cv_Jordan_Horrillo.pdf`
- **Labor Day Fires paper source (.qmd)**: `/Users/jordanhorrillo/Haber Research Group Dropbox/Haber Research/fires/LaborDayFires/Horrillo_labor_day_fires.qmd`
- **GitHub account**: jhorrillo
- **Existing GitHub Pages projects**: `potential-markets-map`, `umpqua-maps-video`
