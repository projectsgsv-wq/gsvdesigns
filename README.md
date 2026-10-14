# GSV Designs (gsvdesigns.com)

All-in-one AI video studio for social media marketing.
Create. Edit. Promote. Publish.

## Stack
- Next.js 14 (App Router) + TypeScript
- Tailwind CSS
- Supabase (auth + database)
- FFmpeg workers (rendering) — integrate later
- AI APIs (text-to-video, TTS, transcription)

## Quick start
```bash
npm install
cp .env.example .env.local
npm run dev
```
Open http://localhost:3000

## Routes
- `/` — landing page
- `/login`, `/signup`
- `/dashboard` — studio shell
  - `/dashboard/ai-video-maker`
  - `/dashboard/editor`
  - `/dashboard/social-ads`
  - `/dashboard/voice-captions`
  - `/dashboard/brand-kit`
  - `/dashboard/planner`
  - `/dashboard/projects`
  - `/dashboard/media-library`
  - `/dashboard/templates`
  - `/dashboard/analytics`
  - `/dashboard/team`
  - `/dashboard/settings`
  - `/dashboard/billing`

## Roadmap
1. MVP: auth, editor, templates, export
2. AI: text-to-video, voice, subtitles, campaign variations
3. Automation: publishing, scheduling, analytics, billing

## Deploy
See **DEPLOY.md** for step-by-step GitHub → Vercel → domain instructions.

Without Supabase keys, the app runs in demo mode (login goes straight to the dashboard).