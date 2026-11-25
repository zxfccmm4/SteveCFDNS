# SteveCFDNS

**English** · [简体中文](README.zh-CN.md)

A native iOS / iPadOS / macOS Cloudflare management client built with SwiftUI — manage DNS records, SSL/TLS, rules, cache, analytics, widgets, and AI ops right from your device.

> **Distribution Repository** — This repository hosts only the compiled packages and documentation. Source code is not published here.

## Download

Get the latest release from [GitHub Releases](https://github.com/zxfccmm4/SteveCFDNS/releases/latest), or download directly from this repository:

| Field | iOS / iPadOS | macOS |
| :--- | :--- | :--- |
| Version | `v1.0.2` (Build `3`) | `v1.0.2` (Build `3`) |
| Package | [`SteveCFDNS_v1.0.2_b3.ipa`](SteveCFDNS_v1.0.2_b3.ipa) (17.3 MB) | [`SteveCFDNS_v1.0.2_b3.dmg`](SteveCFDNS_v1.0.2_b3.dmg) (20.1 MB) |
| Architecture | `arm64` (iPhone & iPad) | Universal (`arm64` + `x86_64`) |
| Signing | Unsigned (Release) | Ad-hoc signed (Release) |
| SHA-256 | `173d042b9dd2ddba1015c93ecfac2900bbc1392f919539fd66dd0682069f59a9` | `d0b7439a45da4c99cf2feb88f0dd05c0f964c4cadf0cc4688c5940fc5b72da2a` |

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
| **AI Assistant** | Multi-conversation AI workspace supporting Apple Intelligence (on-device & Private Cloud Compute) and remote providers (OpenAI, Anthropic Claude, Google Gemini, DeepSeek, OpenRouter, xAI Grok, Ollama, Magpie, custom OpenAI/Anthropic-compatible endpoints). Features full-text history search, thinking disclosure, collapsible tool execution cards, domain scope filtering, and per-conversation inline confirmation for write operations. |
| **Cloudflare Skills** | 8 built-in operational playbooks — DNS migration audit, SSL/TLS hardening, cache tuning, WAF threat triage, Workers inspection, full-account health check, email deliverability (SPF/DKIM/DMARC), and Page Rules migration — plus per-conversation pinned skills and custom `SKILL.md` import. |
| **Widgets** | 8 Home Screen widgets: Zone Status, Traffic Overview, Traffic Metrics, Traffic Trend, Zone Health, Zone Monitor, Multi-Zone Compare, and Zone Highlight. |
| **Siri & Shortcuts** | App Intents for purging zone cache, listing zones, creating DNS records, and toggling Development Mode. |
| **Multi-Account & Diagnostics** | Manage multiple Cloudflare API Tokens in system Keychain, probe token permissions with fix suggestions, and view cached data offline via SwiftData. |
| **macOS Experience** | Collapsible conversation history sidebar, native Markdown export, hover message actions, quick model switcher in the toolbar, searchable model picker with vendor filters and recommended badges. |

## What's New in v1.0.2 (Build 3)

- **Multi-Conversation AI Workspace**: Added two-tier disk-persisted conversation history with pinned/date buckets, full-text search across titles and message bodies, rename, duplicate, fork from any message, conversation compression, and Markdown export (including thinking blocks and tool executions).
- **Rich Message & Streaming Experience**: Added message copy, edit & resend, regenerate, fork, and delete actions; shimmering collapsible Thinking disclosure and Tool Execution cards; and resilient long-lived SSE streaming with automatic retry on transient network/HTTP errors.
- **Scoped Context & Isolated Approvals**: Added domain/account scope filter capsules, per-conversation model overrides and pinned Skills strip, configurable context token budget with atomic pruning, optional cross-session memory, and `TaskLocal`-isolated inline write approvals with optional 1-hour grant.
- **Apple Private Cloud Compute & Platform Polish**: Added Private Cloud Compute toggle with automatic safe fallback; iOS 26.1 `tabViewBottomAccessory` collapsed composer on iPhone; and full macOS feature parity with a collapsible conversation sidebar and native `NSSavePanel` export.
- **Security**: Removed the hardcoded fallback API key in `ZoneRepository`, relying solely on local `Secrets.plist`.

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
