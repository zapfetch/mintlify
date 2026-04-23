# zapfetch/mintlify

Public docs for [ZapFetch](https://zapfetch.com) — served at [docs.zapfetch.com](https://docs.zapfetch.com) via Mintlify.

This is the public-facing documentation source. Internal design docs, plans, and retros live in a separate private repo.

## Structure

```
docs.json                navigation + theme config
en/                      English docs
  index.mdx              landing / overview
  migrate-from-firecrawl.mdx
  billing.mdx
  rate-limits.mdx
  errors.mdx
  quickstart/
    curl.mdx
    python.mdx
    nodejs.mdx
zh/                      Chinese docs (3 pages, more coming)
ja/                      Japanese (placeholder — coming in W7-9)
ko/                      Korean (placeholder — coming in W7-9)
images/                  assets referenced from MDX
```

## Local preview

```bash
npm install -g mintlify
mintlify dev
```

Open http://localhost:3000.

## Publishing

Mintlify auto-deploys on every push to `main` (configured via Mintlify Dashboard → GitHub integration).

Custom domain `docs.zapfetch.com` is set up in Mintlify Dashboard and pointed via Cloudflare CNAME.

## AI-agent friendly exports

Mintlify auto-generates (no code needed):

- `/llms.txt` — summary for LLMs
- `/llms-full.txt` — full documentation content
- `/{any-page}.md` — plaintext version of every page
- `/mcp` — auto-generated MCP server exposing `search` over docs content

## Related repos

- [zapfetch/mcp](https://github.com/zapfetch/mcp) — operational MCP server (scrape / crawl / search tools). Complements the docs MCP auto-generated here.
- [zapfetch/sdks](https://github.com/zapfetch/sdks) — client libraries (Go, Python, JS).
- [zapfetch/firecrawl](https://github.com/zapfetch/firecrawl) — API backend fork.

## Contributing

Content is MDX. See [Mintlify's MDX guide](https://www.mintlify.com/docs/create/text). For SEO, keep the top-level `title` + `description` frontmatter filled — no `order:` field (navigation is controlled in `docs.json`).

## License

Documentation content is CC BY 4.0. See `LICENSE`.
