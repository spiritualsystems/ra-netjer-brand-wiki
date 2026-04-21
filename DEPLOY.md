# Deployment & Hidden-URL Hosting

This wiki is **public but unlisted** — hosted on GitHub, accessible only through a long, obscure URL that is shared privately with contributors, VAs, and LLMs.

The goal is practical obscurity, not cryptographic secrecy:
- Anyone with the link can read the wiki (by design).
- The link itself is hard to guess.
- The repo is not advertised, indexed, or linked from public sites.

This "secret garden" pattern is enough for the wiki's purpose (sharing brand context with collaborators) without the friction of real authentication.

---

## Option A — Public GitHub repo with obscure name (recommended, simplest)

GitHub renders markdown natively. Contributors and LLMs read the wiki directly on github.com.

### Steps

1. **Generate a long random slug for the repo name.** A 20–40 char slug with mixed case, digits, and separators is fine. Example:
   ```
   rn-brand-wiki-7k3jH9pQx2vN8mR4
   ```
   You can use: `openssl rand -base64 18 | tr -dc 'A-Za-z0-9' | head -c 24`

2. **Create the GitHub repo as public** under your preferred account / org:
   ```
   https://github.com/<owner>/rn-brand-wiki-7k3jH9pQx2vN8mR4
   ```

3. **Push this directory to the repo.** See the "First push" section below.

4. **Do not link to the repo** from any public site, social profile, or indexed page. Do not add topics/tags. Don't mention the URL in GitHub discussions or issues in other repos.

5. **Share the URL privately** with contributors, VAs, and LLM prompts as needed.

### Why this works

- Search engines don't reliably index public GitHub repos by URL alone without inbound links. A never-linked repo with a high-entropy name is effectively unlisted.
- Every file renders as readable markdown on github.com. No hosting, no build step, no DNS required.
- Updates are a normal `git push`.

### Caveats

- The URL is **not** a secret. Anyone who obtains it can read the wiki. Treat it like an unlisted Google Doc: share privately, don't commit anything you'd be embarrassed by if the link leaked.
- If a contributor is careless and shares the URL in a public forum, search engines may eventually index it. Rotate to a new obscure repo if that happens.
- GitHub's default search does index repo names. The high-entropy slug defeats keyword discovery.

---

## Option B — GitHub Pages with a long random subdomain path

For a prettier reading experience (rendered HTML, navigation), add GitHub Pages.

### Steps

1. Set up Option A first (the public repo).
2. In the repo's Settings → Pages, enable GitHub Pages from the `main` branch at `/` root.
3. The site will be served at:
   ```
   https://<owner>.github.io/rn-brand-wiki-7k3jH9pQx2vN8mR4/
   ```
   The long repo slug becomes the long URL path.
4. Optionally add a minimal Jekyll theme (`_config.yml` with `theme: jekyll-theme-minimal`) — nothing more is required.
5. GitHub Pages sites can be indexed by search engines. To reduce discoverability, add a `robots.txt` at the repo root:
   ```
   User-agent: *
   Disallow: /
   ```

### Caveat

GitHub Pages URLs are cheap to guess by brute-forcing common repo names. The entropy of the slug matters more than it does with plain github.com browsing.

---

## Option C — Netlify / Cloudflare Pages with a long random subdomain

For full control over the URL and headers:

1. Connect the repo to Netlify (or Cloudflare Pages).
2. Set the site name to a long random slug so the URL becomes something like `https://rn-wiki-8fK2p9xQ.netlify.app/`.
3. Add a `netlify.toml` that serves markdown-as-HTML, or pre-render with a simple static site generator (Astro, 11ty, MkDocs).
4. Add a `_headers` file:
   ```
   /*
     X-Robots-Tag: noindex, nofollow
   ```
5. Add `robots.txt`:
   ```
   User-agent: *
   Disallow: /
   ```

---

## First push

From this directory:

```bash
git init
git add .
git commit -m "Initial public brand wiki"
git branch -M main

# replace <owner> and the slug with your own values
git remote add origin https://github.com/<owner>/rn-brand-wiki-<long-random-slug>.git
git push -u origin main
```

From here on, edits work like any other git repo: edit, commit, push.

---

## Rotating to a new URL

If a URL leaks or you want to rotate:

1. Create a new repo with a fresh high-entropy slug.
2. Push the same contents to the new repo.
3. Share the new URL with contributors.
4. Archive or delete the old repo.

Rotation is cheap because everything is markdown in git. There's no deployed database, no stale credentials, no lingering cache.

---

## What NOT to publish here

See [`CLAUDE.md`](CLAUDE.md) for the full guardrails. In short, keep out:

- Individual mentee names, stories, or arcs
- Internal business data (specific pricing tiers, revenue, team compensation)
- Team personnel details
- Private biographical material Ra hasn't chosen to make public
- Anything sourced from private mentorship or operational calls
- Strategy / positioning intended for internal consumption

**When in doubt, leave it out.** The URL is unlisted but not secret — treat everything here as readable by anyone who ends up with the link.
