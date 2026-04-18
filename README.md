# JARVIS Mesh Status

Public status page for the JARVIS AI mesh, powered by [Upptime](https://upptime.js.org).

- Status page: https://sakbark.github.io/jarvis-mesh-status/
- Checks every 5 minutes from GitHub Actions runners
- Alerts via Pushover (high priority)

## What this monitors

Only **publicly reachable** endpoints — Tailscale Funnel routes and third-party services JARVIS depends on. Internal LAN services (192.168.50.x) and Tailnet-only services (100.x) are monitored separately via:

- Uptime.com (15 internal checks)
- Healthchecks.io (dead-man switches for crons and heartbeats)
- Custom Uptime Kuma on CT301

## Endpoints

See `.upptimerc.yml` for the full list.

## Secrets required

Set in GitHub repo **Settings > Secrets and variables > Actions**:

- `PUSHOVER_APP_TOKEN` — Pushover application token (JARVIS system category)
- `PUSHOVER_USER_KEY` — Pushover user key (Saad)
- `GH_PAT` — GitHub Personal Access Token with `repo` + `workflow` scopes (for Upptime workflows that commit history files)

## Rollback

Delete this repo — no external dependencies other than Pushover keys (stored in .env + Bitwarden, reusable).
