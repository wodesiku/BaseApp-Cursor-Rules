# Farcaster Mini App Development Guide

Use this document as a template to build a functional Farcaster Mini App. Use the `@` symbol to load your specific project documents into the cursor context.

---

## APPLICATION IDEA:
[WRITE YOUR APP IDEA HERE]

---

## FILE STRUCTURE:
```text
project/
├── index.html
├── style.css
├── game.js
├── icon.html
├── package.json
└── .well-known/
    └── farcaster.json
```
*Note: The structure may vary depending on the app but should remain Farcaster-compatible and unchanged unless necessary.*

---

## TECHNICAL REQUIREMENTS:

### index.html:
- Meta tag: `<meta name="fc:frame" content="vNext">`
- Meta tag: `<meta name="base:app_id" content="[TO BE ADDED LATER]">`
- Mobile viewport: `maximum-scale=1.0, user-scalable=no`
- Script: `type="module"`

### game.js:
- Initialize Farcaster SDK:
  `import { sdk } from 'https://esm.sh/@farcaster/frame-sdk';`
  `sdk.actions.ready();`
- Implement mobile touch controls.

### icon.html:
- Use Canvas to generate a 200x200 `icon.png`.
- Use Canvas to generate a 600x400 `preview.png`.
- Include download links for both.

### package.json:
```json
{
  "name": "mini-app",
  "version": "1.0.0",
  "scripts": {
    "dev": "npx serve . -p 3000"
  },
  "devDependencies": {
    "serve": "^14.2.0"
  }
}
```

### farcaster.json:
```json
{
  "accountAssociation": {
    "header": "[TO BE OBTAINED FROM FARCASTER]",
    "payload": "[TO BE OBTAINED FROM FARCASTER]",
    "signature": "[TO BE OBTAINED FROM FARCASTER]"
  },
  "frame": {
    "version": "1",
    "name": "[APP NAME]",
    "subtitle": "[SHORT DESCRIPTION]",
    "description": "[DETAILED DESCRIPTION]",
    "iconUrl": "https://[DOMAIN]/icon.png",
    "homeUrl": "https://[DOMAIN]",
    "imageUrl": "https://[DOMAIN]/preview.png",
    "splashImageUrl": "https://[DOMAIN]/icon.png",
    "splashBackgroundColor": "#000000",
    "primaryCategory": "games",
    "tags": ["game", "arcade", "farcaster"],
    "tagline": "[MAX 30 CHARACTERS]",
    "heroImageUrl": "https://[DOMAIN]/preview.png",
    "screenshotUrls": ["https://[DOMAIN]/preview.png"],
    "ogTitle": "[OG TITLE]",
    "ogDescription": "[OG DESCRIPTION]",
    "ogImageUrl": "https://[DOMAIN]/preview.png"
  }
}
```

---

## ❌ DON'T:
- **Do not** use SVGs (PNG is required).
- **Do not** write long taglines.
- **Do not** add a `webhookUrl`.
- **Do not** add `noindex`.
- **Do not** add unnecessary features.

## ✅ DO:
- Keep it simple and functional.
- Add mobile touch controls.
- Ensure responsive design.

---

## LOCAL TESTING:
After completing the app, run these commands in the terminal:
```bash
npm install
npm run dev
```
Open `http://localhost:3000` in your browser to test.

Go to `http://localhost:3000/icon.html` to:
1. Click **"Download icon.png"**.
2. Click **"Download preview.png"**.
3. Move the downloaded files into your project folder.

---

## 🚀 INITIAL DEPLOY (GitHub + Vercel):
1. Create a new repo on GitHub.
2. Run the following commands:
```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin [REPO_URL]
git push -u origin main
```
3. Go to Vercel and connect your GitHub repo.
4. Copy the URL once the deployment is complete.

---

