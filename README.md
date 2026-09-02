# Erika & Hilde

Evidence-led static website prototype for Erika & Hilde, Weigandufer 9, Berlin-Neukölln.

## Live site

https://prithiraj.github.io/erika-hilde/

Published with GitHub Pages from `main` via `.github/workflows/pages.yml`.

## Files

- `DESIGN_PLAN.md` — evidence baseline, design rationale, rights notes and acceptance criteria.
- `index.html` — German primary page.
- `en/index.html` — English mirror.
- `assets/styles.css` — mobile-first editorial styling; no framework.
- `impressum.html` / `datenschutz.html` — minimal factual drafts for review.

## Run locally

Any static file server works, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/`.

## Production blockers

1. Replace all images labelled **Demo image** with owner-controlled or commercially licensed photography.
2. Confirm opening hours: current Google/local listing says 16:00–01:00 daily; the legacy official site still says daily from 15:00.
3. Replace the evidence-only offer section with the current owner-confirmed menu/offer if desired.
4. Have Impressum/Datenschutz reviewed against the actual production hosting and services.
5. Add an owner-controlled Open Graph image after photography is available.

No JavaScript, analytics, WebGL/Three.js or external font dependency is required.
