# SteveCFDNS

[English](README.md) · **简体中文**

为开发者与站点管理员打造的原生 iOS / iPadOS / macOS Cloudflare 管理客户端（SwiftUI），随时随地管理域名、DNS 记录、SSL/TLS、规则、缓存、流量分析、桌面小组件与 AI 运维助手。

> **分发仓库说明** — 本仓库仅用于发布编译后的安装包与说明文档，不包含源码。

## 下载

前往 [GitHub Releases](https://github.com/zxfccmm4/SteveCFDNS/releases/latest) 下载，或直接获取仓库根目录下的安装包：

| 项目 | iOS / iPadOS | macOS |
| :--- | :--- | :--- |
| 版本 | `v1.0.1`（Build `2`） | `v1.0.1`（Build `2`） |
| 安装包 | [`SteveCFDNS_v1.0.1_b2.ipa`](SteveCFDNS_v1.0.1_b2.ipa)（17.0 MB） | [`SteveCFDNS_v1.0.1_b2.dmg`](SteveCFDNS_v1.0.1_b2.dmg)（19.4 MB） |
| 架构 | `arm64`（支持 iPhone 与 iPad） | 通用二进制（`arm64` + `x86_64`） |
| 签名状态 | 未签名（Release 构建） | Ad-hoc 临时签名（Release 构建） |
| SHA-256 | `c5ecbbc80d40f51846ffb9b507283e7158455f068f9d9850f06679d0a739e29c` | `5bed82d5c7846cb054f36d53cd17e1596f4c0caeaab8fdd2f9bd633b00ad4def` |

## 安装方式

### iOS / iPadOS

本 IPA 为**未签名**版本，任选其一安装：

- **TrollStore** — 直接导入安装，无需重签。
- **AltStore / SideStore / Sideloadly** — 使用个人 Apple ID 重签后侧载安装。
- **自有证书** — 使用个人开发者或分发证书重签安装。

> 说明：使用免费 Apple ID 重签时，受限于扩展数量与 App Group 权限，桌面小组件功能可能无法完整保留；完整体验建议使用 TrollStore 或完整开发者证书签名。

### macOS

DMG 内的 App 为 **Ad-hoc 临时签名**，未经过公证。安装到「应用程序」后首次打开：

1. 在访达中右键 `SteveCFDNSMac.app` → **打开**，再次确认即可。
2. 若仍被系统拦截，可在终端执行 `xattr -cr /Applications/SteveCFDNSMac.app`，或在「系统设置 → 隐私与安全性」中允许打开。

## 系统要求

- **iOS / iPadOS 17.0+**（`arm64`）；或 **macOS 26.0+**（支持 Apple 芯片与 Intel）
- **iOS / iPadOS 26.0+** 及支持 Apple Intelligence 的设备可使用端侧 AI 助手与日志智能分析；macOS 端可直接使用任意已配置的远程 AI 服务商
- 一个可用的 [Cloudflare API Token](https://dash.cloudflare.com/profile/api-tokens)

## 核心功能

| 模块 | 说明 |
| :--- | :--- |
| **域名管理（Zones）** | 查看 Zone 状态、名称服务器与套餐信息，切换开发模式，一键全站或按 URL 清理缓存，查询域名注册/到期时间并导出日历提醒。 |
| **DNS 记录** | 完整的增删改查、搜索、筛选、导入与导出（支持 `A`、`AAAA`、`CNAME`、`MX`、`TXT`、`NS` 等常见类型及 Cloudflare 代理开关）。 |
| **SSL/TLS** | 查看并切换加密模式，检查边缘证书包详情与状态。 |
| **规则中心** | 统一管理 Page Rules、WAF / 防火墙自定义规则以及各阶段 Rulesets。 |
| **流量分析** | 请求数、页面浏览、访客与带宽趋势，并新增缓存命中率、缓存带宽占比与威胁拦截统计。 |
| **Workers** | 只读查看当前账户已部署的 Cloudflare Workers 脚本。 |
| **AI 助手** | 支持端侧 Apple 智能，也支持远程服务商（OpenAI、Anthropic Claude、Google Gemini、DeepSeek、OpenRouter、xAI Grok、Ollama、Magpie 及自定义 OpenAI / Anthropic 兼容接口）。可自然语言查询域名、DNS、流量与缓存；所有写操作均需人工确认卡片。 |
| **Cloudflare Skills** | 内置 8 套运维规范：DNS 迁移审计、SSL/TLS 加固、缓存调优、WAF 威胁排查、Workers 巡检、全账户健康巡检、邮件解析与防伪造审计、页面规则现代化迁移，并支持导入自定义 `SKILL.md`。 |
| **桌面小组件** | 内置 8 款 WidgetKit 小组件：域名状态、流量概览、流量指标、流量趋势、站点健康、站点监控、多站点对比、重点域名高亮。 |
| **Siri 与快捷指令** | 支持通过快捷指令或语音清除 Zone 缓存、列出 Zone、创建 DNS 记录、切换开发模式。 |
| **多账户与权限诊断** | 支持保存并切换多个 Cloudflare API Token（系统 Keychain 加密存储），一键检测 Token 缺失权限并给出修复建议；基于 SwiftData 的本地离线缓存与过期提示。 |
| **macOS 体验优化** | 桌面优先的助手布局、工具栏快捷模型切换、可搜索的模型选择器（含厂商筛选与推荐标记）。 |

## v1.0.1（Build 2）更新内容

- 新增 macOS 通用 DMG 分发包，与 iOS IPA 同步发布。
- 修复 Google Gemini 服务商图标显示异常，以及多个内置品牌 SVG 的解析问题。
- iPhone 端「快速添加 AI 服务商」卡片改为完整显示服务商名称，不再截断。
- AI 助手支持一次查询**账户下全部活跃域名**（domain 留空），输出缓存命中率、缓存带宽占比与威胁拦截数。
- 收紧工具提示词：禁止使用 `example.com` 等占位域名，遇到「找不到」时自动改用 `list_zones` 返回的真实域名重试。
- 新增 3 套内置 Skill：全账户健康巡检、邮件解析与防伪造审计、页面规则迁移。
- 重新设计 macOS 端「选择模型」与「Cloudflare 助手」页面：更宽的消息气泡、快捷示例卡片与内联模型切换。

## 支持语言

简体中文 · 繁體中文 · English · 日本語 · 한국어

## 隐私与安全

- 所有 Cloudflare API Token 均保存在本机系统 Keychain 中。
- Cloudflare 管理请求直连官方 `api.cloudflare.com`。
- 域名注册与到期查询仅对你主动查看的域名发起 RDAP / WHOIS 查询。
- 选择远程 AI 服务商时，对话内容与工具查询结果会发送至该服务商；所有写操作仍需人工确认后才会执行。

## 联系

- X / Twitter：[@st7evechou](https://twitter.com/st7evechou)
- Telegram：[t.me/st7evee](https://t.me/st7evee)
