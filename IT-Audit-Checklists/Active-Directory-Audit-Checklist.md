# Active Directory Security Audit Checklist

**Document Reference:** AUD-AD-002  
**Target Domain:** Identity & Access Management (IAM), Domain Infrastructure  
**Auditor Profile Focus:** CISA / IT Internal Audit  
**Classification:** Sanitized Enterprise Audit Work Program

---

## 1. Audit Objective & Scope
The objective of this work program is to evaluate the security configuration, operational management, and administrative privileges within the corporate Active Directory (AD) environment. The scope covers domain controller hardening, password policy enforcement, administrative group segregation, and account lifecycle management.

---

## 2. Audit Procedures & Control Verification

### Phase 1: Account & Password Policy Governance
This phase verifies that logical access controls match corporate policy and industry standards (e.g., NIST, CIS Benchmarks).

- [ ] **AD-1.1: Password Complexity Enforcement**  
  *Procedure:* Extract and review the Default Domain Policy settings. Verify that password complexity is enabled, minimum password length is set to at least 12 characters (or per local regulations), and history remembers at least 24 past passwords to prevent immediate reuse.  
  *Evidence Required:* Group Policy Object (GPO) settings report (`gpresult` or HTML export).

- [ ] **AD-1.2: Account Lockout Thresholds**  
  *Procedure:* Verify that account lockout policies are configured to mitigate brute-force attempts. Recommended threshold is no more than 5 to 10 failed login attempts, with a lockout duration of at least 30 minutes.  
  *Evidence Required:* Default Domain Policy Account Lockout settings screen capture or backup configuration export.

- [ ] **AD-1.3: Inactive & Dormant Accounts**  
  *Procedure:* Review the process for identifying and disabling inactive accounts. Query Active Directory for user and computer accounts that have not authenticated within the last 90 days. Cross-verify a sample of disabled accounts against recent HR resignation logs.  
  *Evidence Required:* Exported list of inactive accounts via PowerShell (`Search-ADAccount -AccountInactive`) and HR exit logs.

---

### Phase 2: Administrative Privileges & Group Membership
This phase addresses the risk of unauthorized privilege escalation and lateral movement.

- [ ] **AD-2.1: Domain Admins & Enterprise Admins Review**  
  *Procedure:* Extract the complete list of members in high-privileged groups (Domain Admins, Enterprise Admins, Schema Admins, Administrators). Verify that membership is strictly minimized (ideally less than 5 named accounts) and that no generic or shared accounts exist in these groups.  
  *Evidence Required:* Direct active membership list exported to CSV.

- [ ] **AD-2.2: Administrative Privilege Segregation**  
  *Procedure:* Verify that system administrators use dedicated administrative accounts (e.g., `adm_john`) for domain management, and standard user accounts (e.g., `john`) for daily tasks like email and web browsing.  
  *Evidence Required:* Sample verification of admin user profiles and HR alignment.

- [ ] **AD-2.3: Service Account Governance**  
  *Procedure:* Review the inventory of Active Directory service accounts. Ensure they are configured with the principle of least privilege, are restricted from interactive interactive domain logons, and where possible, utilize Group Managed Service Accounts (gMSA) for automated password rotation.  
  *Evidence Required:* List of service accounts showing User Rights Assignment GPOs ("Deny log on locally", "Deny log on through Remote Desktop Services").

---

### Phase 3: Domain Controller Hardening & Logging
This phase evaluates physical and logical protections around the AD servers themselves.

| Control Ref | Control Objective | Testing Step / Methodology | Expected Result |
| :--- | :--- | :--- | :--- |
| **AD-3.1** | DC OS Hardening | Verify that only essential roles and services are running on Domain Controllers. Print/File sharing, web servers (IIS), or third-party tools must be absent. | Zero non-AD components installed on bare-metal or VM instances. |
| **AD-3.2** | Audit Policy Configuration | Check Advanced Audit Policy Configurations via GPO to ensure successful/failed account logons, directory service changes, and privilege uses are captured. | Logging policy explicitly configured, not left to default "No Auditing". |
| **AD-3.3** | SIEM Integration | Confirm that security event logs from all Domain Controllers are forwarded in real-time to a centralized SIEM or SOC monitoring cluster. | Log ingestion flows validated for all operational DCs with alerts active for anomalous admin group modifications. |

---

## 3. Working Notes & Observations Tracker
*Auditors can use this section during fieldwork to note variances, exceptions, or observations.*

* **Observation 1:** 
* **Observation 2:**
