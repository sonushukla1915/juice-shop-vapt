# OWASP Juice Shop – Web Application VAPT

## Project Overview

This project demonstrates a Web Application Vulnerability Assessment and Penetration Testing (VAPT) exercise performed on the OWASP Juice Shop intentionally vulnerable web application.

The objective was to identify, validate, document, and recommend remediation for common web application security vulnerabilities in a controlled local lab environment.

## Scope

- Target: OWASP Juice Shop
- Environment: Localhost
- Target URL: http://localhost:3000
- Testing Type: Web Application VAPT
- Tools Used: Burp Suite, Burp Browser, Docker, OWASP Juice Shop

## Vulnerabilities Identified

| ID | Vulnerability | Severity |
|---|---|---|
| F-01 | SQL Injection – Authentication Bypass | Critical |
| F-02 | DOM-Based Cross-Site Scripting (XSS) | Medium |
| F-03 | Broken Object Level Authorization (BOLA/IDOR) | Medium |
| F-04 | Sensitive Data Exposure | Medium |
| F-05 | Weak Authentication Controls | Medium |
| F-06 | Improper Error Handling & Missing Security Headers | Low/Medium |

## Methodology

The assessment followed a practical VAPT workflow:

1. Reconnaissance
2. Application Mapping
3. Vulnerability Identification
4. Manual Validation
5. Evidence Collection
6. Risk Assessment
7. Remediation Recommendations
8. Documentation

## Key Findings

### SQL Injection

A SQL injection vulnerability was identified in the login functionality.

The vulnerability allowed authentication bypass using a crafted SQL input in the login request.

### DOM-Based XSS

A DOM-based Cross-Site Scripting vulnerability was validated through the application's search functionality.

### BOLA / IDOR

Authorization testing showed that changing a basket object ID could expose another user's basket data without changing the authenticated session.

### Sensitive Data Exposure

Sensitive internal information was accessible through the application's `/ftp` endpoint.

### Weak Authentication Controls

Repeated failed login attempts did not trigger an effective account lockout or CAPTCHA mechanism in the tested lab environment.

### Improper Error Handling

An invalid API endpoint returned a detailed server-side error containing internal implementation information.

The response also lacked important security headers such as Content-Security-Policy and Strict-Transport-Security.

## Remediation

Recommended security improvements include:

- Use parameterized queries and prepared statements.
- Implement proper output encoding and input validation.
- Enforce server-side authorization checks for every object.
- Remove sensitive files from publicly accessible directories.
- Implement rate limiting and account lockout controls.
- Disable detailed production error messages.
- Configure appropriate security headers.
- Apply secure authentication and session management practices.

## Skills Demonstrated

- Web Application Security
- Vulnerability Assessment
- Penetration Testing
- OWASP Top 10
- Burp Suite
- HTTP Request/Response Analysis
- SQL Injection Testing
- XSS Testing
- IDOR/BOLA Testing
- Authentication Testing
- Security Documentation
- Risk Assessment
- Remediation Planning

## Disclaimer

This project was conducted only against the intentionally vulnerable OWASP Juice Shop application running in a controlled local laboratory environment.

No unauthorized systems were tested.

## Author

**Sonu Shukla**

BCA – Cyber Security

GitHub: https://github.com/sonushukla1915
