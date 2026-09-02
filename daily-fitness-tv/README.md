# Daily Fitness TV — Roku runtime assets

Served at `https://hastech.online/daily-fitness-tv/` via GitHub Pages (hastech.online).

Only large **decorative** images live here so the Roku channel package stays
under Roku's 4 MB limit (Static Analysis Requirement 3.7). Channel icons and the
splash screens remain bundled locally in the Roku package, as Roku requires.

- `manifest.json` — hosting contract / documentation.
- `v1/images/` — full-screen backgrounds, downloaded by the app at runtime:
  - `home_background.jpg` — shared background behind Home/Categories/Programs/Profile/etc.
  - `onboarding_1.jpg`, `onboarding_2.jpg`, `onboarding_3.jpg` — first-run onboarding pages.
- `placeholder.png` — tiny fallback.

Not hosted here: Dailymotion video/playlist data & playback (unchanged), channel
icons, splash screens, in-app logo.

To publish updated art without a Roku rebuild: overwrite the files in `v1/images/`
(keep the names), commit, push. For a new asset set, add `v2/` and bump
`REMOTE_ASSET_VERSION` in `components/lib/RemoteAssets.brs`.
