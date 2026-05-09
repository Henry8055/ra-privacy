---
layout: default
title: RA – Site Machine Manager · Support
permalink: /en/support/
---

# RA – Site Machine Manager · Support

**Effective Date:** May 8, 2026 &nbsp;&nbsp; **Last Updated:** May 10, 2026
**Applies to:** RA – Site Machine Manager macOS / Windows v2.10.31 and later
**Bundle ID:** `com.armada.rapc`

> Looking for the [Privacy Policy](https://henry8055.github.io/ra-privacy/en/) instead?

---

## 1. Quick Help

| Need | Action |
| ---- | ------ |
| **Email support** | [hujuheng@gmail.com](mailto:hujuheng@gmail.com) (response within 1–2 business days) |
| **Bug report / feature request** | [Open a GitHub issue](https://github.com/Henry8055/ra-privacy/issues) |
| **System status / outage** | Check the email above for incident notifications |
| **Reviewer test account** | `apple-reviewer / ApplePass2026!` (read-only, demo data) |

We aim to respond within **2 business days** for paid customers and best-effort for evaluation users.

---

## 2. Product Overview

RA – Site Machine Manager is a desktop operations console for engineers maintaining large fleets of industrial computing nodes across remote sites. Core capabilities:

- **Centralised monitoring** — live status, temperature, fan speed, network metrics and alerts
- **Bulk configuration** — push parameters and credentials to many nodes at once
- **Shift reporting** — production summary and exception logs exported to CSV / Excel
- **Multi-site fleet view** — scales from a single rack to thousands of nodes
- **Role-based access** — admin / operator / viewer separation

The app is delivered as a sandboxed macOS / Windows desktop application; all device communication happens **either over the local LAN or via your own backend** that you deploy.

---

## 3. System Requirements

| Platform | Minimum | Recommended |
| -------- | ------- | ----------- |
| **macOS** | 12.0 (Monterey) | 14.0 (Sonoma) or later, Apple Silicon or Intel |
| **Windows** | 10 21H2, 64-bit | 11 22H2 or later |
| **RAM** | 4 GB | 8 GB+ |
| **Disk** | 500 MB | 2 GB+ |
| **Network** | Reachable LAN to managed nodes; HTTPS to your backend | 1 Gb/s LAN |
| **Display** | 1280 × 800 | 1920 × 1080+ |

---

## 4. Getting Started

1. **Install** from the Mac App Store or download the Windows installer from your organisation's distribution channel.
2. **Launch** the app. On first run, you will be asked for the backend URL provided by your organisation.
3. **Sign in** with the credentials issued by your administrator.
4. **Add a site** → **Add nodes** (manual entry or LAN scan).
5. **Configure alerts** under *Settings → Alerts*.

A 4-minute walk-through video is available on request — email us.

---

## 5. Frequently Asked Questions

### 5.1 The app cannot connect to my backend
- Confirm the backend URL is correct (typically `https://<your-host>/api/v1`).
- Confirm your firewall / proxy allows outbound HTTPS to that host.
- macOS users: ensure the app has *Local Network* permission (System Settings → Privacy & Security → Local Network).
- Verify the server's TLS certificate is valid and not expired. RA pins the production certificate; an expired or replaced certificate will be reported as `Connection rejected`.

### 5.2 LAN scan finds no devices
- Both your Mac and the target nodes must be on the same broadcast domain (no VLAN isolation).
- Some node vendors require a vendor-specific port; configure it under *Settings → Discovery*.
- Antivirus or VPN software may block multicast — temporarily disable to test.

### 5.3 I forgot my password
Password reset is performed by your organisation's administrator on the backend, not by this app. Contact your administrator.

### 5.4 How do I export data?
*Reports → Export* generates a CSV (default) or Excel file. Exported files are written to a folder you choose; the app does not upload them anywhere.

### 5.5 Where are local logs stored?
- **macOS:** `~/Library/Containers/com.armada.rapc/Data/Library/Logs/`
- **Windows:** `%APPDATA%\ra-pc\logs\`

When reporting a bug, please attach the most recent `app-YYYY-MM-DD.log`.

### 5.6 Does the app collect personal data?
No advertising/tracking SDKs, no analytics that leave your device, no IDFA. Diagnostic logs are stored **locally only**. See the [Privacy Policy](https://henry8055.github.io/ra-privacy/en/) for full details.

### 5.7 Is the app compatible with Apple Silicon?
Yes — the macOS build is a universal binary (x86_64 + arm64) and runs natively on M1/M2/M3 Macs.

### 5.8 The app shows "Connection rejected" after my certificate was renewed
The app pins the SHA-256 fingerprint of the production certificate. After a backend certificate rotation, install the latest app update from the Mac App Store, which contains the refreshed pin.

---

## 6. Reporting a Bug

Please include:

1. **App version** (Help → About, or top-right of the navigation panel)
2. **OS version**
3. **Steps to reproduce**
4. **Expected vs. actual behaviour**
5. **Screenshot** (drag onto the email)
6. **Log file** (see §5.5)

Send to **[hujuheng@gmail.com](mailto:hujuheng@gmail.com)** or open an issue at [github.com/Henry8055/ra-privacy/issues](https://github.com/Henry8055/ra-privacy/issues).

We will reply with a ticket ID and target fix version.

---

## 7. Security Disclosures

If you discover a security vulnerability, **do not file a public issue.** Email
[hujuheng@gmail.com](mailto:hujuheng@gmail.com) with subject prefix `[SECURITY]`. We will acknowledge within 2 business days and coordinate disclosure responsibly.

---

## 8. Release & Update Channel

- macOS users: updates are delivered through the **Mac App Store** automatically.
- Windows users: updates are delivered through your organisation's distribution channel.
- Release notes are published in-app under *Help → What's New* and on this page (below).

---

## 9. Recent Releases

| Version | Date | Highlights |
| ------- | ---- | ---------- |
| **2.10.31** | 2026-05-10 | First Mac App Store release; signing chain finalised |
| 2.10.30 | 2026-05-09 | fastlane-based release pipeline |
| 2.10.x | 2026-04 ~ 05 | Performance and stability improvements |

For the full changelog, see *Help → What's New* inside the app.

---

## 10. Contact

| Channel | |
| ------- | -- |
| **Email** | [hujuheng@gmail.com](mailto:hujuheng@gmail.com) |
| **GitHub Issues** | [github.com/Henry8055/ra-privacy/issues](https://github.com/Henry8055/ra-privacy/issues) |
| **Privacy Policy** | [/en/](https://henry8055.github.io/ra-privacy/en/) · [/zh/](https://henry8055.github.io/ra-privacy/zh/) |
| **Response SLA** | 2 business days |

---

中文版：[/zh/support/](https://henry8055.github.io/ra-privacy/zh/support/)
