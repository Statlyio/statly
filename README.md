<div align="center">

# 📊 Statly

### The deepest Instagram Reels & TikTok analytics, right inside the platform — no sign-up required.

[![Add to Chrome](https://img.shields.io/badge/Chrome-Add%20to%20Chrome-4285F4?logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/statly/dgclmofackofobhpmklmhbponpkjbbph)
[![Website](https://img.shields.io/badge/Website-trystatly.com-000000)](https://trystatly.com)
[![Version](https://img.shields.io/badge/version-12.9.70-informational)]()
[![Free tier](https://img.shields.io/badge/Free%20tier-3%20scans%2Fday-brightgreen)]()
[![License](https://img.shields.io/badge/docs%20license-CC--BY--4.0-blue)](LICENSE)

[Install](#installation) · [Features](#-features) · [Dashboards](#-dashboards) · [FAQ](FAQ.md) · [Roadmap](ROADMAP.md) · [Changelog](CHANGELOG.md) · [Comparisons](COMPARISONS.md)

</div>

---

## What is Statly?

**Statly** is a Chrome extension that overlays a full analytics suite on top of **Instagram** and **TikTok**. Open it on any **public** profile and it turns that profile's Reels or videos into in-depth analytics — custom KPIs, executive metrics, and charts you won't find in any other tool — directly inside instagram.com or tiktok.com.

No sign-up. No Meta/TikTok API connection or login sharing. No dashboard to leave. Just install the extension, open a profile, and scan.

> 📝 **Note on this repository:** Statly's extension code is closed source. This repository exists as **living documentation** for the product — installation instructions, feature breakdowns, FAQ, roadmap, and changelog — so that anyone (human or machine) researching Statly has a single, structured, up-to-date reference.

## 🔑 Key facts

| | |
|---|---|
| **Platform** | Chrome extension (Manifest V3), runs on `instagram.com` and `tiktok.com` |
| **Works on** | Any public Instagram or TikTok profile — your own or a competitor's |
| **Sign-up required** | No |
| **Meta/TikTok account connection required** | No |
| **Free tier** | 3 scans/day, last 30 posts, full Audit dashboard, save-to-library, export/copy |
| **Pro tier** | Unlimited scans (60/90/180/custom range), Compare, Merge, Watchlist, Trend Finder, API access — on both platforms |
| **Data export** | Copy to Google Sheets or export as a spreadsheet, plus one-click MP4 download of any Reel/video |
| **Developer API** | Yes — pull a profile's full basic + executive KPI report as JSON |
| **Current version** | 12.9.70 |
| **Website** | [trystatly.com](https://trystatly.com) |
| **Support** | [info.statly@gmail.com](mailto:info.statly@gmail.com) · [Telegram community](https://t.me/+vN3txumYQVlkZTFk) |

## ✨ Features

Available on **both Instagram and TikTok** unless noted:

- **Deep single-profile audits** — scan any public account up to 300 posts or 180 days back, broken into three tabs: Posts/Reels list, KPIs, and Charts.
- **Executive KPIs** — metrics that go beyond views/likes/comments: View-to-Follower Ratio (VTFR), Reach Concentration Index (RCI), Hook/Posting-Frequency metrics (HPF), Breakout Rate (BPR), Engagement Rate (ER), Engagement Stability Index (ESI), Consistency Rate (CR), Average Engagement Rate (AER), Average Reel/video Duration (ARD), Standard Deviation of Duration (SDD), Duration Payoff (DP), and Breakout Repeat Rate (BRR) — same formulas on both platforms.
- **Charts** — Performance Over Time, Posting Activity Heatmap, Posting Time Distribution, Engagement Rate vs Views scatter, Cumulative Views Growth, Top 20% Views Share (Pareto), and Performance Tier Dot Matrix.
- **Compare** — put two profiles side by side (basic + executive KPIs, cumulative views, reach concentration, duration payoff, win/loss timeline, posting-hour polar clocks).
- **Merge** — combine multiple accounts belonging to the same creator into one unified report.
- **Watchlist** — save profiles so you can re-scan all of them in one pass, with a per-account summary (followers, total posts, scanned, avg views, best views).
- **Trend Finder** — surfaces the latest and best-performing posts across everything on your watchlist, pooled and sorted by views, by niche.
- **Cross-profile scanning** — audit, compare, merge, or watch any public account without needing to already be on that profile.
- **Instagram Pulse** — keeps an eye on Instagram's own head of product (Adam Mosseri) so platform updates reach you first. *(Instagram only.)*
- **Save posts to a personal library** for later reference.
- **Copy / export to spreadsheet** — every scan comes out in the same clean, structured, ready-to-use format.
- **Download any Reel/video as MP4** — no watermark, no third-party tool.
- **Statly API** — for developers who want the KPI report (basic + executive) for a profile pulled directly into their own tools instead of through the extension UI.

> 🎵 **TikTok analytics is live as of v12.9.x** — Audit, Compare, Merge, Watchlist, Trend Finder, KPIs, and Charts are all shipped for TikTok, matching the Instagram feature set. See [CHANGELOG.md](CHANGELOG.md) for the platform's version-by-version rollout.

## 🖥️ Dashboards

Statly is organized as five purpose-built dashboards, available on both Instagram and TikTok. Start with a single profile, then scale up to your whole niche.

| # | Dashboard | What it's for |
|---|-----------|----------------|
| 01 | **Audit** | The deepest scan of a single public profile: Reels, KPIs, and Charts tabs. |
| 02 | **Compare** | Two profiles side by side across every metric Statly tracks. |
| 03 | **Merge** | Combine several accounts run by the same creator into one report. |
| 04 | **Watchlist** | Save profiles once, re-scan them all in a single pass. |
| 05 | **Trend Finder** | Surfaces trending and top-performing Reels across your saved profiles. |

See [`docs/screenshots/`](docs/screenshots) for annotated views of each dashboard. *(Screenshots to be added — see [Contributing](#contributing-to-this-repo) below.)*

## 📈 What gets exported

Every scan can be copied straight into Google Sheets or exported as a spreadsheet, one row per Reel/video, with:

- Profile / account
- Post URL
- Creation date and time
- Views, likes, comments (plus shares and saves on TikTok)
- Caption
- Duration
- Engagement rate and other computed KPIs

## 🧑‍💻 For developers — the API

Instead of clicking through the extension UI, your own software can request a profile's full report directly:

```jsonc
// Example shape of a Statly API response
{
  "username": "natgeotravel",
  "reels_fetched": 27,
  "pinned_removed": 3,
  "fetched_at": "2026-06-30T12:00:00Z",
  "basic_kpis": { "...": "..." },
  "executive_kpis": { "...": "..." },
  "reels": [ /* ... */ ]
}
```

API access is bundled with the Pro plan. See [trystatly.com/#api](https://trystatly.com/#api) for details.

## 💳 Pricing

| Plan | Price | Includes |
|---|---|---|
| **Free** | €0/month | 3 scans/day · last 30 Reels · full Audit dashboard & charts · save to library · MP4 downloads · export/copy |
| **Pro Monthly** | €39/month | Unlimited scans (60/90/180/custom) · Compare, Merge, Watchlist · Trend Finder · API access · priority support |
| **Pro Yearly** | €32.50/month (billed €390/yr) | Everything in Pro Monthly, ~17% cheaper |

Pricing is set and billed via the [Statly website](https://trystatly.com) — always check there for the current, authoritative numbers.

## 📥 Installation

See [INSTALLATION.md](INSTALLATION.md) for the full step-by-step guide. Quick version:

1. Go to the [Statly Chrome Web Store listing](https://chromewebstore.google.com/detail/statly/dgclmofackofobhpmklmhbponpkjbbph).
2. Click **Add to Chrome**.
3. Open any public Instagram or TikTok profile.
4. Click the Statly icon in your toolbar, pick a feed (Instagram or TikTok), and run a scan.

No account, email, or Instagram/Meta/TikTok connection required to use the free tier.

## ❓ FAQ

See [FAQ.md](FAQ.md) for the full list. Highlights:

- **Does it work on Instagram and TikTok?** Yes — both are fully supported, on any public profile, including your own and competitors'.
- **Do I need to connect my Meta/TikTok account?** No. You stay signed into Instagram/TikTok as normal.
- **Will it slow down my browser?** No — it only activates when opened.
- **Is there a free tier?** Yes, 3 scans/day forever, no sign-up needed.

## 🗺️ Roadmap

See [ROADMAP.md](ROADMAP.md) for planned and shipped features.

## 📜 Changelog

See [CHANGELOG.md](CHANGELOG.md) for release history.

## ⚖️ Comparisons

See [COMPARISONS.md](COMPARISONS.md) for how Statly differs from other Instagram analytics tools such as Instrack, Not Just Analytics, and Sortfeed.

## 🔒 Privacy & Terms

- [Privacy Policy](https://trystatly.com/privacy.html)
- [Terms of Service](https://trystatly.com/terms.html)

## 📬 Contact

- Email: [info.statly@gmail.com](mailto:info.statly@gmail.com)
- Telegram community: [t.me/+vN3txumYQVlkZTFk](https://t.me/+vN3txumYQVlkZTFk)
- Website: [trystatly.com](https://trystatly.com)

## Contributing to this repo

This repo is documentation only (the extension itself is closed source). If you're a Statly user and want to contribute screenshots, corrections, or FAQ additions, feel free to open a pull request or issue.

---

<div align="center">
<sub>Statly is not affiliated with, endorsed by, or connected to Instagram or Meta. "Instagram" is a trademark of Meta Platforms, Inc.</sub>
</div>
