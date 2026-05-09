# RA Mining Operations Management — Privacy Policy

**Effective Date**: May 8, 2026
**Last Updated**: May 8, 2026
**Applies to**: RA macOS / Windows v2.10.28 and later

---

## 1. Introduction

This Privacy Policy describes how the developer (hereinafter "we", "us") collects, uses, stores, and protects information when you use **RA Mining Operations Management** (hereinafter "the App"), a desktop tool for mining-site operations personnel.

If you do not agree with any term of this Policy, please stop using the App. Continued use constitutes acceptance of this Policy.

---

## 2. Information We Collect

The App collects only the minimum information required to deliver its core operations features:

| Category | Items | How Collected | Purpose |
|---|---|---|---|
| Account info | username, encrypted login token | manually entered | login & access control |
| Device config | miner IPs, models, serial numbers, pool URLs | manually entered / local-network scan | device management & monitoring |
| Diagnostic logs | error stack, performance metrics, action timestamps | recorded locally by the App | troubleshooting & performance tuning |
| Crash info | call stack & OS version at crash time | stored locally only (the Mac App Store build sends no crash data to any third-party service) | reproduction & fixing |

**We do NOT collect**:
- your real name, government ID, postal address, or phone number
- your location (GPS or IP-based)
- contacts, photos, microphone, or camera data
- any identifiers used for advertising or third-party tracking (IDFA, cookies, etc.)

---

## 3. How We Use Information

We use the above information solely to:

1. **Provide app functionality** — authentication, miner monitoring, reporting, alerts
2. **Local diagnostics** — log files on your device to help debug issues
3. **OS compatibility** — adapt UI/feature behaviour to the host OS

We do **NOT**:
- use the data for advertising or push marketing
- sell or rent the data to any third party
- use the data to train any machine-learning model

---

## 4. Where Information Is Stored

| Type | Location |
|---|---|
| Account tokens | macOS Keychain / Windows Credential Locker (OS-encrypted) |
| Config & cache | App sandbox (macOS: `~/Library/Containers/com.armada.rapc/`) |
| Log files | `logs/` directory inside the App sandbox |
| Business data | The remote server you configure (outside the App's control) |

The App itself **does not upload any personal information to any third-party server**. Any remote business server you connect to is deployed and managed by you or your organisation.

---

## 5. Sharing With Third Parties

The App embeds **no third-party analytics or tracking SDK**. It communicates over the network with two kinds of endpoints:

1. **Business backends you configure** — e.g. your mining site's management service. The privacy practices of these services are outside the scope of this Policy; contact your organisation's administrator for details.
2. **Miner devices themselves** — the App talks to miners directly over the LAN to read/write parameters; this traffic is not uploaded anywhere external.

---

## 6. Network Security

- All communication with remote backends defaults to **HTTPS / TLS 1.2 or higher**.
- Communication with LAN miners follows the protocol provided by the miner vendor (some vendors only support plain HTTP, valid only inside the local network).
- App updates are delivered through the macOS App Store / Microsoft Store; the App contains **no in-app self-update mechanism**.

---

## 7. Your Rights

You may at any time:

- **View** every device/account record you have entered
- **Modify / delete** records directly inside the App
- **Export** data to CSV / Excel via the built-in export feature
- **Erase all local data** by uninstalling the App; the OS removes the sandbox contents

To remove data stored on your organisation's remote server, please contact your organisation's administrator.

---

## 8. Children's Privacy

The App is a professional operations tool **not directed at children under 13**, and we do not knowingly collect information from minors.

---

## 9. Policy Changes

If we make material changes to this Policy, we will:

- Display a prominent notice on the App's main screen or at the top of this page
- Update the "Last Updated" date at the top of this page

Continued use of the App after changes constitutes acceptance of the revised Policy.

---

## 10. Contact

For questions about this Policy or your personal information, contact:

- **Email**: `hujuheng@gmail.com`
- **GitHub Issues**: `https://github.com/Henry8055/ra-privacy/issues`
- **Postal address**: ``

We aim to respond within **15 business days**.

---

> A [Chinese version](./privacy-policy-zh.md) is also available. If there is any conflict between the two language versions, the Chinese version prevails.
