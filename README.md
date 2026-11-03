# oval-coming-soon

The placeholder page for [oval.vote](https://oval.vote) until the real site exists. A single
static `index.html` with no build step.

## Deploying

The `Pages` workflow publishes the repository root to GitHub Pages on every push to `main`. For
the first deployment, set **Settings → Pages → Build and deployment → Source** to
**GitHub Actions**; after that, pushing is the whole release process.

To serve it at `oval.vote`, add the custom domain under the same settings page and point the
domain's DNS at GitHub Pages.

## Previewing

Open `index.html` in a browser, or serve the directory:

```sh
python3 -m http.server 8000
```
