# BookSedonaTours.com — Owner's Manual

**Site:** Unique Sedona Experiences (booksedonatours.com)
**What this is:** A plain HTML/CSS website. No framework, no build step, no database, no proprietary platform. Every page is a file you can open in a browser. Anyone — you, a freelancer, or any AI — can edit these files with zero special tooling. That is deliberate: this site cannot be held hostage by any vendor or any assistant.

## The files
- `index.html` — homepage
- `jeep-tours.html`, `grand-canyon-tours.html`, `antelope-canyon-tours.html`, `vortex-tours.html`, `wine-tours.html`, `night-tours.html` — category pages
- `gift-cards.html` — gift card info page (checkout itself runs on the Base44 gift card app)
- `blog.html` + `blog/` — the Sedona Journal blog index and posts
- `tours/` — one page per tour (41 pages)
- `styles.css` — ALL design/styling for the whole site lives in this one file (colors are the variables at the top: --rust, --sand, --ink, etc.)
- `images/` — photos (Kendra's own Sedona photos)
- `sitemap.xml`, `robots.txt` — for Google; already point at booksedonatours.com

## How booking works
Every "Book This Tour" button links to Kendra's Viator partner shop:
`https://www.viator.com/partner-shop/visit-lancaster-pa/Sedona-Arizona`
That link carries her affiliate tracking. If Viator ever gives her per-product deep links, swap the `href` on individual tour pages' Book buttons — the link lives in exactly one place per page (search the file for "viator.com").

The phone number shown site-wide is (717) 925-0891. To change it, find-and-replace `+17179250891` and `(717) 925-0891` across all files.

## Common edits (any text editor, or ask any AI)
- **Change a price:** open the tour's page in `tours/`, find the `$` amount in the facts box, change it. Also change it on the category page card and homepage card if that tour appears there (search all files for the tour name).
- **Change tour text:** same file — the paragraphs under "About this tour."
- **Add a tour:** copy any file in `tours/`, rename it, replace its title, meta description, text, price and rating. Then add a card for it on its category page (copy an existing card block) and add its URL to `sitemap.xml`.
- **Add a blog post:** copy `blog/amitabha-stupa-sedona.html`, rename, replace content, add a card on `blog.html`, add the URL to `sitemap.xml`.
- **Change colors/fonts:** edit the variables and font lines at the top of `styles.css` — one place changes the whole site.

## How to put it online (one-time, ~15 minutes)
Recommended setup — everything in accounts YOU own:
1. **GitHub (free):** create an account at github.com if you don't have one. Create a new repository (e.g. `booksedonatours`) and upload this folder's contents (GitHub's web upload works — drag and drop).
2. **Hosting — pick one:**
   - **Cloudflare Pages (recommended, free):** cloudflare.com → Pages → Connect to Git → pick the repo → framework preset "None" → deploy. Then add the custom domain `booksedonatours.com` in the Pages project; Cloudflare walks you through the DNS step (easiest if the domain's DNS is also moved to Cloudflare — free).
   - **GitHub Pages (simplest, free):** in the repo, Settings → Pages → deploy from branch `main`. Add the custom domain there; at your registrar, point the domain's DNS to GitHub Pages (GitHub shows the exact records).
3. After it's live, any edit pushed to the GitHub repo republishes the site automatically in about a minute. You can edit files right in GitHub's web editor (pencil icon) — no software needed.
4. **Google Search Console:** search.google.com/search-console → add property for booksedonatours.com → verify (DNS TXT record) → submit `sitemap.xml`. This is how Google finds the pages.

## Registrar / DNS note
The domain booksedonatours.com was bought 2026-11-14 (registrar: wherever Kendra bought it — check the receipt email). The only DNS job is pointing the domain at the host chosen above. Nothing about the site files changes if you switch hosts later: download the repo, upload it anywhere, done.

## Gift cards
Checkout runs on a separate Base44 app ("Sedona Gift Cards") because payments need an app, not static files. Build spec: `base44-sedona-gift-cards-prompt.md` in this folder. The main site's `gift-cards.html` links to it. If Base44 ever goes away, any checkout tool (Stripe Payment Links are the simplest) can replace it — only the button link on `gift-cards.html` changes.

## The rule this site was built under
Kendra owns: the domain, the files, the hosting account, the Viator relationship, the gift card app. No assistant or platform sits in the middle. If you are an AI reading this to make an edit: make the edit in the files, keep the structure and tone consistent, update `sitemap.xml` if you add a page, and never move the site onto a proprietary builder.
