# Project

## Vulnerability Assessment

### Problem Statement

Previously, our organization lacked visibility into the current vulnerability landscape across our assets. This gap in security insights posed significant risks as potential vulnerabilities in our infrastructure and applications could go undetected and unaddressed.

### Solution Implemented

To address this critical issue, I implemented a two-pronged approach to enhance our vulnerability assessment capabilities:

**Dependency Checking Service Integration**: Deployed a dependency checking service and integrated it directly into our CI/CD pipeline. This service systematically scans our codebase for known vulnerabilities in dependencies upon each commit, ensuring that any newly introduced or existing vulnerabilities are promptly identified.

**AWS Config Activation**: Enabled AWS Config to conduct a thorough configuration and compliance audit across our AWS accounts. This tool provided valuable insights into several security issues, including:
        Detection of inline policies that could circumvent standard security protocols.
        Identification of accounts not enforcing Multi-Factor Authentication (MFA), a critical security best practice.
        Assessment of our IAM roles and policies for non-conformity to our organization's security standards.

### Impact

The deployment of the dependency checking service and the activation of AWS Config significantly improved our security operations by providing:

 **Real-Time Vulnerability Insights**: Continuous visibility into vulnerabilities allowed for immediate remediation actions, significantly reducing the window of exposure to potential security threats.
    Enhanced Security Posture: Addressing configuration and compliance issues across our AWS infrastructure ensured that our security measures are robust and conform to best practices.
    Cost-Effective Solution: This approach provided a low-cost yet highly effective method to safeguard our assets, demonstrating significant ROI in terms of security enhancements relative to the investment.

### Challenges 

**Long List of Issues**:

It appeared this sort of assessment had not been conducted in a long time. So the list of vulnerabilities was very long, with several Critical and High rated issues discovered. The developer teams did not have the capacity to go through the list and determine which of their services is affected and apply mitgation reccomendations.

### Resolutions

**Long List of Issues**:

To make it easier, I went through the Critical and High rated issues, spent the time to gain context on the affect service and determined if an immediate fix was needed or that it was a false positive. This activity significantly reduced the issues that actually needed fixes vs ones that weren't applicable. I outlined the data gathred in documentation to shared with leadership and developers and was able to get agreement to fix certain issues.