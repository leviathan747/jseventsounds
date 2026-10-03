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

In the repository, go to **Settings → Pages** and set **Source** to
"Deploy from a branch", branch `main`, folder `/docs`. The site is then
served at `https://<github-user>.github.io/jseventsounds/`.

All paths in the site are relative, so it works both at that address and at
a custom domain.

## Adding a custom domain later

1. At the domain registrar, add DNS records:
    - For `www`: a `CNAME` record pointing to `<github-user>.github.io`.
    - For the apex domain: `A` records to `185.199.108.153`, `185.199.109.153`,
      `185.199.110.153`, and `185.199.111.153`.
1. In **Settings → Pages → Custom domain**, enter the domain and save.
   GitHub commits a `docs/CNAME` file for you.
1. Once the certificate is issued, check **Enforce HTTPS**.
