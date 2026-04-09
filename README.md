# HARDWARE.co — Static Site

Recovered and redesigned static version of hardware.co, originally a WordPress site.

## 🚀 Deploy to GitHub Pages

### Option A — Automated (recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Under *Source*, select **GitHub Actions**
4. The included workflow (`.github/workflows/deploy.yml`) handles the rest automatically on every push to `main`

### Option B — Manual (simplest)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Under *Source*, select **Deploy from a branch**
4. Choose `main` branch and `/ (root)` folder
5. Click Save — your site will be live at `https://<your-username>.github.io/<repo-name>/`

### Option C — Custom domain (hardware.co)

After GitHub Pages is enabled:

1. Go to **Settings → Pages → Custom domain**
2. Enter `hardware.co` and click Save
3. Add these DNS records at your domain registrar:

```
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     <your-username>.github.io
```

4. Wait for DNS propagation (up to 48h)
5. Tick **Enforce HTTPS** once the cert is issued

The `CNAME` file in this repo tells GitHub Pages which custom domain to use.

---

## 📁 Structure

```
hardware-co/
├── index.html          # Main page
├── CNAME               # Custom domain config
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions auto-deploy
└── README.md
```

## ✏️ Editing Content

Everything is in `index.html`. Key sections to update:

- **Batch number** — search for `Batch #7` and update
- **Email** — replace `apply@hardware.co` and `hello@hardware.co`
- **Stats** — the four numbers in `.stats-bar`
- **Program timeline** — the four `.timeline-item` blocks
- **Footer links** — replace `#` hrefs with real URLs

## 🎨 Customization

CSS variables at the top of `<style>`:

```css
--orange: #ff4d00;   /* Brand accent color */
--black: #0a0a0a;    /* Background */
--white: #f5f2ec;    /* Text */
```
