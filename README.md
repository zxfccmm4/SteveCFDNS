# SteveCFDNS

**English** · [简体中文](README.zh-CN.md)

A native iOS / iPadOS / macOS Cloudflare management client built with SwiftUI — manage DNS records, SSL/TLS, rules, cache, analytics, widgets, and AI ops right from your device.

> **Distribution Repository** — This repository hosts only the compiled packages and documentation. Source code is not published here.

## Download

Get the latest release from [GitHub Releases](https://github.com/zxfccmm4/SteveCFDNS/releases/latest), or download directly from this repository:

| Field | iOS / iPadOS | macOS |
| :--- | :--- | :--- |
| Version | `v1.0.1` (Build `2`) | `v1.0.1` (Build `2`) |
| Package | [`SteveCFDNS_v1.0.1_b2.ipa`](SteveCFDNS_v1.0.1_b2.ipa) (17.0 MB) | [`SteveCFDNS_v1.0.1_b2.dmg`](SteveCFDNS_v1.0.1_b2.dmg) (19.4 MB) |
| Architecture | `arm64` (iPhone & iPad) | Universal (`arm64` + `x86_64`) |
| Signing | Unsigned (Release) | Ad-hoc signed (Release) |
| SHA-256 | `c5ecbbc80d40f51846ffb9b507283e7158455f068f9d9850f06679d0a739e29c` | `5bed82d5c7846cb054f36d53cd17e1596f4c0caeaab8fdd2f9bd633b00ad4def` |

## Installation

### iOS / iPadOS

The IPA is **unsigned**. Choose any of the following sideloading methods:

- **TrollStore** — Install directly without re-signing.
- **AltStore / SideStore / Sideloadly** — Re-sign with your Apple ID and install.
- **Custom Signing Certificate** — Re-sign with your own developer or distribution certificate.

> Note: When re-signing with a free Apple ID, iOS limits active extensions and App Group entitlements; Home Screen Widgets require the main app and widget extension to share an App Group.

### macOS

The DMG is **ad-hoc signed** but not notarized. After installing to `/Applications`, allow it once:

1. Right-click `SteveCFDNSMac.app` → **Open**, then confirm.
2. If macOS still blocks it, run `xattr -cr /Applications/SteveCFDNSMac.app` in Terminal, or allow it under **System Settings → Privacy & Security**.

## Requirements

- **iOS / iPadOS 17.0+** (`arm64`), or **macOS 26.0+** (Apple silicon & Intel)
- **iOS / iPadOS 26.0+** on an Apple Intelligence-capable device for the on-device AI Assistant and AI Log Insights; on macOS, any configured remote AI provider works
- A [Cloudflare API Token](https://dash.cloudflare.com/profile/api-tokens)

## Features

| Module | Highlights |
| :--- | :--- |
| **Zones** | View zone status, name servers, plan details, toggle Development Mode, purge full or per-URL cache, inspect domain registration/expiration dates, and add renewal reminders to Calendar. |
| **DNS Records** | Create, edit, delete, search, filter, import, and export DNS records (`A`, `AAAA`, `CNAME`, `MX`, `TXT`, `NS`, etc.) with Cloudflare Proxy toggles. |
| **SSL/TLS** | Switch encryption modes and inspect edge certificate packs. |
| **Rules Center** | Manage Page Rules, WAF / Firewall custom rules, and phase-based Rulesets. |
| **Analytics** | Requests, page views, unique visitors, bandwidth trends, plus cache hit rate, cached bandwidth ratio, and threat counters. |
| **Workers** | Read-only list of deployed Cloudflare Workers scripts. |
| **AI Assistant** | Works with Apple Intelligence on-device models and remote providers (OpenAI, Anthropic Claude, Google Gemini, DeepSeek, OpenRouter, xAI Grok, Ollama, Magpie, custom OpenAI/Anthropic-compatible endpoints). Natural-language queries over zones, DNS, traffic and cache; write operations always require card confirmation. |
| **Cloudflare Skills** | 8 built-in operational playbooks — DNS migration audit, SSL/TLS hardening, cache tuning, WAF threat triage, Workers inspection, full-account health check, email deliverability (SPF/DKIM/DMARC), and Page Rules migration — plus custom `SKILL.md` import. |
| **Widgets** | 8 Home Screen widgets: Zone Status, Traffic Overview, Traffic Metrics, Traffic Trend, Zone Health, Zone Monitor, Multi-Zone Compare, and Zone Highlight. |
| **Siri & Shortcuts** | App Intents for purging zone cache, listing zones, creating DNS records, and toggling Development Mode. |
| **Multi-Account & Diagnostics** | Manage multiple Cloudflare API Tokens in system Keychain, probe token permissions with fix suggestions, and view cached data offline via SwiftData. |
| **macOS 优化** | Desktop-first assistant layout, quick model switcher in the toolbar, searchable model picker with vendor filters and recommended badges. |

## What's New in v1.0.1 (Build 2)

- Added macOS distribution as a universal DMG, alongside the iOS IPA.
- Fixed the Google Gemini provider icon rendering and several SVG parsing issues in bundled brand icons.
- Quick-add provider cards on iPhone now show complete provider names instead of truncating them.
- AI assistant can now query **all active zones at once** (leave the domain empty), reporting cache hit rate, cached bandwidth ratio, and threat counts.
- Hardened tool prompts so the model never invents placeholder domains such as `example.com`, and always retries with real zones returned by `list_zones`.
- Added three built-in Skills: full-account health check, email deliverability audit, and Page Rules modernization.
- Redesigned the macOS model picker and Cloudflare assistant pages with wider message bubbles, sample prompt cards, and an inline model switcher.

## Languages

English · 简体中文 · 繁體中文 · 日本語 · 한국어

## Privacy & Security

- Cloudflare API Tokens are stored locally in the system Keychain.
- Cloudflare management requests connect directly to `api.cloudflare.com`.
- Domain expiration lookups query RDAP / WHOIS only for domains you explicitly view.
- When a remote AI provider is selected, chat content and tool results are sent to that provider; all write operations still require manual confirmation.

## Contact

- X / Twitter: [@st7evechou](https://twitter.com/st7evechou)
- Telegram: [t.me/st7evee](https://t.me/st7evee)
