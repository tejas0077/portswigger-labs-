# PortSwigger Lab: Username Enumeration via Different Responses

## 🔐 Lab Overview
This PortSwigger Web Security Academy lab demonstrates how authentication systems can accidentally leak information about valid usernames through inconsistent response messages or lengths.

The objective of the lab:

1. Enumerate a valid username using different server responses.
2. Brute‑force the password for this username.
3. Successfully log in and access the user account.

---

## 🛠 Tools Used
- Burp Suite Intruder  
- HTTP Request/Response Analysis  
- Custom Username and Password Wordlists  

---

## 🧩 Methodology

### 1️⃣ Username Enumeration
I intercepted the login request using Burp Suite and sent it to Intruder.  
I tested multiple usernames using a **Sniper** attack.

One specific username returned a **different response length**, indicating:



