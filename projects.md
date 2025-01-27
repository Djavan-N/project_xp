# Projects

## JWT Refactor

### Problem Statement

Previously, our application utilized forever-lived JWTs for client authentication to the backend. This approach posed significant security risks, primarily due to the potential for token compromise, which could allow unauthorized access for an indefinite period.

### Solution Implemented

To enhance security and comply with best practices, I led the initiative to refactor the authentication system. The key components of this refactor included:

**Token Management**: Introduced a dual-token approach, issuing short-lived access tokens and longer-lived refresh tokens. This method limits the lifespan of any compromised token, significantly reducing potential damage.

**Route Development**: Developed new API routes to enable clients to request new tokens and to invalidate existing tokens for reasons such as expiration or administrative actions.

**Database Integration**: Implemented a new database table dedicated to storing token metadata. This table allows for efficient validation checks, including token expiration and invalidation status.

**Security Enhancements**: Established comprehensive token validation mechanisms to ensure all tokens are checked for expiration and verified against the new database for any invalidation flags.

**Backward Compatibility**: Implemented logic to distinguish between legacy and new tokens, allowing the system to support both during a transitional phase. This approach ensured that existing users experienced no disruption in service while we phased out the legacy tokens.

**Testing and Quality Assurance**: Created a suite of automated tests to verify the functionality of token generation, validation, and management processes, ensuring robust security and functionality.

### Impact

This project significantly bolstered the security of our application by mitigating the risks associated with token compromise. The new system not only enhances user trust but also aligns our authentication practices with industry standards.

## Zero Trust to Replace VPN

### Problem Statement

Our existing setup used a VPN for user access to the frontend of an administrative application, with VPN IPs being allow-listed as the primary access control measure. Authentication was managed through Google as the identity provider. Users frequently experienced slow and inconsistent VPN connections, leading to significant frustration and delays.
Solution Implemented

To address these challenges, I spearheaded the development of a more robust and reliable access system based on the principles of Zero Trust architecture. The solution comprised the following key components:

**Modern Authentication**: Implemented mutual TLS (mTLS) combined with an OAuth2 proxy to ensure a secure and streamlined authentication process. This approach utilized Kubernetes to deploy an ingress controller that terminated mTLS connections and managed the OAuth proxy integration.
    
**Identity Management**: Continued to leverage Google as the identity provider, ensuring a seamless transition and user experience while enhancing security.
    
**Certificate Distribution**: Developed a Mobile Device Management (MDM) profile to distribute client certificates required for mTLS, facilitating secure and straightforward device management.
    
**Authentication Flow**: Configured the system so that upon successful validation of the client certificate (mTLS), users were redirected to Google's authentication page. Following successful identity verification, users gained access to the administrative application.
   
**Deployment and Scalability**: Utilized Kubernetes for deploying and scaling the ingress and proxy components efficiently, ensuring high availability and resilience.

### Impact

This transition to a Zero Trust model significantly improved the security and reliability of access to critical administrative applications. By eliminating the VPN and implementing a dual-authentication mechanism, the solution not only reduced user frustration due to connectivity issues but also enhanced our overall security posture. This project demonstrates a successful application of modern security practices to improve operational efficiency and user satisfaction.