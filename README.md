# Carpenter Street Neighbors & Friends

A simple static website for our block of Carpenter Street, Philadelphia. It replaces the old Google Sites page.

## What's here

- `index.html` — the whole site (news, events, resources, contact)
- `styles.css` — styling (light and dark mode)

No build step, no frameworks. Open `index.html` in a browser to preview.

## Updating the site

- **News post:** copy an `<article class="card">` block in the News section and edit it. Newest first.
- **Event:** copy an `<li>` in the Upcoming section.
- Anything in `[brackets]` is a placeholder still to fill in.

Then commit and push (or edit files directly on github.com):

```bash
git add .
git commit -m "Add October block update"
git push
```

## Hosting

Hosted on GitHub Pages at **carpenterstreetphilly.com** (set in the `CNAME` file).

1. On GitHub: repo **Settings → Pages → Deploy from branch → `main` / root**. Custom domain: `carpenterstreetphilly.com`. Tick **Enforce HTTPS** once it's available.
2. In GoDaddy DNS for **carpenterstreetphilly.com**:
   - Delete any existing `A` record for `@` (GoDaddy's parked page).
   - Add four `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record: `www` → `carpenter-street-friends.github.io`
3. In GoDaddy for **carpenterstphilly.com**: **Forwarding → Add forwarding**, permanent (301), to `https://carpenterstreetphilly.com`.

DNS can take up to a few hours to update.
