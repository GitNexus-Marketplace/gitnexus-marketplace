# How to Submit Your App to This Category

## Step 1 — Bundle your app

```bash
npx gitnexus-bundler build -i server.js -f "npm run build" -s out
```

This produces `gitnexus-bundle.cjs` and `gitnexus.json` in your project directory.

## Step 2 — Host your bundle

Upload `gitnexus-bundle.cjs` to a public CDN. **Cloudflare Pages is strongly recommended** — it's free with unlimited bandwidth and has no rate limits.

```
pages.cloudflare.com → Create project → Upload assets
Drag your .cjs file → Deploy
URL: https://your-project.pages.dev/your-app.cjs
```

Do NOT use GitHub Releases as your primary CDN — it has a 1 GB/month bandwidth limit on free accounts.

## Step 3 — Open a PR

Fork this repo and add one entry to `registry.json`:

```json
{
  "id": "your-app-slug",
  "name": "Your App Name",
  "description": "What your app does in one sentence (max 160 chars)",
  "author": "your-github-username",
  "repo": "https://github.com/you/your-repo",
  "bundleUrl": "https://your-project.pages.dev/your-app.cjs",
  "tags": ["tag1", "tag2"],
  "addedAt": "YYYY-MM-DD"
}
```

Rules:
- `id` must be unique and lowercase with hyphens only
- `repo` must be a public GitHub repository
- `bundleUrl` must be a direct URL to a `.cjs` file on a public CDN
- `tags` maximum 5
- No duplicate submissions
- App must be open-source

## Requirements

- Your app must be **open-source** with a public GitHub repository
- Your bundle must be compatible with WebContainers (no native C++ modules)
- Your app must boot and respond on port 8080
- No malware, spam, or misleading apps

Maintainers will review your PR. There is no automated merge — all reviews are manual.
