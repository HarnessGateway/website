# website

The HarnessGateway landing page: what the open-source platform is, the professional services around it, the three
demos, how to self-host, and the waitlist for the hosted version.

It is one static page with no build step. Everything published is in `site/`:

| File | What it is |
|---|---|
| `site/index.html` | the page |
| `site/styles.css` | its styles: the console's palette (off-white paper, orange for action, navy for headings) |
| `site/assets/` | the mascot, the three demo recordings and their preview stills, the social preview image |

## Preview it

```bash
python3 -m http.server --directory site 8080     # http://localhost:8080
```

## Publish it

A push to `main` runs `.github/workflows/pages.yml`, which uploads `site/` to GitHub Pages. The repository's Pages
source is **GitHub Actions**. The custom domain is set under Settings → Pages; all links in the page are relative, so
it also works at `https://harnessgateway.github.io/website/`.

## Change the contact address

"Talk to us", "Join the waitlist" and "Contact" are `mailto:` links to one address. Search `site/index.html` for
`mailto:` to change it.
