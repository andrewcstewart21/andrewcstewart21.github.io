# Your Name — Portfolio Site

A clean, single-page portfolio built with plain HTML/CSS/JS — no build tools,
no npm install, nothing to compile. Just edit the text and push.

## What's here

```
index.html      → all page content (edit this first)
css/style.css   → all styling and color/font choices
js/script.js    → small scroll animations
assets/         → put your resume.pdf and any images here
```

## 1. Edit your content

Open `index.html` in any text editor. Search for anything wrapped in
`[brackets]` or styled in italics — those are placeholders for you to
replace:

- Your name (appears in the `<title>`, hero, nav initials, footer)
- Email, LinkedIn, GitHub links
- Thesis title and one-line summary
- 2–3 project cards (delete any you don't need, or copy the pattern to add more)
- Education details

Drop your résumé PDF into `assets/resume.pdf` — the "Résumé" link in the
sidebar already points there.

### Adding writing samples / course reports

Each non-thesis project card has a "Read the report →" link at the bottom.
These already point to specific filenames inside `assets/reports/`:

| Project card              | Expected file                                  |
|----------------------------|------------------------------------------------|
| Slip Recovery Training     | `assets/reports/slip-recovery-report.pdf`       |
| Lower-Limb Exoskeleton     | `assets/reports/exoskeleton-report.pdf`         |
| XR Object Manipulation     | `assets/reports/xr-object-manipulation-report.pdf` |

Just drop your PDFs into `assets/reports/` using those exact filenames and
the links will work immediately — no HTML editing needed.

If you'd rather use your own filenames, open `index.html`, find the
`<a href="assets/reports/...">Read the report →</a>` line under the
project you want to change, and update the path to match your file.

Want to link to something other than a PDF (a Google Doc, a live demo,
a GitHub repo)? Just replace that same `href` value with the URL.

### Adding your photo

Right now the sidebar shows your initials in a circle instead of a photo.
To use a real photo:
1. Add an image file to `assets/` (e.g. `assets/photo.jpg`).
2. In `index.html`, find this block near the top of the sidebar:
   ```html
   <div class="avatar" aria-hidden="true">
     <span class="avatar-initials">YN</span>
   </div>
   ```
3. Replace the `<span>` line with:
   ```html
   <img src="assets/photo.jpg" alt="Your Name">
   ```

## 2. Preview it locally (optional)

Just double-click `index.html` — it'll open in your browser. No server needed.

## 3. Put it on GitHub Pages

1. Create a new repository on GitHub. If you want your site at
   `https://yourusername.github.io`, name the repo exactly
   `yourusername.github.io`. Otherwise, name it whatever you like (e.g.
   `portfolio`) — it'll be published at `https://yourusername.github.io/portfolio`.

2. Push these files to that repository. Easiest way, using GitHub's website:
   - Click **Add file → Upload files** on your new repo's page.
   - Drag in `index.html`, the `css` folder, the `js` folder, and `assets`.
   - Commit the changes.

   Or, if you're using the command line:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/yourusername/your-repo-name.git
   git push -u origin main
   ```

3. Turn on GitHub Pages:
   - Go to your repo → **Settings → Pages**.
   - Under "Build and deployment", set **Source** to "Deploy from a branch".
   - Set **Branch** to `main` and folder to `/ (root)`.
   - Click **Save**.

4. Wait about a minute, then refresh the Pages settings page — it'll show
   your live URL at the top (something like
   `https://yourusername.github.io/your-repo-name/`).

## Making changes later

Edit any file, commit, and push — GitHub Pages redeploys automatically
within a minute or two. No other steps needed.

## Customizing further

- **Colors/fonts**: all defined at the top of `css/style.css` under
  `:root { ... }` — change the hex values there and they'll update everywhere.
- **Adding a project**: copy one `<article class="project">...</article>`
  block in `index.html` and paste it inside `.project-grid`.
- **Removing the scroll animation**: delete the `<script src="js/script.js">`
  line in `index.html`.
