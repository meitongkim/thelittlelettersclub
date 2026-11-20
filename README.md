# The Little Letters Club — website

Static website for The Little Letters Club (TLLC), Singapore. Plain HTML, CSS and JavaScript: no build step, no server code.

## Put it on GitHub Pages

1. Create a new GitHub repository (for example `tllc-website`).
2. Upload **everything inside this folder** to the repository root (drag the files into GitHub's "Add file → Upload files" page, or use `git push`). `index.html` must be at the top level.
3. In the repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.
5. Custom domain (`thelittlelettersclub.sg`): in **Settings → Pages → Custom domain**, enter the domain, then add the DNS records GitHub shows you at your domain registrar. Tick **Enforce HTTPS** once it is available.

It also works on Netlify, Vercel or Cloudflare Pages: point them at this folder, no build command.

To preview locally: run `python3 -m http.server` in this folder and open http://localhost:8000 (opening the files directly with `file://` will not load the pages).

## What's in here

| Path | What it is |
|---|---|
| `index.html` | Home |
| `about.html`, `team.html`, profile pages (`meitong.html`, `kym.html`, `lynn.html`, `harman.html`, `laks.html`, `kafia.html`) | About and team |
| `programmes.html`, `event.html`, `collection.html`, `gallery.html`, `journal.html`, `article.html` | Our work and stories |
| `volunteer.html`, `getinvolved.html`, `exco.html`, `community.html`, `supportus.html`, `opportunities.html`, `remote.html`, `creators.html` | Getting involved |
| `chapters.html`, `india.html` | Chapters |
| `letterbox.html`, `letterpreview.html` | The Little Letterbox (drafts are saved only in the visitor's own browser) |
| `contact.html`, `support.html`, `404.html` | Contact, FAQ & policies, not-found page |
| `tokens.css`, `site.css`, `letterbox.css`, `ds/` | Styles |
| `assets/` | All images (TLLC artwork, mascots, stickers) |
| `js/tllc-runtime.js` | Small page renderer used by every page |
| `js/preact.min.js` | Preact 10 (MIT licence, see `js/PREACT-LICENSE.txt`) |

Each page's text and layout lives inside that page's HTML file, in the `<script type="application/x-tllc-template">` blocks (layout) and the `TLLC.define(...)` blocks (data such as programme lists, team members, postbox notes and gallery items).

## Before launch: things that are honest placeholders

- **Forms do not send anything yet.** Contact, volunteer interest, EXCO application, partnership and newsletter forms show a clear "prototype, nothing was sent" message. Connect each to a form service or your backend before relying on them.
- **No logins or database.** Private areas (HQ, the volunteer console, the Little Creator dashboard) are not included in this site.
- **Gallery:** no real photographs are published yet; the frames are labelled illustrations. Add real photos only after publication approval and media consent are recorded.
- **Little Postbox:** the first notes are kindness prompts drafted for TLLC review. Edit, add or remove them in `index.html` (search for `POSTBOX`).
- Confirm consent for every person on the Team and profile pages, and confirm the Instagram handle, before going public.

Generated from the TLLC Claude Design canvas.
