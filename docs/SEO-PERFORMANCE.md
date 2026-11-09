# SEO & Performance

Single-page apps are fast to use but, by default, invisible to search engines and link
previews: every URL returns the same empty HTML. This is how the platform avoids that.

## Server-rendered `<head>` for a client-rendered app

For every page URL the server returns the SPA shell with a page-specific head:

| Signal | Source |
|---|---|
| `<title>`, meta description | The record's SEO fields, falling back to its summary and then its body |
| Canonical URL | Fixed site origin + path, never query strings |
| Robots | `index` for public content; `noindex` for account, cart, search and admin areas |
| Open Graph / Twitter cards | Title, description, image, type (`article` for news) |
| Structured data (JSON-LD) | `Organization`, `WebSite` + `SearchAction`, `Service`, `NewsArticle`, `JobPosting`, `Person`, `Book`, `BreadcrumbList` |
| HTTP status | `200` for real pages, `404` for unknown or unpublished slugs (no "soft 404s") |

Only published content is ever described, using the same visibility rules as the public API.
After the first load, the React app keeps these tags in sync as the user navigates.

`robots.txt` and `sitemap.xml` are generated from live data. Public API endpoints stay
crawlable, because search engines render the app and need its data.

## Performance

- **Code splitting:** the admin console, customer area, rich-text editor and PDF reader are
  separate chunks loaded on demand, so public pages ship only what they render.
- **Caching:** content-hashed assets are cached for a year (`immutable`); HTML always
  revalidates so deployments take effect immediately; rendered heads are cached server-side
  and invalidated on each frontend deployment.
- **Stateless public HTML:** page responses set no cookies, so they stay cacheable.
- **PWA:** the service worker precaches only the small app shell, caches JavaScript on first
  use, and serves public content network-first with an offline fallback.
- **Compression:** gzip/brotli for text assets.

## Measuring

Search Console and Bing Webmaster Tools (sitemap submitted), Rich Results Test for structured
data, and Lighthouse / Core Web Vitals for performance.
