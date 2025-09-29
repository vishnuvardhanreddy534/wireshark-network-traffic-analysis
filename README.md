# wireshark-network-traffic-analysis
# Wireshark Network Traffic Analysis

This repository documents the process of capturing and analyzing network traffic using **Wireshark**. The analysis highlights the dangers of transmitting data over HTTP and the importance of using **HTTPS** for secure communication.

---

## 📌 Project Overview

The main goal of this project was to demonstrate how sensitive information can be exposed over unencrypted HTTP traffic. Using Wireshark, we captured login requests where credentials were transmitted in plaintext. The study emphasizes why websites must enforce **HTTPS (TLS/SSL)** to protect users.

---

## 🔎 Key Findings

* A `POST` request was observed to **userinfo.php** on `testphp.vulnweb.com`.
* Request used: `application/x-www-form-urlencoded`.
* Credentials exposed in plaintext:

  * **Username**: `vishnu`
  * **Password**: `123456`
* Data was transmitted via **HTTP** (unencrypted).
* Without HTTPS, attackers can intercept and read sensitive data.

---

## ⚠️ Security Implications

Using HTTP instead of HTTPS exposes:

* **Login credentials** to interception.
* Risk of **man-in-the-middle (MITM) attacks**.
* **Identity theft** and account takeovers.
* Potential for **large-scale breaches** if reused credentials are compromised.

---

## ✅ Recommendations

* Enforce **HTTPS** across all applications.
* Install and configure valid **TLS/SSL certificates**.
* Redirect all HTTP traffic to **HTTPS**.
* Use **HSTS (HTTP Strict Transport Security)** to prevent protocol downgrade attacks.
* Combine with **MFA (Multi-Factor Authentication)** for stronger security.

---

## 📂 Files in Repository

* `Wireshark_Network_Analysis.pdf` → Detailed report with screenshot and findings.
* `Screenshot.png` → Captured Wireshark traffic image.
* `README.md` → Project documentation (this file).

---

## 🚀 How to Reproduce

1. Install [Wireshark](https://www.wireshark.org/).
2. Capture login requests on a site using **HTTP** (for testing only).
3. Observe the plaintext credentials in the packet capture.
4. Compare by repeating the same process on an **HTTPS-enabled site** — credentials will be encrypted and unreadable.
5. Document the difference between **HTTP vs HTTPS**.

---

## 📖 Conclusion

This project demonstrates why **HTTPS is essential**. Unlike HTTP, HTTPS ensures confidentiality, integrity, and authentication by encrypting all traffic. Organizations must adopt HTTPS to protect users and build trust in their applications.

---

### 👤 Author

Vishnu Vardhan
📧 Contact: *(vishnuvardhan.tella@gmail.com)*
