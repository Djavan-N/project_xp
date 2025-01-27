# Project

## Zero Trust to Replace VPN

### Problem Statement

Our previous system utilized a VPN for user access to the frontend of an administrative application, with VPN IPs being allow-listed as the primary access control measure. Google was used as the identity provider. The VPN setup frequently resulted in slow and inconsistent connections, causing significant user frustration and delays.

### Solution Implemented

To address these challenges, I spearheaded the development of a more robust and reliable access system based on the principles of Zero Trust architecture. The solution comprised the following key components:

* **Modern Authentication**: Implemented mutual TLS (mTLS) combined with an OAuth2 proxy to ensure a secure and streamlined authentication process. This approach utilized Kubernetes to deploy an ingress controller that terminated mTLS connections and managed the OAuth proxy integration.
    
* **Identity Management**: Continued to leverage Google as the identity provider, ensuring a seamless transition and user experience while enhancing security.
    
* **Certificate Distribution**: Developed a Mobile Device Management (MDM) profile to distribute client certificates required for mTLS, facilitating secure and straightforward device management.
    
* **Authentication Flow**: Configured the system so that upon successful validation of the client certificate (mTLS), users were redirected to Google's authentication page. Following successful identity verification, users gained access to the administrative application.
   
* **Deployment and Scalability**: Utilized Kubernetes for deploying and scaling the ingress and proxy components efficiently, ensuring high availability and resilience.

### Impact

This transition to a Zero Trust model significantly improved the security and reliability of access to critical administrative applications. By eliminating the VPN and implementing a dual-authentication mechanism, the solution not only reduced user frustration due to connectivity issues but also enhanced our overall security posture. This project demonstrates a successful application of modern security practices to improve operational efficiency and user satisfaction.

### Challenges 

* **Timelines**: The initial timeline for this project was set at two months, with no existing documentation on the desired or current design.

### Resolutions

* **Timelines**: Due to the significant impact on users, I prioritized this project at the highest level. I first implemented the solution locally to ensure it was functional before deploying it in our test environment. After confirming the solution's effectiveness in testing, I proceeded with production development. Post-deployment, I dedicated time to creating comprehensive documentation, including managing the certificate chain for mTLS, the distribution of certificates, and visual flow diagrams for peer review.