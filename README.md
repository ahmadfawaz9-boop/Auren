# AUREN — Workout Tracker (GitHub Pages edition)

## One-time setup (no Netlify)

1. Create a free account at https://github.com if you don't have one.
2. Create a **public** repository named `auren-workout-tracker` (or any name).
3. In the repository choose **Add file → Upload files**. Upload the **individual files** from this folder (`index.html`, `app.js`, `style.css`, `sw.js`, `manifest.webmanifest`, `icon.svg`, `exercise-placeholder.svg`, `.nojekyll`); do **not** upload the enclosing folder or ZIP as a single file. Commit the changes.
4. Open **Settings → Pages → Build and deployment**. Set **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)**, and save.
5. Wait for GitHub Pages to publish. Your address will be `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.
6. On Samsung Chrome, open the address, then choose **⋮ → Add to Home screen → Install** (wording may vary).

## Updating the app without reinstalling

When you request a change, updated files can be provided here. Upload the changed files to the **same GitHub repository**, replacing the existing files and committing them. GitHub Pages redeploys automatically. On the next online launch or when you return to the app, its service worker checks for updates. A page reload may be needed before new UI appears. **There is no need to reinstall the home-screen app.**

This is **not** automatic publishing by ChatGPT: you still need to upload changed files unless you connect an authorized deployment workflow. The installed app can fetch updates, but ChatGPT cannot independently push code to your GitHub account from this chat.

## Your data

Workout history, weights, reps, custom exercises, plans, and photos are saved locally in your browser's `localStorage`. Ordinary code updates on the **same origin and path** preserve them. Do not rename the repo, change domains, clear site storage, or use a different browser unless you first export a backup. Go to **Settings → Export backup** regularly. Import backup restores your data if needed. A new app version should preserve the data schema; complex future changes may require a migration.

## Included features

- Four-day beginner Upper/Lower routine, six exercises/day
- Set-level kg and reps tracking, active workout recovery, history and personal records
- Exercise library filtered by muscle, replacement suggestions and custom exercises
- Weekly planner with recommended splits and exercise counts
- Rest timer, progress chart, JSON export/import
- Premium black-and-blue mobile layout and offline-capable PWA shell

**Exercise photos:** Default images are linked to a third-party public repository, so some may fail or be unavailable offline. The app shows a fallback illustration and supports uploading your own photos for local storage. A fully verified bundled photo library is **not** included.

## Notes

- GitHub Pages hosting requires the repository to be public on GitHub Free; avoid uploading private workout logs or personal files to the repository.
- Core app works offline after the first successful visit. GitHub Pages is HTTPS and free for this use case, subject to GitHub's service limits.
- This version does not sync data across devices. Back up before changing phones.

## Branding and data migration
AUREN uses the supplied A + wave logo for its icons. The app retains the previous `form_tracker_v1` localStorage key intentionally, so an update on the **same GitHub Pages URL** keeps your existing workout records. Do not change the repository URL if you already installed FORM without first exporting a backup. Existing installations may retain their old icon/name until Chrome refreshes the installed app metadata; reinstalling is sometimes required to change the launcher label, but not for routine feature updates.
