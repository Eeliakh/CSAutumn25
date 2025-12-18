# 1️⃣ Introduction

**Tester(s):**  
- Name:  Eeli Ösberg NTIS22K

**Purpose:**  
- Describe the purpose of this test (e.g., identify vulnerabilities in registration and authentication flows).
testing the page for any vulnerabilities, issues or potential threatening bugs.

**Scope:**  
- Tested components: Registeration, create an account
- Exclusions: none?
- Test approach: Gray-box / Black-box / White-box

**Test environment & dates:**  
- Start:  09.12.25
- End:  18.12.25
- Test environment details (OS, runtime, DB, browsers): chrome based browser, ZAP, Docker, Windows 11

**Assumptions & constraints:**  
- e.g., credentials provided, limited time, etc.
None to note. Freedom with the Zap, and deadline by 18.12.2025
---

# 2️⃣ Executive Summary

**Short summary (1-2 sentences):**  

Using ZAP to test any possible problems with the registeration and webpage. Anything that can be taken as a risk, or matter to be an issue.

**Overall risk level:** (Low / Medium / High / Critical)

*NOTE FOR TEACHER* pictures are in the same folder with the report. they have respective names for the matter.

HIGH RISK

500 internal server error during fuzzer
- "-H "Content-Type: application/x-www-form-urlencoded" was a payload, and it caused 500 error. *HAS BEEN FIXED*


**Top 5 immediate actions:**  
1.  no age verification, Add proper validation to fix this. (you can still use date from future.) 🟠
2.  you can create an admin account. 🔴
3.  input validation has been reinforced.
4.  Added google encryption
5.  dos vector and threat has been reinforced.

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-04 | 🟠 Low | no age validation | Accepts any age, like day before. | ![age is invalid](image-3.png) |
| F-05 | 🔴 HIGH | the page lets you make admin account | admin selection | Phase-1/part 2/age validation and administrator account.png |

---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)
[test report](../../2025-11-28-ZAP-Report-.md)
**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).

---

**Instructions (CMD version):**
1. Run OWASP ZAP baseline scan:  
   ```bash
   zap-baseline.py -t https://example.com -r zap_report_round1.html -J zap_report.json
   ```
2. Export results to markdown:  
   ```bash
   zap-cli report -o zap_report_round1.md -f markdown
   ```
3. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---