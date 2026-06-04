# NRB IT Guidelines - Regulatory Compliance Mapping

**Document Reference:** REG-NRB-003  
**Target Sector:** Banking & Financial Institutions (BFIs) / Class A Commercial Banks  
**Regulatory Baseline:** Nepal Rastra Bank (NRB) IT Guidelines  
**Classification:** Public Domain / Sanitized Compliance Framework

---

## 1. Purpose & Objectives
This framework maps the specific mandates of the Nepal Rastra Bank (NRB) IT Guidelines to actionable technical controls and audit procedures. It serves as an internal checklist for GRC leads and IT Auditors to ensure regulatory compliance before recurring statutory audits.

---

## 2. Regulatory Control Matrix

### Section A: IT Governance & Strategy
Ensuring that executive oversight and institutional structures align with regulatory expectations.

- [ ] **NRB-1.1: IT Steering Committee Oversight** *Guideline Mandate:* BFIs must constitute a high-level IT Steering Committee to oversee IT strategy, investments, and security operations.  
  *Audit Procedure:* Review board minutes to verify the formation of the IT Steering Committee. Confirm that meetings are held at least quarterly and that the head of IT operations reports directly to this body.  
  *Evidence:* Approved IT Steering Committee charter, meeting calendar, and signed minutes of the past 3 quarters.

- [ ] **NRB-1.2: Independent IT Audit Function** *Guideline Mandate:* An independent IT Audit must be conducted periodically by competent, certified professionals (e.g., CISA) reporting directly to the Audit Committee.  
  *Audit Procedure:* Verify that the IT Audit function is independent of the daily IT operations team. Check the tracking mechanism for previous IT audit observations.  
  *Evidence:* Past annual external IT Audit report, Management Response tracker, and board-level Audit Committee sign-offs.

---

### Section B: Information Security & Infrastructure Resilience
Tactical baselines for protecting core banking architecture and critical processing zones.

| NRB Ref | Control Objective | Technical Implementation Baseline | Audit Testing Methodology |
| :--- | :--- | :--- | :--- |
| **Section 3** | Information Security Policy | Formulate an all-encompassing, board-approved Information Security Policy aligned with ISO 27001 parameters. | Review the policy's last review date to ensure it has been updated within the trailing 12 months. |
| **Section 5** | Data Center & DR Synchronization | Ensure that critical transaction logs and core databases are replicated to the Disaster Recovery (DR) site with acceptable RPO/RTO parameters. | Request the latest data replication logs and the verified report from the most recent annual DR drill. |
| **Section 7** | Digital Channels & API Security | Secure all open API integration touchpoints, third-party vendor platforms, and single-window service connections (e.g., Nagarik App integration baselines). | Verify that multi-factor authentication (MFA) is strictly enforced, data is encrypted in transit using TLS 1.3, and annual API penetration testing certificates are valid. |

---

### Section C: Incident Reporting & Operations
Mandates governing unexpected production anomalies or systemic data breaches.

- [ ] **NRB-3.1: Central Bank Reporting Timelines** *Guideline Mandate:* Major cybersecurity incidents, systemic data breaches, or critical core banking outages must be reported to the regulator within the prescribed windows.  
  *Audit Procedure:* Examine the Incident Response Plan (IRP) to ensure it contains explicit workflows and escalation templates detailing communication channels to the central bank's supervisory division.  
  *Evidence:* Written corporate Incident Communication Policy and current emergency contact matrix.

---

## 3. Local Threat Landscape & Field Observations
*This space is utilized during recurring GRC reviews to track localized threat trends affecting regional infrastructures (e.g., regional ransomware campaigns targeting SWIFT infrastructure or local network skimming vectors).*

* **Note 1:** * **Note 2:** ```

---

## Step 2: Save (Commit) Your Document

1. Scroll down to the bottom of the page to the **Commit changes...** section.
2. In the first input field, type: `Add NRB IT Guidelines regulatory compliance mapping template`
3. Click the green **Commit changes** button.

---

## Step 3: Integrate It into Your Homepage (`README.md`)

Now let's add this final section to your main landing page directory.

1. Click on your repository name **`cybersecurity-grc-toolkit`** at the top left to return to the root folder list.
2. Click on **`README.md`**.
3. Click the **pencil icon** on the right to edit the file.
4. Scroll down to the bottom of the toolkit sections list (just right above `## 🛠️ How to Utilize These Resources`) and add this new category markdown text block:

```markdown
### 🌏 [Regional Compliance & Local Resources](./Regional-Compliance-Resources)
*Specialized compliance mappings tailored to local regulatory mandates.*
* **[NRB IT Guidelines Compliance Mapping](./Regional-Compliance-Resources/NRB-IT-Guidelines-Mapping.md):** An actionable governance and technical control matrix mapped directly to central bank directives for banking and financial institutions (BFIs).
