
# 🧠 Cybersecurity Exercise: USB Found in a Parking Lot

**Scenario:**  
An employee finds a USB flash drive in the company parking lot. Curious, they plug it into their office workstation to see what's on it.

## 🔥 What Could Go Wrong?

- **Malware Infection:** The USB may contain auto-run malware or a dropper that installs a backdoor.
- **Data Breach:** Malware could exfiltrate sensitive files, keystrokes, or credentials.
- **Privilege Escalation:** If run with admin rights, it could install rootkits or gain lateral movement inside the network.
- **Ransomware Deployment:** Malicious code could encrypt internal files and demand payment.

## ❗Security Mindset: Red Flags

- Unknown USB media is a classic **baiting attack**.
- Plugging it into a corporate device bridges a trusted/untrusted boundary.
- Assumes physical security failures won't lead to cyber threats.

## ✅ What Should Be Done Instead?

1. **Do Not Plug It In!**
   - Treat unknown hardware like unknown software: potentially malicious.

2. **Report It Immediately:**
   - Notify the IT/security team or follow your internal incident reporting procedure.

3. **Isolate the Device (if already inserted):**
   - Disconnect the computer from the network.
   - Do **not** interact with any files on the USB.

4. **Let Security Teams Handle It:**
   - The USB should be examined in a secure, sandboxed environment.
   - Forensic tools (like Autopsy or FTK) can be used to inspect contents safely.

5. **Conduct Awareness Training:**
   - Teach employees about the risks of physical vectors like USB drives.
   - Reinforce policies on hardware use and data handling.

## 💬 Real-World Examples

- **Stuxnet:** Originally spread via USB drives in air-gapped environments.
- **Red Team Exercises:** Many security tests include “USB bait drops” to see if staff will plug them in.

> 🧠 **Cybersecurity Mindset:**  
> “If it's too easy, it might be a trap. Assume malicious intent until proven safe.”
