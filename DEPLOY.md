# How to put gsvdesigns.com online

## 1. Run it on your computer (optional, to test)
1. Install Node.js 20 LTS from https://nodejs.org
2. Unzip this folder, open a terminal inside it, then run:
   ```
   npm install
   cp .env.example .env.local      (Windows: copy .env.example .env.local)
   npm run dev
   ```
3. Open http://localhost:3000

Without Supabase keys the site runs in **demo mode**: Log in / Sign up go straight to the dashboard.

## 2. Upload the code to GitHub
1. Create a free account at https://github.com
2. Click **New repository** → name it `gsvdesigns` → Create.
3. Click **uploading an existing file**, drag in everything from this folder
   (NOT `node_modules` or `.next` if they exist) → **Commit changes**.

## 3. Deploy on Vercel (free)
1. Go to https://vercel.com → **Sign up with GitHub**.
2. **Add New → Project** → pick `gsvdesigns` → **Import**.
3. Framework is detected as Next.js. Click **Deploy**.
4. In about 1–2 minutes you get a live link like `gsvdesigns.vercel.app`.

## 4. Turn on real accounts (Supabase)
1. Create a project at https://supabase.com
2. Project Settings → API → copy **Project URL** and **anon public key**.
3. In Vercel: Project → Settings → **Environment Variables**, add:
   - `NEXT_PUBLIC_SUPABASE_URL` = your Project URL
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY` = your anon key
4. Deployments → ⋯ → **Redeploy**.
5. In Supabase → Authentication → URL Configuration, set Site URL to `https://gsvdesigns.com`.

## 5. Connect your domain gsvdesigns.com
1. Vercel → Project → Settings → **Domains** → add `gsvdesigns.com` (and `www.gsvdesigns.com`).
2. At your domain registrar (GoDaddy, Namecheap, etc.) add the DNS records Vercel shows, usually:
   - `A` record, host `@`, value `76.76.21.21`
   - `CNAME` record, host `www`, value `cname.vercel-dns.com`
3. Wait 5 min – a few hours. Vercel adds HTTPS automatically.

## Updating the site later
Edit files on GitHub (or push from your computer). Vercel redeploys automatically on every change.
