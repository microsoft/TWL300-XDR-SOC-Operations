---
title: 'Exercise 06: Unified incident investigation in Defender XDR'
layout: default
nav_order: 8
has_children: true
---

# Exercise 06: Unified incident investigation in Defender XDR

## Exercise learning objectives  

- Use unified **Incidents**, **Attack story**, and **Entity timelines** to trace the kill chain.  
- Run **Advanced Hunting (KQL)** to expand scope and quantify blast radius.  
- Document containment, remediation actions, and evidence for **root cause analysis (RCA)**.  

**Estimated time:** 60 minutes  

---

## CISO Overview - Scenario and goals 

Zava Oil & Resources faces a cross-domain incident: a targeted phishing attack led to credential reuse and suspicious lateral movement to a file server, followed by an OAuth app consent and an endpoint alert on a known credential dumper.  

Your goal: take ownership fast, show the full attack chain, stop the spread across **endpoints**, **identities**, **email**, and **apps**, and produce evidence and metrics for the post-incident review (owner, actions, timelines, and residual risk).  

This exercise uses the **Defender XDR unified portal**, enabling the team to investigate one incident end-to-end instead of switching across products.  
