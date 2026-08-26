# PumpLog v2.4.3

A lightweight iPhone-friendly Progressive Web App (PWA) for daily arm feeder work and pull-ups.

## Color system

- Tangerine Tango: `#FF5B19`
- Charcoal: `#161616`
- Platinum: `#E5E3D2`
- Powder Blue: `#AECACD`

## Included

- Daily biceps, triceps and pull-up logging
- Streak tracking
- Workout history
- Progress overview
- 90-day challenge
- Local iPhone-safe date handling
- JSON backup/export
- JSON restore
- Offline PWA support
- iPhone Home Screen support and safe-area spacing

## Publish with GitHub Pages

1. Create a new **public** GitHub repository, for example `pumplog`.
2. Upload **the contents of this folder** to the repository root. `index.html` must be at the top level of the repository.
3. Commit the files to the `main` branch.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select `main` and `/ (root)`, then click **Save**.
7. Wait for GitHub Pages to publish the site.
8. Open the resulting HTTPS URL in Safari on the iPhone.
9. Tap **Share → Add to Home Screen → Add**.

Typical URL:

`https://YOUR-USERNAME.github.io/pumplog/`

## Future updates

When you change the app later:

1. Update the files in GitHub.
2. Increase the cache version at the top of `sw.js`, for example:

`pumplog-v2.3.0` → `pumplog-v2.3.1`

3. Commit the changes.

The service worker uses a network-first strategy for page navigation, so online launches prefer the newest `index.html`, while the app remains available offline.

## Data

Workout data is stored locally in the browser/PWA using `localStorage`. GitHub does not receive the workout history. Use **History → Backup / Export JSON** regularly. A backup can be restored with **History → Restore JSON Backup**.


## v2.1 changes
- Biceps now use one Repetitions field instead of separate left/right fields.
- Triceps now use one Repetitions field instead of separate left/right fields.
- Added optional Notes fields to Biceps and Triceps.
- History now displays Biceps, Triceps, and Pull-up notes.
- Old v2 backups with left/right rep fields remain import-compatible.


## v2.3 changes

- Added progression coaching for Biceps and Triceps.
- Rule: reach the recorded rep target for 3 consecutive sessions at the same working weight.
- After 3 successful sessions, the app recommends exactly +0.5 kg.
- No larger automatic weight jumps are suggested.
- Weight changes are recommendations only; the app never changes the user's entered weight automatically.
- A missed target at the same weight resets the consecutive-success run.
- Pull-up phase targets remain unchanged in v2.3.


## Pull-up progression (v2.3)

- Set an explicit **Target total reps** value.
- Hit or exceed that same target for **3 consecutive logged sessions**.
- PumpLog then recommends **exactly +2 total reps** for the next target.
- The app never changes the target automatically; the suggestion remains under your control.
- Changing the target starts a fresh 0/3 progression run. A miss at the same target resets the consecutive run.
- Older backups without a pull-up target remain importable; those old sessions are not retroactively counted toward the 3-session progression rule.

## v2.4.3 changes

- Simplified the app header to show only **PumpLog**.
- Removed the header emoji and the "Daily arms + pull-up feeder workouts" subtitle.
- Removed exercise emojis from Biceps, Triceps, Pull-ups, and their Progress/Plans headings.
- Reduced header height to show more workout content on iPhone.
- Updated the PWA cache to `pumplog-v2.4.3`.

- Added responsive progress charts for **Biceps**, **Triceps**, and **Pull-ups**.
- Biceps and Triceps charts plot working weight over the most recent 12 logged sessions.
- Pull-up chart plots total reps and shows the current target as a dashed reference line.
- Added summary metrics for each exercise, including target adherence, sessions, averages, bests, and totals.
- Added progression-history cards derived from recorded weight/target increases.
- Existing v2.3 logging, +0.5 kg arm progression, +2 rep pull-up progression, backup/restore, and PWA behavior remain unchanged.


- Added the PumpLog app icon to the in-app header beside the app name.
- Refreshed the PWA icon files in `icons/` with the new PumpLog logo.
- GitHub repository structure should keep the three app icons inside the `icons/` folder, not at the repository root.
