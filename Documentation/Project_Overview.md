# Project Overview

## 1. Introduction

This project demonstrates practical web application security testing using OWASP Juice Shop and OWASP ZAP.

The lab provides a controlled environment for assessing an intentionally vulnerable web application, identifying potential security weaknesses, analyzing security findings, and documenting recommended remediation measures.

The assessment includes automated scanning and manual review of selected security alerts to better understand common web application security risks.

## 2. Project Objectives

- Deploy OWASP Juice Shop using Docker.
- Configure OWASP ZAP for web application security testing.
- Perform passive and active security assessments.
- Identify potential web application vulnerabilities and security misconfigurations.
- Analyze security findings and evaluate their potential impact.
- Review vulnerability severity and prioritize remediation.
- Document assessment results and recommended security improvements.

## 3. Assessment Scope

The assessment is limited to the intentionally vulnerable OWASP Juice Shop application deployed within a dedicated Oracle VirtualBox virtual machine.

The application is accessed locally from the Mac host through SSH local port forwarding.

OWASP ZAP is used to assess the local application. Testing does not include unrelated external websites, systems, or networks.

## 4. Assessment Methodology

The project follows a structured web application security testing process:

1. Deploy OWASP Juice Shop in the Ubuntu virtual machine using Docker.
2. Configure local access through SSH port forwarding.
3. Configure OWASP ZAP and the browser for application testing.
4. Perform passive scanning while browsing the application.
5. Perform an active scan against the authorized local application.
6. Review and analyze the security alerts reported by OWASP ZAP.
7. Evaluate potential security impact and severity.
8. Document findings and recommended remediation measures.

## 5. Expected Outcomes

- Successful deployment of OWASP Juice Shop.
- Functional OWASP ZAP testing configuration.
- Completion of passive and active security scans.
- Identification and documentation of potential security weaknesses.
- Analysis of vulnerability severity and potential impact.
- Recommended remediation strategies.
- Screenshots and supporting documentation demonstrating the assessment process.

## 6. Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| OWASP Juice Shop | Intentionally vulnerable web application |
| OWASP ZAP | Web application security testing |
| Docker | Application deployment |
| Ubuntu Linux Server | Lab operating system |
| Oracle VirtualBox | Virtual machine hosting |
| Firefox | Browser-based application testing |
| SSH | Secure remote access and port forwarding |
| GitHub | Project documentation and evidence storage |

## 7. Project Deliverables

The project includes the following documentation and evidence:

- Project overview and lab environment documentation.
- Web application assessment methodology and results.
- Vulnerability analysis.
- Remediation recommendations.
- Final assessment summary.
- Screenshots documenting application deployment, ZAP configuration, and security findings.

## 8. Conclusion

This project demonstrates a practical approach to web application security testing using OWASP Juice Shop and OWASP ZAP.

It provides hands-on experience with application assessment, security alert analysis, risk evaluation, and remediation planning.

The project also demonstrates the importance of validating scanner findings and distinguishing potential vulnerabilities from confirmed security issues.
