# vacti-profile

The public profile site for **VACTI**, an autonomous AI penetration testing platform.

It is a single, static, zero-build HTML page that explains how VACTI works and why it is
built the way it is: a Debian or Kali engine that enrolls to a self-hosted control plane,
runs an agent swarm behind deterministic probers and confirmation oracles, and writes back
verifiable, evidence-grade findings.

## What is in here

```text
index.html                     the whole page (hero, how it works, capabilities,
                               advantages, architecture, open source, footer)
styles.css                     the white + blue design system
assets/logo.svg                VACTI shield + radar wordmark logo
assets/icon.svg                square app / favicon mark
.github/workflows/deploy.yml   GitHub Pages deploy on push to main
.nojekyll                      tells GitHub Pages to serve files as-is
```

There is no build step and no runtime dependency. Fonts (Inter and JetBrains Mono) are the
only external request, loaded from Google Fonts.

## Run it locally

Any static file server works. For example:

```bash
# Python (no install)
python3 -m http.server 8080

# or Node
npx serve .
```

Then open <http://localhost:8080>.

## Deploy

The site is plain static files, so it hosts anywhere.

### GitHub Pages (included)

A workflow at `.github/workflows/deploy.yml` publishes the site on every push to `main`.
After the first push:

1. Open the repository **Settings -> Pages**.
2. Set **Source** to **GitHub Actions**.
3. Push to `main`. The site deploys to `https://<owner>.github.io/<repo>/`.

The `.nojekyll` file keeps Pages from reprocessing the output.

### Cloudflare Pages / Netlify

Point the provider at this repository and leave the build command empty:

- **Build command:** (none)
- **Output directory:** `/` (the repository root)

## Customize

- **Colors:** the design tokens live at the top of `styles.css` under `:root`
  (navy `#0A3D62`, blue `#2563EB`, off-white `#F7F9FC`). Change them in one place.
- **Copy:** all text is in `index.html`, grouped by section with clear comments.
- **Logo:** swap `assets/logo.svg` and `assets/icon.svg`. Both are plain SVG.
- **Links:** repository URLs live in the Open source section and the nav.

## License

MIT. See [LICENSE](LICENSE).

Only ever run VACTI against targets you are authorized to test.
