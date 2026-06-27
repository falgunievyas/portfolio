# Falguni Vyas — Personal Portfolio

A 6-page personal brand site built around a "ledger / passbook" visual theme — fitting for a banking & employability trainer. Pure HTML/CSS/JS, no build step, ready for GitHub Pages.

## Pages
- `index.html` — Home
- `about.html` — About / Story
- `programs.html` — Training Programs
- `services.html` — Services & Pricing
- `testimonials.html` — Testimonials (placeholder grid, see below)
- `contact.html` — Contact form

## Before you publish — 3 things to finish

### 1. Add your real photo
Replace `assets/img/falguni-portrait.jpg` with your actual photo.
- Keep the filename the same (or update the `src` in `index.html`'s hero section if you rename it)
- Recommended: a portrait-orientation photo (roughly 4:5 ratio) works best with the layout

### 2. Add your testimonial screenshots
1. Drop your screenshot images into `assets/img/testimonials/` (e.g. `testimonial-01.jpg`, `testimonial-02.jpg`, etc.)
2. Open `testimonials.html`
3. Each placeholder block currently looks like this:
   ```html
   <div class="testi-placeholder">Screenshot 01<br>Drop image in<br>assets/img/testimonials/</div>
   ```
4. Replace it with:
   ```html
   <div class="testi-card">
     <img src="assets/img/testimonials/testimonial-01.jpg" alt="Student feedback">
     <div class="cap">Shared by a student</div>
   </div>
   ```
5. There are 12 placeholder slots ready — add more `testi-card` blocks or remove unused ones if you have fewer/more than 12.

### 3. Connect your contact form
1. Go to [formspree.io](https://formspree.io) and sign up for a free account
2. Create a new form — you'll get an endpoint URL like `https://formspree.io/f/abc12345`
3. Open `contact.html`, find this line:
   ```html
   <form class="form-block" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
4. Replace `YOUR_FORM_ID` with your real ID from Formspree.
5. Formspree's free plan has a monthly submission limit — check their site for current limits.

## Editing content
All text content is directly inside the HTML files — no CMS, no database. To edit anything (program descriptions, pricing, bio text), open the relevant `.html` file in any text editor and change the text between the tags.

- **Pricing**: search `service-row` blocks in `services.html`
- **Programs**: search `card` blocks in `programs.html` and the preview section in `index.html`
- **Bio/story**: `about.html`
- **Stats (students trained, etc.)**: `ledger-row` blocks in `index.html`

## Deploying to GitHub Pages
1. Create a new GitHub repository (e.g. `falguni-portfolio`)
2. Upload all files in this folder to the repository (keep the folder structure — `assets/` must stay alongside the `.html` files)
3. Go to your repo's **Settings → Pages**
4. Under "Source," select the `main` branch and `/ (root)` folder
5. Save — GitHub will give you a live URL, usually `https://yourusername.github.io/falguni-portfolio/`
6. It can take a few minutes to go live the first time

## Notes
- The site is fully responsive (mobile, tablet, desktop) and works without JavaScript except for the mobile menu toggle.
- All social links in the footer point to: LinkedIn (@falguni-vyas), Instagram (@falgunievyas), YouTube (@falgunivyas-neurogpt) — update these in all 6 files if they ever change (search for `footer-socials`).
- Fonts (Fraunces, Work Sans, JetBrains Mono) load from Google Fonts via CDN — requires internet connection to display correctly, which is standard for any live website.
