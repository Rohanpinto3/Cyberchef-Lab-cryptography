# Cyberchef Lab (cryptography)

---

## **What is CyberChef?**

A **web-based "digital Swiss Army knife"** for encoding, decoding, encryption, and data analysis.

**Website:** [https://cyberchef.io/](https://cyberchef.io/)

---

## **Purpose:**

- **Decode/encode** data quickly
- **Analyze** malware artifacts
- **Convert** between formats
- **Extract** hidden information

go to the cyberchef website , Let’s use cyberchef to explore and experiment some of the cryptographic algorithm.

  

![image.png](image.png)

# **Let's explore MD5 hashing in CyberChef!** 🔍

---

### Step 1. go to search type md5 and drag&drop it to the recipe

 

![image.png](image%201.png)

in input let’s try adding something basic like “password123” and check out the hash output 

![image.png](image%202.png)

here you can see we i used 11 length long input which encrypted into 32 length long hash string 

### lets tweak it a little and change some characters to see different hash output:

![image.png](image%203.png)

Look  changing p → P & 3 → 4 makes different in hash output.

### **Password123 → 482c811da5d5b4bc6d497ffa98491e38**

### **Password124 → 0da21eca396b1532f6cccf167234b441**

**COMPLETELY DIFFERENT hashes!** 🔥

## **The Security Lessons:**

### **1. Avalanche Effect**

- **Tiny change** (3→4) = **Completely different hash**
- This is **by design** - prevents guessing patterns

### **2. Case Sensitivity**

- `password123` vs `Password123` would also give **different hashes**
- **Capitalization matters** in hashing

### **3. Why This Matters for Security:**

- **Password storage:** Websites store hashes, not plain passwords
- **File integrity:** Small file corruption = different hash = detect tampering
- **Malware detection:** One byte change in malware = different hash fingerprint

---

# **Let's explore sha256 hashing in CyberChef!** 🔍

---

### lets remove md5 from the recipe and drag & drop sha2 & size 256

![image.png](image%204.png)

![image.png](image%205.png)

### **Input 1: `testing_hash`**

**SHA256:** `dfb0f806c5cea0ce97d87eac5688064180a065c0af4c3c907b4cc3892c6ec544`

### **Input 2: `"testing_hash"` (with quotes)**

**SHA256:** `ea4b36331330ee91b1a24a425253a2e645643d219cbccc44e4e03fcec4cb3f93`

**COMPLETELY DIFFERENT!**

## **The Key Security Lesson:**

### **Hashing Includes EVERY Character:**

- Letters, numbers, symbols, spaces, **even quotes!**
- `testing_hash` ≠ `"testing_hash"`
- The **quotes are part of the input** and change the hash

---

---

```
## **Cryptography Lab - CyberChef**
### **MD5 & SHA256 Hashing Experiments**

**Exercises Completed:**
1. MD5 hashing - Avalanche effect demonstration
2. SHA256 vs MD5 comparison  
3. Character sensitivity testing

**Key Findings:**
- Tiny input changes create completely different hashes
- Quotes and symbols are included in hash calculations
- SHA256 produces longer, more secure hashes than MD5

**Lab Completion**
- **Date:** November 15, 2025
- **Status:** ✅ COMPLETED
---
```