# QuitScroll — Social Media Liberation PWA

A 6-day evidence-based program to break free from social media addiction, integrating 8 therapeutic methods with voice narration.

## What's in this folder

```
quitscroll-pwa/
├── index.html      ← Main app (React + all content)
├── manifest.json   ← PWA manifest (app name, icons, theme)
├── sw.js           ← Service worker (offline support)
├── favicon.png     ← Browser tab icon
├── favicon.svg     ← Vector favicon
└── icons/
    ├── icon-192.png  ← App icon (192x192)
    └── icon-512.png  ← App icon (512x512)
```

## Deploy in 2 minutes (Vercel — recommended)

### Option A: Vercel Dashboard (no terminal needed)
1. Go to [vercel.com](https://vercel.com) and sign up (free)
2. Click **"Add New → Project"**
3. Choose **"Import Third-Party Git Repository"** OR just drag the `quitscroll-pwa` folder
4. Deploy — done! You get a URL like `quitscroll-xyz.vercel.app`
5. Optionally add a custom domain in Settings → Domains

### Option B: Vercel CLI
```bash
npm i -g vercel
cd quitscroll-pwa
vercel
```
Follow prompts. Live in 30 seconds.

### Option C: Netlify (also free)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the `quitscroll-pwa` folder onto the dashboard
3. Done — instant URL

### Option D: GitHub Pages
1. Create a GitHub repo
2. Push the contents of `quitscroll-pwa/` to the repo
3. Settings → Pages → Source: main branch → Save
4. Live at `yourusername.github.io/repo-name`

## How users install it as an app

Once deployed, users visit your URL on their phone and:

**Android:** Chrome shows an "Add to Home Screen" banner automatically, or tap the ⋮ menu → "Install app"

**iPhone:** Open in Safari → tap Share → "Add to Home Screen"

The app then:
- Appears on their home screen with the QuitScroll icon
- Opens fullscreen (no browser bar)
- Works offline after first visit
- Looks and feels like a native app

## Custom domain setup

For a professional URL like `quitscroll.com`:
1. Buy a domain (~$10/year from Namecheap, Google Domains, etc.)
2. In Vercel/Netlify, add the domain in project settings
3. Update DNS records as instructed (usually just add a CNAME record)

## Future improvements

- **Persistent storage:** Add localStorage or IndexedDB to save journal entries and progress across sessions
- **Push notifications:** Add daily reminders using the Push API
- **Analytics:** Add privacy-friendly analytics (Plausible, Umami) to track usage
- **Play Store listing:** Wrap with [Bubblewrap](https://github.com/nickvidal/nickvidal.github.io) (Google's TWA tool) to list as a Play Store app directly from the PWA — no code changes needed
