# J&S Event Sounds Website

Static one-page site for J&S Event Sounds, hosted on GitHub Pages.

## Layout

- `docs/` is the published site (`index.html`, `styles.css`, `favicon.svg`, `assets/`).
- `sources/` holds the original artwork and flyer. It is not published.

## Preview locally

```sh
cd docs
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## GitHub Pages settings

The site publishes from branch `main`, folder `/docs`, at the custom domain
<https://jseventsounds.com>. The domain is stored in `docs/CNAME`; don't
delete that file.

## DNS (GoDaddy)

| Type | Name | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `leviathan747.github.io` |

After DNS resolves, check **Enforce HTTPS** in **Settings → Pages**.

## SEO files

- `docs/robots.txt` and `docs/sitemap.xml` point at the custom domain.
  Update `<lastmod>` in the sitemap when the page content changes.
- `docs/index.html` has canonical, Open Graph, and schema.org
  `EntertainmentBusiness` data in its `<head>`. Keep the phone numbers,
  email, and prices there in sync with the visible page.
