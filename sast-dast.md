# Project

## SAST 

### Problem Statement

We had no security capability to detect and report on issues found in code or at runtime.

### Solution Statement

To address this vulnerability, I spearheaded the integration of a Static Application Security Testing (SAST) solution into our CI/CD pipeline, specifically within GitHub Actions. This solution was configured to activate on every code push, enhancing our security measures with minimal disruption to developer workflows. Key features of the implemented SAST solution included:

**Automated Scanning**: Automated scans for critical security flaws such as SQL injections, hardcoded secrets, and inadequate error handling, ensuring comprehensive coverage across the codebase.
   
**Integration with GitHub**: The SAST tool was seamlessly integrated with GitHub, where it automatically reviewed each pull request. If issues were detected, the tool commented directly on the PR with detailed findings, enhancing visibility and accountability.
    
**JIRA Integration**: For each issue identified, the system automatically created a JIRA ticket, assigning it to the relevant team for remediation. This integration ensured that security issues were tracked and resolved in line with our project management workflows.
    
**Continuous Feedback**: This setup not only prevented potential security breaches but also served as a continuous feedback mechanism for developers, fostering better security practices throughout the development lifecycle.

### Impact
The integration of the SAST tool significantly enhanced our security posture by embedding automated, real-time security checks into our development pipeline. This proactive approach has substantially reduced the risk of introducing new vulnerabilities into production, thereby safeguarding our application and enhancing trust with our users. The project demonstrated a strong commitment to security and operational excellence, aligning with industry best practices for secure software development.