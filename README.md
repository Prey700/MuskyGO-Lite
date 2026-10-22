# MyskyGO Lite

A responsive, mobile-first social network and business promotion UI prototype inspired by the supplied references. Includes a home feed, stories, profile, activity-style messaging inbox, online indicators, voice-call and voice-note placeholders, marketplace, promotion flow, theme switching, mobile curved navigation, dashboard menu, and illustrative admin dashboard.

## Run locally

This is a static website. Open `index.html` in a browser, or serve the folder with any static file server, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy with GitHub Pages

1. Create a GitHub repository named `myskygo-lite` (or choose another name).
2. Upload `index.html` and `README.md` to the repository's root on the default branch.
3. In **Settings → Pages**, choose **Deploy from a branch**, select the default branch and `/ (root)`, then save.
4. Wait for the Pages deployment to finish. The site URL will be shown in Settings → Pages.

## Important prototype boundaries

This is a front-end prototype, not a production social network. Feed posts, reactions, chat messages and theme preferences are client-side/demo interactions. Real authentication, user accounts, database persistence, real-time presence and messaging, secure photo/audio upload, actual voice calls, push notifications, ad billing and delivery, marketplace payments, reporting/moderation, and protected admin access still require a backend and security review. Admin figures are illustrative. No video calling feature is included by design. Do not use real personal or payment data in this demo.

## Suggested production architecture

- Frontend: React/Next.js or retain static UI while validating UX.
- Authentication and roles: managed identity provider, server-enforced RBAC and MFA for admins.
- Data: PostgreSQL with migrations, access controls and backups.
- Realtime chat/presence: WebSockets or a managed realtime service; object storage for photos and audio.
- Voice-only calling: WebRTC audio with authenticated signaling and TURN infrastructure.
- Ads: campaign review, targeting consent, spend caps, billing provider and analytics.
- Marketplace: seller verification, moderation, payment provider, dispute and refund handling.
- Safety: report/block flows, rate limiting, privacy controls, audit trails and data deletion/export.
