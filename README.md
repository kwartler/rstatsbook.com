# rstatsbook.com

Book site for **Ted Kwartler's** practical R titles: *Text Mining in Practice with R*, *Sports Analytics in Practice with R*, and *Applied Sport Business Analytics*, plus datasets and course links.

Static site, no build step. Hosted on **GitHub Pages** with the custom domain `www.rstatsbook.com`.

## Structure

```
index.html          Main page (Books / Text Mining / Sports / Data / About)
404.html            Custom not-found page
assets/style.css    Design system + all styling (R-blue theme)
assets/favicon.svg  Site icon (R monogram)
assets/og-image.png Social-share preview image (1200x630)
CNAME               Custom domain (www.rstatsbook.com)
robots.txt / sitemap.xml / .nojekyll
```

## SEO built in

- `Book` structured data (JSON-LD `ItemList`) so search engines understand the titles and author
- Open Graph + Twitter Card tags with a branded preview image
- Canonical URL, meta description, keywords, `robots.txt`, `sitemap.xml`
- Cross-links to [tedkwartler.com](https://tedkwartler.com/), Amazon, and GitHub

> Note: the dataset/code links currently point to `github.com/kwartler`. Update them to the exact companion repositories when ready (search `index.html` for `github.com/kwartler`).

## Deploy to GitHub Pages

1. Repo is pushed to `github.com/kwartler/rstatsbook.com`.
2. **Settings -> Pages** -> Source: **Deploy from a branch**, Branch: **`main` / root**, Save.
3. `CNAME` sets the domain to `www.rstatsbook.com`.

## DNS setup

Because the site uses the `www` subdomain, add one **CNAME record**:

```
CNAME   www   kwartler.github.io
```

To also serve the apex `rstatsbook.com` (redirecting to www), add the four GitHub Pages A records to `@`:

```
A   @   185.199.108.153
A   @   185.199.109.153
A   @   185.199.110.153
A   @   185.199.111.153
```

Enable **Enforce HTTPS** in Settings -> Pages once the certificate is issued.
