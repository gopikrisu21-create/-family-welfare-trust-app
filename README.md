# Family Welfare Trust App

A self-contained, installable (PWA) app for the Thankam Karunnaakara Pilla
Family Welfare Trust. All data (people, photos, the trust deed, items,
occasions) is stored only on the device it's used on, inside the browser's
local storage — nothing is uploaded anywhere.

## Deploying on Vercel

1. Go to vercel.com and log in (or create a free account).
2. Click "Add New" → "Project" → "Deploy" and choose "Upload" (or drag this
   whole folder onto the Vercel dashboard) — no GitHub repo is required.
   Alternatively, if you have the Vercel CLI: run `vercel` from inside this
   folder and follow the prompts, then `vercel --prod` to go live.
3. Once deployed, open the given `https://your-project.vercel.app` link.
4. Open Menu → **Install App** inside the app for a one-tap install button
   (Android/desktop Chrome/Edge) or step-by-step Add-to-Home-Screen
   instructions (iPhone/iPad Safari).

## Using it on two devices (you + your wife)

Since all data lives locally on each device, your phone/PC and her phone
will have **separate, independent copies** of the app once each is
installed from the same link. If you want her institute's data kept
completely separate from your trust data, that's exactly what happens
automatically — nothing is shared between installs unless you use
Menu → Backup & Restore to move a backup file between devices.

## Files

- `index.html` — the whole app (unchanged functionally from the browser
  version, plus the install-app support).
- `manifest.json` — tells the phone the app's name, icon, and that it
  should open full-screen like a native app.
- `sw.js` — service worker; caches the app shell so it loads and works
  fully offline, even before the first launch after install.
- `icons/` — app icons in all sizes Android/iOS expect (teal
  clipboard-and-checkmark design), plus a favicon.
- `vercel.json` — minor header tweaks recommended for PWAs on Vercel.

No build step, no dependencies — it's plain static files.
