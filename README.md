# The Unseated Juror — placeholder site

Static coming-soon page for [theunseatedjuror.com](https://theunseatedjuror.com).

## Vercel

1. Import this repo in Vercel (same account as Classwise).
2. Framework preset: **Other** (no build command).
3. **Output Directory:** `public` (or leave blank — `vercel.json` sets this). The page is `public/index.html`.
4. **Do not** set a build command.
5. **Domains → Add** `theunseatedjuror.com` and `www.theunseatedjuror.com` (primary).
6. **Domains → Add** `unseatedjuror.com` and `www.unseatedjuror.com` — Vercel will still attach them; `vercel.json` redirects those hosts to `https://theunseatedjuror.com`.

## GoDaddy (leave DNS only; remove Website Builder / hosting)

For **theunseatedjuror.com** (primary):

| Type  | Name | Value |
|-------|------|--------|
| A     | `@`  | `76.76.21.21` |
| CNAME | `www` | `cname.vercel-dns.com` |

For **unseatedjuror.com** (redirect via Vercel):

| Type  | Name | Value |
|-------|------|--------|
| A     | `@`  | `76.76.21.21` |
| CNAME | `www` | `cname.vercel-dns.com` |

Use the exact A/CNAME targets Vercel shows after you add each domain (they usually match the table above). Turn off GoDaddy forwarding if it conflicts with Vercel.

Propagates in minutes to 48 hours. SSL is automatic on Vercel once DNS is correct.