# Enterprise Cyber Hygiene Assessment Checklist

**Document Reference:** GRC-CH-002  
**Target Audience:** IT Operations, Internal Security Teams, System Administrators  
**Framework Alignment:** CIS Controls (Essential Cyber Hygiene), NIST CSF  
**Classification:** Public Domain / Sanitized Operational Checklist

---

## 1. Purpose & Scope
This checklist defines the foundational cyber hygiene practices required to minimize an organization's attack surface. These baseline controls are designed to prevent up to 80% of common automated cyber attacks by ensuring proper asset management, credential security, vulnerability patching, and data protection.

---

## 2. Core Cyber Hygiene Domains

### Domain 1: Inventory & Asset Control
*You cannot protect what you do not know exists.*

- [ ] **CH-1.1: Active Hardware Inventory** *Control:* Maintain an updated inventory of all physical and virtual machines connected to the corporate network. Automatically alert or block unauthorized devices using Network Access Control (NAC) or DHCP logs.
- [ ] **CH-1.2: Software Asset Inventory** *Control:* Document all authorized software applications deployed across enterprise endpoints. Ensure unauthorized or unapproved software (e.g., untrusted VPNs, personal file-sharing tools) is actively uninstalled or blocked.

---

### Domain 2: Identity & Access Management (IAM)
*Securing the keys to the kingdom.*

- [ ] **CH-2.1: Multi-Factor Authentication (MFA) Enforcement** *Control:* Enforce MFA across all corporate entry points without exception. Prioritize critical channels: corporate emails, virtual private networks (VPNs), and cloud service consoles.
- [ ] **CH-2.2: Principle of Least Privilege** *Control:* Restrict local administrative privileges on user endpoints. Standard users must not run daily operations with administrative rights, reducing the impact of malware execution.
- [ ] **CH-2.3: Credential Hardening** *Control:* Enforce a strong password baseline (minimum 12+ characters, alphanumeric, with complexity) and completely ban default vendor passwords on all network hardware, firewalls, and systems.

---

### Domain 3: Vulnerability & Patch Management
*Closing the windows before the storm hits.*

| Control Ref | Control Activity | Operational Baseline Requirement | Verification Frequency |
| :--- | :--- | :--- | :--- |
| **CH-3.1** | Operating System Patching | Deploy critical security patches to all operating systems (Windows, Linux, macOS) within 14 days of release. | Bi-Weekly / Monthly |
| **CH-3.2** | Third-Party App Updates | Update business-critical third-party software (browsers, PDF readers, office suites) to eliminate known vulnerabilities. | Monthly |
| **CH-3.3** | Perimeter Firmware Updates | Review and apply security firmware updates on perimeter routers, firewalls, and edge gateways immediately upon vendor notification. | Critical/As Released |

---

### Domain 4: Data Protection & Backup Hygiene
*Your last line of defense against ransomware.*

- [ ] **CH-4.1: Automated, Regular Backup Schedules** *Control:* Ensure critical business data, databases, and configuration files are backed up automatically at defined intervals (e.g., daily incremental, weekly full).
- [ ] **CH-4.2: Immutable or Offline Backups** *Control:* Maintain at least one copy of critical backups isolated from the primary network (air-gapped, offline, or using immutable cloud storage) to prevent ransomware from encrypting the backup files.
- [ ] **CH-4.3: Regular Backup Restoration Tests** *Control:* Periodically test the actual restoration process of your backup files. A backup is only as good as its ability to successfully restore operational systems during a crisis.

---

## 3. Annual Review and Sign-Off Log
* Track adjustments made to patch cycles based on emerging exploit data.
* Validate MFA exception lists to ensure no accounts are left exposed.
