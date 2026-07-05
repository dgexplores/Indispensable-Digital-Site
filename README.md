# Indispensable Digital — Website

Multi-page marketing site built with [Astro](https://astro.build). Fully static output — fast, SEO-friendly, and free to host.

## Pages

| URL | File |
|---|---|
| `/` | `src/pages/index.astro` (Home) |
| `/services/` | `src/pages/services.astro` |
| `/approach/` | `src/pages/approach.astro` |
| `/work/` | `src/pages/work.astro` |
| `/about/` | `src/pages/about.astro` |
| `/contact/` | `src/pages/contact.astro` |
| `404` | `src/pages/404.astro` |

Shared pieces live in `src/layouts/BaseLayout.astro` (SEO head, Organization JSON-LD) and `src/components/` (Header, Footer, CtaSection, ServicesGrid). Site-wide styles: `src/styles/global.css`.

## Commands

```bash
npm install        # once
npm run dev        # local dev server at http://localhost:4321
npm run build      # production build into dist/
npm run preview    # preview the production build
```

## SEO built in

- Unique `<title>` + meta description per page
- Canonical URLs, Open Graph and Twitter Card tags
- `sitemap-index.xml` auto-generated on build (`@astrojs/sitemap`)
- `robots.txt`, semantic HTML, JSON-LD Organization schema
- Zero client-side rendering — pure HTML, so crawlers see everything

**Before going live:** the site URL is set to `https://www.indispensabledigital.com` in `astro.config.mjs` — update it if the domain changes. Add `public/founder.jpg` (about page photo) and optionally `public/og-image.jpg` (1200×630 social share image).

## Deploy for free

### Cloudflare Pages (recommended)
1. Push this folder to a GitHub repository.
2. In the Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**.
3. Framework preset: **Astro**. Build command `npm run build`, output directory `dist`.
4. Add your custom domain under the project's **Custom domains** tab.

### Netlify / Vercel
Same flow — connect the GitHub repo, both auto-detect Astro. Build command `npm run build`, publish directory `dist`.
