# Changelog

All notable changes to Statly will be documented here. Format loosely follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [12.9.70] — current

TikTok host permissions, manifest, background routing, and popup platform picker are current as of this build. TikTok analytics now covers Audit, Compare, Merge, Watchlist, Trend Finder, KPIs, and Charts — matching Instagram feature-for-feature.

## [12.8.2] — Sync latest Instagram changes from production

- Brought the production Instagram dashboard up to date with two Web Store changes:
  1. Thumbnail fallback chain: when a signed CDN URL 403s, fall back to a session-redirect URL, then a grey placeholder.
  2. "Trial ended" modal: shows once after the 7-day trial expires, with an Upgrade path to Lemon Squeezy.
- TikTok files, manifest, background, and popup wiring unchanged in this release.

## [12.8.1] — Fix chart sizing (TikTok)

- Charts now render at fixed, Instagram-style heights (line ~320px, scatter ~280px, cumulative ~220px, pareto ~190px, time ~220px) instead of scaling height with width, so each chart fills its row without ballooning vertically.

## [12.8.0] — Audit KPIs + Charts (TikTok)

- **KPIs tab**: Basic KPIs (Total/Avg/Median Views, Likes, Comments; Total Posts; Avg Daily Posts; Median Duration) plus Executive KPIs (VTFR, RCI, HPF, BPR, ER, ESI, CR, AER, ARD, SDD, DP, BRR) — identical formulas to Instagram.
- **Charts tab**: Performance Over Time (metric toggle), Posting Activity Heatmap, Posting Time Distribution, Engagement Rate vs Views scatter, Cumulative Views Growth, Top 20% Views Share (Pareto), Performance Tier Dot Matrix — all with hover tooltips.

## [12.7.2] — Audit post cards match Instagram sizing + hover (TikTok)

- Rebuilt post cards to Instagram's exact compact grid layout, tinted metric bars, and smaller typography.
- Added Instagram's hover "lift" effect (card raises with a soft shadow) on each post card.

## [12.7.1] — Audit full-screen (TikTok, matches Instagram)

- Audit is now a full-screen feature like on Instagram: the sidebar hides during Audit, replaced by a minimal top bar (logo · ← Home · close).
- Loading screen rebuilt to match Instagram exactly: spinner ring + "Analyzing" + gradient progress bar, full-screen.

## [12.7.0] — Audit dashboard: Posts tab (TikTok)

- Audit results now render as a full report dashboard (matching the Instagram Reels tab): dark header with avatar, @handle, Followers/Likes/Videos counts, Posts/KPIs/Charts tabs, and New Scan.
- Toolbar: Sort By (views/likes/comments/shares/saves/engagement/newest/oldest), Copy, Export, post count.
- Ranked post cards with proportional metric bars for Views, Likes, Comments, Shares, Saves, Engagement Rate, and Duration.
- Copy (clipboard summary) and Export (CSV including engagement %) both shipped. KPIs/Charts tabs were stubbed here and shipped in 12.8.0.

## [12.6.0] — Watchlist & Trend Finder (TikTok)

- **Watchlist**: add creators (saved across sessions); "Scan watchlist" sweeps them in one tab and returns a per-account summary (followers, total videos, scanned, avg views, best views), cached with a "Last scanned …" indicator.
- **Trend Finder**: add creators (saved); "Find trends" sweeps them and pools their videos into one table sorted by views (top 50) — the current best performers across the list.
- Both reuse the same one-tab sweep with an "X of N" progress loader as Compare/Merge. Default 30 videos/account.

## [12.5.0] — Compare & Merge (TikTok)

- **Compare**: enter two creators, scan both, and see two result tables side by side.
- **Merge**: add 2–6 creators, scan all, and get one combined table (with an Account column) sorted by views, plus per-account badges.
- Both sweep through creators using a single reused foreground tab behind the Statly loading screen with an "X of N" counter — no tab-per-profile.

## [12.4.0] — Cross-profile TikTok scanning

- Type any @username in Audit and scan it without needing to already be on that profile.
- Under the hood: a background "ghost" tab briefly opens the target profile, captures TikTok's own signed request, paginates in the background, then closes.
- If you're already viewing the target profile, Statly still uses the faster in-page path.

## [12.3.0] — Initial TikTok support

- First TikTok build: host permissions for tiktok.com and its CDNs, a self-contained TikTok dashboard and scanner, and an updated "Choose a feed" picker (Instagram + TikTok).
- Captures TikTok's own `/api/post/item_list/` request and paginates by cursor, reusing TikTok's session signature.
- MVP scope: scans the profile currently being viewed; sidebar shows Audit only, with Compare/Merge/Watchlist marked "Soon" (shipped in 12.5.0–12.6.0 above).

## [1.0.0] — Initial public release (Instagram)

- Audit, Compare, Merge, Watchlist, and Trend Finder dashboards for Instagram.
- Executive KPIs: View-to-Follower Ratio, Breakout Rate, Duration Payoff, and more.
- Save Reels to a personal library; export/copy to spreadsheet; one-click MP4 download.
- Statly API for Pro users; free tier of 3 scans/day, last 30 Reels.
- Pro Monthly and Pro Yearly plans via Lemon Squeezy; viewer seats for read-only team sharing; dark mode.

---

### How to use this changelog

- Add a new `## [version] — description` section at the top for every release.
- Group changes under `Added`, `Changed`, `Fixed`, `Removed`, and `Deprecated` where useful.
- Link the version heading to the relevant Chrome Web Store update or release notes if available.
