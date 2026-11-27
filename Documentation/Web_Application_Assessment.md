# Web Application Security Assessment

## 1. Assessment Overview

This document records the security testing activities performed against the OWASP Juice Shop web application.

The assessment uses OWASP ZAP to identify potential security weaknesses and evaluate the application's security configuration.

## 2. Assessment Objectives

- Discover accessible application pages and functionality.
- Perform automated security scanning using OWASP ZAP.
- Identify potential web application vulnerabilities.
- Conduct manual testing of selected security weaknesses.
- Review and document security alerts.

## 3. Testing Scope

The assessment is limited to the locally deployed OWASP Juice Shop application.

Target Application:

`http://127.0.0.1:3000`

## 4. Testing Methodology

The assessment includes the following activities:

1. Verify application availability.
2. Configure OWASP ZAP.
3. Browse the application to discover pages and functionality.
4. Perform passive security scanning.
5. Perform authorized active testing against the lab application.
6. Review and validate security findings.
7. Document evidence and observations.

## 5. Vulnerability Categories

The assessment examines relevant security issues, including:

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Authentication weaknesses
- Access control weaknesses
- Session management issues
- Security misconfigurations

## 6. Initial Passive Scan Results

An initial passive security scan was performed using OWASP ZAP while browsing the OWASP Juice Shop application.

The scan identified **10 alerts** across three severity levels and informational observations.

### 6.1 Alert Summary

| Severity | Number of Alerts |
|---|---:|
| High | 0 |
| Medium | 4 |
| Low | 3 |
| Informational | 3 |
| **Total** | **10** |

### 6.2 Medium Alerts

The initial scan identified the following medium-severity alerts:

- Content Security Policy (CSP) Header Not Set
- Private IP Disclosure
- Missing Clickjacking Protection
- Session ID in URL

### 6.3 Low Alerts

The following low-severity alerts were identified:

- Private IP Disclosure
- Timestamp Disclosure
- X-Content-Type-Options Header Missing

### 6.4 Informational Alerts

The scan also reported these informational observations:

- Suspicious Comments
- Modern Web Application Detected
- Information Disclosure Through Shared Cache

Informational alerts provide observations or testing recommendations and do not necessarily represent confirmed vulnerabilities.

### 6.5 Initial Observations

The initial passive scan identified potential security configuration weaknesses and information disclosure concerns.

The alerts will be reviewed further to understand their evidence, potential impact, and appropriate remediation measures.

The initial scan did not identify any high-severity alerts.

### 6.6 Scan Evidence

Screenshots documenting the initial scan and individual alerts are stored in the repository's `Screenshots` directory.

The findings were reassessed during subsequent authorized active scanning of the local OWASP Juice Shop application.

## 7. Active Scan Results

An authorized active security scan was performed using OWASP ZAP against the locally deployed OWASP Juice Shop application.

The active scan identified **12 alerts** across four severity levels.

### 7.1 Alert Summary

| Severity | Number of Alerts |
|---|---:|
| High | 1 |
| Medium | 4 |
| Low | 3 |
| Informational | 4 |
| **Total** | **12** |

### 7.2 High-Severity Alert

The active scan identified the following high-severity alert:

**Potential SQL Injection**

- Affected endpoint: `/rest/products/search`
- Parameter: `q`
- Severity: High
- Scan type: Active scan

ZAP reported that SQL injection may be possible through the product search parameter.

The application returned a SQLite database syntax error in response to the test input. The error response also exposed the SQL query used by the application.

This behavior suggests potentially unsafe SQL query construction and information disclosure.

However, the syntax error alone does not confirm successful SQL injection or arbitrary database command execution. Further validation would be required.

### 7.3 Medium-Severity Alerts

The active scan identified the following medium-severity alerts:

- Content Security Policy (CSP) Header Not Set
- Cross-Origin Resource Sharing (CORS) Misconfiguration
- Missing Clickjacking Protection
- Session ID in URL

These findings indicate potential security configuration weaknesses and session management concerns.

The CORS alert indicates that arbitrary third-party origins may be permitted to read responses from unauthenticated API endpoints.

### 7.4 Low-Severity Alerts

The following low-severity alerts were identified:

- Private IP Disclosure
- Timestamp Disclosure
- X-Content-Type-Options Header Missing

These findings indicate potential information disclosure and missing HTTP security headers.

### 7.5 Informational Alerts

The active scan also reported the following informational observations:

- Suspicious Comments
- Modern Web Application Detected
- Information Disclosure Through Shared Cache
- Additional informational alert requiring further review

Informational alerts provide observations or testing recommendations and do not necessarily represent confirmed vulnerabilities.

### 7.6 Active Scan Observations

The active scan identified one high-severity potential SQL injection issue that was not reported during the initial passive scan.

The application returned database error details, including the SQL query, suggesting that user-supplied input may be affecting SQL query construction.

The scan also identified a CORS misconfiguration that was not included in the initial passive scan results.

The remaining medium- and low-severity alerts were also observed during the initial passive scan.

All findings require appropriate review before determining their actual exploitability and security impact.

### 7.7 Active Scan Evidence

The active scan findings were reviewed in OWASP ZAP.

The SQL injection alert was documented with supporting screenshot evidence.

Screenshot:

`Screenshots/Vulnerability_Findings/14_sql_injection_alert.png`

## 8. Conclusion

The initial passive scan and subsequent active scan identified several potential security weaknesses in the OWASP Juice Shop application.

The most significant finding was the potential SQL injection issue affecting the product search endpoint, where the application returned database error information.

Additional findings involved CORS configuration, HTTP security headers, session management, and information disclosure.

These results provide a foundation for further vulnerability analysis, risk evaluation, and remediation recommendations.
