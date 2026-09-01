# Forge Compliance

**Version:** `v1.3.13` · released `2026-09-01`

Official **distribution** repository for **Forge Compliance** — the self‑hosted field operations
& compliance platform: jobs, service reports with PDF sign‑off, on‑site sign‑on & attendance,
equipment/assets, incidents, clients & suppliers, document control, staff & training, and notifications.

> This repo contains only what you need to **run** the product — `docker-compose.yml`, this guide, and
> `.env.template`. It holds **no application source**. The app runs as prebuilt images pulled from GitHub
> Container Registry (GHCR).

## What you'll need (from your purchase email / re‑download portal)
- Your **licence key** — to activate the app.
- Your **registry access token** (+ username) — to pull the private images.

Lost them? Re‑download any time from the **“Re‑download your licence”** page on our website using your
purchase email and licence key.

---

## ⚡ Quick start (copy‑paste)
Prereqs: a Linux host with **Docker** + **Docker Compose v2**.
```bash
# 1. Sign in to the image registry (username + token are in your purchase email)
echo <ACCESS_TOKEN> | docker login ghcr.io -u <REGISTRY_USERNAME> --password-stdin

# 2. Get the deploy files (this repo)
git clone https://github.com/dpbattaglia-gps/forge_compliance-app.git
cd forge_compliance-app

# 3. Configure
cp .env.template .env
#   then edit .env → set JWT_SECRET (openssl rand -hex 32) and APP_BASE_URL

# 4. Launch
docker compose up -d
```
Then open `http://<host>:8080`, log in, and go to **Settings → Licence** to paste your licence key. Done.

Full details below.

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
