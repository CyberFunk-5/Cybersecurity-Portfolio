
# 🛡️ Incident Handler Journal

**Incident ID:** INC-2025-001  
**Reported Date:** 2025-06-01  
**Reported By:** John Doe (IT Helpdesk)  
**Classification:** Malware Infection via Removable Media  
**Severity:** High  
**Status:** Resolved

---

## 📋 Summary

At approximately 09:23 AM on June 1st, 2025, an employee reported unusual system behavior after inserting an unknown USB device found in the office parking lot. Immediate action was taken to isolate the device and contain any potential threat.

---

## 🕒 Timeline of Events

| Time         | Event Description                                       |
|--------------|--------------------------------------------------------|
| 09:23 AM     | Employee reports slow system response after inserting USB |
| 09:25 AM     | Device is disconnected and workstation is isolated from network |
| 09:30 AM     | Security team alerted and incident ticket created      |
| 09:45 AM     | USB analyzed in sandbox environment – detected malware (Trojan) |
| 10:00 AM     | Workstation imaged and quarantined                     |
| 11:30 AM     | Malware removed and forensics completed                |
| 01:00 PM     | Employee debriefed and given security awareness material |
| 03:00 PM     | Security memo sent organization-wide                   |

---

## 🔍 Technical Details

**Malware Identified:** Trojan.GenericKD.6348023  
**Vector:** Auto-run script on USB drive  
**Payload:** Attempts to open a reverse shell and collect keystrokes  
**Indicators of Compromise (IoCs):**
- MD5: `9f7a1e3d6f08d2ff34b7a5a3b3c12345`
- File: `autorun.inf`, `winupdater.exe`
- IP Address: `192.0.2.123` (Command & Control server)

---

## ✅ Mitigation & Response

- USB drive secured and stored for evidence
- Workstation isolated and reimaged
- Blocked associated IPs on firewall
- Network scan completed – no lateral movement detected
- Reviewed and updated endpoint protection policies
- Refreshed USB device security training for staff

---

## 📘 Lessons Learned

- Removable media policies need better enforcement
- Endpoint detection worked as expected
- Employee awareness training needs regular refresh

---

## 👣 Follow-Up Actions

- [x] Update USB usage policy
- [x] Deploy USB device control across all endpoints
- [ ] Conduct a red team simulation involving physical vectors
- [x] Archive and close incident in case management system

---

*Prepared by:*  
**Jane Smith**  
Cybersecurity Incident Handler  
*Date:* 2025-06-02
