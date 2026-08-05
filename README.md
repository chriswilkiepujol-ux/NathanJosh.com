# nathanjosh.com

Media kit / brand partnership landing page for Josh & Nathan. Static single-page site — no build step needed.

## Files
- `index.html` — the whole site (HTML + CSS inline, Google Fonts loaded via CDN)

## Deploy: GitHub → Vercel

### 1. Push this to GitHub
```bash
cd nathanjosh-site
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/nathanjosh-site.git
git push -u origin main
```
(Create the empty repo first at github.com/new — name it whatever you like, e.g. `nathanjosh-site`, don't initialize it with a README so the push above doesn't conflict.)

### 2. Import into Vercel
1. Go to vercel.com → **Add New... → Project**
2. Import the GitHub repo you just pushed
3. Framework preset: **Other** (it's plain static HTML, no build command needed)
4. Deploy — Vercel gives you a `*.vercel.app` URL immediately

### 3. Point nathanjosh.com at it
1. In the Vercel project → **Settings → Domains** → add `nathanjosh.com` (and `www.nathanjosh.com` if you want both)
2. Vercel shows you DNS records to add at your domain registrar:
   - **Apex domain (nathanjosh.com):** A record → `76.76.21.21`
   - **www subdomain:** CNAME → `cname.vercel-dns.com`
3. Add those records in your registrar's DNS settings. Propagation is usually minutes, sometimes up to a few hours.

### Making future edits
Once this is connected, any push to `main` auto-deploys:
```bash
git add .
git commit -m "Update photos"
git push
```
Vercel picks it up and redeploys automatically — no manual redeploy step.

## What's still placeholder
- Content library photos/videos (currently styled color blocks)
- Stats (followers, engagement, demographics)
- Package pricing (`€[XXX]`)
- Instagram links point to real handles already; double check they're correct
