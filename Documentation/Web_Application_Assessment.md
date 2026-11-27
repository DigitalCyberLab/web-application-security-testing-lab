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

The assessment will include the following activities:

1. Verify application availability.
2. Configure OWASP ZAP.
3. Browse the application to discover pages and functionality.
4. Perform passive security scanning.
5. Perform authorized active testing against the lab application.
6. Review and validate security findings.
7. Document evidence and observations.

## 5. Vulnerability Categories

The assessment will examine relevant security issues, including:

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

The findings will be reassessed during subsequent testing, including authorized active scanning of the local OWASP Juice Shop application.
