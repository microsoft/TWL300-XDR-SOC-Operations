---
title: Introduction
layout: home
nav_order: 1
---

# TechWorkshop L300 XDR SOC Operations

## **Learning objectives**:  
At the end of this workshop, you will be able to:

- Differentiate responsibilities across architecture, engineering, and operations to align workflows with Microsoft Defender XDR.
- Investigate incidents by pivoting across entities and mapping attack scope, timing, and indicators using Attack Story.
- Execute Automated Investigation and Response (AIR) workflows to contain and remediate threats effectively.
- Validate remediation outcomes, re-hunt for residual activity, and prioritize posture improvements with Secure Score.
- Integrate learned skills into ongoing SecOps practices that strengthen operational rigor and customer security programs.




## **Lab objectives**:
By the end of this workshop, you'll be able to:

- Establish a unified prevention baseline by evaluating Secure Score, Exposure Management, and configuration gaps across MDO, MDE, MDI, and MDA for all personas.
- Implement consistent email threat protection with Microsoft Defender for Office 365 (Safe Links, Safe Attachments, Anti-phish) to prevent BEC and credential phishing.
- Deploy and validate endpoint protection and response capabilities using Microsoft Defender for Endpoint (EDR in block mode, ASR rules, Tamper Protection, automated remediation).
- Strengthen identity protection by fully deploying Microsoft Defender for Identity (MDI) sensors across DCs, ADFS, and Entra ID to detect lateral movement and credential theft.
- Discover and govern cloud app usage through Microsoft Defender for Cloud Apps (MDA) using Cloud Discovery, sanctioned/unsanctioned tagging, and session controls.
- Perform unified incident investigation using Microsoft Defender XDR's incident and attack story views to trace cross-domain attack paths and understand the blast radius.
- Configure automated attack disruption and containment mechanisms to stop ongoing attacks across endpoints, identities, and cloud apps with minimal analyst intervention.
- Conduct root cause analysis (RCA) by mapping alert chains, identifying failed controls, and recommending permanent configuration hardening measures.
- Develop persona-based response playbooks that define prevention, detection, investigation, and remediation actions for CISO, Security Architects, Security Engineers, and SOC Analysts.
- Quantify business and operational impact by translating technical risk metrics (MTTR, Secure Score improvements, exposure reduction) into executive-level insights.
- Implement governance and reporting frameworks for visibility, compliance alignment, and continuous improvement across hybrid and frontline workforces.
- Create a sustainable SecOps maturity roadmap integrating Defender XDR components, ensuring measurable outcomes and automation adoption.



## **Customer scenario**:

Zava Oil & Resources, a Canadian energy company with 26,000 employees, operates in the oil, gas, and petrochemical sectors and is expanding into downstream retail and digital logistics management. This growth strategy is driving the adoption of Microsoft 365 and Defender security solutions to support hybrid operations across office staff and frontline workers. However, the company's mixed licensing model-Microsoft 365 E3, F3, and Defender for Office 365 P2-has led to inconsistent security coverage, resulting in uneven visibility and gaps across endpoints, identities, and cloud workloads.

As Zava scales its digital footprint, it faces key challenges including alert fatigue, slow investigations, and limited visibility into the full attack chain. Incomplete deployment of Microsoft Defender for Endpoint (MDE) and Defender for Identity (MDI) has left blind spots, particularly across unmanaged devices and domain controllers. Manual remediation processes, coupled with limited automation and skill disparities within the SOC, have increased response times and operational risk. Leadership also lacks consistent metrics like Secure Score and Mean Time to Respond (MTTR) to assess security maturity and effectiveness.

Zava's tactical needs center on gaining unified visibility into their environment, protecting identities and endpoints, managing access securely, and automating response workflows. Their goal is to standardize security controls across hybrid users while maintaining compliance and reducing risk. Yet, the organization is cautious about the perceived complexity of Defender XDR integration, the learning curve for staff, and potential business disruption from automation.

Microsoft's value proposition directly addresses these concerns through a cross-platform, multi-cloud Defender XDR ecosystem that integrates endpoint, identity, cloud app, and email protection. This unified approach combines Microsoft Defender for Office 365 (MDO), Defender for Endpoint (MDE), Defender for Cloud Apps (MDA), and Defender for Identity (MDI) with AI-driven automation and Copilot for Security to reduce alert fatigue, improve time-to-remediation, and strengthen Zero Trust posture. By leveraging Secure Score, Threat Analytics, and Exposure Management, Zava's leadership can align cybersecurity investments with measurable business outcomes-enhancing both resilience and executive confidence.