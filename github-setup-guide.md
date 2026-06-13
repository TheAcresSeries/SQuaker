# GitHub Website Setup Guide
## The Acres Series — Shane Michael Quaker

---

## What You're Building

A single-page website (`index.html`) that matches your hand-drawn wireframe:

```
┌─────────────────────────────────────────────────────┐
│        THE ACRES SERIES                             │
│        ~ A Mindtraveler in a Modern World ~         │
├──────────┬──────────────────────────┬───────────────┤
│  ACRES   │  ACRES SYNOPSIS          │  ACRES STATS  │
│  Cover   │  Full plot description   │  Pages/Words  │
│          │  + Chapter List          │  Buy Button   │
├──────────┼──────────────────────────┼───────────────┤
│  SCAR    │  SCAR SYNOPSIS           │  SCAR STATS   │
│  Cover   │  Full plot description   │  Pages/Words  │
│          │  + Chapter List          │  Buy Button   │
├──────────┼──────────────────────────┼───────────────┤
│  ARC     │  ARC SYNOPSIS            │  ARC STATS    │
│  Cover   │  Full plot description   │  Pages/Words  │
│          │  + Chapter List          │  Buy Button   │
├──────────┴──────────────────────────┴───────────────┤
│  NEXT VIDEO DROPS  │  AUTHOR  │  CONTACT            │
│  NEXT - ARTHUR 2040           │  ART                │
└─────────────────────────────────────────────────────┘
```

All of this is built into the `index.html` file provided.

---

## Files You Need

Before starting, make sure you have these files in one folder on your computer:

```
acres-series/
├── index.html          ← PROVIDED — the complete website
├── acres-cover.jpg     ← PROVIDED — Acres book cover image
├── scar-cover.jpg      ← PROVIDED — Scar book cover image
├── arc-cover.jpg       ← PROVIDED — Arc book cover image
└── author-photo.jpg    ← ADD THIS — your author photo (optional)
```

---

## PHASE 1 — Create Your GitHub Account

**Step 1: Sign up for GitHub**
1. Go to **https://github.com** in your browser.
2. Click the green **Sign up** button.
3. Enter your email address.
4. Create a password (write it down somewhere safe).
5. Choose a username — suggestion: `acres-series` or `shanequaker` or `shanemichaelquaker`.
6. Complete the verification puzzle.
7. Click **Create account**.
8. GitHub sends a confirmation email — open it and click **Verify email address**.

---

## PHASE 2 — Create the Repository

A "repository" is the folder on GitHub that holds all your website files.

**Step 2: Create a new repository**
1. Once logged in, click the **+** icon in the top-right corner of the page.
2. Select **New repository** from the dropdown.
3. Fill in the fields:
   - **Repository name:** `acres-series`
   - **Description:** `Official website for The Acres Series by Shane Michael Quaker`
   - **Visibility:** Select **Public** (required for free hosting)
   - Check the box: **Add a README file**
4. Click the green **Create repository** button.

You now have an empty repository at:
`https://github.com/YOURUSERNAME/acres-series`

---

## PHASE 3 — Enable GitHub Pages (Free Hosting)

**Step 3: Turn on GitHub Pages**
1. Inside your repository, click the **Settings** tab (gear icon, top of the page).
2. In the left sidebar, scroll down and click **Pages**.
3. Under **Source**, click the dropdown that says **None** and select **main**.
4. The folder should stay as `/ (root)`.
5. Click **Save**.
6. GitHub shows a message: *"Your site is ready to be published."*
7. After 1–2 minutes, your site will be live at:
   `https://YOURUSERNAME.github.io/acres-series/`

---

## PHASE 4 — Upload Your Files

**Step 4: Upload index.html and the cover images**

Option A — Upload through the GitHub website (easiest, no software needed):
1. Go to your repository page on GitHub.
2. Click **Add file** → **Upload files**.
3. Drag and drop all of these files into the upload box:
   - `index.html`
   - `acres-cover.jpg`
   - `scar-cover.jpg`
   - `arc-cover.jpg`
   - `author-photo.jpg` (if you have one)
