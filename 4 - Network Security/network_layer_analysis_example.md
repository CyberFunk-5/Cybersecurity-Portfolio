
# 🌐 Real-World Example: Analyzing Network Layer Communication

## Scenario

A user reports that they cannot reach `example.com` from their workstation. As a network analyst, your task is to analyze the issue using Layer 3 tools and packet captures.

---

## 🛠️ Tools Used

- `ping`
- `traceroute`
- `tcpdump`
- **Wireshark** (for deep packet inspection)

---

## 📋 Step-by-Step Investigation

### 1. **Check Connectivity Using Ping**

```bash
ping example.com
```

**Result:**
```
PING example.com (93.184.216.34): 56 data bytes
Request timeout for icmp_seq 0
Request timeout for icmp_seq 1
```

> 🔎 Suspected Issue: ICMP packets are not being returned – could be blocked or unreachable.

---

### 2. **Trace the Route**

```bash
traceroute example.com
```

**Result:**
```
1  192.168.1.1 (Router)         1.123 ms
2  10.0.0.1 (ISP Gateway)       5.456 ms
3  * * *
4  * * *
```

> 🧠 Interpretation: Packets are leaving the local network but are dropped beyond the ISP gateway.

---

### 3. **Capture Packets Using tcpdump**

```bash
sudo tcpdump -i eth0 host 93.184.216.34 -nn
```

**Sample Output:**
```
09:12:31 IP 192.168.1.100 > 93.184.216.34: ICMP echo request
09:12:32 IP 93.184.216.34 > 192.168.1.100: ICMP echo reply
```

> 🟢 Indicates that the host *is* responding. So the issue is local to the user or firewall policies.

---

### 4. **Analyze Packet in Wireshark**

- **Source IP:** 192.168.1.100
- **Destination IP:** 93.184.216.34
- **Protocol:** ICMP
- **TTL:** 64
- **Flags:** 0x00
- **Checksum:** Valid

> ✅ No fragmentation, TTL is normal, ICMP is reaching destination.

---

## 🧠 Conclusion

- The destination server is reachable.
- `ping` fails due to a **local firewall rule** blocking ICMP replies.
- DNS and routing are functioning properly.
- Confirmed via `tcpdump` and Wireshark that packets arrive and replies are being dropped locally.

---

## 🛡️ Remediation

- Adjust local firewall rules to allow ICMP echo replies.
- Verify host-based security software policies.

---

## 📘 Key Takeaways

- Always confirm what’s happening on the wire using **tcpdump** or **Wireshark**.
- ICMP blocking is common for security, but can impact diagnostics.
- Network Layer analysis reveals true packet flow regardless of system error messages.

