# techdays.ai

Landing page for [techdays.ai](https://techdays.ai) — immersive, executable AI-fluency learning for enterprises.

Deployed as a Cloudflare Worker (static assets + a thin TS shim for the www redirect and security headers).

## Develop

```sh
wrangler dev
```

## Deploy

```sh
wrangler deploy
```

Routes: `techdays.ai` and `www.techdays.ai` (custom domains, DNS + certs managed by the Worker deploy).
