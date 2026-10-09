# BuddyBridge Static Site

A complete static rebuild of the BuddyBridge website (youth nonprofit helping neurotypical kids understand, include, and stand up for neurodivergent peers). Ready to deploy to **GitHub Pages**.

## File tree

```
buddybridge-site/
├── index.html            # Home
├── video-series.html     # Video Series (8 episodes)
├── volunteer.html        # Volunteer + embedded Google Form
├── events.html           # Events
├── how-to-help.html      # How to Help
├── faq.html              # FAQ (17 questions)
├── about-us.html         # About Us (founder story + kindness note)
├── mission-impact.html   # Our Mission & Impact (stats + impact)
├── partnerships.html     # Partnerships (FCSN)
├── advocacy.html         # Advocacy (video toolkit for schools)
├── contact.html          # Contact
├── laws-reference.html   # Laws & Reference (+ legislation history)
├── styles.css            # Navy/gold brand stylesheet
├── assets/
│   ├── daniel-sean-badminton.png   # Founders photo (About Us)
│   └── fcsn-logo.png               # FCSN partner logo
└── README.md
```

All internal links are relative, so the site works both locally (`open index.html`) and on GitHub Pages (including project subpaths like `username.github.io/buddybridge/`).

## Deploy to GitHub Pages

### 1. Create the repository
- On GitHub, create a new repository (e.g. `buddybridge`).
- Do **not** initialize with a README (we already have one).

### 2. Push the site
```bash
cd ~/workspace/buddybridge-site
git init
git add .
git commit -m "BuddyBridge static site"
git branch -M main
git remote add origin https://github.com/<YOUR-USERNAME>/buddybridge.git
git push -u origin main
```
(Replace `<YOUR-USERNAME>` with the GitHub username. If using SSH, use the SSH remote URL instead.)

### 3. Enable GitHub Pages
- Go to the repo on GitHub → **Settings** → **Pages**.
- Under "Build and deployment", set **Source** to **Deploy from a branch**.
- Set **Branch** to `main` and folder to `/ (root)`. Click **Save**.
- After ~1 minute the site is live at `https://<YOUR-USERNAME>.github.io/buddybridge/`.

### 4. (Optional) Custom domain
- In Settings → Pages, add the custom domain under "Custom domain" and follow GitHub's DNS instructions (A records or CNAME).
- The site uses relative links, so it works unchanged under a custom domain.

## Notes
- The Volunteer page embeds the live Google Form via iframe — no backend needed.
- The Contact page form is intentionally non-functional (static site): it shows a friendly "being connected" notice on submit. Wire it to a real endpoint (e.g. Formspree) when an inbox is chosen.
- Content was replicated from the live Weebly site (buddybridge.weebly.com) in October 2026, with the approved overrides: corrected "Watch the Video Series" link, new About Us copy, Partnerships/FCSN content, Advocacy page, and the legislation-history section.
