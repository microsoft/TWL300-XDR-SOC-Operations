---
title: 'Exercise 00: Set up the environment'
layout: default
nav_order: 2
has_children: true
---

# Exercise 00: Set up the environment

## Tenant and licensing
- New or existing Azure Subscription with **Owner** permissions.
- Active Microsoft 365 tenant with **security.microsoft.com** access.
- Ensure your global admin account is licensed:
   - **Microsoft 365 E5** would cover all the following requirements:
      - ** Defender for Endpoint Plan 2**. Part of:
         - Microsoft 365 E5/A5/G5
         - Microsoft 365 E5 Security (and A5/G5/F5 Security)
         - Microsoft 365 F5 Security and compliance
         - Windows 11 Enterprise E5/A5
         - Windows 10 Enterprise E5/A5
      - **Microsoft Defender for Office 365 Plan 2**. Part of:
         - Microsoft 365 E5/A5/G5
         - Microsoft 365 E5 Security (and A5/G5/F5 Security)
         - Microsoft 365 F5 Security & Compliance
         - Office 365 E5/A5/G5
      - (Optional) **Exchange Online Plan 1**. Part of:
         - Microsoft 365 E5/A5/G5
         - Microsoft 365 E3/A3/G3
         - Office 365 E5/A5/G5
         - Office 365 E3/A3/G3
         - Office 365 E1

## Roles
**Global Admin** role for environment configurations.

 {: . important }
 > Real-world deployments should use granular RBAC assignments.

## Persona mapping - User roles


| **Persona** | **Primary focus** | **Permissions required** |
|:------------|:------------------|:-------------------------|
| Chief Information Security Officer (CISO) | Approve scope, licenses, risk guardrails, who gets what roles | Global Admin (approve), no scripting |
| Security Architecture Team | Reference architecture, RBAC model, policy baselines (MDO/MDE/MDCA), exposure metrics | Security Administrator/Global Reader |
| Security Engineering & Administration | Build Azure lab infra, create users & assign licenses, configure baselines, onboard devices, turn on integrations | Global Admin (setup), Security Admin, Exchange Admin |
| SOC Analyst | Validate that data is flowing, run safe simulations (phish/EICAR), confirm unified incidents and hunting | Security Operator / Security Reader |

### Resources you’ll use

- **Skillable lab VM**  
  - Your primary workstation for the entire lab.  

- **Azure subscription (your own)**  
  - You must have **Owner** on this subscription.  
  - Used to create the **rg-xdr-lab** resource group and deploy the **winvm-mde** VM and its supporting network resources.

- **Microsoft 365 / Entra ID tenant**  
  - Hosts all user accounts, roles, and licenses used in the exercises.  
  - Defender XDR, Defender for Endpoint, Defender for Office 365, and Defender for Cloud Apps are all tied to this tenant.

- **Lab personas (created by script)**  
  - `ciso`, `arch1`, `eng1`, `admin1`, `soclead`, `analyst1`, `user1`, `user2`  
  - These are created and role-assigned by script in **Task 01** and reused throughout later exercises.

- **winvm-mde (Azure VM)**  
  - A Windows VM deployed into **rg-xdr-lab** in your subscription.  
  - Onboarded to Defender for Endpoint and used to:
    - Generate test alerts (EICAR file, browsing SaaS sites).  
    - Validate endpoint configuration, ASR rules, isolation, and Live Response.