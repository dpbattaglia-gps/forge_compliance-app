# Forge Compliance

**Version:** `V1.0.1` · released `2026-08-13`

Self‑hosted deployment for **Forge Compliance** — field operations & compliance:
jobs, service reports with PDF sign‑off, on‑site sign‑on & attendance, equipment/assets,
incidents, clients & suppliers, document control, staff & training, and notifications.

> This repository is **deploy‑only** and is regenerated automatically on every release.
> It contains no application source — it runs the prebuilt Forge Compliance images from GHCR.

---

## 1. Requirements
- A Linux host with **Docker** and **Docker Compose v2**.
- Access to pull the private images from GitHub Container Registry (GHCR).
- A public hostname (typically fronted by a **Cloudflare Tunnel** or reverse proxy).

## 2. Sign in to GHCR (private images)
```bash
echo <GHCR_READ_TOKEN> | docker login ghcr.io -u <your-github-user> --password-stdin
```
Use a GitHub token with `read:packages`.

## 3. Configure
```bash
cp .env.template .env
```
Edit `.env` and set at minimum:
- `JWT_SECRET` — a long random secret, e.g. `openssl rand -hex 32` (**required**).
- `APP_BASE_URL` — the public URL used in emails/links, e.g. `https://app.yourcompany.com`.
- `COOKIE_SECURE=1` when served over HTTPS (Cloudflare); `0` only for plain‑HTTP LAN testing.

Image tags are **already pinned** to this release. SMTP and Cloudflare Access SSO are
optional here and can also be configured later in **Settings**.

## 4. Run
```bash
docker compose up -d
```
The app is served on `http://<host>:${HTTP_PORT}` (default **8080**). Point your
Cloudflare Tunnel / reverse proxy at that port.

## 5. First run
1. Log in with your administrator account.
2. **Settings → Licence** → activate your licence (online key or offline signed file).
3. Optional: **Settings → Integrations** → enable **Cloudflare Access SSO**
   (password sign‑in remains available as a fallback).

## 6. Upgrade to a new release
```bash
# pull the tags pinned in the new .env.template, then:
cp .env.template .env      # keep your existing secrets/values; only image tags change
docker compose pull
docker compose up -d
```

## 7. Backups
All data lives in the `mongo_data` volume. Back it up regularly:
```bash
docker compose exec -T mongo mongodump --archive | gzip > forge-backup-$(date +%F).gz
```

---

See [`CHANGELOG.md`](./CHANGELOG.md) for what changed in this release.
