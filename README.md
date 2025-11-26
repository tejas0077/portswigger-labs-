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


This confirmed that the username exists.

 ✔ Valid Username Found:


 ### 2️⃣ Password Brute‑Force
I replaced the password parameter with a payload position and ran a brute‑force attack.

Most responses had length **3142**, but one response had length **187**, indicating a successful login (HTTP 302 redirect).

### 🎯 Valid Password Identified
(The exact password depends on lab run, not included here for ethical reasons.)

---

## 📚 Key Learnings

- Authentication mechanisms must use **consistent error messages**.
- Response length/behavior can reveal sensitive information.
- Intruder is highly effective for enumeration and brute‑forcing.
- Proper input validation and rate limiting are essential for security.

---

## 🏁 Lab Status  
✔ Successfully Completed  

 