## FARCASTER VERIFICATION:
1. Go to [warpcast.com/~/developers/mini-apps](https://warpcast.com/~/developers/mini-apps).
2. Enter your URL and copy the `accountAssociation` details.
3. Paste these details into `farcaster.json`.
4. Replace all `[DOMAIN]` placeholders with your Vercel URL.

---

## BASE APP VERIFICATION:
1. Select "Add Mini App" in the Base App.
2. Enter your URL.
3. Copy the provided `base:app_id`.
4. Update the meta tag in `index.html`:
   `<meta name="base:app_id" content="[YOUR_ID]">`

---

## UPDATING AFTER CHANGES:
Run these commands after every update:
```bash
git add .
git commit -m "Update"
git push
```
Vercel will deploy the changes automatically.Commit 1 line - Randomly generated at 2025-06-10T06:04:55
Commit 2 line - Randomly generated at 2025-06-10T06:05:19
Commit 3 line - Randomly generated at 2025-06-10T06:06:48
Commit 4 line - Randomly generated at 2025-06-10T06:16:18
Commit 5 line - Randomly generated at 2025-06-10T06:17:11
Commit 6 line - Randomly generated at 2025-06-10T06:22:38
Commit 7 line - Randomly generated at 2025-06-10T06:29:51
Commit 8 line - Randomly generated at 2025-06-10T06:35:45
Commit 9 line - Randomly generated at 2025-06-10T06:38:28
Commit 10 line - Randomly generated at 2025-06-10T06:44:06
Commit 11 line - Randomly generated at 2025-06-10T06:45:23
Commit 12 line - Randomly generated at 2025-06-10T06:55:15
Commit 13 line - Randomly generated at 2025-06-10T07:06:59
Commit 14 line - Randomly generated at 2025-06-10T07:09:32
Commit 15 line - Randomly generated at 2025-06-10T07:15:23
Commit 16 line - Randomly generated at 2025-06-10T07:18:53
Commit 17 line - Randomly generated at 2025-06-10T07:19:39
Commit 18 line - Randomly generated at 2025-06-10T07:34:00
Commit 19 line - Randomly generated at 2025-06-10T07:37:29
Commit 20 line - Randomly generated at 2025-06-10T07:41:08
Commit 21 line - Randomly generated at 2025-06-10T07:46:04
Commit 22 line - Randomly generated at 2025-06-10T07:47:50
Commit 23 line - Randomly generated at 2025-06-10T07:56:31
Commit 24 line - Randomly generated at 2025-06-10T08:05:25
Commit 25 line - Randomly generated at 2025-06-10T08:05:35
Commit 26 line - Randomly generated at 2025-06-10T08:10:27
Commit 27 line - Randomly generated at 2025-06-10T08:15:11
Commit 28 line - Randomly generated at 2025-06-10T08:25:45
Commit 29 line - Randomly generated at 2025-06-10T08:28:08
Commit 30 line - Randomly generated at 2025-06-10T08:29:31
Commit 31 line - Randomly generated at 2025-06-10T08:32:48
Commit 32 line - Randomly generated at 2025-06-10T08:34:26
Commit 33 line - Randomly generated at 2025-06-10T08:35:41
Commit 34 line - Randomly generated at 2025-06-10T08:39:07
Commit 35 line - Randomly generated at 2025-06-10T08:49:15
Commit 36 line - Randomly generated at 2025-06-10T09:03:42
Commit 37 line - Randomly generated at 2025-06-10T09:07:47
Commit 38 line - Randomly generated at 2025-06-10T09:09:38
Commit 39 line - Randomly generated at 2025-06-10T09:17:32
Commit 40 line - Randomly generated at 2025-06-10T09:20:45
Commit 41 line - Randomly generated at 2025-06-10T09:25:42
Commit 42 line - Randomly generated at 2025-06-10T09:25:59
Commit 43 line - Randomly generated at 2025-06-10T09:29:25
Commit 44 line - Randomly generated at 2025-06-10T09:33:39
Commit 45 line - Randomly generated at 2025-06-10T09:34:09
Commit 46 line - Randomly generated at 2025-06-10T09:36:30
Commit 47 line - Randomly generated at 2025-06-10T09:37:25
Commit 48 line - Randomly generated at 2025-06-10T09:50:03
Commit 49 line - Randomly generated at 2025-06-10T09:50:31
Commit 50 line - Randomly generated at 2025-06-10T09:51:57
Commit 51 line - Randomly generated at 2025-06-10T10:02:59
Commit 52 line - Randomly generated at 2025-06-10T10:03:33
Commit 53 line - Randomly generated at 2025-06-10T10:08:51
Commit 54 line - Randomly generated at 2025-06-10T10:14:31
Commit 55 line - Randomly generated at 2025-06-10T10:23:26
Commit 56 line - Randomly generated at 2025-06-10T10:30:08
Commit 57 line - Randomly generated at 2025-06-10T10:52:36
Commit 58 line - Randomly generated at 2025-06-10T10:55:07
Commit 59 line - Randomly generated at 2025-06-10T10:55:40
Commit 60 line - Randomly generated at 2025-06-10T11:10:30
Commit 61 line - Randomly generated at 2025-06-10T11:17:13
Commit 62 line - Randomly generated at 2025-06-10T11:26:24
Commit 63 line - Randomly generated at 2025-06-10T11:30:25
Commit 64 line - Randomly generated at 2025-06-10T11:37:20
