# Project Portfolio

This repository serves as a collection of key projects I have led or contributed to significantly, showcasing my skills and experiences in software development, security, and DevOps practices. Below are detailed descriptions of some standout projects. Click the links to see more details.

## Table of Contents
- [JWT Refactor](jwt.md)
- [Zero Trust to Replace VPN](vpn-zt.md)
- [SAST Integration](sast-dast.md)
- [Vulnerability Assessment](vuln.md)
- [Internal Pentest](pentest.md)

---

## [JWT Refactor](jwt.md)

### Problem Statement
Previously, our application utilized forever-lived JWTs for client authentication to the backend. This approach posed significant security risks.

### Solution
Implemented short-lived access and refresh tokens, developed new API routes for token management, and enhanced token validation mechanisms.

### Impact
Enhanced security by mitigating the risks associated with token compromise and aligning our authentication practices with industry standards.

---

## [Zero Trust to Replace VPN](vpn-zt.md)

### Problem Statement
Users experienced slow and inconsistent connections using a traditional VPN setup for accessing an administrative application.

### Solution
Developed a Zero Trust architecture using mTLS and OAuth2 proxy, deployed via Kubernetes, improving connection reliability and security.

### Impact
Improved user satisfaction and application security, demonstrating successful application of modern security practices.

---

## [SAST Integration](sast-dast.md)

### Problem Statement
Lacked a proactive security mechanism to detect and report issues within the codebase or at runtime.

### Solution
Integrated a SAST solution into the GitHub Actions pipeline to automatically scan every push and manage issues through JIRA.

### Impact
Reduced the risk of vulnerabilities in production, enhancing the security posture of our applications.

---

## [Vulnerability Assessment](vuln.md)

### Problem Statement
Lacked visibilty into current vulnerability landscape for our assets

### Solution
Integrated dependecy checking our libraries and enabled AWS Config to identify vulnerabilities.

### Impact
Identified high risk vulnerabilities present and recommended solutions to mitigate risk

## [Internal Penetration Test](pentest.md)

### Problem Statement
A pentest of our assets had not been conducted in nearly 6 years

### Solution
Conduct a pentest, outline methodology, deliverables and provide recommendations

### Impact
Identified low, medium and high issues from the test and drove development teams to fix higher risk issues within a week.