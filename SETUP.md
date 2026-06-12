# PackAndWild — GitHub Pages + Ionos Domain Setup

## STEP 1 — Create the GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **+** → **New repository**
3. Name it exactly: `packandwild.de`
4. Set to **Public** (required for free GitHub Pages)
5. Leave all checkboxes empty
6. Click **Create repository**

---

## STEP 2 — Upload the Site Files

### Option A — via GitHub web interface (no Git required)

1. Open your repo at `https://github.com/YOURNAME/packandwild.de`
2. Click **Add file** → **Upload files**
3. Drag in `index.html` — click **Commit changes**
4. Create the hiking folder:
   - Click **Add file** → **Create new file**
   - Type `hiking/index.html` as the filename (GitHub creates the folder automatically)
   - Paste the contents of your `hiking/index.html`
   - Click **Commit changes**

### Option B — via Git CLI (faster for many files)

```bash
git clone https://github.com/YOURNAME/packandwild.de.git
# Copy your files into the cloned folder
cp index.html packandwild.de/
mkdir packandwild.de/hiking
cp hiking/index.html packandwild.de/hiking/
cd packandwild.de
git add .
git commit -m "Initial site"
git push
```

---

## STEP 3 — Enable GitHub Pages

1. In your repo, go to **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main` — Folder: `/ (root)`
4. Click **Save**
5. Wait ~1 minute — GitHub will show:
   > "Your site is live at `https://YOURNAME.github.io/packandwild.de/`"

**Test it** at that URL before connecting your domain.

---

## STEP 4 — Connect packandwild.de via Ionos DNS

### 4a — Add your custom domain in GitHub

1. Go to **Settings** → **Pages**
2. Under **Custom domain**, type: `packandwild.de`
3. Click **Save**
4. GitHub will create a `CNAME` file in your repo — leave it there

### 4b — Configure DNS records in Ionos

Log in to Ionos → **Domains & SSL** → Click `packandwild.de` → **DNS**

**Delete** any existing A records or CNAME for the root domain (`@`), then add:

| Type  | Host | Value               | TTL  |
|-------|------|---------------------|------|
| A     | @    | 185.199.108.153     | 3600 |
| A     | @    | 185.199.109.153     | 3600 |
| A     | @    | 185.199.110.153     | 3600 |
| A     | @    | 185.199.111.153     | 3600 |
| CNAME | www  | YOURNAME.github.io. | 3600 |

> Replace `YOURNAME` with your actual GitHub username.

**DNS propagation takes 15 minutes to 48 hours.** Usually under 1 hour with Ionos.

---

## STEP 5 — Enable HTTPS / SSL

1. Once your domain resolves (you can access `packandwild.de` in browser):
2. Go back to GitHub → **Settings** → **Pages**
3. Check **Enforce HTTPS** (the checkbox becomes available once DNS is verified)
4. GitHub provides the SSL certificate automatically via Let's Encrypt — free, auto-renews

---

## STEP 6 — Verify Everything

Check these URLs all work and redirect correctly:

- [ ] `https://packandwild.de` — loads homepage
- [ ] `https://www.packandwild.de` — redirects to non-www
- [ ] `https://packandwild.de/hiking/` — loads hiking category page
- [ ] `http://packandwild.de` — auto-redirects to https

---

## Folder Structure Reference

```
packandwild.de/               ← GitHub repo root
├── index.html                ← Homepage (EN)
├── CNAME                     ← Auto-created by GitHub (don't delete)
├── hiking/
│   └── index.html
├── vanlife/
│   └── index.html            ← Build next
├── camping/
│   └── index.html
├── edc/
│   └── index.html
├── travel/
│   └── index.html
├── home/
│   └── index.html
├── about/
│   └── index.html
├── de/
│   └── index.html            ← German homepage
└── de/
    ├── wandern/
    │   └── index.html
    └── ... (other DE pages)
```

---

## After Deploy — Checklist

- [ ] Update AWIN profile: add `https://packandwild.de` as your site URL
- [ ] Connect Pinterest profile to `packandwild.de`
- [ ] Replace all `href="#"` placeholder affiliate links with real AWIN deep links
- [ ] Build remaining 5 category pages (vanlife, camping, edc, travel, home)
- [ ] Add German homepage at `/de/index.html`
- [ ] Add Impressum page at `/imprint/` (required by German law)
- [ ] Add Datenschutzerklärung at `/privacy/` (required by GDPR)
- [ ] Submit sitemap to Google Search Console
