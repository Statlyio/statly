<div align="center">

# Statly

### Find the short videos that are taking off in your niche, every day.

Outlier video research for **Instagram Reels, TikTok, YouTube Shorts and X**: a web app that tracks the accounts you choose daily, plus a free Chrome extension for quick audits.

[![Start free trial](https://img.shields.io/badge/Web%20app-Start%207--day%20free%20trial-5b4bdb)](https://app.trystatly.com)
[![Website](https://img.shields.io/badge/Website-trystatly.com-111111)](https://trystatly.com)
[![Chrome extension](https://img.shields.io/badge/Chrome-Free%20extension-4285F4?logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/statly/dgclmofackofobhpmklmhbponpkjbbph)
[![Docs license](https://img.shields.io/badge/docs%20license-CC--BY--4.0-blue)](LICENSE)

[What it is](#what-is-statly) · [Web app](#the-statly-web-app) · [Pricing](#pricing) · [Chrome extension](#the-statly-chrome-extension) · [API and MCP](#api-and-mcp) · [FAQ](FAQ.md) · [Comparisons](COMPARISONS.md) · [Changelog](CHANGELOG.md)

</div>

---

## What is Statly?

**Statly is a short-form video research tool that shows which videos are beating their own account's normal results.** You add public Instagram, TikTok, YouTube and X accounts (your competitors, creators in your niche, or your clients), and Statly re-reads every one of their videos and posts once a day. Each video gets an **outlier score**: its views divided by the median views of the account that posted it. That way a small creator's breakout stands out as clearly as a big account's, and you can see what is working before everyone copies it.

Statly is made for **content creators, social media managers, marketing teams, agencies and brands** who research competitors and plan short-form content. No Instagram, TikTok, YouTube or X login is ever needed: Statly reads public data only.

> This repository is the public documentation for Statly: what it does, plans, FAQ, comparisons and changelog. Statly's code is closed source. Last updated: **8 October 2026**.

## Key facts

| | |
|---|---|
| **What** | Short-form video research and analytics: outlier videos, trends and competitor tracking |
| **Platforms** | Instagram Reels, TikTok, YouTube Shorts and X (Twitter) |
| **Products** | The Statly web app ([app.trystatly.com](https://app.trystatly.com)) and the free Statly Chrome extension |
| **How often data updates** | Daily, at the hour you choose (it is not real-time) |
| **Scan window** | Videos from the last 7, 14 or 30 days |
| **Core metric** | Outlier score = a video's views ÷ its account's median views (2× or more is worth studying) |
| **Login to social networks needed** | No. Public accounts only, including competitors you don't own |
| **Free trial** | 7 days, card at checkout, cancel any time before it ends |
| **Paid plans** | Starter €39, Scale €89, Agency €179 a month, or custom (Enterprise) |
| **Team access** | Workspaces with viewer, editor and admin roles |
| **API and MCP** | Read-only REST API and an MCP server for Claude, ChatGPT and Cursor (Scale and above) |
| **Made by** | Miltiadis Themelis, Greece |
| **Website** | [trystatly.com](https://trystatly.com) |
| **Support** | [info@trystatly.com](mailto:info@trystatly.com) · [Telegram community](https://t.me/+vN3txumYQVlkZTFk) |

---

## The Statly web app

The web app at [app.trystatly.com](https://app.trystatly.com) is Statly's main product. It scans the accounts you track on Statly's servers every day, so your data is ready even when your computer is off.

![Statly Trend Finder: videos scored against their own account's median](https://trystatly.com/statly-trendfinder-preview.png)

### Features

- **Daily tracking on four platforms.** Add public Instagram, TikTok, YouTube and X accounts. Every video and post inside your scan window is re-read once a day: views, likes, comments, shares and saves.
- **Outlier detection.** Every video is compared with its own account's average and median, so real breakouts stand out instead of just the biggest accounts.
- **Trend Finder.** The videos growing fastest right now (compared with each account's normal day), this week's top outliers, top sounds, and filters and sorting across all your niches. [Learn more](https://trystatly.com/trend-finder).
- **Watchlist.** Group accounts into niches (by topic, brand or client) and see each account's full table: views, likes, comments, engagement rate, growth, vs average and vs median, posting times and video lengths. [Learn more](https://trystatly.com/watchlist).
- **Growth charts.** Each video's views day by day, so you can see whether it is still climbing or has flattened.
- **Library.** Save the videos worth studying, tag them, sort them into folders and download them for reference.
- **Workspaces and teams.** Separate workspaces for each client or brand, with viewer, editor and admin roles.
- **Notifications.** Alerts when a video takes off, in Slack, Discord or Telegram.
- **CSV export.** Export the Watchlist, the Trend Finder and any account's videos to CSV.
- **API and MCP.** Connect your own tools, or ask Claude, ChatGPT or Cursor about your data in plain English (see [API and MCP](#api-and-mcp)).

![Statly Watchlist: niches with outliers, views and engagement](https://trystatly.com/watchlist-niches.png)

### How it works

1. **Start a 7-day free trial** at [app.trystatly.com](https://app.trystatly.com): name your workspace, add your first account, pick the hour your data should be ready, and choose a plan.
2. **Add the accounts you want to watch** and group them into niches. Paste a handle or a profile link from Instagram, TikTok, YouTube or X.
3. **Every morning**, Statly has re-read every video in your window. Open the Trend Finder to see what is taking off, and the Watchlist to study each account.

## Pricing

| Plan | Monthly | Yearly | Videos tracked at once | Seats | API and MCP |
|---|---|---|---|---|---|
| **Free trial** | Free for 7 days | | 500 (20 accounts) | 5 | No |
| **Starter** | €39/month | €390/year | 2,000 | 5 | No |
| **Scale** | €89/month | €890/year | 5,000 | 10 | Yes |
| **Agency** | €179/month | €1,790/year | 10,000 | Unlimited | Yes |
| **Enterprise** | Custom | Custom | Custom | Unlimited | Yes |

- "Videos tracked at once" means every video inside your scan window, across all the accounts you track.
- Scale and Agency can add **extra videos**: +1,000 videos for €20 a month, up to +2,000 (monthly billing).
- The trial asks for a card at checkout and becomes your plan after 7 days unless you cancel.
- Every web app plan, the free trial included, also removes the Chrome extension's free limits.
- Current prices always live on [trystatly.com/pricing](https://trystatly.com/pricing).

---

## The Statly Chrome extension

The free [Statly Chrome extension](https://chromewebstore.google.com/detail/statly/dgclmofackofobhpmklmhbponpkjbbph) ("Statly - All In One Social Analytics") audits any public Instagram, TikTok, YouTube or X account while you browse. Open a profile, click the Statly icon, and it reads the account's recent videos and shows which ones beat the account's normal results, right on the page. The numbers are worked out in your own browser, and no social login is needed.

The extension scans when you click. **Daily tracking is the web app's job**: use the extension to check an account quickly, and the web app to follow it every day.

- **Audit:** one account's recent posts with views, likes, comments, engagement rate and how each compares with the account's median.
- **Compare and Merge:** two accounts head to head, or several accounts pooled into one report.
- **Watchlist and Trend Finder:** save accounts into niches and surface the posts that pull far above their account's normal results.
- **Charts and KPIs:** performance over time, posting times, and executive KPIs such as View-to-Follower Ratio (VTFR), Breakout Performance Rate and Duration Payoff. Definitions: [glossary](https://trystatly.com/glossary).
- **Export:** CSV export and copy links.
- **Transcripts:** transcribe Instagram, TikTok and X videos with your own free Groq key.

**Free limits:** 3 scans a day (shared by Audit, Compare and Merge), and a Watchlist and Trend Finder of 2 niches with 3 accounts each. No Statly account is needed to use it. Every web app plan, the 7-day free trial included, removes these limits: connect the extension in the web app under Settings → Chrome extension. Teammates with the Viewer role stay on the free limits.

**Coming in version 12.5.1** (in Chrome Web Store review): the full YouTube dashboard for every user, a download button on an open Instagram Reel, TikTok video or X post, and **"Add to Statly"**, which adds an audited account to a web app niche in one click.

Store facts (7 October 2026): version 12.5.0, category Social Networking, rated 5.0 out of 5, 491 users. Try it without installing: [live demo](https://trystatly.com/demo).

---

## API and MCP

Included with Scale, Agency and Enterprise from the first paid day (not on Starter or during the free trial).

- **Statly API:** a read-only REST API for your workspace: niches, tracked accounts, videos and posts with outlier scores, top sounds and the Library. It reads what the daily scan already collected and never starts a scan. Keys are created in the app under Settings → API & MCP, sent as `Authorization: Bearer YOUR_KEY`. Limits: 60 calls a minute and 10,000 a day per workspace. Docs: [api.trystatly.com](https://api.trystatly.com).
- **Statly MCP:** connect Claude, ChatGPT or Cursor at `https://mcp.trystatly.com/mcp`, sign in with Statly and press Allow. The assistant reads one workspace (including post thumbnails) and can't change anything. [Learn more](https://trystatly.com/mcp).

```http
GET https://api.trystatly.com/v1/workspace
Authorization: Bearer YOUR_KEY
```

Example question for an AI assistant connected through MCP: *"Which videos in my Fitness niche beat their account's usual views this week, and what do the top ones have in common?"*

---

## Who uses Statly

- **Creators** find the ideas already working for others in their niche. [For creators](https://trystatly.com/for-creators)
- **Marketers and social media managers** follow competitors daily and separate real breakouts from big accounts' normal days. [For marketers](https://trystatly.com/for-marketers)
- **Agencies** run one workspace per client, with team roles, alerts and the API. [For agencies](https://trystatly.com/for-agencies)

## Learn more

- [What is an outlier video?](https://trystatly.com/what-is-an-outlier-video): the definition, the outlier score, and where to draw the line.
- [How Statly measures short-form video](https://trystatly.com/statly-methodology-short-form-video-analytics): the methodology.
- [Glossary](https://trystatly.com/glossary): every metric in plain English.
- [FAQ](FAQ.md) · [Comparisons](COMPARISONS.md) · [Getting started](INSTALLATION.md) · [Roadmap](ROADMAP.md) · [Changelog](CHANGELOG.md)

## Privacy and terms

- [Privacy Policy](https://trystatly.com/privacy)
- [Terms of Service](https://trystatly.com/terms)

## Contact

- Email: [info@trystatly.com](mailto:info@trystatly.com)
- Telegram community: [t.me/+vN3txumYQVlkZTFk](https://t.me/+vN3txumYQVlkZTFk)
- Website: [trystatly.com](https://trystatly.com)

---

<div align="center">
<sub>Statly is not affiliated with, endorsed by, or connected to Instagram, Meta, TikTok, YouTube, Google or X. All trademarks belong to their owners.</sub>
</div>
