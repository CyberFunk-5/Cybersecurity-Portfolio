
# 🔐 Compare Hash Function Exercise

## 📌 Objective

Demonstrate how different cryptographic hash functions work and why they're sensitive to even small changes in input. Understand the importance of collision resistance in cybersecurity.

---

## ⚙️ Tools Used

- [CyberChef](https://gchq.github.io/CyberChef/)
- Screenshot tool
- Markdown (for this documentation)

---

## 🧪 Input Examples

```text
Input A: Hello, World!
Input B: Hello, world!
```

> Note the only difference: “W” (uppercase) vs “w” (lowercase)

---

## 🧮 Generated Hashes

| **Algorithm** | **Input A Hash** | **Input B Hash** |
|---------------|------------------|------------------|
| **MD5**       | `65a8e27d8879283831b664bd8b7f0ad4` | `6cd3556deb0da54bca060b4c39479839` |
| **SHA-1**     | `d3486ae9136e7856bc42212385ea797094475802` | `7e8767b3fd243e5e5f447b2c6d8d6e3aaf7e7f1e` |
| **SHA-256**   | `315f5bdb76d078c43b8ac0064e4a0164612b1fce77c869345bfc94c75894edd3` | `64ec88ca00b268e5ba1a35678a1b5316d212f4f366b2477232534a8aeca37f3c` |

---

## 📸 Screenshots

### 🔹 MD5 Comparison
![MD5 Hash Comparison](https://imgur.com/a/qYT9wBc)

### 🔹 SHA-1 Comparison
![SHA-1 Hash Comparison](https://i.imgur.com/tqJZdjY.png)

### 🔹 SHA-256 Comparison
![SHA-256 Hash Comparison](https://i.imgur.com/JkCCQx9.png)

---

## ❓ Why This Matters

Even a single-character change results in drastically different hashes. This is called the **avalanche effect**, and it's critical for:

- **Password security**
- **Data integrity**
- **Digital signatures**
- **Blockchain transactions**

---

## 🛡️ Key Takeaways

- Hash functions are deterministic but extremely sensitive to input changes.
- MD5 and SHA-1 are no longer safe for security purposes due to known collisions.
- Always use modern hash algorithms (e.g., SHA-256, SHA-3).

---

## 📁 How to Run This Yourself

1. Go to [CyberChef](https://gchq.github.io/CyberChef/)
2. Paste `Hello, World!` and apply MD5, SHA-1, and SHA-256 recipes.
3. Do the same with `Hello, world!`
4. Observe and compare results.

---

## 📂 License

This exercise is part of a personal cybersecurity learning portfolio. Feel free to fork and customize for educational use.
