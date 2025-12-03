---
title: 'Exercise 04: Identity threat detection and response with MDI'
layout: default
nav_order: 6
has_children: true
---

# Exercise 04: Identity threat detection and response with MDI

## Exercise learning objectives  

- Verify sensor coverage (**DCs**, **ADFS**, **AD CS**, **Entra Connect**), sensor health, and **Identity Secure Score**.  
- Learn where to find this information across different parts of the **Defender XDR portal**.  
- Identify **Lateral Movement Paths (LMPs)** and create a **honeytoken** account.  
- Investigate identity alerts (for example, **DCSync** or **Pass-the-Ticket**) and define immediate mitigations.  

**Estimated time:** 90 minutes  

---

## CISO Overview - Scenario and goals

Zava Oil & Resources is observing credential-theft attempts and suspected lateral movement within their hybrid Active Directory.  

Your mandate:  
- Prove sensor coverage.  
- Expose high-risk identity paths.  
- Plant a decoy (**honeytoken**) to catch intruders early.  
- Rehearse a rapid SOC response using the **Defender XDR** portal's **Identities** capabilities (MDI).  

**Success criteria:** Improved **Identity Secure Score**, verified **ITDR dashboards**, and a rehearsed end-to-end response for DCSync/Pass-the-Ticket activity.  