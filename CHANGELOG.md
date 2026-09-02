# Changelog

All notable changes to the Forge Compliance product are documented here.
Newest release first.

## v1.3.25 — 2026-09-02

- Add and edit equipment directly from the mobile job page, with fields for make, model, serial number, rating, and details.
- Equipment entered on a job now stays linked for reporting and photo tagging, making job records more consistent.
- Updated the notifications recipient layout so chips are easier to scan and fit better on the page.
- Kept the preview/test button in its own space for a cleaner, more usable notifications screen.

## v1.3.24 — 2026-09-02

- Maintenance release.

## v1.3.23 — 2026-09-02

- The preview/test action is now a separate button column, making it easier to spot and clearly distinct from recipient choices.
- You can now send a test alert to yourself directly from the recipient setup modal.
- Notification recipient routing has been fixed so the right managers receive report submitted and expiring competency alerts.
- Web push notifications are now much easier to set up in production, with the needed settings and key file wiring fixed.
- A ready-to-use VAPID key setup has been added, so push notifications can be enabled without needing local Python tools.
- The setup guide and environment template were updated with simpler Docker-based steps for generating and configuring push keys.
- Once push is configured, the iOS app can show the “Turn on notifications” card and Forge notifications in the iOS settings page.

## v1.3.22 — 2026-09-02

- Fixed a notification-routing bug so alerts now reach the right people more reliably, including manager-based recipients.
- Improved push notification delivery so “report ready for review” and similar alerts are less likely to be missed.
- Audited notification sending across the app and corrected remaining recipient-type issues.

## v1.3.21 — 2026-09-02

- Added a “Test push notification” button in Admin > Settings > Notifications so admins can verify push alerts are working.
- Improved push notification reliability by automatically re-sending the device’s current subscription whenever the app opens or returns to the foreground.
- Made push setup easier to troubleshoot by confirming the push endpoint is active and properly protected, rather than unavailable.

## v1.3.20 — 2026-09-02

- Fixed a login/logout issue so users can sign out and back in more reliably.
- Improved the Cloudflare Access sign-in flow to handle short delays after logout.
- Reduced the chance of being temporarily blocked from logging back in after ending a session.

## v1.3.19 — 2026-09-02

- Added a branded sign-out screen so users see a clear “Signing you out…” message before being logged out.
- Improved logout behavior to redirect more smoothly after sign-out.

## v1.3.18 — 2026-09-01

- Fixed Cloudflare sign-out so users are properly re-challenged by Access instead of being dumped back to the app login screen.
- Improved logout behavior to remove the brief “flash” of the wrong page during sign-out.

## v1.3.17 — 2026-09-01

- Fixed Microsoft sign-in so users stay on the same site they started on, instead of being bounced to the Cloudflare access page.
- Improved logout behavior so it uses the current site’s address and only shows the Cloudflare logout step when it’s actually needed.
- Added support for multiple Microsoft redirect addresses, so each site can use the right login path automatically.
- Resolved an issue that could send users to the wrong host after successful login when the app base URL was set to a public address.
- Added test coverage to prevent this login/logout host mix-up from coming back.

## v1.3.16 — 2026-09-01

- Fixed sign-in on the internal domain so the app no longer routes users through Cloudflare during login.
- Improved authentication handling to keep the internal Microsoft/Entra login flow on the correct domain.

## v1.3.15 — 2026-09-01

- Fixed an issue where older Forge versions could appear as separate offline servers after an update.
- Improved server tracking so machines are recognized consistently across version or image changes.

## v1.3.14 — 2026-09-01

- Fixed logout so LAN users stay on the local domain instead of being sent through Cloudflare sign-out.
- Removed a brief password-form flash when signing out on the Cloudflare domain, making logout smoother.
- Cleaned up unused code and files from the app to reduce bloat and keep the product lean.

## v1.3.13 — 2026-09-01

- Simplified sign-in so login flows are more reliable behind Cloudflare Access.
- Fixed the “Something went wrong” error that could block users from logging in.
- Added clearer push notification handling and messaging.
- Added a bell badge to make unread alerts easier to spot.

## v1.3.12 — 2026-09-01

- See outstanding work at a glance with a red count badge on the Actions tab and on the app icon.
- Open job photos in a full-screen in-app viewer with swipe and arrow navigation, then return cleanly to the job page.
- Browse attached files as thumbnail grids for easier review on mobile.
- Fixed Microsoft sign-in errors caused by a date/time mismatch during the login callback.

## v1.3.11 — 2026-08-31

- Added an Actions hub on mobile to bring together your due training, licences, renewals, and team approvals in one place, with quick approve/reject actions.
- Let managers approve or reject items directly from the mobile app without leaving the main workflow.
- Added an admin-only option to hide owners or other excluded staff from personnel lists, approvals, training views, and related tracking screens.
- Improved compliance views so excluded accounts no longer clutter team lists or reporting.
- Simplified our release process so updates are generated automatically from recent changes.
- Reduced build overhead by stopping an extra backend image from being published on every update.

