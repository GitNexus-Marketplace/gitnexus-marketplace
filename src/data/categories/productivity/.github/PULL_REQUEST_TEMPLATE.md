## App Submission Checklist

Before a maintainer can merge your PR, please confirm the following:

- [ ] I have added exactly **one entry** to `registry.json` — not a separate folder or file
- [ ] My `id` is unique, lowercase, and uses hyphens only (e.g. `my-ai-tool`)
- [ ] My `repo` points to a **public GitHub repository**
- [ ] My `bundleUrl` points to a working `.cjs` file hosted on a public CDN
- [ ] My bundle was built with `gitnexus-bundler` and runs on port 8080
- [ ] My app does **not** use native C++ modules (bcrypt, sqlite3, canvas, etc.)
- [ ] My app is open-source and free to use
- [ ] My description is 160 characters or less

**App description (1-2 sentences):**
...

**Link to repository:**
https://github.com/...

**Bundle CDN URL:**
https://...
