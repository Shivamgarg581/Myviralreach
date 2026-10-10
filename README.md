# MyViralReach — Creator Partnership Workspace

MyViralReach is an influencer marketing workspace for managing brands, creators, outreach drafts, campaigns, follow-ups, deals and commission tracking.

## Stack
- Next.js App Router + TypeScript
- Supabase Auth and Postgres with per-user Row Level Security
- Google OAuth and Gmail API for inbox search, Gmail drafts, and user-confirmed sending
- Responsive dashboard for desktop and Android mobile browsers

## Features in this branch
- Email/password sign-up, sign-in, sign-out and password-reset email
- Overview cards for brands, creators, outreach drafts, campaigns, deals and follow-ups
- Create, search, edit and delete brand, creator, campaign, deal, follow-up and outreach records
- 20% default commission calculation for each deal
- Personalized outreach draft starter; drafts are saved for review
- Gmail OAuth, inbox search, Gmail draft creation and explicit confirmation before sending
- Settings and database connectivity diagnostics
- SQL migration with user-scoped RLS policies

## Setup required before the app can work
1. In Supabase SQL Editor, run `supabase/migrations/001_platform.sql`.
2. In Vercel project settings, configure these environment variables for Production and Preview:
   - `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY`
   - `SUPABASE_SERVICE_ROLE_KEY` (server-side only; never expose this key in client code)
   - `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`
   - `GOOGLE_REDIRECT_URI=https://myviralreach.vercel.app/api/google/callback`
   - `TOKEN_ENCRYPTION_KEY` (exactly 64 hexadecimal characters)
   - `APP_STATE_SECRET` (a long random secret used to validate OAuth state)
3. In Google Cloud, enable the Gmail API and add the exact redirect URI above to the OAuth client. Configure the OAuth consent screen and add test users if the app remains in Testing.
4. Redeploy after changing environment variables.

Generate secrets privately in a trusted terminal, for example `openssl rand -hex 32` for the token encryption key and another independent random value for `APP_STATE_SECRET`. Never paste secrets into GitHub, public chat, or browser code. If a Google client secret was previously exposed, rotate it.

## Local development
```bash
npm install
cp .env.example .env.local
npm run dev
```
Fill `.env.local` with values from your own project before testing.

## Important behavior and limits
- Sending a Gmail draft requires a deliberate click and confirmation. No automated bulk emails or follow-ups are sent.
- AI Outreach currently generates a personalized starter draft from brand details; it does not call an external AI model.
- Follow-ups are stored as dated reminders in the dashboard; external push/email notifications are not yet configured.
- Before public production use, verify Supabase Auth email confirmation, Google OAuth consent/scopes, database policies and Vercel environment variables.
- The original marketing landing page is retained as `index.html`, while the Next.js app's root route is the CRM workspace.