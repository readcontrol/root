# Changelog

All notable changes to ReadControl (the macOS app users download) are recorded
here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and versions track the app's `CFBundleShortVersionString`. See
[RELEASE.md](./RELEASE.md) for how a release is cut.

## 0.3.0 - 2026-09-16

### Added

- Settings › Typography can now set the reader's **Width** — the measure the
  article is laid out to — from Extra Small (520 pt) through Extra Large
  (960 pt), with Medium (680 pt) the previous fixed value and still the default.
- Settings › Typography can now set the reader's **Line Height** — Tight, Snug,
  Normal, Relaxed, or Loose (1.25 to 2.25 in even quarter-steps), with Normal
  (1.75) the previous fixed value and still the default.
- The Typography settings show a live sample that reflects the chosen font, size,
  width, and line height together.
- Both are also adjustable from the appearance popover at the bottom of the
  sidebar, without opening Settings: two icon-capped sliders matching the
  font-size slider already there.
- The reader now **remembers where you stopped** and opens an article at that
  paragraph. The point is anchored to a block of the article, not to a scroll
  height, so it holds after you change the font, size, width, or line height.
  It is stored beside the article in your library, so it travels with your
  files to your other devices.
- Reaching the **end of an article marks it read** and clears the saved point.
  The article stays open, even in the Unread view, where its row leaves the list.
  A short article that fits on screen is never marked read on its own — you
  have to scroll it.
- Reopening the app **opens the article you were reading**, even when the list
  doesn't show it — it is further down than the first page, or outside the
  view you reopen on. If that article was deleted, the app opens the first one
  in the list, as before.

### Changed

- The sidebar filters now narrow in order — smart view, then rating, then tag,
  as the sidebar reads top to bottom. Changing one clears the narrower ones
  below it, so switching from ★5 to ★4 drops the tag you had applied, and
  going from Read back to All drops both. Previously they changed
  independently, which left the list scoped by a combination you hadn't asked
  for — often empty, for a reason hidden in a collapsed section.

### Fixed

- The article header now shares the reader's measure instead of a fixed 680 pt,
  so the title stays flush with the body copy at every width.

## 0.2.0 - 2026-08-10

### Added

- Onboarding and Settings › Extensions link to the browser extension on the
  Chrome Web Store and Firefox Add-ons, now that the listings are public.

### Changed

- Onboarding is now a compact two-step sheet (choose a library, then add the
  extension); the main window opens larger on first run and keeps the size you
  leave it at afterward.
- Refreshed the welcome article copy.

### Removed

- The bundled extension download and its load-unpacked (sideload) instructions,
  replaced by the store links above.

## 0.1.1 - 2026-08-07

### Added

- Onboarding step after choosing a library: download the browser extension and
  load it unpacked, with a link to the source at
  <https://github.com/readcontrol/extension>.
- Settings › Extensions offers the same extension download and load-unpacked
  instructions for Chrome/Edge/Brave and Firefox.

### Changed

- Settings › Extensions no longer links to the Chrome Web Store / Firefox Add-ons
  listings while the extension is still under review; it hands out the packaged
  download instead.

## 0.1.0

- Initial release: browse, read, search, tag, and rate your library; native
  SwiftUI reader; in-app updates via Sparkle.
