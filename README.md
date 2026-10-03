# QRX — Interactive QR Experience Platform

A polished starter platform for creating QR codes that open games, quizzes, music, cards, image choices and other web experiences.

## What is included

- Mobile-first public landing page
- Private Supabase-authenticated admin area
- Create experiences
- Experience types: music, quiz, game, cards, choice, custom
- Stable public URLs such as `/e/my-qr`
- QR PNG generation from the admin dashboard
- Public experience pages
- Visit counter RPC
- Supabase Row Level Security policies
- Ready for Next.js/Vercel deployment

## Important

This project is intentionally structured for a real hosted application. It is not a fake "password hidden in JavaScript" admin panel.

You must connect it to your own Supabase project before public deployment.

## Setup

1. Install Node.js 20+.
2. Create a free Supabase project.
3. In Supabase, open SQL Editor and run `supabase/schema.sql`.
4. Copy `.env.example` to `.env.local`.
5. Put your Supabase URL and anon/publishable key in `.env.local`.
6. Run:

   npm install
   npm run dev

7. Open `http://localhost:3000`.
8. Open `/admin` and create the account you will use to manage experiences.
9. Create your first experience and download its QR PNG.

## Deploy

The normal production path is:

GitHub → Vercel → Supabase

Add the same environment variables to your Vercel project.

## Spotify note

A website cannot bypass Spotify's playback rules. For music experiences, use Spotify links/embeds or other legally permitted playback methods. Do not try to copy or host Spotify audio files yourself.

## Extending the builder

The current schema stores flexible JSON in `content`, so new experience types can be added later without redesigning the entire database.

Recommended future additions:
- drag-and-drop quiz builder
- timed games
- leaderboards
- analytics dashboard
- QR branding/logo controls
- password-protected experiences
- scheduled activation
- custom themes
- richer Spotify embed handling
- image upload storage
- custom domains
