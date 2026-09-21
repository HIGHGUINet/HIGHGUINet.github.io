# HIGHGUINet.github.io

Guisik Kim's personal homepage. Built with Jekyll + GitHub Actions — pushing to `main`
automatically builds and deploys to `https://highguinet.github.io`.

## Adding a publication or award (auto-deployed)

1. Put the PDF (or image) file in `paper/<year>/`.
2. Add an entry to the relevant file: `_data/publications.yml` (`type: journal` or
   `conference`), `_data/awards.yml` (awards), `_data/patents.yml` (patents), or
   `_data/news.yml` (news).
3. `git add -A`, `git commit`, `git push` — GitHub Actions builds and deploys
   automatically (takes 1-2 minutes).

## One-time setup

1. Create a new public GitHub repo named `HIGHGUINet/HIGHGUINet.github.io`.
2. Locally:
   ```
   git remote add origin https://github.com/HIGHGUINet/HIGHGUINet.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. In the repo's Settings → Pages → Build and deployment → Source, select **GitHub Actions**.
4. Check `https://highguinet.github.io` after a moment.

## Local preview (optional, requires Ruby)

```
bundle install
bundle exec jekyll serve
```

## TODO

- Once the ICIP 2026 Grand Challenge paper (`ICIP_2026_Grand_Challenge_Paper_GUISIK_KIM_camera_ready.pdf`)
  is officially published, add the `pdf` field in `_data/publications.yml` and remove it from
  `.gitignore` (title/authors are already filled in)
- Once the ACCV 2026 paper (`418_Interference_Gated_Continu.pdf`, "Interference-Gated Continual
  Learning for Deepfake Detection") is officially published: fill in the real author list in
  `_data/publications.yml` (currently TODO — the source PDF is an anonymous submission copy),
  add the `pdf` field, and remove it from `.gitignore`
- Swap the profile photo (`figures/me.png`) for a different one if desired
- Fill in patent numbers in `_data/patents.yml` (US/EP/JP, and the missing KOR ones)

## PDF publishing policy

The following PDFs are kept out of the public repo (listed in `.gitignore`; the local copy
stays in `paper/`):
- Papers in subscription journals (IEEE TIP, T-ITS, GRSL, MTAP, IET Computer Vision, etc.)
- Papers not yet officially published (ICIP 2026 Grand Challenge, ACCV 2026)

Open-access journals (IEEE Access, Sensors/MDPI, etc.) and already-published
conference/workshop papers have their PDFs published as usual.

A cropped teaser figure (`image:` field) is fine to publish even when the `pdf` field is
withheld — it's a small preview, not full paper distribution.
