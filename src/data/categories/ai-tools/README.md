# AI Tools — GitNexus Marketplace Category

This registry lists open-source AI-powered Node.js tools and apps that can be launched instantly in the browser via the GitNexus Marketplace.

## How to submit your app

1. **Bundle your app** using `npx gitnexus-bundler build -i server.js -f "npm run build" -s out`
2. **Host your bundle** on Cloudflare Pages (free, unlimited bandwidth — recommended) or any public CDN
3. **Open a PR** to this repo adding one entry to `registry.json`

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full submission guide.

## Registry format

All apps are listed in a single [`registry.json`](./registry.json) file. Each entry follows this structure:

```json
{
  "id": "your-app-slug",
  "name": "Your App Name",
  "description": "One-line description, max 160 chars",
  "author": "your-github-username",
  "repo": "https://github.com/you/your-repo",
  "bundleUrl": "https://your-project.pages.dev/your-app.cjs",
  "tags": ["ai", "openai"],
  "addedAt": "2026-03-04"
}
```

## Registry limit

This category has a **soft cap of 500 apps**. When we approach that limit, a sub-category will be created.
