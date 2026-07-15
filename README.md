# Now & Next — Setup Guide

## What's new in this version
- Each lesson can have its own background picture (tap a lesson in the
  config screen, then "Choose picture"). It shows behind the Now/Next tile
  with a dark overlay so the text stays easy to read.
- The **Next** tile is now bigger and more prominent than the **Now** tile.
- Text and spacing automatically scale to fit whatever screen it's opened
  on — phone, tablet, or a small watch-size browser — no manual switch
  needed.
- Pictures are stored on-device only (same as your timetable) — nothing is
  uploaded anywhere.

This folder is a complete, working app. You don't need to write or edit any
code — just follow the steps for the option you want.

---

## Option A: Get it installable on phones/tablets (recommended first step)

This uses **GitHub Pages**, a free hosting service. No coding, just uploading
files through a website.

1. Go to https://github.com and create a free account (if you don't have one).
2. Click the **+** icon top-right → **New repository**.
   - Name it something like `now-and-next`.
   - Set it to **Public**.
   - Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Drag in every file from this folder (`index.html`, `manifest.json`,
   `service-worker.js`, `README.md`, and the whole `icons` folder) and click
   **Commit changes**.

   > If you already have a previous version hosted, just upload these files
   > into the same repository — GitHub will ask to replace the old ones.

5. Go to the repository's **Settings** tab → **Pages** (left sidebar).
6. Under "Branch", choose `main` and folder `/ (root)`, then **Save**.
7. Wait about a minute, then refresh — GitHub will show you a live URL like:
   `https://yourusername.github.io/now-and-next/`
8. Open that URL on your phone:
   - **Android (Chrome)**: tap the **⋮** menu → "Install app" or "Add to Home
     screen".
   - **iPhone/iPad (Safari)**: tap the **Share** icon → "Add to Home Screen".
9. It now behaves like a real app: its own icon, opens full-screen, and keeps
   working even with no internet connection.

If you already had the app installed from before, reopen it once while
connected to the internet — it will quietly update itself to this new
version in the background.

Anyone you send that same URL to can install it too — each person's
timetable and pictures stay private to their own device.

---

## Option B: Get a sideload-able Android APK

Once your app is live at a URL (from Option A):

1. Go to https://www.pwabuilder.com
2. Paste in your GitHub Pages URL and click **Start**.
3. Click **Package for stores** → choose **Android**.
4. Keep the default settings and click **Generate** — it will download a
   `.zip` file containing an `.apk` (and an `.aab` for the Play Store later).
5. Transfer the `.apk` to an Android phone (email it to yourself, or use a
   USB cable) and tap it to install. You may need to allow
   "Install unknown apps" for whichever app you used to open the file —
   Android will prompt you for this the first time.

---

## Option C: Publish to the Google Play Store (when you're ready)

1. Create a Google Play Console account at https://play.google.com/console
   (one-time $25 registration fee).
2. Use the `.aab` file from the PWABuilder step above (Option B, step 4).
3. Follow Play Console's guided setup: app name, screenshots, description,
   content rating questionnaire, and privacy policy link (a one-page note
   saying the app stores your timetable and pictures only on your own
   device is enough, since there's no server involved).
4. Submit for review. Google typically takes a few days to approve new apps.

More detail on the Android packaging step:
https://docs.pwabuilder.com/#/builder/android

---

## Making changes later

If you ever want to tweak colors, text, or behavior, just edit `index.html`
in a text editor and re-upload it to GitHub (drag the new version in the same
way as step 4 above — it will ask to replace the old one). Everyone's
installed app will pick up the update automatically next time they open it
with an internet connection.
