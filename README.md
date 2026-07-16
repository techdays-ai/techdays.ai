# techdays.ai

Landing page for [techdays.ai](https://techdays.ai) — immersive, executable AI-fluency learning for enterprises.

Deployed as a Cloudflare Worker (static assets + a thin TS shim for the www redirect and security headers). Follows the [org conventions](https://github.com/techdays-ai/.github/blob/main/docs/CONVENTIONS.md): Bun-only, TypeScript strict, oxlint + Biome.

## Develop

```sh
bun install
bun run dev          # wrangler dev
bun run lint         # oxlint
bun run check        # biome ci
bun run typecheck    # wrangler types && tsc --noEmit
bun test
```

## Deploy

CI deploys automatically: every PR uploads a preview version (URL commented on the PR), merges to `main` run `wrangler deploy` to production. Manual deploy: `bun run deploy`.

Routes: `techdays.ai` and `www.techdays.ai` (custom domains, DNS + certs managed by the Worker deploy).

## Content

Guides, courses, prompts, skills, and plugin entries live under [`content/`](content/README.md) as frontmattered Markdown — the docs-to-course pipeline consumes that directory as data.
