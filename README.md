# techdays.ai

Landing page for [techdays.ai](https://techdays.ai) — immersive, executable AI-fluency learning for enterprises.

Deployed as a Cloudflare Worker (static assets + a thin TS shim for the www redirect and security headers).

## Pages

- `/` — landing page
- `/guides/agents-and-skills/` — interactive stage-03 lesson: a live agent lab (editable skills, runnable in-browser), a fire-in-place prompt template, and A2A / MCP-UI / A2UI grounding. Self-contained single file, no build step.

## Develop

```sh
wrangler dev
```

## Deploy

```sh
wrangler deploy
```

Routes: `techdays.ai` and `www.techdays.ai` (custom domains, DNS + certs managed by the Worker deploy).
