# mmsquared.ca

Plain HTML and one stylesheet. No build step, no framework. Every link is relative, so the folder works on any static host.

```
index.html        Home: intro, the Z/S/P strip, one exercise from the lessons, Now, links onward
teaching.html     Philosophy, practices, courses, materials
research.html     Areas, publications, background
projects.html     Interactive lessons + student-team projects
students.html     Working with me (for UTM students)
site.css          All styling (light and dark)
lessons/          The four interactive lessons and their hub
img/headshot.jpg  Portrait (281 px; replace with a larger original if you have one)
favicon.svg, CNAME
```

## Moving off Framer (GitHub Pages, about 15 minutes plus DNS time)

1. Create a public repository, e.g. `moassem89/mmsquared.ca`, and upload the contents of this folder to its root (keep `CNAME`).
2. Repository → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`. Under *Custom domain*, enter `www.mmsquared.ca` and save.
3. At the registrar where mmsquared.ca is registered (not Framer, unless you bought it through them), replace the Framer DNS records with:
   - `CNAME` record: `www` → `moassem89.github.io`
   - four `A` records for the bare domain `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
4. When GitHub shows the domain as verified, tick *Enforce HTTPS*.
5. Check the live site on a phone, then cancel the Framer site plan. Not before: the old site stays up until DNS switches.

## Editing later

Each page is readable HTML. To add a paper, copy an `<li>` in `research.html`. To change "Now", edit the three `<li>` in `index.html`. Update the "Updated October 2026" stamp in each footer when you do.

## Before going live

- Add your CV as `cv.pdf` and a link to it (header or footer), if you want one public.
- Email shown is mo.mahmoud@utoronto.ca, assembled by a two-line script so it is not in the page source as plain text.
- Confirm the 2026 teaching additions (CSC236 Fall 2026, CSC263 Summer 2026, CSC363 Winter 2026).
