# Tinker Tribe — starter site

A plain HTML/CSS/JS site. No build step, no database, no framework —
just three files (`index.html`, `styles.css`, `script.js`) you can edit
directly and deploy for free on GitHub Pages.

## 1. Put it on GitHub

1. Create a GitHub account if you don't have one: https://github.com/join
2. Create a new repository.
   - If this will be your *main* site (e.g. for `yourname.github.io`), name
     the repo exactly `<your-github-username>.github.io`.
   - Otherwise any name works (e.g. `tinker-tribe-site`) — it'll just live at
     `yourusername.github.io/tinker-tribe-site/` unless you add a custom
     domain (step 3).
3. Upload `index.html`, `styles.css` and `script.js` to the root of that
   repo (GitHub's web UI has an "Add file → Upload files" button — no
   command line needed).

## 2. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` (or `master`) and folder to `/ (root)`. Save.
4. Wait 1–2 minutes. GitHub will show you a live URL like
   `https://yourusername.github.io/tinker-tribe-site/`.

That's it — the site is live and free.

## 3. Add your own domain (optional, ~₹700–1000/year)

1. Buy a domain from any registrar (Namecheap, Porkbun, BigRock, GoDaddy).
   Check the **renewal price**, not just the first-year price, before buying.
2. In your repo, add a new file at the root named exactly `CNAME`
   (no extension) containing just your domain, e.g.:
   ```
   tinkertribe.in
   ```
3. In **Settings → Pages**, enter the same domain under "Custom domain" and
   save. GitHub will show a DNS check.
4. At your domain registrar, add these DNS records (exact values GitHub
   publishes here: https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site):
   - For an apex domain (`tinkertribe.in`): four `A` records pointing to
     GitHub's IP addresses.
   - For a `www` subdomain: a `CNAME` record pointing to
     `yourusername.github.io`.
5. DNS can take anywhere from a few minutes to ~24 hours to propagate.
   Once it does, tick "Enforce HTTPS" in the Pages settings.

## 4. Editing content

Everything visible is plain text inside `index.html` — section by section,
in the same order it appears on the page (hero, topics, workshops, gallery,
join). No templating, so you can just open the file and edit text directly.

Things to replace before you consider it "live":
- `https://instagram.com` in the Join section → your real Instagram profile
  link.
- `mailto:hello@example.com` → your real contact email.
- The "Upcoming batches" note under Workshops → real dates once confirmed,
  or swap in an embedded Google Form / Tally form for bookings.
- The four `.gallery-block` divs → real photos once you have them from a
  workshop (replace the `<div>` with an `<img>` tag, same class names will
  keep the layout).
- If you decide to tweak the name further (e.g. add "the" or change
  casing), do a find-and-replace for "Tinker Tribe" across `index.html`,
  `styles.css` comments, and the `<title>`/meta tags.

## 5. When you outgrow static

The "team formation" feature (kids posting project ideas and finding
teammates) will need a backend + database — this static setup intentionally
doesn't include one yet. When you're ready, Supabase or Firebase (both have
free tiers) are a reasonable next step, added alongside this same static
front end rather than replacing it.

## 6. Knowledge library (`learn/`)

- `learn/index.html` — the searchable library page (topic filters + search box)
- `learn/*.html` — online lessons (robot car wiring, electronics, motors, aeromodeling, micro RC plane)
- `learn/files/` — printable PDF guides (space, maths, English, birds)
- `learn/diagrams/` — diagrams used inside the lessons

To add a new PDF guide: put it in `learn/files/`, then copy one of the
"Printable guide" cards in `learn/index.html` and change its link, title,
description and `data-cat` / `cat-…` topic.

Keep the photo credits printed inside the bird guides — those photos are
Creative Commons licensed and the licence requires the credit line.
