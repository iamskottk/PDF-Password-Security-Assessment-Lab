# 🔐 PDF Password Security Assessment Lab
**Security Assessment Report · Week 03**

![Cybersecurity](https://img.shields.io/badge/Focus-Cybersecurity-blue)
![John the Ripper](https://img.shields.io/badge/Tool-John%20the%20Ripper-red)
![Johnny GUI](https://img.shields.io/badge/GUI-Johnny-orange)
![Networkwalks](https://img.shields.io/badge/Validation-Networkwalks-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
### Assessment Information

| **Assessment Detail** | **Information** |
|---|---|
| **Prepared By** | ![Kabo Sekoto](https://img.shields.io/badge/KABO%20SEKOTO-Assessment%20Analyst-0078D4?style=flat-square) | |
| **Assessment Type** | Authorised Security Assessment |
| **Assessment Environment** | Controlled Cybersecurity Training Laboratory |
| **Operating Platform** | Windows |
| **Primary Tool** | ![John the Ripper](https://img.shields.io/badge/John%20the%20Ripper-Password%20Recovery-red?style=flat-square) **(Johnny GUI)** |
| **Secondary Tool** | ![Networkwalks](https://img.shields.io/badge/Networkwalks-Secondary%20Validation-blue?style=flat-square) |
| **Assessment Targets** | **3 Password Protected PDF Documents** |
### Assessment Status
![Status](https://img.shields.io/badge/STATUS-COMPLETED-success?style=for-the-badge)

---

## 1. EXECUTIVE SUMMARY

This assessment evaluated the password security of three password protected PDF documents within an authorized cybersecurity training environment.

The assessment simulated an attacker obtaining password hash material from protected documents and attempting offline password recovery.

The assessment consisted of four primary stages:

1. Password hash extraction
2. Offline password recovery using John the Ripper
3. Secondary recovery validation using Networkwalks
4. Authentication validation against the original protected documents

All three target documents were successfully recovered and subsequently opened using the recovered credentials.

### Assessment Results

| Metric              |   Result |
| ------------------- | -------: |
| Documents Assessed  |        3 |
| Hashes Extracted    |      3/3 |
| Passwords Recovered |      3/3 |
| Documents Validated |      3/3 |
| Overall Validation  | **100%** |

> **Key Conclusion:** The tested PDF passwords were recoverable using the techniques applied during this assessment.

---

## 2. ASSESSMENT OBJECTIVE

The objective of this assessment was to evaluate whether the password protection applied to three authorized PDF documents could withstand password recovery techniques after acquisition of the associated password hash material.

The assessment was designed to demonstrate:

* Hash extraction
* Offline password analysis
* Password recovery
* Independent recovery verification
* Authentication testing
* Security evidence collection
* Security reporting

---

## 3. SCOPE

### 3.1 In Scope

| Asset                   | Quantity | Purpose                   |
| ----------------------- | -------: | ------------------------- |
| Password protected PDFs |        3 | Security assessment       |
| PDF hash material       |        3 | Password recovery testing |
| Recovered credentials   |        3 | Authentication validation |

### 3.2 Out of Scope

The following were not targeted:

* Unrelated files
* Personal accounts
* Unauthorized documents
* External organisations
* Third party credentials

---

## 4. ASSESSMENT ENVIRONMENT

| Component        | Configuration                                |
| ---------------- | -------------------------------------------- |
| Operating System | Windows                                      |
| Primary Tool     | John the Ripper                              |
| Interface        | Johnny GUI                                   |
| Secondary Tool   | Networkwalks                                 |
| Target Type      | Password-protected PDF                       |
| Environment      | Authorised Cybersecurity Training Laboratory |

> **Tooling clarification:** *John the Ripper was used through the Johnny graphical interface on Windows. Kali Linux was **not** used for this Week 03 assessment*.

## 5. METHODOLOGY

A controlled workflow was followed to recover and verify access to the protected PDF files:

```text
🔒 Protected PDFs
       │
       ▼
🔑 Hash Extraction
       │
       ▼
🛠️ John the Ripper
   Johnny GUI • Windows
       │
       ▼
🔓 Password Recovery
       │
       ▼
🌐 NetworkWalks
     Validation
       │
       ▼
✅ Password Verification
       │
       ▼
📄 PDF Access Confirmed
```

---

## 6. PHASE 1 — HASH EXTRACTION

### Tool / Activity

**Password-hash extraction**

Password hash material was extracted from each of the three protected PDF documents.

### Evidence

Screenshots demonstrating successful hash extraction are provided in the `evidence/` directory.

### Result

**3/3 target hashes successfully obtained.**

The extracted hash material was subsequently used for password recovery testing.

---

## 7. PHASE 2 — OFFLINE PASSWORD RECOVERY

### Tool

**John the Ripper · Johnny GUI**

The extracted hash material was processed using John the Ripper through the Johnny graphical interface on Windows.

The purpose of this stage was to determine whether the document passwords could be recovered through offline password analysis techniques.

### Evidence

Screenshots demonstrating the password recovery process are provided in the `evidence/` directory.

### Result

**3/3 document passwords successfully recovered.**

> Actual recovered passwords are intentionally excluded from this public repository.

---

## 8. PHASE 3 — SECONDARY RECOVERY VALIDATION

### Tool

**Networkwalks**

A secondary recovery workflow was performed using the Networkwalks training environment.

This provided an additional method of demonstrating recovery of the protected document credentials.

### Evidence

Screenshots demonstrating the secondary recovery workflow are provided in the `evidence/` directory.

### Result

**Secondary recovery workflow completed against all three authorised targets.**

---

## 9. PHASE 4 — AUTHENTICATION VALIDATION

Password recovery alone was not treated as the final validation point.

Each recovered credential was entered into its corresponding protected PDF to confirm that the recovered value provided actual access to the document.

### Evidence

Screenshots demonstrating successful authentication are provided in the `evidence/` directory.

### Result

**3/3 documents successfully authenticated and opened.**

---

# 10. FINDINGS

## Finding F-01 — Recoverable PDF Credentials

| Category        | Details                |
| --------------- | ---------------------- |
| Finding ID      | F-01                   |
| Category        | Credential Security    |
| Affected Assets | PDF 01, PDF 02, PDF 03 |
| Status          | **Confirmed**          |

### Observation

All three tested PDF credentials were successfully recovered using the assessment techniques.

### Evidence

* Hash material was successfully obtained for all three targets.
* John the Ripper successfully recovered credentials for all three targets.
* Secondary recovery testing was completed.
* Recovered credentials successfully opened all three protected PDFs.

### Security Significance

An individual who obtains the necessary password-hash material may be able to conduct offline password recovery attempts without repeatedly interacting with the protected document itself.

The effectiveness of such attacks depends on factors including:

* Password strength
* Password predictability
* Password reuse
* The protection mechanism used by the document

---

# 11. IMPACT

If the same password characteristics were used to protect sensitive business documents, successful password recovery could potentially result in unauthorised disclosure of protected information.

Potential consequences include:

* Unauthorised document access
* Exposure of confidential information
* Credential compromise
* Data disclosure
* Increased risk from password reuse

The actual business impact would depend on the sensitivity of the protected documents and whether the same credentials were reused elsewhere.

---

# 12. SECURITY RECOMMENDATIONS

## 12.1 Password Strength

Use long, unique and unpredictable passwords for protected documents.

## 12.2 Password Reuse

Do not reuse document passwords for:

* Email accounts
* Corporate systems
* Cloud services
* Administrative accounts
* Other sensitive documents

## 12.3 Credential Exposure

Treat exposed password hash material as sensitive information and restrict access accordingly.

## 12.4 Encryption

Where sensitive information is involved, use appropriate document encryption and strong cryptographic protection rather than relying solely on a weak password.

## 12.5 Credential Rotation

If a protected document password is suspected to have been exposed or recovered by an unauthorised party:

1. Replace the password.
2. Review related systems for password reuse.
3. Assess whether other documents or accounts may use the same credential.

---

# 13. ASSESSMENT RESULTS

| Target    | Hash Extraction | John Recovery | Networkwalks | Authentication |
| --------- | :-------------: | :-----------: | :----------: | :------------: |
| PDF 01    |        ✅        |       ✅       |       ✅      |        ✅       |
| PDF 02    |        ✅        |       ✅       |       ✅      |        ✅       |
| PDF 03    |        ✅        |       ✅       |       ✅      |        ✅       |
| **Total** |     **3/3**     |    **3/3**    |    **3/3**   |     **3/3**    |

### Overall Assessment

**3/3 targets successfully recovered and authenticated.**

---

# 14. EVIDENCE MANAGEMENT

### 01 — PDF 1 Hash Extraction

![PDF 1 Hash Extraction](01-hash-pdf1.png)

### 02 — PDF 2 Hash Extraction

![PDF 2 Hash Extraction](02-hash-pdf2.png)

### 03 — PDF 3 Hash Extraction

![PDF 3 Hash Extraction](03-hash-pdf3.png)

### 04 — PDF 1 Password Recovery

![PDF 1 Password Recovery](04-johnny-pdf1.png)

### 05 — PDF 2 Password Recovery

![PDF 2 Password Recovery](05-johnny-pdf2.png)

### 06 — PDF 3 Password Recovery

![PDF 3 Password Recovery](06-johnny-pdf3.png)

### 07 — PDF 1 Networkwalks Validation

![PDF 1 Networkwalks Validation](07-networkwalks-pdf1.png)

### 08 — PDF 2 Networkwalks Validation

![PDF 2 Networkwalks Validation](08-networkwalks-pdf2.png)

### 09 — PDF 3 Networkwalks Validation

![PDF 3 Networkwalks Validation](09-networkwalks-pdf3.png)

---

# 15. TOOLS & SKILLS

## Tools

* **John the Ripper**
* **Johnny GUI**
* **Networkwalks**

## 🛡️ Skills Demonstrated

| 🔐 **Security & Technical Skills** | 📋 **Assessment & Documentation** |
|---|---|
| 🔑 Password Hash Extraction | 📊 Security Evidence Collection |
| 🔓 Offline Password Recovery | 🛡️ Defensive Security Analysis |
| ✅ Credential Validation | 📝 Security Documentation |
| 📄 PDF Security Assessment | 📑 Security Reporting |

---

# 16. LIMITATIONS

This assessment was conducted against three designated training documents and should not be interpreted as a comprehensive assessment of PDF security mechanisms in general.

The results represent the behaviour of the specific documents and credentials tested within the authorised laboratory environment.

The assessment does not establish that all PDF documents using similar protection mechanisms would produce the same results.

---

# 17. AUTHORISATION & ETHICAL USE

All testing was performed against designated laboratory files within an authorised cybersecurity training environment.

No unauthorised systems, accounts, documents, or credentials were targeted.

Recovered passwords are intentionally excluded from this public repository.

---

# 18. CONCLUSION

The assessment successfully demonstrated the complete attack-and-validation lifecycle against three authorised password-protected PDF documents.

The testing progressed through:

**Hash Acquisition → Password Recovery → Secondary Validation → Authentication**

All three authorized targets were successfully recovered and subsequently validated by opening the corresponding protected documents.

### Final Result

> **3/3 targets successfully recovered and validated.**

---

## Analyst

### Kabo Sekoto
**🔐 Junior Cybersecurity Practitioner**

> `Learning → Cracking → Testing → Securing`

This Week 03 assessment documents practical password recovery and security testing using **John the Ripper through the Johnny graphical interface on Windows** and **NetworkWalks tools** used as part of the workflow. The project demonstrates hands on analysis, password recovery, verification and successful access to protected PDF files.

<p align="center">
  <a href="https://linkedin.com/in/kabosekoto">
    <img src="https://img.shields.io/badge/🔵_LinkedIn-Professional%20Profile-0A66C2?style=for-the-badge" />
  </a>
  &nbsp;
  <a href="https://www.youtube.com/@IamSkottK">
    <img src="https://img.shields.io/badge/🔴_YouTube-Cybersecurity%20Lab-FF0000?style=for-the-badge" />
  </a>
</p>


---
