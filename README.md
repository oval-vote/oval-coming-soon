# oval-coming-soon

The placeholder page for [oval.vote](https://oval.vote) until the real site exists: one
`index.html` styled with the Oval design system from
[`@oval-vote/brand`](https://www.npmjs.com/package/@oval-vote/brand).

## Developing

Tooling is managed with [mise](https://mise.jdx.dev), which reads `.node-version`.

```sh
npm ci
npm run build      # copies index.html and the brand package's tokens, components, and logo into dist/
npm run preview    # builds, then serves dist/ at http://localhost:8000
npm run check      # formatting and the build; CI runs this
```

Updating the design system is a version bump of `@oval-vote/brand`.

## Deploying

Every push to `main` that passes `npm run check` deploys `dist/` to GitHub Pages. For the first
deployment, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**; after
that, pushing is the whole release process.

To serve it at `oval.vote`, add the custom domain under the same settings page and point the
domain's DNS at GitHub Pages.