4. Scroll down to the **Commit changes** section.
5. In the first text box, type: `Add website files`
6. Click the green **Commit changes** button.
7. Wait 1–3 minutes, then visit your GitHub Pages URL to see the live site.

Option B — Upload using Git on your computer (for ongoing updates):
```bash
# Install Git from https://git-scm.com if you haven't already

# 1. Clone your repository to your computer
git clone https://github.com/YOURUSERNAME/acres-series.git

# 2. Copy your website files into the acres-series folder

# 3. Navigate into the folder
cd acres-series

# 4. Stage all files
git add .

# 5. Commit with a description
git commit -m "Add website files"

# 6. Push to GitHub
git push origin main
```

---

## PHASE 5 — Personalize the Website

After uploading, open `index.html` in any text editor (Notepad on Windows, TextEdit on Mac) and find these sections to update:

**1. Update your author bio** — find this line and replace the placeholder text:
```
Shane's writing is rooted in a love of American history...
```
Replace with your real bio.

**2. Add your contact information** — find these lines and update:
```html
<a href="mailto:your@email.com">your@email.com</a>
<a href="#">@theacresseries</a>
```
Replace with your real email and social media handles.

**3. Add "Where to Buy" links** — find the three buy buttons:
```html
<a href="#contact" class="buy-btn">Where to Buy</a>
```
Replace `#contact` with the actual Amazon/Barnes & Noble URL once the books are listed.

**4. Add your author photo** — find this line:
```html
<div class="author-avatar">SQ</div>
```
Replace with:
```html
<img src="author-photo.jpg" alt="Shane Michael Quaker" class="author-avatar">
```
Then upload `author-photo.jpg` to your repository.

**5. Add video embeds when ready** — find the video placeholder cards:
```html
<div class="video-card">Acres — Trailer Coming Soon</div>
```
Replace with a YouTube embed:
```html
<iframe width="100%" height="100%" src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
  frameborder="0" allowfullscreen style="border-radius:4px;"></iframe>
```

After any edit: save the file, re-upload it to GitHub (repeat Step 4), and the live site updates within a minute.

---

## PHASE 6 — Optional: Custom Domain

If you want the site to be at `www.theacresseries.com` instead of `github.io`:

1. Purchase a domain from Namecheap, GoDaddy, or Google Domains (~$12/year).
2. In your domain registrar's DNS settings, add a **CNAME record**:
   - Name: `www`
   - Value: `YOURUSERNAME.github.io`
3. In GitHub → Settings → Pages, enter your custom domain (e.g. `www.theacresseries.com`).
4. Check **Enforce HTTPS**.
5. Wait up to 24 hours for the domain to propagate.

---

## PHASE 7 — Launch Checklist

Before sharing the link publicly, verify:

- [ ] All three book covers load correctly
- [ ] All three synopses display
- [ ] Chapter lists expand and collapse when clicked
- [ ] Book stats (pages, chapters, words) are visible
- [ ] Navigation bar links scroll to the right sections
- [ ] Author section has real bio text
- [ ] Contact section has real email / social links
- [ ] "Next Book — Arthur 2040" section is visible
- [ ] Site looks good on your phone (test in mobile browser)
- [ ] Footer shows correct copyright year

---

## Your Final File Structure on GitHub

```
acres-series/               ← Your GitHub repository
├── index.html              ← The complete one-page website
├── acres-cover.jpg         ← Acres cover (Book 1)
├── scar-cover.jpg          ← Scar cover (Book 2)
├── arc-cover.jpg           ← Arc cover (Book 3)
├── author-photo.jpg        ← Your author photo
└── README.md               ← Auto-created by GitHub
```

---

## Your Live URL

Once complete, your site is live and shareable at:

**`https://YOURUSERNAME.github.io/acres-series/`**

Add this link to:
- Your Amazon Author Central page
- Your Goodreads author profile
- Instagram / TikTok bio
- Email signature
- Any press releases or promotional materials

---

*Guide prepared for The Acres Series — Acres, Scar, Arc — by Shane Michael Quaker.*
