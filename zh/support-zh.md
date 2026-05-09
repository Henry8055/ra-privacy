---
layout: default
title: RA – Site Machine Manager · 技术支持
permalink: /zh/support/
---

# RA – Site Machine Manager · 技术支持

**生效日期：** 2026 年 5 月 8 日 &nbsp;&nbsp; **最近更新：** 2026 年 5 月 10 日
**适用版本：** RA – Site Machine Manager macOS / Windows v2.10.31 及以上
**Bundle ID：** `com.armada.rapc`

> 需要查看 [隐私政策](https://henry8055.github.io/ra-privacy/zh/)？

---

## 1. 快速联系

| 你需要 | 操作 |
| ----- | ---- |
| **邮件支持** | [hujuheng@gmail.com](mailto:hujuheng@gmail.com)（1–2 个工作日内回复） |
| **Bug / 功能反馈** | [GitHub Issues](https://github.com/Henry8055/ra-privacy/issues) |
| **服务状态 / 故障公告** | 通过上述邮箱发送 |
| **审核测试账号** | `apple-reviewer / ApplePass2026!`（只读、含演示数据） |

我们对付费客户承诺 **2 个工作日**内首次响应；评估用户尽力支持。

---

## 2. 产品简介

RA – Site Machine Manager 是一款面向远程站点工业计算节点运维工程师的桌面运维控制台，核心能力：

- **集中监控** — 实时查看运行状态、温度、风扇转速、网络指标和告警
- **批量配置** — 一次性向多台节点下发参数和凭据
- **班次报告** — 生产汇总和异常日志，可导出为 CSV / Excel
- **多站点机群视图** — 支持从单机柜到上千节点
- **基于角色的访问控制** — 区分管理员 / 操作员 / 只读

应用以沙盒形式分发；所有节点通信仅通过**本地局域网**或**您自部署的后端**。

---

## 3. 系统要求

| 平台 | 最低 | 推荐 |
| ---- | ---- | ---- |
| **macOS** | 12.0 (Monterey) | 14.0 (Sonoma) 及以上，Apple Silicon 或 Intel |
| **Windows** | 10 21H2，64 位 | 11 22H2 及以上 |
| **内存** | 4 GB | 8 GB 及以上 |
| **磁盘** | 500 MB | 2 GB 及以上 |
| **网络** | 与受管节点 LAN 可达；可访问您的后端 HTTPS | 千兆局域网 |
| **分辨率** | 1280 × 800 | 1920 × 1080 及以上 |

---

## 4. 快速上手

1. **安装** —— Mac 用户从 Mac App Store 下载；Windows 用户从所在组织的分发渠道下载安装包。
2. **启动** —— 首次运行需要填写贵组织提供的后端服务地址。
3. **登录** —— 使用管理员发放的账号密码。
4. **新建站点 → 添加节点**（手动录入或局域网扫描）。
5. 在 **设置 → 告警** 中配置告警规则。

需要 4 分钟入门视频可来邮索取。

---

## 5. 常见问题

### 5.1 无法连接后端
- 确认后端地址正确（通常形如 `https://<your-host>/api/v1`）。
- 检查防火墙 / 代理是否允许该地址的出站 HTTPS。
- macOS 用户：在 *系统设置 → 隐私与安全性 → 本地网络* 中允许本应用。
- 确认服务器 TLS 证书有效。RA 对生产证书启用了固定校验（pinning），证书过期或被替换时会报 `连接被拒绝`。

### 5.2 局域网扫描找不到设备
- Mac 与目标节点必须在同一广播域（无 VLAN 隔离）。
- 部分厂家需指定专用端口，可在 *设置 → 发现* 中配置。
- 杀毒软件或 VPN 可能屏蔽组播，建议先临时关闭测试。

### 5.3 忘记密码
密码重置由所在组织的管理员在后端完成，应用本身不提供重置入口；请联系管理员。

### 5.4 如何导出数据？
*报表 → 导出*，默认 CSV，可选 Excel；文件保存在你指定的本地目录，应用不会上传到任何地方。

### 5.5 本地日志在哪？
- **macOS：** `~/Library/Containers/com.armada.rapc/Data/Library/Logs/`
- **Windows：** `%APPDATA%\ra-pc\logs\`

报 Bug 时请附上最近一份 `app-YYYY-MM-DD.log`。

### 5.6 应用是否收集个人信息？
不嵌入广告 / 跟踪 SDK，不上传分析数据，不使用 IDFA。诊断日志**仅本地保存**。详见 [隐私政策](https://henry8055.github.io/ra-privacy/zh/)。

### 5.7 是否兼容 Apple Silicon？
兼容。macOS 包是 Universal Binary（x86_64 + arm64），在 M1/M2/M3 Mac 上原生运行。

### 5.8 后端证书续期后应用提示"连接被拒绝"
应用对生产证书做了 SHA-256 指纹固定校验。后端证书轮换后，请到 Mac App Store 安装包含新指纹的最新版本。

---

## 6. 提交 Bug

请提供以下信息：

1. **应用版本号**（帮助 → 关于；或导航栏右上角）
2. **操作系统版本**
3. **复现步骤**
4. **预期表现 vs 实际表现**
5. **截图**
6. **日志文件**（见 5.5）

发送至 **[hujuheng@gmail.com](mailto:hujuheng@gmail.com)** 或在 [github.com/Henry8055/ra-privacy/issues](https://github.com/Henry8055/ra-privacy/issues) 提交 issue。

我们会回复工单编号和预计修复版本。

---

## 7. 安全漏洞披露

发现安全漏洞，请**不要**公开提交 issue。请发邮件至 [hujuheng@gmail.com](mailto:hujuheng@gmail.com) ，主题以 `[SECURITY]` 开头。我们会在 2 个工作日内确认并按负责任披露原则协同处理。

---

## 8. 发布与更新渠道

- macOS：通过 **Mac App Store** 自动更新。
- Windows：通过组织内分发渠道更新。
- 更新日志在应用内 *帮助 → 新功能* 中查看，本页下方亦同步。

---

## 9. 最近版本

| 版本 | 日期 | 要点 |
| ---- | ---- | ---- |
| **2.10.31** | 2026-05-10 | 首个 Mac App Store 发布版本；签名链路完整打通 |
| 2.10.30 | 2026-05-09 | 引入 fastlane 自动化发布流水线 |
| 2.10.x | 2026-04 ~ 05 | 性能与稳定性改进 |

完整更新日志见应用内 *帮助 → 新功能*。

---

## 10. 联系方式

| 渠道 | |
| ---- | -- |
| **邮箱** | [hujuheng@gmail.com](mailto:hujuheng@gmail.com) |
| **GitHub Issues** | [github.com/Henry8055/ra-privacy/issues](https://github.com/Henry8055/ra-privacy/issues) |
| **隐私政策** | [/en/](https://henry8055.github.io/ra-privacy/en/) · [/zh/](https://henry8055.github.io/ra-privacy/zh/) |
| **响应时效** | 2 个工作日 |

---

English version: [/en/support/](https://henry8055.github.io/ra-privacy/en/support/)
