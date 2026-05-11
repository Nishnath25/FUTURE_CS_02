# 🔐 Phishing Email Detection & Awareness Report

### Future Interns — Cybersecurity Internship | Task 2

---

## 📌 About This Project

This project analyzes **3 real phishing email samples** collected from a public security research repository. Each email was examined using professional cybersecurity tools to identify attack indicators, classify risk levels, and provide prevention guidelines for employees and organizations.

This task was completed as part of the **Future Interns Cybersecurity Internship Program — Task 2**.

---

## 📧 Emails Analyzed

| # | Email Type | Claimed Sender | Real Sending Server | Risk Level |
|---|---|---|---|---|
| 1 | Inheritance Scam (Advance Fee Fraud) | icloud.com (spoofed) | mail.decipherhealth.in | 🔴 PHISHING |
| 2 | Payment Fraud (MercadoPago) | mercadopago.com.br (spoofed) | soldrun.com | 🔴 PHISHING |
| 3 | Fake Prize Scam (Kohl's) | kohls.com (spoofed) | gybatedtioneer.net | 🔴 PHISHING |

---

## 🔍 Key Findings

### Email 1 — Inheritance Scam
- Sender and recipient had the **same spoofed iCloud address**
- Reply-To redirected to attacker's Gmail (ftom1346@gmail.com)
- SPF: Softfail ❌ | DKIM: None ❌ | DMARC: Fail ❌
- 68 minute suspicious delivery delay detected
- Classic Advance Fee Fraud — no URL, reply-based attack

### Email 2 — MercadoPago Payment Phishing
- Claimed to be from mercadopago.com.br — actually sent from soldrun.com
- SPF: Fail ❌ | DKIM: Fail ❌ | DMARC: Fail ❌
- Malicious URL (ii-dnuqnaqtnq-rj.a.run.app) flagged by **7/95 vendors on VirusTotal**
- Hidden tracking pixel embedded to spy on victims
- Hidden random words used to evade spam filters

### Email 3 — Kohl's Fake Prize Phishing
- Fake sender domain ri69aezzhy.com — not related to kohls.com
- SPF: None ❌ | DKIM: None ❌ | DMARC: No Record Found ❌
- Malicious redirect link (t.co) flagged as Phishing on VirusTotal
- Fake unsubscribe link (dtherhproblem.us) also flagged as Phishing
- Hundreds of hidden random codes used for spam filter evasion
- Duplicate Content-Length headers — technical evasion trick

---

## 🛠️ Tools Used

| Tool | Purpose | Link |
|---|---|---|
| GitHub — phishing_pot | Real phishing email samples | github.com/rf-peixoto/phishing_pot |
| Google Header Analyzer | Email routing & header analysis | toolbox.googleapps.com/apps/messageheader |
| MXToolbox | SPF, DKIM, DMARC verification | mxtoolbox.com/EmailHeaders.aspx |
| VirusTotal | Malicious URL scanning | virustotal.com |
| Canva | Professional report design | canva.com |

---

## 🔎 Analysis Approach

1. **Sample Collection** — Collected 3 real phishing .eml files from phishing_pot GitHub repository
2. **Header Extraction** — Opened raw email files and copied the full email header
3. **Header Analysis** — Pasted headers into Google Header Analyzer to examine email routing
4. **Authentication Verification** — Used MXToolbox to check SPF, DKIM, and DMARC results
5. **URL Scanning** — Copied suspicious links and scanned them safely using VirusTotal
6. **Indicator Identification** — Documented all phishing red flags found in each email
7. **Risk Classification** — Classified each email as Safe / Suspicious / Phishing
8. **Report Creation** — Documented all findings with screenshots as evidence in a professional report
9. **Prevention Guidelines** — Created Do's and Don'ts awareness guide for employees

---

## 📊 Authentication Results Summary

| Email | SPF | DKIM | DMARC | VirusTotal |
|---|---|---|---|---|
| Email 1 — Inheritance Scam | Softfail ❌ | None ❌ | Fail ❌ | No URL (reply-based attack) |
| Email 2 — MercadoPago | Fail ❌ | Fail ❌ | Fail ❌ | 7/95 vendors — MALICIOUS |
| Email 3 — Kohl's Prize Scam | None ❌ | None ❌ | None ❌ | Flagged as Phishing |

---



## 🛡️ Prevention Guidelines

### ✅ Do's
- Always verify the sender's email domain carefully
- Hover over links before clicking to see the real destination
- Contact IT/Security team if you receive a suspicious email
- Use Multi-Factor Authentication (MFA) on all accounts
- Call the sender on a known number to verify urgent requests
- Report phishing emails to your security team immediately

### ❌ Don'ts
- Never click links in unexpected or urgent emails
- Never enter your password on sites reached via email links
- Never transfer money based only on email instructions
- Never open attachments from unknown senders
- Never share OTPs, passwords, or PINs via email
- Never click "Unsubscribe" in suspicious emails

---

## 👤 Intern Details

- **Name:** NISHANTH
- **Program:** Future Interns — Cybersecurity Internship
- **Task:** Task 2 — Phishing Email Detection & Awareness System
- **Date**:12 May 2026

---

## 🔗 References

- Phishing Email Samples: https://github.com/rf-peixoto/phishing_pot
- Phishing Mail Examples: https://github.com/autinerd/phishing-mail-examples
- Google Header Analyzer: https://toolbox.googleapps.com/apps/messageheader/
- MXToolbox: https://mxtoolbox.com/EmailHeaders.aspx
- VirusTotal: https://www.virustotal.com

---

> **"When in doubt — don't click. Verify first."**
