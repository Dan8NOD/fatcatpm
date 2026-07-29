# FatCat Property Management

Static marketing site at [fatcatpm.com](https://fatcatpm.com). Owner intake → Supabase. Skyline parallax + scroll-reveal hero.

## Stack
- Single `index.html` (no bundler, no framework)
- Vanilla JS + CSS (Inter)
- Mobile-first responsive, pointer-glow only on desktop

## Editing
Edit `index.html` directly. Commit on a feature branch, push, open PR. GitHub Pages auto-deploys from `main`.

## Forms
Owner intake → Supabase table `fatcatpm_intake` (anon-insertable, RLS lets anyone post; only Dan reads). Same project as NOD-ify (`iubxycckgrplbpdbncfk`).

Notifications on new submissions → `POST /api/notify` on the [fatcatpm-portal](https://github.com/Dan8NOD/fatcatpm-portal) Vercel project. Set `RESEND_API_KEY`, `NOTIFY_EMAIL`, `WEBHOOK_SECRET` in Vercel env, then point a Supabase DB webhook at the URL.

## Related
- [fatcatpm-portal.vercel.app](https://portal-fatcatpm.vercel.app) — owner + admin portal (magic-link login, weekly reports, tickets)
- [fatcatam.com](https://fatcatam.com) — parent asset management company
- [negotiatorsondemand.com](https://negotiatorsondemand.com) — negotiation training app
