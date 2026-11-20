# SteveCFDNS

**English** · [简体中文](README.zh-CN.md)

A native iOS & iPadOS Cloudflare management client built with SwiftUI — manage DNS records, SSL/TLS, rules, cache, analytics, widgets, and on-device AI ops right from your device.

> **Distribution Repository** — This repository hosts only the compiled IPA package and documentation. Source code is not published here.

## Download

Get the latest release from [GitHub Releases](https://github.com/zxfccmm4/SteveCFDNS/releases/latest) or download [`SteveCFDNS_v1.0_b1.ipa`](SteveCFDNS_v1.0_b1.ipa) directly from this repository.

| Field | Value |
| :--- | :--- |
| Version | `v1.0` (Build `1`) |
| Package | [`SteveCFDNS_v1.0_b1.ipa`](SteveCFDNS_v1.0_b1.ipa) (16.5 MB) |
| Architecture | `arm64` (iPhone & iPad) |
| Signing | Unsigned (Release) |
| SHA-256 | `10a2981f8cebb3a880ddea51868eeae8de6ef52b02a4d50dd7b2bc85e5baf2e3` |

## Installation

The IPA is **unsigned**. Choose any of the following sideloading methods:

- **TrollStore** — Install directly without re-signing.
- **AltStore / SideStore / Sideloadly** — Re-sign with your Apple ID and install.
- **Custom Signing Certificate** — Re-sign with your own developer or distribution certificate.

> Note: When re-signing with a free Apple ID, iOS limits active extensions and App Group entitlements; Home Screen Widgets require the main app and widget extension to share an App Group.

## Requirements

- **iOS / iPadOS 17.0+** (`arm64`)
- **iOS / iPadOS 26.0+** on an Apple Intelligence-capable device for the on-device AI Assistant and AI Log Insights
- A [Cloudflare API Token](https://dash.cloudflare.com/profile/api-tokens)

## Features

| Module | Highlights |
| :--- | :--- |
| **Zones** | View zone status, name servers, plan details, toggle Development Mode, purge full or per-URL cache, inspect domain registration/expiration dates, and add renewal reminders to Calendar. |
| **DNS Records** | Create, edit, delete, search, filter, import, and export DNS records (`A`, `AAAA`, `CNAME`, `MX`, `TXT`, `NS`, etc.) with Cloudflare Proxy toggles. |
| **SSL/TLS** | Switch encryption modes and inspect edge certificate packs. |
| **Rules Center** | Manage Page Rules, WAF / Firewall custom rules, and phase-based Rulesets. |
| **Analytics** | View requests, page views, unique visitors, and bandwidth trends. |
| **Workers** | Read-only list of deployed Cloudflare Workers scripts. |
| **Apple Intelligence** | On-device Cloudflare assistant (iOS 26+) for natural-language queries, human-confirmed DNS record creation/deletion cards, and AI log diagnostics. |
| **Widgets** | 8 Home Screen widgets: Zone Status, Traffic Overview, Traffic Metrics, Traffic Trend, Zone Health, Zone Monitor, Multi-Zone Compare, and Zone Highlight. |
| **Siri & Shortcuts** | App Intents for purging zone cache, listing zones, creating DNS records, and toggling Development Mode. |
| **Multi-Account & Diagnostics** | Manage multiple Cloudflare API Tokens in system Keychain, probe token permissions with fix suggestions, and view cached data offline via SwiftData. |

## Languages

English · 简体中文 · 繁體中文 · 日本語 · 한국어

## Privacy & Security

- Cloudflare API Tokens are stored locally in the iOS Keychain.
- Cloudflare management requests connect directly to `api.cloudflare.com`.
- Domain expiration lookups query RDAP / WHOIS only for domains you explicitly view.

## Contact

- X / Twitter: [@st7evechou](https://twitter.com/st7evechou)
- Telegram: [t.me/st7evee](https://t.me/st7evee)
