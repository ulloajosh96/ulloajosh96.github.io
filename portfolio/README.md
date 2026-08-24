# Joshua Ulloa — Portfolio Site

No build tools, no dependencies to install. Free to host.

## File structure

```
index.html              the main page (hero, project cards, about, contact)
style.css                all the styling, shared by every page
images/                  put your result screenshots, plots, and renders here
projects/
  _template.html          copy this to start a brand new project detail page
  rocket-engine.html       detail page for each project, linked from index.html
  europa-plasma.html
  laser-thermal-ml.html
  neutron-star.html
  cosmology.html
  iceman.html
```

## Get it online for free (GitHub Pages)

1. Create a free GitHub account if you don't have one: https://github.com/join
2. Create a new repository. Two options:
   - Name it exactly `[your-username].github.io` (e.g. `ulloajosh96.github.io`), this gives you a clean URL like `https://ulloajosh96.github.io`
   - Or name it anything else (e.g. `portfolio`), your URL will be `https://[username].github.io/portfolio`
3. Upload the whole folder (`index.html`, `style.css`, the `images` folder, and the `projects` folder) to the repository. On the GitHub website, drag the entire folder contents into the upload area, GitHub preserves the folder structure automatically.
4. Go to the repo's **Settings** tab → **Pages** (left sidebar) → under "Build and deployment," set Source to **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
5. Wait 1 to 2 minutes, then visit the URL GitHub gives you. That's it, it's live and free forever.

Alternative if you'd rather not use GitHub at all: go to https://app.netlify.com/drop and drag the whole folder onto the page. It gives you a live URL in seconds, also free.

## How to add result images to a project

1. Save your image (a plot, screenshot, or CAD render) into the `images` folder. Keep the filename simple, no spaces, e.g. `mass-radius-curves.png`.
2. Open the matching file in `projects/` (e.g. `projects/neutron-star.html`).
3. Find the `<div class="gallery">` block under **Results**. Delete the `gallery-placeholder` div and replace it with:
   ```html
   <div class="gallery-item">
     <img src="../images/mass-radius-curves.png" alt="Describe the image here">
     <div class="caption">A short caption explaining what this shows</div>
   </div>
   ```
4. You can add more than one `gallery-item` block if you have multiple images.
5. Save, and re-upload (or edit directly on GitHub, see below).

## How to add a code snippet to a project

1. Open the matching file in `projects/`.
2. Find the `<div class="code-block">` under **Code Highlight**.
3. Replace the placeholder comment with your actual code, keep it short, 10 to 20 lines that show the interesting part, not the whole file.

## How to link to your full code on GitHub

1. Put your actual project code in its own GitHub repository (or one repo with a folder per project).
2. Open the matching file in `projects/`, find the commented-out line near the top that looks like:
   ```html
   <!-- <a class="btn primary" href="#" target="_blank" rel="noopener">View code on GitHub</a> -->
   ```
3. Delete the `<!--` and `-->` around it, and replace the `#` with your repo's URL.

## How to add a brand new project

1. Copy `projects/_template.html`, rename it to something like `projects/new-project.html`.
2. Edit the title, summary, and overview text inside.
3. Go to `index.html`, find the `PROJECT CARD TEMPLATE` comment inside `<section id="projects">`, copy one whole `<div class="card">...</div>` block, paste it, and edit the text and tags.
4. In that new card, change the "Full writeup" link's `href` to `projects/new-project.html`.
5. Save both files and re-upload, or edit directly on GitHub (see below).

## How to update anything after it's already live

Everything can be edited right in the browser, no re-uploading needed:
1. Go to your repository on GitHub, click the file you want to change.
2. Click the pencil (edit) icon in the top right of the file view.
3. Make your changes, scroll down, click **Commit changes**.
4. The live site updates automatically within a minute or two.

## Notes

- No build step, no npm, no server. Static files only, works identically wherever you host it.
- If you want a custom domain later (e.g. `joshuaulloa.com`) instead of the free `.github.io` URL, that costs roughly $10 to $15 a year through a registrar like Namecheap or Cloudflare, entirely optional.
