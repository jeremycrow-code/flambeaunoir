# Flambeau Noir archive site

Static files for flambeaunoir.org. Same network chrome as JeremyCrow.com and LuciferianResearch.org (Playfair Display + Roboto, crimson `#990000`, light/dark toggle, shared top nav). Flambeau Noir adds a second row of archive links.

## Publish

Replace the current repo contents with this folder (keep your repo’s `.git`).

```bash
# from your existing flambeau noir repo
cp -R /path/to/flambeaunoir-site/* .
git add -A
git commit -m "Archive rebuild"
git push
```

Vercel: root directory = repo root, output = none (static). Point the domain at the deployment.

`www.flambeaunoir.org` did not resolve at build time; the apex `flambeaunoir.org` did. Add a `www` CNAME to the Vercel host if you want both.

## What this does not change

JeremyCrow.com and LuciferianResearch.org stay their own repos and CSS files. Only the Conference item in their nav needs to keep pointing at https://flambeaunoir.org/. No shared stylesheet required.

## After you ship

- Add a contact email on `contact.html` if you want mail to land off JeremyCrow.com.
- Drop poster scans into an `/images` folder and link them from `art.html`.
- Expand 2012 / 2014 speaker lists when programmes turn up.
