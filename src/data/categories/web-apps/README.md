# Web Apps — GitNexus Marketplace Category

This registry lists open-source Web Apps Node.js tools and apps that can be launched instantly in the browser via the GitNexus Marketplace.

## How to submit your app

1. **Bundle your app** using `npx gitnexus-bundler build -i server.js -f \"npm run build\" -s out`
2. **Host your bundle** on Cloudflare Pages (free, unlimited bandwidth — recommended)
3. **Open a PR** to this repo adding one entry to `registry.json`

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full guide.

## Registry format

All apps are listed in a single [registry.json](./registry.json). Each entry:

```json
{
  \"id\": \"your-app-slug\",
  \"name\": \"Your App Name\",
  \"description\": \"One-line description, max 160 chars\",
  \"author\": \"your-github-username\",
  \"repo\": \"https://github.com/you/your-repo\",
  \"bundleUrl\": \"https://your-project.pages.dev/your-app.cjs\",
  \"tags\": [\"tag1\", \"tag2\"],
  \"addedAt\": \"YYYY-MM-DD\"
}
```

## Registry limit

Soft cap: **500 apps per category**. Sub-categories will be created as needed.