## v1.3.10 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.9 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.8 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.7 — 2026-08-31

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.6 — 2026-08-28

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.5 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.4 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.3 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.2 — 2026-08-27

- All four items are implemented and verified

## v1.3.1 — 2026-08-27

- AI error deep-link
- AI Calls audit log
- AI tuning knobs + shared helper + reviewer-picked photos + thinking-safe parsing — built & tested (7/7)
- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.3.0 — 2026-08-27

- AI error deep-link
- AI Calls audit log
- AI tuning knobs + shared helper + reviewer-picked photos + thinking-safe parsing — built & tested (7/7)
- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.2.1 — 2026-08-27

- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.2.0 — 2026-08-26

- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.1 — 2026-08-25

**Automated release notes + GitHub Release**
- **Name**: desc` lines) render tidily. You can always hand-polish any single release by editing it on the Releases tab afterwards

**Servers Page: Cluster Dashboard + Guarded Failover**
- **Settings → Servers** (admin-only, on every node): live replica-set view — "This server is PRIMARY (master) / STANDBY" banner, per-member health, replication lag, uptime, priority/votes, auto-refresh, plus a warning when you're on 2 voting members. Single-server installs just show "standalone" - **Guarded actions replace every §5 docker-exec command**: Step down primary (Mongo refuses without a caught-up standby), Promote this node (locked until NO primary is reachable + typed PROMOTE; force-reconfig on the survivor — split-brain refused server-side), and Re-add mem…
- **Tested with a full disaster drill** on a real local 2-member replica set: killed the primary → promote unlocked → promoted → old node re-added and rejoined as SECONDARY (no split-brain) → step-down handed primary back → watchdog fired both down and recovered alerts. All guard rails (wrong confirm, primary-alive refusal, quorum failures) verified; preview restored to standalone afterwards - **To enable on your cluster**: create the `forgecluster` Mongo user and set `MONGO_CLUSTER_URL` + `CLUSTER_SELF_HOST` per the new §5b in MULTI_SERVER_SETUP.md (compose + env.template updated). ⚠️ Not yet run on your real Synology/Nebula cluster — t…

**Nameplate Reader + Incident AI Assist**
- **Nameplate Reader**: "Read nameplate (AI)" in the Serviced Equipment detail sheet — snap/pick a photo (camera capture on mobile) and the VLM pre-fills OEM, model, serial, rating and appends extras (voltage/year/etc) to Details; you review…
- **Incident AI Assist**: new "AI assist" panel in the incident GPS review — one click gives a summary, suggested severity (with Apply button when it differs), likely root cause, and suggested corrective actions each with "+ Add" into the real…
- **Testing**: full E2E verified with a mock OpenAI-compatible server — nameplate field-fill in the browser, assist with photos routed to the vision model, vision-off fallback to the main model, persistence, and "+ Add" flow all pas…

**Quiet Hours + Vision (VLM) AI Upgrades**
- **Quiet hours**: the server sync nudge now skips workers inside their My Profile quiet hours (same window as email) and fires once the window ends — tested with per-user prefs and safe defaults
- **Vision (VLM)**: new Settings → AI/LLM "Enable vision (VLM)" toggle + optional separate vision model (blank = main model). Scanned/no-text PDFs are now rendered to page images for the VLM everywhere (report proof-check, cert/insurance…
- **Testing**: backend unit tests 5/5 + testing agent iteration_106 — 11/11 backend, 100% frontend, no defects. Note: preview has no live LLM, so real qwen3.8-VL output quality is yours to validate — point Settings → AI/LLM at your…

**Web Push + Server Nudge + Tunable Timing**
- **Closed-app push (VAPID)**: new backend push router + `core/push_service.py`, VAPID keys generated (private PEM git-ignored, public key in env), service-worker `push` handler, and `lib/push.js` opt-in. The "Remind me" button now registers a real…
- **Server nudge**: a background `sync_nudge_loop` pushes a reminder to a worker's phone when their offline sign-on stays unsynced past the threshold — even if the app is shut. The client reports its queue state (`reportQueueState`) when…
- **Tunable timing**: admins set "Nudge workers after (minutes unsynced)" in Settings → Notifications (`sync_nudge_minutes`, default 30, 5–1440), used by both the in-app nudge and the server push

**Auto-Retry Nudge + App-Tile Badge**
- **Fixed the blocker**: `window.forgeOffline` now exposes `updateAppBadge` + `oldestAgeMs` (the missing hook that caused the earlier `is not a function` test error; the real app already imported them directly). - The feature set was already…

**Tappable sync badge — details + retry**

**Offline photos + sync badge**
- **Offline photos**: the offline queue now holds an image
- **Risk photos offline**: when a worker attaches a risk photo with no signal, it's stored as a blob with a local preview; `finalize()` chains its upload before the sign-on so the photo lands with the record on sync
- **Sync badge**: a calm, generic pill on the mobile home — "{n} waiting to sync" when offline, "Syncing…" when online, hidden when nothing's queued. Verified it renders ("1 waiting to sync") and auto-clears. Kept it simple as you aske…

**Offline sign-on**

**Worker mobile app — Phase 1**

**What I built for your exact setup**

**Built all four + fixed your Mongo error's real cause**

**Clarified backup question + fixed a real backup gap**

**Both requested features**
- **Compliance timeline — insurance type**: supplier/personnel insurance records now display the actual insurance type in the timeline label (backend `compliance.py`, already in place — confirmed)
- **Editable job files**: added an Edit action + dialog to the job Files tab (`JobDetail.jsx`) driven by the existing job-scoped `PUT /api/jobs/{jid}/files/{fid}` endpoint. Managers can edit name, note/description and re-link equipment; visibi…

**1. Save default view (per‑user)**

**1. Autosave scheduling**

**Serviced Equipment — reminder rules + bulk edit + sort/filter**
- **Precedence:** most‑specific rule wins, and a rule with a **client set always beats a client‑agnostic (global)** one — verified: `ZZMTM · THYCON · MPX` got the client rule (L1@3mo, L2@12mo), while `OtherCo · THYCON · MPX` fell back to the global rule. - Each reminder **links to a Task Type** (L1/L2, selectable). - **Auto‑applies on equipment creation**; existing gear gets a manual **"Apply matching rule"** (single) or **"Apply rules"** (bulk) button. - **Never clobbers your hand‑edited reminders** — verified a manual reminder survived a rule re‑apply while the rule ones refreshed. **Bulk edit**: Select rows →
- **"Apply rules"** runs matching rules across the selection. **Table sort/filter**: Every shown column is now

**Your question: does an email go out?**
- **Licence key**: **Registry username + access token** - A 5‑step quick setup: open the guide → `docker login` (ready‑to‑paste) → configure `.env` → `docker compose up -d` → activate in Settings → Licence - A link to the

**Security Audit + Remediation**
- **SEC-001 (CRITICAL) — privilege escalation to Administrator**: any manager (or personnel-write user) could set a teammate's role to `admin`/`gps_manager` via invite or user-update and take over the platform. Fixed with a role-hierarchy guard (`_assign_role_allowed`) on both endpo…
- **SEC-002 (HIGH) — unauthenticated file-download signing oracle**: the public sign-on "attach file" endpoint needed no session and would sign a download URL for any stored file id. Fixed: attach now requires a valid job attendance, the file must have been uploaded via the public uplo…
- **SEC-003 (MEDIUM) — SSRF in webhook test**: blocked private/loopback/link-local/metadata targets + disabled redirects. Verified: metadata IP & localhost → 400. Accepted/low-risk items (CORS via env, demo seed password, admin-only regex search, self-only templat…

**Photo compression + send-history detail**
- **Compress Large Files**: the Send dialog now has a "Downscale large photos before sending" toggle (default on when photos are selected). The backend downscales image attachments to max 1600px / JPEG q80 via Pillow before sending (report PDF &…
- **Send History Detail**: each send is now logged with recipients + the exact attachment filenames, shown as a "Send history" section in the report History popover. Verified: log recorded `['report.pdf','photo.jpg']`. Backend logic verified wi…

**Report send/re-upload enhancements**
- **Re-upload Notify**: submitting a corrected version of a rejected report now notifies admins + in-house managers + the person who rejected it ("ready for review & sign-off"). Verified: notification created (2 recipients), same report id k…
- **Ignored-file Notice**: the send endpoint returns `{attached, ignored}` and the Send dialog shows a warning toast when selected files can't be attached. Verified: bogus ids → ignored=2, attached=1 (report file)
- **Attachment Size Guard**: `/jobs/{jid}/review-files` now returns each file's size; the Send dialog shows per-file MB + total, warns inline over ~15 MB, and asks to confirm before sending an oversized batch. Verified: size returned correctly. A…

**Image slimming + release automation**

**Why the build crashed**
- **Removed my duplicates:** `dist/`, `forge-compliance-app/`, the root `.dockerignore`, and `.github/workflows/build-images.yml`. Only your original **`docker-publish.yml`** remains. - **Kept two safe, non-duplicative wins**: `server.py` now imports the storefront router only when `STOREFRONT_ENABLED=1` (no behaviour change — product installs default to `0`). - Added `backend/.dockerignore` so tests/pycache/.env stay out of the backend ima…

**Confirmed — here's the clean model and what to do**

**Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)**

**Admin Integrations tab + Cloudflare Access diagnostics**

**Licence-server default + Forge Compliance branding**

**Cloudflare Access SSO + dedicated marketing SMTP**

**Landing form + spam protection + Licensing (model B)**

**Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100%, no issues)**
- **Email validation**: invalid emails like "test" / "test@" are now blocked on the Try-the-demo, Buy-the-licence and Stripe-checkout flows — frontend regex + backend `EmailStr` (returns 422). A valid email is required to proceed
- **Simplified form**: removed the

**Why your Stripe keys weren't in the panel**

<details><summary>Other changes in this release</summary>

- Saved both, in one place
- Added a copy‑paste **⚡ Quick start** right below "What you'll need" — four commands (registry login → clone → configure → `docker compose up -d`), then "open :8080 → Settings → Licence." The detailed sections remain below for anyone who wants the full walkthrough
- Done — and verified end‑to‑end in preview
- Done. Here's the honest summary of what I changed and why it's now genuinely a cleaner product build
- All three fixes verified
- All done and verified locally by simulating the release step. Here's what changed
- Everything's ready. Here's the summary
- The workflow will now fail fast with a clear message if the token is missing. The root cause is that the `DEPLOY_REPO_TOKEN` secret isn't set, and GitHub's built‑in `GITHUB_TOKEN` **cannot** push to a *different* repo — so cross‑repo release sync needs your own token. Here's the exact one‑time setup
- auto-commit for dd50b24a-93fc-4c43-b073-c5839b90e44c
- auto-commit for 90038171-906c-47a3-a6ed-09cb6bdf0f7f
- auto-commit for 73f1a8de-d1c2-465f-962f-3d658ca8eb14
- auto-commit for 40842568-337a-4502-9558-bcaadd966832
- auto-commit for 317ca021-7b6d-4b1f-a238-e152cb15bcbe
- auto-commit for aa828f44-40e8-4021-b5be-699c8460491c
- auto-commit for 08a76b4e-6f27-4af9-bc6f-fda789142122
- auto-commit for 15261869-52a7-482c-bb23-39d9ed83567e
- auto-commit for a1834077-4dcb-474e-9dff-3ba2b8d46dfc
- auto-commit for cee717a9-2db9-46a3-ae1b-87adeab362cd
- auto-commit for 4cc27742-0ec3-4cc0-a535-ef6e316971de
- auto-commit for 330d9b94-a627-4aa4-adf7-f701eeffbb89
- auto-commit for 7d0d7787-a6f6-43cd-b8c7-7fa7d6cfd399
- auto-commit for d00459b3-4b80-4624-98b5-70bbc1bf5536
- auto-commit for adbe6aba-2d61-4074-8c9e-22623cff2a53
- auto-commit for 707a54b9-c82b-4c38-9cc7-7e2f1f23b056
- auto-commit for 9c1ad122-6dd5-4a50-a98e-7bb910f16c89
- auto-commit for 25249b7d-4ce7-4262-a8ff-be479508edce
- auto-commit for 667aef6f-70fa-4804-bb0f-ab2ee8b3d2b7
- auto-commit for d772edfb-35fe-469f-b3b1-f980535e4e5d
- auto-commit for ec209cef-740a-40f5-80ff-b4096c3f0d11
- auto-commit for 443b736e-def3-49c2-ab9b-8418a74fff2c
- auto-commit for bd1e2856-0957-4827-9116-99ea7e3160b4
- auto-commit for ba550bc8-5f34-49f4-b277-64ab4a111a09
- auto-commit for 427723f6-5213-4d1d-bb73-f3fea7b0bdb8
- auto-commit for d8aa87d7-4014-459e-89fe-a0e1d1302596
- auto-commit for ee734092-d588-46ba-8c39-e72ce41812aa
- auto-commit for 9dfab80e-fc30-4753-99f9-ed31b2878a26
- auto-commit for b60de77e-7702-4d5d-98ce-9d3e4969e3f7
- auto-commit for 004f953a-dea1-45d7-96ea-c89ac4d498c0
- auto-commit for 24c711f4-1fe6-47c7-bdd2-78c1b17a82ee
- auto-commit for c341b6bc-8c5f-471c-814b-d7ab2e3f0885
- auto-commit for eb531240-7512-4d6c-b393-54d3785fa47f
- auto-commit for 24c577da-fa95-4323-9580-af2ef7fddeef
- auto-commit for 5c4332d5-7b96-40c2-9a17-5acae0ea716f
- auto-commit for 111e5d2c-0b9c-4a81-b0f7-616789d1ec3a
- auto-commit for dca0879c-642a-406f-9e7d-6c7ed9be4d32
- auto-commit for 50768d62-19b8-475c-9fa6-34d9f2c7d3c7
- auto-commit for 45c5a173-4a5f-44c2-8689-93ea88cdfc7d
- auto-commit for 1655b06b-bc27-4de2-add4-6a4f9b6a666d
- auto-commit for 80c1a00f-4a68-4003-99eb-f0d5a64c236b
- auto-commit for f4046475-5fb5-4495-a23d-5fa64d2fdfec
- auto-commit for e8b1b4cd-edad-488a-8bfe-d8817f33c6da
- auto-commit for 5fd874ad-31d3-484e-b4e1-e3ecc3d52308
- auto-commit for 809f3053-c1f7-4544-a951-b021826d41a6
- auto-commit for a75f66cb-7889-4baa-b98d-22407ed55d3c
- auto-commit for 1907b96b-7518-42bd-ab33-c34f774ba263
- auto-commit for 7dff893f-6e65-4449-9092-d58d8d72a178
- auto-commit for 6b0627a2-b4f7-4e98-950a-a9b510105f8b
- auto-commit for 7d0d7c64-4cbc-412e-963e-8db912d52122
- auto-commit for 2d1dd3b3-317e-48b4-9e08-b23911620d13
- auto-commit for 35bed9ae-90d6-462b-ba0a-348f708aed4b
- auto-commit for ea21377d-bfd0-4ddd-aacb-5b666a5237e9
- auto-commit for ad4aad25-5a70-4c74-8833-2f5a4edf1c14
- auto-commit for aedf0a01-b423-4ec9-a8c4-d69152889ac0
- auto-commit for b55e6dee-444b-4a16-84fe-e6dbe42392aa
- auto-commit for a6072ea2-05bc-4e68-b4b9-dd18aed15601
- auto-commit for c7932162-377a-4716-b5e9-75657d1716b6
- auto-commit for bd1176ef-076f-4534-a639-e95d1fe4ac9f
- auto-commit for 5ad5b582-f6dd-4f94-a7ed-f6f7a70cf792
- auto-commit for c59737c0-c203-45da-af06-287d8a6bb6fe
- auto-commit for 53490539-f2bf-4171-99c6-c61c5c964166
- auto-commit for c69338d4-ec2b-4f31-a666-e08ca548e40d
- auto-commit for 3952e6f4-6cd2-4ab5-8539-0ef0aa7bd994
- auto-commit for 1b42f1ba-9309-480c-821a-52ef6b9aa5e6
- auto-commit for e3f4171e-d98d-4c6b-8647-8be889fe22a3
- auto-commit for ff4f4b2b-b1d4-487d-93f6-27faa39a150c
- auto-commit for d099390d-6c3a-44a7-94c6-34e43b5d9e23
- auto-commit for 58463889-fa5e-4263-9e68-36411b4baa95
- auto-commit for 313f8408-8944-437f-95bb-9c2c907d8709
- auto-commit for ef355c84-fdb4-478e-af6f-c27c62867578
- auto-commit for 07e5ced0-e514-4a3d-98b3-f9d0c2d438ac
- auto-commit for 1d684242-5b5f-4497-82f6-750ca9a6e8fe
- auto-commit for 3e99ace1-610e-46e6-8d4d-5e2512d84775
- auto-commit for 9f27c648-fe57-44c7-9310-6b1aa51b6bf3
- auto-commit for f05c6203-3035-400c-aa16-e2994738656d
- auto-commit for 019afaa7-7b96-4a6e-8f1e-afb1dac5d1c4
- auto-commit for 69dae3d4-7d50-4888-b2db-d87fd2861520
- auto-commit for c08cee1e-2c37-419d-9ad9-f8a1c9b7b8ed
- auto-commit for 3630f303-5ca1-430d-9110-265fb3b4c988
- auto-commit for d36ca572-e123-43fd-99a8-4a7eeffbe523
- auto-commit for 0297c06b-2e3b-411c-bb67-4522f0d8d196
- auto-commit for 9c6dc734-220c-46d8-a39a-f8b5ac330698
- auto-commit for 270a62b7-f83d-4895-b82f-635b474d4129
- auto-commit for 45d165c0-6b90-41aa-b9ba-075e11fcbf10
- auto-commit for 8e91267d-e654-4871-be31-cac620d9a809
- auto-commit for 7fc464dd-0b0d-4124-b6f5-5cfca66df46a
- auto-commit for 8b426112-3b8f-4513-aba2-f8e5c5ea54c7
- auto-commit for 347832b7-cd21-4c0b-b4f0-f7cf5aa3cd05
- auto-commit for 350fe710-6e09-40ff-9d79-5c56cb595d31
- auto-commit for 160c43cd-9d25-4f11-930c-5b10972c0dc9
- auto-commit for 87d0c218-04fe-44d6-91ae-9afdadec48b4
- auto-commit for 4abe6141-4cb6-4a1f-8529-d7b29c603cbb
- auto-commit for 2c2904a7-1667-4818-82f2-6f52bf6575d7
- auto-commit for deef5c59-6de8-480b-a9eb-435ddfd0b637
- auto-commit for 1b109dd6-91e9-4fc5-b15c-9793cbb67dc2
- auto-commit for b5eca32e-e742-4c8f-bdc9-111df912a8f5
- auto-commit for 2f3580be-e688-4520-90a9-29df4adebaed
- auto-commit for 8edcf44c-982d-4b31-b178-1f6148bcf4ec
- auto-commit for a1f9d927-d9ef-4d76-9b9c-97a02a4863c0
- auto-commit for d986d94b-5829-47bc-aaa4-3cd63cb425c5
- auto-commit for 066e53fd-2e2b-4a2f-8dfb-13d9fec51e45
- auto-commit for 4e2eb8f6-4f3f-4f71-9803-dbbf27ef7b78
- auto-commit for 745a8a37-de50-4bf1-a6de-cd2ca55d6261
- auto-commit for 779c4d4d-3150-494f-a4b1-b5dfca4f94c8
- auto-commit for 8965a211-301f-444c-9526-633612cdc186
- auto-commit for c43dc4e3-d661-4aae-8430-6c2393185a39
- auto-commit for 695e77fb-40cf-4daa-b299-93d15798e3f1
- auto-commit for 279fc023-a25b-49c4-a57d-63bafc0859aa
- auto-commit for 7d28dd6b-3c9a-467d-85e0-38be7d5e776c
- auto-commit for f038e04a-47f0-4397-ab53-f692257dabe0
- auto-commit for b35ef5fd-70f3-4721-9df5-450a71895aa2
- auto-commit for bb802936-eea6-4aab-8abe-8caed93d9abb
- auto-commit for 979e8136-6d27-4d5d-8be4-6b1dc5e17dd7
- auto-commit for 08d1ce77-90a6-4a93-b9ef-a2bb75fa57fa
- auto-commit for 7ea8ab5f-ec0e-4eed-afe8-4b967a5fbc9a
- auto-commit for 778d3bd0-fc70-4447-9b83-4150efc03410
- auto-commit for 5908f804-4c8a-4dca-9023-62619456e4ba
- auto-commit for 9b409c9b-73f4-46a0-9198-477b04651474
- auto-commit for 6ad2df2c-11cb-4e94-ae2d-96a9d9f274fe
- auto-commit for 01283028-c369-4daf-8eb1-4739eff62f21
- auto-commit for 93a7d2f7-451d-4adc-ab91-466125314103
- auto-commit for e2cbf85d-4bf8-4fe3-a47e-7bdb91d0d2e2
- auto-commit for 85cd5cd1-65e2-4237-a81d-bfa79e159f39
- auto-commit for 50196493-76dc-496f-b6f5-9c5e078d030e
- auto-commit for 60fb427f-1f7c-4241-b03c-7f2d81087042
- auto-commit for 092ba65c-b98b-401d-809d-72a5d9917009
- auto-commit for 81f57196-efdd-40d7-95fb-c7a7b3d96797
- auto-commit for 3576385d-3e0c-4533-82bd-6b986bed99f8
- auto-commit for 50e313ac-2733-4562-9616-4f7fe8e9cbc4
- auto-commit for c4fbc0ee-a1c7-4bc0-9fbf-9aaf818c015b
- auto-commit for a5c86b19-6121-4b2c-a5e0-c8437c109dcc
- auto-commit for cc10b078-9d8a-49ec-b484-b8ebc6ef4c8a
- auto-commit for a400d5f0-e8a1-4f0f-9b04-f201647c20ff
- auto-commit for 7bb544e3-6e1c-4948-9bd7-6dc7a1c5a1f9
- auto-commit for 04406d68-51d2-445a-af83-38f8b59bd82c
- auto-commit for e00cb451-b1be-490c-9ad1-85ce678effd6
- auto-commit for 22c3ec85-fc50-4139-a9b0-08b1d363882f
- auto-commit for dcd3c6e8-e2e3-4ae0-b5e7-2b26f04213e3
- auto-commit for 76883d44-0c3f-4cdd-91c6-59c97b659871
- auto-commit for 72073aa6-9f93-49ba-8e9e-77630f0b285c
- auto-commit for 17f20357-982e-4bbf-bf2b-e43daef4d252
- auto-commit for 6f9374bb-0d40-4d3f-9521-a6f8e5f211fd
- auto-commit for 0f573e69-3655-4581-aebd-dc08a67cb97e
- auto-commit for b267e0b7-c396-4fc8-b829-2260a694fb02
- auto-commit for 802eb0c9-1686-44b1-9b44-2e7ccbfb0bee
- auto-commit for 01cf0ad9-7c0f-4d8e-a18b-68f8eccc2d16
- auto-commit for 9977aea9-77ec-41c1-a06e-4bfd1979ffb5
- auto-commit for 588d1ecd-c80e-4d21-9a9c-707d973db666
- auto-commit for 800d9c09-8b24-4ea3-b308-b1d090c1faa8
- auto-commit for cda2d81b-9092-462d-b118-f2e045b61948
- auto-commit for 6accae02-1659-4a6e-9840-e28055c882fc
- auto-commit for 1e183dae-818d-447f-9018-65e31337d7a3
- auto-commit for 3f1ee679-c69e-4cae-b11b-ed84b9394a72
- auto-commit for 5269a225-a8b2-4d1a-b7ce-1bc8bfddf681
- auto-commit for 84a98cc0-8a70-41a9-b0e1-448180b676c4
- auto-commit for 4ec9ee31-07dd-4e94-ae2e-ad3b9f7fc12c
- auto-commit for e920904a-774b-4564-af30-340f112a8855
- auto-commit for 9b04a3d7-7094-4d48-841d-d255d1d1e9b9
- auto-commit for 39d08377-295c-4ad6-89be-d4e5e3d7b2d9
- auto-commit for 6a75a66d-b1aa-4aad-9aae-70a4d7f905a5
- auto-commit for 8426efb2-8a93-4fb4-9d04-7edd0445be03
- auto-commit for 8be90fae-849b-4059-b39c-7f4e62de9e7b
- auto-commit for 87f9430d-1d37-46ba-8fab-8c9236b64250
- auto-commit for 877d3b5c-ce7f-4ddb-b668-2c689c6ef340
- auto-commit for ce636ed6-22fa-43db-b101-23588bf9bec2
- auto-commit for e61d95ea-47f0-434e-92c5-fe466e78e6f3
- auto-commit for 965bab17-e4b2-44f4-915a-1082b4ded5d7
- auto-commit for 121477de-68e6-46eb-b4bc-ed4885bf73b3
- auto-commit for 0ad4f229-7a3c-472d-97d6-44feead3d054
- auto-commit for ed73dc87-6f3f-435e-b444-94f0d698c785
- auto-commit for 1b1927db-b48b-409a-8b1c-b2d0751e2a38
- auto-commit for 43abd4d8-2a41-4c13-b183-dc7b736ba63e
- auto-commit for 64197907-1878-4802-893c-688115735c1e
- auto-commit for 084c8eaa-91ce-46c0-a109-5e46fe4112bd
- auto-commit for d14d07cb-1d83-4076-a829-1b85300ddb96
- auto-commit for 9832418e-74e2-492c-b499-bc5c5afd95f3
- auto-commit for 4e7e86fc-2b45-42a4-a81d-3011096f3497
- auto-commit for 932b6f93-e4ff-43d7-b7ca-3f09805309d9
- auto-commit for f3690b05-03f5-42ff-a982-a63daa05722e
- auto-commit for 656ce96f-71b7-4761-87dd-3858931be6d5
- auto-commit for 5ba1778e-3ad3-4e06-86fb-06a45a292184
- auto-commit for afe22675-44f1-45d2-9dfd-627609377489
- auto-commit for 026b4cb3-1a2f-4bc6-ab21-057135b82301
- auto-commit for 85482fcb-a543-43af-af61-b8f3a3b21e47
- auto-commit for 7a536230-0483-4192-8053-cba2e57a7a15
- auto-commit for d4df70d1-8755-4662-a6e6-e74c7ac5161e
- auto-commit for 916e0e6c-181c-413f-9361-b41896df324d
- auto-commit for 0f6c99ab-ee3a-43d7-94ea-e48da7650572
- auto-commit for aa326480-bf60-4c6d-ae87-f828f135425f
- auto-commit for ac56d2c0-5c76-424a-a275-a6e64c714693
- auto-commit for 022240ff-d135-47be-b982-cb38cb1eb8b0
- auto-commit for baa4dcb5-b519-4a4d-b49e-6c879394b58f
- auto-commit for 59f8d83c-f2f7-41bb-a47b-4980211a30eb
- auto-commit for 09fbd106-beb8-456f-a13b-57178ac21366
- auto-commit for acfd0025-6f90-4c94-bf4f-f04fe9271f4c
- auto-commit for 288b9bfe-1a63-4a84-96ea-937f5b39e92a
- auto-commit for 0a99ecd3-ad6a-453a-a2ef-cc0378a31b93
- auto-commit for c4679ceb-01ed-4c69-8c38-15297f89f346
- auto-commit for ca67c465-eeda-454b-b79e-8d1e407453bf
- auto-commit for 17934888-6663-4084-8c18-1ce3901c19e6
- auto-commit for 5820fa08-7ae9-4c20-a900-3b80278d7542
- auto-commit for 4712160b-908d-4177-a0b5-6a4903e719d5
- auto-commit for 3ad1765f-595c-404a-b9c1-5438ce389923
- auto-commit for ac2830ca-10cf-4ef0-850b-06d56e693932
- auto-commit for 834faf54-73eb-4308-af94-ef4b48fe77fb
- auto-commit for ebb6639d-dd0a-4d89-a464-b91f94fa1a7c
- auto-commit for 20b510c1-757d-40da-98d5-41ee633392c1
- auto-commit for 6f4917f5-40b2-4f3f-bd7f-b5749f1cd051
- auto-commit for 0eb7e1f5-0854-4b4f-94fc-5dd530ceefd0
- auto-commit for d5f1a0e1-8e87-4838-b916-ba18c19813e9
- auto-commit for 6eb02b01-e396-4f10-bb0a-ad6a24ab27b4
- auto-commit for 85ae4a81-85ef-47b0-8b3c-964d6f8cf8f8
- auto-commit for 46a4d2f8-7b75-4100-90c7-9e51d0ae6669
- auto-commit for b0c72605-e499-4f05-90a2-ba323a35f309
- auto-commit for 8f2c9a35-7773-471e-9b6b-6d55e9028c2c
- auto-commit for 09fde956-d5da-466e-9558-d595e54227da
- auto-commit for cd3b60bf-dfab-4f47-9f8d-dee4f02b1885
- auto-commit for 67e1d967-629e-4e0c-8ea1-d8cb9f176058
- auto-commit for e5e4ef03-18b4-44a8-821f-9cafb3334321
- auto-commit for a4b44d86-0964-4baa-8b7c-0ab6e754315f
- auto-commit for ed962cb5-9bd5-4266-b7e7-cdd81063428e
- auto-commit for 5386ef05-d2c1-4d83-924d-70eeb59e0620
- auto-commit for 1c4d6967-1261-493e-a56c-60a590b0e65e
- auto-commit for ca708073-b0ea-4fd4-b001-81baee9b27bc
- auto-commit for 3f23ce08-fa89-491b-8e8b-bc30b4f003c9
- auto-commit for df45870d-0e19-4838-990e-628c4214b939
- auto-commit for ccfb136f-7380-4d68-859b-681e9dda8a55
- auto-commit for 831b0fea-8a88-4263-b874-3576f7c2610b
- auto-commit for d38bdf72-99e3-43ea-8876-74f225f7bfa6
- auto-commit for 330da219-5552-464e-9286-e6d6aae9b0d6
- auto-commit for d2d86ca8-cd07-496a-8afe-d8cbbbb6ee15
- auto-commit for 550ef197-9a06-41cd-a885-34fc2600ea5a
- auto-commit for 6ebe5be9-9acb-40ea-8dd8-7f24ed5164ac
- auto-commit for 4f99ceb9-6212-48d8-8d6c-b9db6e8e7b57
- auto-commit for 344fc6b0-f8c2-461c-a49e-77a5c8648579
- auto-commit for 99d35861-486c-437d-b8c8-9e225774620d
- auto-commit for 88d433f4-997f-484f-bcce-609c368c6a2b
- auto-commit for 708294e6-aacb-44a6-912e-e16e3c015fd6
- auto-commit for c26ad314-dc78-44e1-b82c-03d5ce4339c2
- auto-commit for 53db3fa4-ae0e-4219-a37a-cf296c91e755
- auto-commit for d3708b79-bc28-4f03-871a-9a6fdb99e22d
- auto-commit for cffacc9b-b056-4e6c-88f9-aba15b575a3b
- auto-commit for 18ccb553-9132-40ce-adb9-abe333f3bd00
- auto-commit for cdec730d-df4b-4f02-a05b-d2c2b0946d43
- auto-commit for 7d877190-348a-4b81-baf8-dbbfbde6ac4d
- auto-commit for 81849472-9f7a-4c03-935f-8c6c023be3ec
- auto-commit for d8160d7b-7e7d-4e21-8946-348684bb2276
- auto-commit for 3b5abf61-c6d4-4750-8307-ec2de12913e4
- auto-commit for 5b287db7-cbec-4f03-bfba-eaced6012bc5
- auto-commit for dd02a861-16b9-44e7-b348-4844832c37fc
- auto-commit for ecbe9820-050b-4305-bedb-61ef787d2821
- auto-commit for c1542edb-4929-4312-8cc6-604a1061bdeb
- auto-commit for 68c47160-761e-4962-a491-cee675b27e9f
- auto-commit for f2130849-07e4-4d14-89c4-a7f544ff280f
- Initial commit

</details>

## v0.9 — 2026-08-25
- Release v0.9.

## v1.0.0
- Initial packaged release: jobs, service reports & PDF approvals, on‑site sign‑on,
  attendance, equipment/assets, incidents, clients & suppliers, document control,
  staff & training, notifications, and admin settings.
- Report delivery: choose related site photos/files as email attachments, optional
  automatic photo downscaling for large attachments, and a per‑report send history.
- Rejected reports can be corrected and re‑uploaded under the same report trail, with
  reviewers/managers notified automatically.
- Cloudflare Access SSO (Settings → Integrations) with password sign‑in fallback.
- Offline + online licence activation (Settings → Licence).
