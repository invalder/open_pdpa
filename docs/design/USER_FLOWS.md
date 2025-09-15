# Example User Flows - Open PDPA Platform

## Data Subject Request (DSAR) Flow
1. Data subject accesses the self-service portal
2. Selects request type (access, deletion, etc.)
3. Completes identity verification
4. Submits request
5. System auto-assigns to Privacy Administrator
6. Automated data discovery and compilation
7. Legal review (if required)
8. Response generated and delivered to data subject
9. Request status and audit trail updated

## Consent Collection Flow
1. User visits website or app
2. Cookie consent banner displayed (locale auto-detected)
3. User selects preferences (accept all, granular, reject)
4. Consent recorded via high-TPS API
5. Consent status available for downstream systems
6. User can update or withdraw consent at any time

## Breach Notification Flow
1. Security system detects anomaly
2. Automated breach classification and risk assessment
3. Privacy Administrator notified
4. Regulatory authority notification triggered (if required)
5. Data subject notification workflow started (if high risk)
6. Remediation and investigation tasks assigned
7. Incident closed and lessons learned documented

## Super Admin Tenant Onboarding Flow
1. Super Admin creates new tenant via admin portal
2. Tenant configuration and resource allocation
3. Tenant receives onboarding instructions
4. Tenant admin sets up users and integrations
5. Platform health and usage monitoring enabled
6. Ongoing support and compliance monitoring

---

*See design wireframes and UI mockups in the design/ directory for visual references.*
