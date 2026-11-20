# SteveCFDNS

[English](README.md) · **简体中文**

为开发者与站点管理员打造的原生 iOS / iPadOS Cloudflare 管理客户端（SwiftUI），随时随地管理域名、DNS 记录、SSL/TLS、规则、缓存、流量分析、桌面小组件与端侧 AI 运维助手。

> **分发仓库说明** — 本仓库仅用于发布编译后的 IPA 安装包与说明文档，不包含源码。

## 下载

前往 [GitHub Releases](https://github.com/zxfccmm4/SteveCFDNS/releases/latest) 下载，或直接获取仓库根目录下的 [`SteveCFDNS_v1.0_b1.ipa`](SteveCFDNS_v1.0_b1.ipa)。

| 项目 | 信息 |
| :--- | :--- |
| 版本 | `v1.0`（Build `1`） |
| 安装包 | [`SteveCFDNS_v1.0_b1.ipa`](SteveCFDNS_v1.0_b1.ipa)（16.5 MB） |
| 架构 | `arm64`（支持 iPhone 与 iPad） |
| 签名状态 | 未签名（Release 构建） |
| SHA-256 | `10a2981f8cebb3a880ddea51868eeae8de6ef52b02a4d50dd7b2bc85e5baf2e3` |

## 安装方式

本 IPA 为**未签名**版本，任选其一安装：

- **TrollStore** — 直接导入安装，无需重签。
- **AltStore / SideStore / Sideloadly** — 使用个人 Apple ID 重签后侧载安装。
- **自有证书** — 使用个人开发者或分发证书重签安装。

> 说明：使用免费 Apple ID 重签时，受限于扩展数量与 App Group 权限，桌面小组件功能可能无法完整保留；完整体验建议使用 TrollStore 或完整开发者证书签名。

## 系统要求

- **iOS / iPadOS 17.0+**（`arm64`）
- 端侧 **Apple 智能助手**与**日志智能分析**需 **iOS / iPadOS 26.0+** 及支持 Apple Intelligence 的设备
- 一个可用的 [Cloudflare API Token](https://dash.cloudflare.com/profile/api-tokens)

## 核心功能

| 模块 | 说明 |
| :--- | :--- |
| **域名管理（Zones）** | 查看 Zone 状态、名称服务器与套餐信息，切换开发模式，一键全站或按 URL 清理缓存，查询域名注册/到期时间并导出日历提醒。 |
| **DNS 记录** | 完整的增删改查、搜索、筛选、导入与导出（支持 `A`、`AAAA`、`CNAME`、`MX`、`TXT`、`NS` 等常见类型及 Cloudflare 代理开关）。 |
| **SSL/TLS** | 查看并切换加密模式，检查边缘证书包详情与状态。 |
| **规则中心** | 统一管理 Page Rules、WAF / 防火墙自定义规则以及各阶段 Rulesets。 |
| **流量分析** | 查看请求数、页面浏览、访客统计与带宽趋势。 |
| **Workers** | 只读查看当前账户已部署的 Cloudflare Workers 脚本。 |
| **Apple 智能助手** | 基于端侧 Foundation Models（iOS 26+），自然语言查询域名/DNS/流量；高危新增或删除 DNS 操作采用待确认卡片机制，人工点击确认后才执行；支持 AI 日志诊断。 |
| **桌面小组件** | 内置 8 款 WidgetKit 小组件：域名状态、流量概览、流量指标、流量趋势、站点健康、站点监控、多站点对比、重点域名高亮。 |
| **Siri 与快捷指令** | 支持通过快捷指令或语音清除 Zone 缓存、列出 Zone、创建 DNS 记录、切换开发模式。 |
| **多账户与权限诊断** | 支持保存并切换多个 Cloudflare API Token（系统 Keychain 加密存储），一键检测 Token 缺失权限并给出修复建议；基于 SwiftData 的本地离线缓存与过期提示。 |

## 支持语言

简体中文 · 繁體中文 · English · 日本語 · 한국어

## 隐私与安全

- 所有 Cloudflare API Token 均保存在本机系统 Keychain 中。
- Cloudflare 管理请求直连官方 `api.cloudflare.com`。
- 域名注册与到期查询仅对你主动查看的域名发起 RDAP / WHOIS 查询。

## 联系

- X / Twitter：[@st7evechou](https://twitter.com/st7evechou)
- Telegram：[t.me/st7evee](https://t.me/st7evee)
