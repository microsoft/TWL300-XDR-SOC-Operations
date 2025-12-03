---
title: '09: Advanced Hunting tables that get populated for these scenarios'
layout: default
nav_order: 9
parent: 'Exercise 00: Set up the environment'
---

## Advanced Hunting tables that get populated for these scenarios



#### Endpoint (Defender for Endpoint - MDE)
Triggered by: VM onboarding + running the EICAR test + normal browsing.

| Table | Description | Expected Events |
|--------|--------------|----------------|
| DeviceInfo | Device enrollment / heartbeat | win11-xdr appears with OS, version, and onboarding status |
| DeviceNetworkEvents | Network connections from the VM | SaaS site connections (dropbox.com, box.com, etc.) |
| DeviceProcessEvents | Process creation | EICAR test file execution command, PowerShell commands |
| DeviceFileEvents | File create/delete/quarantine | EICAR file write + quarantine event |
| DeviceRegistryEvents | Registry changes (less relevant here) | Standard OS operations |
| DeviceEvents | Generalized telemetry (sensors, defender agent) | Mixed OS events, endpoint telemetry |
| AlertInfo / AlertEvidence | Alert and entity relationship | "EICAR test file detected" alert |

---

#### Email (Defender for Office 365 - MDO)
Triggered by: Safe Links/Safe Attachments policies + Attack Simulation (Credential Harvest).

| Table | Description | Expected Events |
|--------|--------------|----------------|
| EmailEvents | High-level metadata about delivered mail | Simulated phish email to user1/user2 |
| EmailUrlInfo | URLs rewritten/analyzed by Safe Links | Rewritten phishing links from simulation |
| EmailAttachmentInfo | Attachments scanned by Safe Attachments | None for credential-harvest sim; present if using malware payloads |
| EmailPostDeliveryEvents | User clicks, report, ZAP actions | User clicking the phish link if they interact |
| AlertInfo / AlertEvidence | Alerts generated for phishing or simulation detection | "Phish
 delivered/simulated phish" incident |

---

#### Cloud Apps (Defender for Cloud Apps - MDCA)
Triggered by: Browsing SaaS sites on the onboarded VM after enabling MDE→MDCA integration.

| Table | Description | Expected Events |
|--------|--------------|----------------|
| CloudAppEvents | Cloud Discovery logs ingested from MDE | URLs/domains for SaaS apps, mapped to known Cloud App IDs |
| CloudAppDiscoveryData | Enriched aggregates for discovered apps (not directly queryable) | Populates Cloud Discovery UI cards |

---

#### Identity / Conditional Access (Entra ID + Identity Protection)
Triggered by: CA policies enforcing MFA + simulated risky sign-ins (user sign-ins to portal).

| Table | Description | Expected Events |
|--------|--------------|----------------|
| IdentityLogonEvents | Sign-in attempts from all users | Normal sign-ins by eng1, arch1, soclead, etc. |
| IdentityDirectoryEvents | Directory operations (role adds, policy creation) | BreakGlass group creation, CA policy updates |
| IdentityQueryEvents | Queries from identity service (rare) | Optional |
| AlertInfo / AlertEvidence | Alerts for risky sign-ins or CA blocks | "Sign-in blocked" if CA denies legacy auth |

---

#### Unified Incidents, Alerts & Entities
Where: Defender XDR **Incidents** page and **Advanced hunting**.

| Table | Purpose | Populated From |
|--------|----------|----------------|
| AlertInfo | Summary record for every alert (any product) | All domains above |
| AlertEvidence | Links alerts to users/devices/mail/URLs | All domains above |
| IncidentInfo (preview) | Unified incident metadata | Aggregated from AlertInfo/Evidence |
| SecurityRecommendation (optional) | Device/email security recommendations | MDE + MDO |