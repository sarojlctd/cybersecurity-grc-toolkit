# Corporate Risk Register & Scoring Matrix

**Document Reference:** GRC-RR-001  
**Target Audience:** Risk Management Committee, CISO, IT Audit Teams  
**Classification:** Public Domain Template (Sanitized)

---

## 1. Overview
This framework provides a standardized methodology for logging, scoring, and tracking corporate IT and cybersecurity risks. It utilizes a classic $5 \times 5$ Risk Matrix to determine the Qualitative Risk Score based on Likelihood and Impact.

---

## 2. Risk Assessment Framework

### Likelihood Rating (1-5)
1. **Rare:** Highly unlikely to occur; may happen only in exceptional circumstances.
2. **Unlikely:** Low probability; could happen at some point.
3. **Possible:** Might occur at some point; has happened in similar organizations.
4. **Likely:** High probability; expected to occur in most circumstances.
5. **Almost Certain:** Expected to occur imminently or multiple times a year.

### Impact Rating (1-5)
1. **Negligible:** Minor localized IT disruption; no financial or regulatory impact.
2. **Minor:** Short-term downtime of non-critical systems; low financial impact.
3. **Moderate:** Partial outage of core systems; minor regulatory notification required.
4. **Major:** Significant operational outage; loss of critical data; direct financial penalty.
5. **Critical:** Complete business paralysis; severe data breach; catastrophic regulatory fines or license revocation.

---

## 3. Active Risk Register Template

| Risk ID | Risk Description | Vulnerability / Root Cause | Initial Likelihood (1-5) | Initial Impact (1-5) | Inherent Risk Score | Mitigation Strategy / Controls | Residual Risk Level | Owner | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **RSK-01** | Ransomware encryption of core systems. | Legacy operating systems; absence of centralized multi-factor authentication (MFA). | 4 | 5 | **20 (Critical)** | Deploy EDR tools, enforce mandatory MFA on all endpoints, isolate immutable backups. | Moderate | Infrastructure Head | Open |
| **RSK-02** | Unauthorized data center physical access. | Outdated biometric logging system; missing CCTV coverage on secondary emergency exit. | 2 | 4 | **8 (Low)** | Upgrade physical access logs, install secondary motion-activated CCTV camera. | Low | Facilities Manager | In Progress |
| **RSK-03** | Regulatory non-compliance fine. | Absence of formalized annual IT General Controls (ITGC) review. | 3 | 4 | **12 (Medium)** | Retain certified CISA professional to establish a recurring quarterly IT Audit cycle. | Low | GRC Lead | Resolved |

---

## 4. Review and Sign-off Log
- [ ] Review risk entries against current threat landscape quarterly.
- [ ] Present Critical and Major inherent risks to the Board of Directors.
- [ ] Update mitigation timelines for all items labeled "In Progress".
