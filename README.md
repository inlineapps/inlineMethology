# Methodology research deck

Research material for team review. Goal: find a suitable method to **rank features** and **define metrics** that we can apply to the whole company.

22 HTML pages, no JavaScript, no external dependencies — works offline, works on GitHub Pages, works inside a zip.

Entry point: **`index.html`**

## Publishing to GitHub Pages

```bash
# from /Users/jasonc/Develop/ops/publish
cd /Users/jasonc/Develop/ops/publish
git init
git add .
git commit -m "Methodology research deck"
git branch -M main

# Create a new public repo on github.com (e.g. "methodology-research")
# then:
git remote add origin git@github.com:<your-username>/<repo-name>.git
git push -u origin main
```

Then on github.com:

1. Go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: **main** · folder: **/ (root)** · Save
4. Wait ~30–60s. URL appears at the top: `https://<your-username>.github.io/<repo-name>/`

Share that URL. Default landing is `index.html`. All cross-page links are relative, so they Just Work.

## Local preview

```bash
cd /Users/jasonc/Develop/ops/publish
python3 -m http.server 8000
# open http://localhost:8000/
```

## What's in here

- `index.html` — landing with goal statement + map of all pages
- `impact-saas-companies.html` — Study A: 10 top SaaS/B2B companies
- `impact-consumer-companies.html` — Study B: 10 top consumer-tech companies
- `methodologies-comparison.html` — 19-method side-by-side table
- `experiment-trustworthiness.html` — Deep-dive on how high-volume A/B testing actually works
- 17 method deep-dives (one per framework): RICE, North Star, Microsoft ExP/CUPED, LinkedIn T-REX, Netflix ABlaze, Booking, Airbnb ERF, Uber XP, DoorDash switchback, Lyft, Pinterest, V2MOM, Pyramid of Clarity, PR-FAQ, HEART, DIBB, Stripe shaping

All sources linked inline; caveats on sourcing called out where second-party (Spotify DIBB, Stripe footnotes).
