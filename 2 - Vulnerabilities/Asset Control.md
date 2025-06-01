# 🧰 Asset Control Exercise – Bruce Wayne

## 🎯 Objective

Demonstrate the implementation and verification of asset control within an enterprise environment. This includes asset inventory management, classification, and access control enforcement.

---

## 🧩 Scenario Overview

**Title:** Untracked Developer Workstations Exposing Source Code  
**Date Identified:** 2025-02-21  
**Detected By:** Routine Internal Audit  
**Environment:** Hybrid (Cloud and On-Prem)

---

## 💼 Background

During a quarterly asset inventory audit, the security team discovered two high-performance workstations used by senior developers that were not listed in the official CMDB (Configuration Management Database). These systems had direct access to the internal Git repositories and no endpoint security agents installed.

---

## 🧾 Asset Details

| Asset Name         | Type           | Owner        | Location     | Classification   | Status     |
|--------------------|----------------|--------------|--------------|------------------|------------|
| `dev-ws-01`        | Workstation    | A. Pennyworth   | HQ - Floor 2 | Internal - Code  | Untracked  |
| `dev-ws-02`        | Workstation    | B. Wayne    | HQ - Floor 2 | Internal - Code  | Untracked  |

---

## 🧪 Risk Assessment

| Risk                | Impact     | Likelihood | Risk Score | Notes |
|---------------------|------------|------------|------------|-------|
| Unauthorized access | High       | Medium     | 12/25      | Repo cloning without MFA or logging |
| Data exfiltration   | High       | Low        | 10/25      | Devices lacked endpoint monitoring |
| Shadow IT exposure  | Medium     | High       | 15/25      | Not in asset inventory              |

---

## 🛠️ Control Measures

| Control Type         | Description                                                      | Implemented |
|----------------------|------------------------------------------------------------------|-------------|
| Inventory Enforcement| Enforced CMDB sync via DHCP/DNS asset discovery                  | ✅ Yes       |
| Endpoint Hardening   | Deployed EDR (SentinelOne) and enabled firewall                  | ✅ Yes       |
| Privilege Management | Restricted repo access via Okta SSO and removed local SSH keys   | ✅ Yes       |
| Asset Tagging        | Devices tagged and barcoded for physical inventory               | ✅ Yes       |
| Policy Update        | Developer onboarding checklist updated with asset registration   | ✅ Yes       |

---

## 🔐 Verification Steps

1. Queried CMDB and Active Directory to match MAC addresses
2. Ran endpoint compliance scan using internal vulnerability scanner
3. Verified EDR and encryption agent installation remotely
4. Reviewed GitHub Enterprise logs for unauthorized activity
5. Cross-validated asset records with physical IT inventory

---

## ✅ Post-Remediation Outcome

- All devices are now tracked and compliant
- Audit log alerts added for unmanaged endpoints
- Asset control policies updated in onboarding SOP
- Quarterly asset reconciliation process automated via API

---

## 📚 Lessons Learned

- Manual inventory alone is insufficient for agile teams
- Asset control must be tightly integrated with DevOps workflows
- Regular audits are critical even for trusted users
- Continuous asset visibility is foundational to Zero Trust

---

**Prepared by:** Bruce Wayne  
**Role:** Cybersecurity Analyst  
**Date:** 2025-05-28

   
