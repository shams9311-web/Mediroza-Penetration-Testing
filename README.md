# Mediroza General Hospital — Penetration Testing

![Project](https://img.shields.io/badge/Project-Penetration%20Testing-red)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Web%20Application-blue)
![Environment](https://img.shields.io/badge/Environment-Kali%20Linux-blueviolet)

## 1. Project Overview

This repository documents a practical web application penetration-testing assessment of **Mediroza General Hospital**.

The assessment focused on identifying security weaknesses in the hospital's web application and server infrastructure, evaluating authentication security, examining PDF document encryption, and investigating sensitive information exposure.

The project followed a black-box penetration-testing approach using Kali Linux and industry-standard security tools.

## 2. Target Information

| Item | Details |
|---|---|
| Organization | Mediroza General Hospital |
| Target Domain | `medirozahospital.com` |
| Application | Hospital Web Application |
| Assessment Type | Black-box Penetration Testing |
| Testing Environment | Kali Linux |
| Project Status | Completed |

## 3. Scope and Authorization

The assessment was conducted under the written authorization provided for the project.

The scope included the designated hospital web application, authentication functionality, accessible server resources, and relevant security weaknesses.

**Testing restrictions:**
- No denial-of-service testing.
- No social engineering.
- Confidential information is excluded from public documentation.
- Evidence is redacted to protect personal and organizational information.

## 4. Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration-testing environment |
| Nmap | Network and service discovery |
| Gobuster | Web directory enumeration |
| cURL | HTTP requests and response analysis |
| Burp Suite | Web application traffic analysis |
| SQLMap | SQL injection testing |
| QPDF | PDF encryption analysis |
| John the Ripper | Password recovery |
| Hashcat | Password hash analysis |
| Wireshark | Network traffic analysis |
| ExifTool | Metadata inspection |

## 5. Reconnaissance and Information Gathering

Initial reconnaissance examined the target domain and its publicly accessible web resources.

Activities included:

- DNS resolution and target identification.
- HTTP and HTTPS response analysis.
- Web server identification.
- TLS protocol and certificate assessment.
- Security header inspection.
- Public page and endpoint discovery.
- Examination of legacy web directories.
- Identification of publicly accessible login interfaces.

## 6. Authentication and SQL Injection Assessment

The patient login functionality was examined for weaknesses in input handling and database interaction.

Activities included:

- Login form analysis.
- Input validation testing.
- SQL injection testing.
- Database error analysis.
- Review of authentication behavior.
- Examination of potential unauthorized access risks.

The assessment identified a database-related SQL syntax error during input testing, indicating a potential SQL injection weakness and verbose database error disclosure.

## 7. PDF Encryption and Password Recovery

Three patient report PDF files were examined as part of the document security investigation.

Activities included:

- PDF encryption identification.
- Encryption metadata analysis.
- PDF hash extraction.
- Password recovery attempts.
- Verification of document accessibility.

Tools used included QPDF, John the Ripper, and Hashcat.

Recovered credentials and confidential document contents are intentionally excluded from this public repository.

## 8. Critical Information Exposure

A historical SQL database backup was identified in the website's legacy directory.

**Affected resource:**

`https://medirozahospital.com/old/mediroza_db_backup_2019.sql`

**Identified file:** `mediroza_db_backup_2019.sql`

The investigation concerned exposure of sensitive organizational information, including:

- Employee salary information.
- Employee-related records.
- Hospital shareholder information.
- Ownership-related records.

Public documentation excludes actual employee salaries, personal identifiers, shareholder details, and raw database contents.

## 9. Security Findings and Potential Impact

The assessment investigated the following security areas:

| Area | Security Concern |
|---|---|
| Authentication | Potential SQL injection and authentication weaknesses |
| Database Errors | Disclosure of database error information |
| PDF Documents | Password-protected sensitive documents |
| Legacy Directories | Exposure of historical server resources |
| Database Backup | Potential disclosure of confidential organizational information |
| Security Configuration | Missing or insufficient HTTP security headers |

Potential business impacts include:

- Unauthorized information disclosure.
- Exposure of confidential organizational data.
- Employee and patient privacy risks.
- Financial and reputational damage.
- Increased opportunities for further attacks.

## 10. Recommendations and Remediation

1. Use parameterized SQL queries and prepared statements.
2. Implement proper server-side input validation.
3. Avoid exposing database errors to public users.
4. Enforce strong authentication and authorization controls.
5. Store database backups outside publicly accessible web directories.
6. Remove unnecessary historical files from production servers.
7. Encrypt sensitive backups and restrict access.
8. Apply appropriate HTTP security headers.
9. Review access logs for suspicious requests.
10. Conduct regular vulnerability assessments and security reviews.

## 11. Evidence

Supporting screenshots and technical evidence are organized in the repository's `Evidence/` directory.

Planned evidence categories:

- `Reconnaissance/`
- `SQL-Injection/`
- `PDF-Password-Recovery/`
- `Database-Exposure/`
- `Final-Assessment/`

Screenshots are intended to demonstrate the testing process, observations, and findings.

## 12. Data Protection

This repository is intended for professional cybersecurity documentation and portfolio demonstration.

The following information is not published:

- Actual patient medical records.
- Employee salary values and personal information.
- Confidential shareholder details.
- Raw database backups.
- Recovered passwords and credentials.
- Authentication tokens or session information.

All public evidence must be reviewed and redacted before publication.

## 13. Conclusion

The Mediroza General Hospital penetration-testing assessment examined web application security, authentication mechanisms, PDF document protection, and server-side information exposure.

The investigation identified security concerns involving database input handling, document encryption, legacy resources, and sensitive information exposure.

This repository presents the assessment methodology, technical observations, evidence, security implications, and recommended remediation measures.

---

**Project:** Mediroza General Hospital — Penetration Testing  
**Assessment Type:** Black-box Web Application Security Assessment  
**Environment:** Kali Linux  
**Status:** Completed
