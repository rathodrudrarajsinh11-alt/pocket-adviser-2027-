# Pocket Adviser 2027

A static, installable study-planner PWA. The app uses Supabase Auth and the `public.user_records` table for optional account-based cloud sync; local storage remains available without signing in.

## Project details

- Cloudflare Pages project: `pocket-adviser-2027`
- Pages URL: https://pocket-adviser-2027.pages.dev
- Supabase project ref: `yyqloliogtfkvnpgprgw`
- Supabase region: Mumbai (`ap-south-1`)
- Supabase publishable key is intentionally used in the browser. Never put a Supabase service-role/secret key in this repository.

## Deploy with Cloudflare Pages (free tier)

1. Create a new GitHub repository named `pocket-adviser-2027`.
2. Upload all files from this folder to the repository root (not inside another nested folder).
3. In Cloudflare Dashboard, open **Workers & Pages → pocket-adviser-2027 → Settings → Builds & deployments** and connect the GitHub repository.
4. Set production branch to `main`.
5. Since this is a static site, leave the build command empty and set the build output directory to `/` (or `.` if the dashboard rejects `/`).
6. Save and trigger a deployment. Future commits to `main` will deploy automatically.

No paid build service or paid add-on is required for this static project. Check the account's current plan/usage limits before enabling any optional feature.

## Supabase Auth URL configuration

In Supabase Dashboard → Authentication → URL Configuration:

- Site URL: `https://pocket-adviser-2027.pages.dev`
- Add Redirect URL: `https://pocket-adviser-2027.pages.dev/**`

Email confirmation may be enabled by default. If signup asks for confirmation, use the confirmation email before signing in. Do not disable security protections just to make signup easier.

## Verify after first deployment

- Open the Pages URL over HTTPS.
- Create a test account and complete email confirmation if prompted.
- Sign in, add a small test task, reload, and check sync status.
- Sign out and verify local app access still works.
- Install from Chrome's menu → **Add to Home screen**.
- Test offline by opening the app once online, then briefly disconnecting.

## Important status

The backend table and row-level security policies have been created. This repository is a static PWA package; a deployment and live authentication/sync test still need to be completed. Do not treat it as a fully verified production release until those checks pass.
