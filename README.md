# Awesome-Website-Page-Speed-Performance-Benchmarking

# Awesome Website Page Speed & Performance Benchmarking

> A curated list of top Website Page Speed and Performance Benchmarking platforms — both SaaS/Hosted commercial solutions and open-source alternatives for measuring, monitoring, and optimizing web performance.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [BrowserStack SpeedLab](#browserstack-speedlab)
  - [Google PageSpeed Insights](#google-pagespeed-insights)
  - [GTmetrix](#gtmetrix)
  - [WebPageTest (Catchpoint)](#webpagetest-catchpoint)
  - [Pingdom Website Speed Test](#pingdom-website-speed-test)
  - [SpeedCurve](#speedcurve)
  - [DebugBear](#debugbear)
  - [Calibre](#calibre)
  - [Dareboost](#dareboost)
  - [Uptrends Speed Test](#uptrends-speed-test)
- [Open-Source Software](#-open-source-software)
  - [Lighthouse](#lighthouse)
  - [sitespeed.io](#sitespeedio)
  - [Lighthouse CI](#lighthouse-ci)
  - [Browsertime](#browsertime)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Website Page Speed and Performance Benchmarking platforms. These are not open-source but are included as reference points for feature comparison.

### BrowserStack SpeedLab
**Type:** Real-device speed testing  
SpeedLab lets QA testers evaluate website speed on real devices and browsers, providing accurate and realistic performance data rather than emulated results [citation:1]. Tests run on actual hardware (e.g., iPhone XS, Windows 10) with real network conditions. Reports cover key metrics including TTFB, response time, page load time, and Core Web Vitals. Supports scheduled tests and sample reports for major sites like Amazon, Netflix, and Airbnb. Free tier available for basic testing [citation:1].  
**Best for:** Teams needing performance validation on real mobile and desktop hardware, particularly for QA workflows.

### Google PageSpeed Insights
**Type:** Lab + field data analysis  
Google's official tool combines Lighthouse lab data with Chrome User Experience Report (CrUX) field data to show how real users experience a page. Provides Core Web Vitals assessment with pass/fail thresholds and prioritized optimization opportunities. The definitive reference for SEO-related performance since Google uses these metrics in ranking.

### GTmetrix
**Type:** Full performance reports with monitoring  
GTmetrix provides Lighthouse-powered reports with Web Vitals (LCP, TBT, CLS), structure audits, and real user metrics from CrUX data [citation:2]. Features include waterfall charts, video/filmstrip playback, 28 global test locations, 55+ simulated mobile devices, and scheduled monitoring with alerts. The MCP integration brings performance data into AI coding tools (Claude, Cursor, GitHub Copilot) for in-context optimization [citation:2]. Free tier available with no credit card required.  
**Best for:** Teams wanting comprehensive reports with monitoring, alerting, and AI-assisted workflow integration.

### WebPageTest (Catchpoint)
**Type:** Deep diagnostic testing (now enterprise IPM)  
The long-standing gold standard for deep performance diagnostics, now fully integrated into Catchpoint's Internet Performance Monitoring platform [citation:3][citation:13]. Retains filmstrips, waterfalls, and no-code experiments while adding scheduled tests, AI-powered dashboards, customizable alerts, RUM integration, and 3,000+ global monitoring agents. Tests can correlate synthetic and real user data across DNS, CDN, APIs, and network layers [citation:13].  
**Best for:** Performance engineers and teams needing the deepest possible diagnostics with enterprise-scale monitoring.

### Pingdom Website Speed Test
**Type:** Simple page speed analysis  
Pingdom's free tool runs a single test from one of 7 locations, reporting a performance grade, page weight, request count, and a waterfall chart [citation:14]. The tool is based on the aging YSlow project, uses older technical metrics rather than Core Web Vitals, and tests only on unthrottled desktop connections — meaning results are faster than real-user experience [citation:14]. Useful for quick checks, but not a substitute for modern benchmarking.  
**Best for:** Quick, free page speed snapshots; not suitable for rigorous benchmarking or Core Web Vitals tracking.

### SpeedCurve
**Type:** Continuous performance monitoring with competitive benchmarking  
SpeedCurve specializes in ongoing performance tracking with synthetic and RUM data. The Vitals dashboard shows Core Web Vitals at the 75th percentile against recommended thresholds [citation:5]. A standout feature is competitive benchmarking: you can monitor competitor sites alongside your own and compare filmstrips, rendering timelines, and specific metrics side-by-side [citation:15]. Retains 100% synthetic data for 13 months for year-over-year comparisons.  
**Best for:** Teams wanting to track performance over time and benchmark against competitors with rich visual comparisons.

### DebugBear
**Type:** Performance monitoring with server timing support  
DebugBear offers lab tests and Real User Monitoring with a focus on actionable insights. The August 2026 release added uptime monitoring, Server Timing header support (making backend performance visible in front-end waterfalls), URL-based conversion tracking, and budget recovery notifications [citation:6]. Custom request headers can now be scoped to specific domains for controlled lab tests.  
**Best for:** Teams wanting modern performance monitoring with backend timing visibility and conversion correlation.

### Calibre
**Type:** Performance monitoring with CLI and API  
Calibre provides synthetic monitoring, RUM, and CrUX data with a developer-friendly CLI and Node.js API. CLI 7.0 added `calibre rum` and `calibre crux` commands for programmatic access to real-user and field data, with JSON output for scripts and code agents [citation:7]. Site listings now show which data sources (Synthetic, CrUX, RUM) are active per site.  
**Best for:** Developers wanting programmatic access to performance data for custom reporting and automation.

### Dareboost
**Type:** Configurable speed testing with UX metrics  
Dareboost runs real Chrome browser tests with highly configurable conditions (screen resolution, bandwidth, latency, HTTP headers, AdBlock) across 13 global locations [citation:8]. Reports include video playback, filmstrip, Speed Index, Start Render, Visually Complete, and a waterfall with full request/response headers. Free first test available without subscription.  
**Best for:** Teams needing fine-grained control over test conditions to replicate specific user segments.

### Uptrends Speed Test
**Type:** Free page speed testing with optimization tips  
Uptrends offers a free page speed test that runs in Chrome or Edge, tracking connection times, response times, download/render times, and page element distributions [citation:9]. Mobile simulation and connection throttling are available. Tests run from 10 locations on the free tier (230+ with a trial). Provides optimization suggestions prioritized by impact.  
**Best for:** Quick free testing with mobile simulation and connection throttling options.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Page Speed and Performance Benchmarking tools. All listed projects offer source code you can run yourself.

### Lighthouse
**Stack:** Node.js | **License:** Apache 2.0  
Google's automated open-source tool for auditing web page quality, covering performance, accessibility, SEO, and more [citation:11]. Runs in Chrome DevTools, via CLI, as a Node module, or through the web UI. Generates a detailed report with scores and specific opportunities for improvement. The performance score is derived from weighted Core Web Vitals and other metrics. Foundational to many commercial tools (GTmetrix, PageSpeed Insights, DebugBear all build on Lighthouse).  
**Best for:** Developers wanting the standard, Google-maintained audit engine that powers most commercial tools.

### sitespeed.io
**Stack:** JavaScript / Node.js | **License:** MIT  
An open-source tool for comprehensive web performance analysis, enabling you to test, monitor, and optimize website speed using real browsers in various environments [citation:10]. 4,900+ GitHub stars with active development (last push October 2025). Supports performance budgets, continuous monitoring, and integration with Graphite/InfluxDB for dashboards. Can run Lighthouse and Browsertime together for combined analysis.  
**Best for:** Teams wanting a full-featured, self-hosted performance testing and monitoring platform with budget enforcement.

### Lighthouse CI
**Stack:** Node.js | **License:** Apache 2.0  
A suite of tools for running Lighthouse in CI/CD pipelines. Asserts performance budgets on every commit, preventing regressions before they reach production. Provides GitHub status checks, temporary public storage for reports, and integration with GitHub Actions, CircleCI, and other CI systems [citation:11].  
**Best for:** Teams wanting to prevent performance regressions through automated CI checks.

### Browsertime
**Stack:** JavaScript / Node.js | **License:** MIT  
A harness for running performance tests in real browsers (Chrome, Firefox, Safari) and collecting metrics including video, filmstrip, HAR files, and performance timings. Can be used standalone or as the browser engine inside sitespeed.io. Provides precise control over browser behavior and network conditions.  
**Best for:** Teams needing fine-grained browser automation for custom performance measurement pipelines.

---

## 📊 Comparison at a Glance

| Software | License | Type | Core Web Vitals | RUM/Field Data | Self-Hosted | Best For |
|----------|---------|------|-----------------|----------------|-------------|----------|
| **BrowserStack SpeedLab** | Proprietary | Real-device testing | ✅ | ❌ | ❌ | Real hardware QA |
| **PageSpeed Insights** | Proprietary | Lab + CrUX | ✅ | ✅ (CrUX) | ❌ | SEO performance reference |
| **GTmetrix** | Proprietary | Reports + monitoring | ✅ | ✅ (CrUX) | ❌ | Comprehensive monitoring + AI |
| **WebPageTest** | Proprietary | Deep diagnostics | ✅ | ✅ (RUM) | ❌ | Deepest diagnostics |
| **Pingdom** | Proprietary | Quick check | Limited | ❌ | ❌ | Free quick snapshots |
| **SpeedCurve** | Proprietary | Monitoring + benchmarking | ✅ | ✅ (RUM) | ❌ | Competitive benchmarking |
| **DebugBear** | Proprietary | Monitoring + server timing | ✅ | ✅ (RUM) | ❌ | Backend timing visibility |
| **Calibre** | Proprietary | CLI + API monitoring | ✅ | ✅ (CrUX/RUM) | ❌ | Programmatic access |
| **Dareboost** | Proprietary | Configurable testing | ✅ | ❌ | ❌ | Custom test conditions |
| **Lighthouse** | Apache 2.0 | Audit engine | ✅ | ❌ | ✅ | Standard audit engine |
| **sitespeed.io** | MIT | Full platform | ✅ | ❌ | ✅ | Self-hosted monitoring |
| **Lighthouse CI** | Apache 2.0 | CI regression prevention | ✅ | ❌ | ✅ (CI) | Budget enforcement |
| **Browsertime** | MIT | Browser harness | ✅ | ❌ | ✅ | Custom measurement pipelines |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Website Page Speed or Performance Benchmarking tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
