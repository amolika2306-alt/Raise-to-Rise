# Raise to Rise Foundation — Website

A single-page static site for the Raise to Rise Foundation (Hyderabad).
No build step, no dependencies — just `index.html` and `logo.png`.

## Files
- `index.html` — the entire site (HTML + CSS + JS inline)
- `logo.png` — the foundation logo, referenced by index.html

## Run locally
Open `index.html` in a browser, or:
```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (pick one)
**Netlify (drag & drop):** go to https://app.netlify.com/drop and drop this folder.

**GitHub Pages:**
```bash
git init && git add . && git commit -m "Raise to Rise site"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
# then enable Pages in repo Settings -> Pages -> deploy from main / root
```

**Cloudflare Pages / Vercel:** connect the repo, framework preset = "None",
build command = none, output directory = `/` (root).

## Customising
Open `index.html` and look for:
- `var GOAL=10000, RAISED=840;`  — update the fundraising numbers (near bottom, in <script>)
- the "Sample drive receipt" block — replace with real drive data
- the three `.card` blocks under "What we do" — edit drive descriptions
- mailto: links — replace with a real UPI / Razorpay / payment link once registered
- the "Registration in progress" pill in the footer — remove once registered

## TODO before going live
- [ ] Register the foundation (Trust / Society / Section 8) + bank account
- [ ] Replace mailto buttons with a real donation/payment link
- [ ] Add real drive photos
- [ ] Set a custom domain
