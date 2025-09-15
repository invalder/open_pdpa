# PDPA vs GDPR Requirements Mapping

## Document Information

- **Document Type**: Regulatory Requirements Mapping
- **Version**: 1.0.0
- **Status**: Draft
- **Last Updated**: 2025-09-15
- **Owner**: Legal Team
- **Reviewers**: Compliance Team, Product Team

## Table of Contents

1. [Mapping Overview](#mapping-overview)
2. [Data Subject Rights Mapping](#data-subject-rights-mapping)
3. [Controller Obligations Mapping](#controller-obligations-mapping)
4. [Processor Requirements Mapping](#processor-requirements-mapping)
5. [Special Situations Mapping](#special-situations-mapping)
6. [Implementation Priority Matrix](#implementation-priority-matrix)

## Mapping Overview

### Purpose
This document provides a detailed side-by-side comparison of Thai PDPA and GDPR requirements, highlighting similarities, differences, and implementation implications for the Open PDPA Platform.

### Key Differences Summary

| Aspect | Thai PDPA | GDPR | Implementation Impact |
|--------|-----------|------|----------------------|
| **Territorial Scope** | Thailand-based controllers/processors | EU residents' data globally | Multi-jurisdiction compliance required |
| **Penalties** | Up to 5M THB or 1% revenue | Up to €20M or 4% revenue | Higher penalty risk under GDPR |
| **Consent Age** | Under 10 years old | Under 16 years old | Different consent validation rules |
| **Breach Notification** | 72 hours to PDPC | 72 hours to DPA | Similar timeline, different authorities |
| **DPO Requirements** | Government/public/large scale | Public/large scale/systematic monitoring | Different trigger criteria |
| **Cross-border Transfer** | Whitelist approach | Adequacy decisions + safeguards | Different transfer mechanisms |

## Data Subject Rights Mapping

### Right of Access

| PDPA Section 30 | GDPR Article 15 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Data subject can request access to personal data | Data subject has right to obtain confirmation and access | Both require access to personal data and processing information | GDPR requires more detailed information (retention periods, automated decision-making) | Extended information package for GDPR compliance |
| **Timeframe**: 30 days | **Timeframe**: 1 month (extendable to 3 months) | Similar timeframes | GDPR allows 2-month extension in complex cases | Configurable response timeframes by jurisdiction |
| **Format**: Not specified | **Format**: Electronic format preferred | Both allow various formats | GDPR specifies electronic format preference | Multiple format support with jurisdiction-specific defaults |
| **Fee**: May charge reasonable fee | **Fee**: Free for first request | GDPR generally free | PDPA allows fees more broadly | Different fee structures by jurisdiction |

**Platform Features**:
- Automated data discovery and compilation
- Jurisdiction-specific information packages
- Configurable response timeframes
- Multiple export formats (PDF, JSON, XML, CSV)
- Fee calculation and payment processing

### Right to Rectification

| PDPA Section 31 | GDPR Article 16 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Right to correct inaccurate or incomplete data | Right to rectification of inaccurate data | Both allow correction of inaccurate data | GDPR explicitly includes completion of incomplete data | Unified rectification workflow covering both scenarios |
| Must notify third parties | Must inform recipients | Both require third-party notification | GDPR exempts notification if impossible or disproportionate | Configurable notification rules with effort assessment |
| **Timeframe**: Without delay | **Timeframe**: Without undue delay | Similar urgency requirements | GDPR emphasizes "undue delay" | Immediate processing with configurable SLA monitoring |

**Platform Features**:
- Data validation and verification workflows
- Automated third-party notification system
- Change tracking and audit trails
- Bulk rectification capabilities
- Exception handling for notification requirements

### Right to Erasure (Right to be Forgotten)

| PDPA Section 32 | GDPR Article 17 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Right to request deletion | Right to erasure "right to be forgotten" | Both provide deletion rights | GDPR has more specific grounds and exceptions | Comprehensive grounds assessment engine |
| **Grounds**: Unlawful processing, withdrawn consent | **Grounds**: 6 specific grounds including public interest | Similar core grounds | GDPR includes public erasure and media coverage scenarios | Extended grounds evaluation with jurisdiction-specific rules |
| **Exceptions**: Legal obligations, public interest | **Exceptions**: Freedom of expression, public health, archiving | Similar exception categories | GDPR more detailed about balancing tests | Automated exception assessment with legal balancing |
| Must inform third parties if data made public | Must take reasonable steps including technical measures | Both require third-party action | GDPR emphasizes technical measures for public data | Advanced third-party notification with technical integration |

**Platform Features**:
- Comprehensive data discovery across all systems
- Grounds and exceptions assessment engine
- Secure deletion with cryptographic verification
- Public data erasure coordination
- Legal hold and exception management

### Right to Data Portability

| PDPA Section 33 | GDPR Article 20 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Right to receive data in structured format | Right to receive and transmit data | Both provide data portability | GDPR includes direct transmission right | Enhanced transmission capabilities for GDPR |
| **Scope**: Data provided by data subject | **Scope**: Data provided by data subject | Same scope limitation | No significant differences | Unified data identification and extraction |
| **Format**: Structured, commonly used | **Format**: Structured, commonly used, machine-readable | Similar format requirements | GDPR emphasizes machine-readability | Machine-readable formats with human-readable options |
| **Limitation**: No adverse effect on others | **Limitation**: Shall not adversely affect rights of others | Same limitation principle | No significant differences | Rights impact assessment before processing |

**Platform Features**:
- Structured data export in multiple formats
- Direct transmission to third-party services
- Rights impact assessment algorithms
- Data validation and integrity verification
- Secure transfer protocols and encryption

### Right to Object

| PDPA Section 34 | GDPR Article 21 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Right to object to processing | Right to object to processing | Both provide objection rights | GDPR has more detailed provisions for different scenarios | Scenario-specific objection handling |
| **Grounds**: Legitimate interests processing | **Grounds**: Legitimate interests, direct marketing, automated decision-making | Similar for legitimate interests | GDPR includes specific marketing and automated decision provisions | Extended objection categories and processing rules |
| Must cease unless compelling legitimate grounds | Must cease unless compelling legitimate grounds | Same balancing test | GDPR provides more guidance on balancing | Automated balancing assessment with legal framework |
| **Marketing**: Must always cease | **Marketing**: Must always cease | Same for direct marketing | No significant differences | Immediate marketing cessation mechanisms |

**Platform Features**:
- Objection reason collection and analysis
- Compelling legitimate grounds assessment
- Automated processing cessation
- Marketing preference management
- Balancing test documentation and audit trails

### Additional GDPR Rights

#### Right to Restriction of Processing (GDPR Article 18)
**Note**: No direct PDPA equivalent

**Platform Implementation**:
- Processing restriction mechanisms
- Restricted data marking and isolation
- Limited processing capability (storage, consent, legal claims)
- Automatic restriction lifting notifications
- Integration with other rights (pending rectification, objection)

#### Protection from Automated Decision-Making (GDPR Article 22)
**Note**: Limited PDPA coverage

**Platform Implementation**:
- Automated decision detection and flagging
- Human intervention workflow triggers
- Right to explanation mechanisms
- Opt-out capabilities for automated processing
- Decision logic transparency tools

## Controller Obligations Mapping

### Legal Basis for Processing

| PDPA Section 6 | GDPR Article 6 | Similarities | Differences | Platform Implementation |
|----------------|----------------|--------------|-------------|------------------------|
| **Legal Bases**: Consent, contract, legal obligation, vital interests, public task, legitimate interests | **Legal Bases**: Same 6 legal bases | Identical legal basis framework | Terminology and interpretation may vary | Unified legal basis management with jurisdiction-specific guidance |
| Must demonstrate lawful basis | Must demonstrate lawful basis | Same demonstration requirement | GDPR emphasizes documentation and accountability | Enhanced documentation and evidence collection |
| **Consent Requirements**: Freely given, specific, informed, clear | **Consent Requirements**: Freely given, specific, informed, unambiguous | Very similar consent standards | GDPR adds "unambiguous" requirement | Consent collection with enhanced clarity validation |

**Platform Features**:
- Legal basis selector with jurisdiction-specific guidance
- Automated legal basis validation and documentation
- Consent quality assessment and optimization
- Legal basis change tracking and impact analysis
- Accountability evidence generation

### Records of Processing Activities

| PDPA Section 23 | GDPR Article 30 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Must maintain processing records | Must maintain processing records | Both require processing activity records | GDPR more specific about record contents | GDPR-compliant record structure with PDPA compatibility |
| **Controller Records**: Categories, purposes, recipients, retention | **Controller Records**: More detailed requirements including legal basis, storage periods | Similar core elements | GDPR requires more comprehensive information | Extended record template covering all GDPR requirements |
| **Processor Records**: Categories, processing activities, transfers | **Processor Records**: Similar but more detailed | Similar processor obligations | GDPR more specific about processor record requirements | Comprehensive processor record management |
| **Exemption**: Organizations with <200 employees | **Exemption**: Organizations with <250 employees | Similar small organization exemptions | Different employee thresholds | Configurable exemption rules based on jurisdiction |

**Platform Features**:
- Automated record generation and maintenance
- Jurisdiction-specific record templates
- Comprehensive data flow documentation
- Legal basis and retention period tracking
- Regular record review and update workflows

### Security of Processing

| PDPA Section 24 | GDPR Article 32 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| Implement appropriate security measures | Implement appropriate technical and organizational measures | Both require appropriate security measures | GDPR more specific about risk-based approach | Risk-based security control implementation |
| **Measures**: Administrative, technical, physical | **Measures**: Pseudonymization, encryption, confidentiality, integrity, availability, resilience | Similar categories | GDPR more specific about technical measures | GDPR technical measures with PDPA administrative controls |
| Consider state of art, costs, risks | Consider state of art, costs, nature, scope, context, risks | Similar risk-based approach | GDPR more detailed risk assessment criteria | Comprehensive risk assessment framework |
| Regular review and updates | Regular testing, assessing, evaluating | Both require ongoing assessment | GDPR emphasizes continuous evaluation | Continuous security monitoring and assessment |

**Platform Features**:
- Risk-based security control selection
- Automated security assessment and monitoring
- Security measure effectiveness tracking
- Regular security review workflows
- Compliance evidence generation

### Data Breach Notification

| PDPA Section 25 | GDPR Articles 33-34 | Similarities | Differences | Platform Implementation |
|-----------------|---------------------|--------------|-------------|------------------------|
| **Authority Notification**: 72 hours to PDPC | **Authority Notification**: 72 hours to supervisory authority | Same timeframe | Different authorities | Multi-authority notification system |
| **High Risk**: Notify data subjects | **High Risk**: Notify data subjects "without undue delay" | Both require data subject notification for high risk | GDPR more specific about timing | Automated risk assessment and notification |
| **Content**: Nature, categories, consequences, measures | **Content**: More detailed requirements | Similar core content | GDPR requires more specific information | GDPR-compliant notification templates |
| **Risk Assessment**: Likelihood and severity | **Risk Assessment**: Similar approach | Same risk-based approach | GDPR more detailed about risk factors | Comprehensive risk assessment algorithms |

**Platform Features**:
- Automated breach detection and classification
- 72-hour notification countdown timers
- Multi-authority notification workflows
- Risk assessment algorithms
- Template-based notification generation
- Data subject notification automation

### Privacy Impact Assessment

| PDPA Section 26 | GDPR Article 35 | Similarities | Differences | Platform Implementation |
|-----------------|-----------------|--------------|-------------|------------------------|
| **Triggers**: High risk to rights and freedoms | **Triggers**: High risk to rights and freedoms | Same risk-based trigger | GDPR more specific trigger criteria | GDPR trigger assessment with PDPA compatibility |
| **Required Elements**: Not specified | **Required Elements**: Systematic description, necessity assessment, risk assessment, mitigation measures | PDPA less prescriptive | GDPR very specific about PIA content | GDPR-compliant PIA template with PDPA elements |
| **Consultation**: With DPO if appointed | **Consultation**: With DPO, data subjects (where appropriate) | Both require DPO consultation | GDPR includes data subject consultation | Extended consultation workflow |
| **Authority Consultation**: If high residual risk | **Authority Consultation**: If high residual risk after mitigation | Same escalation requirement | Similar authority consultation triggers | Automated authority consultation triggers |

**Platform Features**:
- DPIA trigger assessment algorithms
- Guided DPIA creation workflows
- Risk assessment and mitigation planning
- Stakeholder consultation management
- Authority consultation workflows
- DPIA review and approval processes

## Processor Requirements Mapping

### Data Processing Agreements

| PDPA Requirements | GDPR Article 28 | Similarities | Differences | Platform Implementation |
|------------------|-----------------|--------------|-------------|------------------------|
| Written agreement required | Written contract required | Both require written agreements | GDPR more specific about contract terms | GDPR-compliant contract templates |
| **Required Terms**: Processing instructions, security measures, breach notification | **Required Terms**: More detailed list including sub-processor approval, data location, audit rights | Similar core terms | GDPR much more comprehensive | Extended contract term management |
| **Sub-processors**: Controller authorization required | **Sub-processors**: Written authorization, same obligations | Similar sub-processor controls | GDPR more specific about sub-processor obligations | Sub-processor management workflows |
| **Audit Rights**: Controller must have audit rights | **Audit Rights**: Controller audit rights specified | Same audit right requirement | GDPR more detailed about audit scope | Comprehensive audit management system |

**Platform Features**:
- Contract template library with jurisdiction-specific terms
- Sub-processor approval and management workflows
- Audit scheduling and tracking system
- Contract compliance monitoring
- Automated contract review and renewal

### Data Transfer Requirements

| PDPA Sections 39-42 | GDPR Chapter V | Similarities | Differences | Platform Implementation |
|---------------------|----------------|--------------|-------------|------------------------|
| **Adequacy**: Whitelist of adequate countries | **Adequacy**: Commission adequacy decisions | Both use adequacy determinations | Different decision-making authorities | Multi-authority adequacy tracking |
| **Safeguards**: Standard contracts, binding rules, certification | **Safeguards**: Similar mechanisms plus additional options | Similar safeguard types | GDPR more safeguard options | Comprehensive safeguard management |
| **Transfer Impact Assessment**: Required for non-adequate countries | **Transfer Impact Assessment**: Required post-Schrems II | Similar assessment requirements | Different legal evolution and emphasis | Schrems II compliant transfer impact assessments |
| **Monitoring**: Ongoing transfer monitoring | **Monitoring**: Ongoing assessment of transfer conditions | Both require continuous monitoring | Different monitoring emphasis | Continuous transfer monitoring and alerting |

**Platform Features**:
- Real-time adequacy decision tracking
- Transfer impact assessment automation
- Safeguard mechanism management
- Cross-border transfer monitoring
- Transfer documentation and evidence collection

## Special Situations Mapping

### Children's Data Processing

| PDPA Approach | GDPR Approach | Similarities | Differences | Platform Implementation |
|---------------|---------------|--------------|-------------|------------------------|
| **Age Threshold**: Under 10 years | **Age Threshold**: Under 16 years (member state flexibility 13-16) | Both have age-based protections | Different age thresholds | Configurable age validation by jurisdiction |
| **Parental Consent**: Required for under 10 | **Parental Consent**: Required for under consent age | Both require parental consent | Different age triggers | Age-based consent collection workflows |
| **Verification**: Reasonable efforts to verify | **Verification**: Reasonable efforts considering available technology | Similar verification standards | GDPR more technology-focused | Technology-appropriate verification methods |

**Platform Features**:
- Age verification and validation systems
- Parental consent collection and management
- Age-appropriate interface design
- Jurisdiction-specific age threshold configuration
- Parental control and monitoring capabilities

### Sensitive Data Processing

| PDPA Approach | GDPR Article 9 | Similarities | Differences | Platform Implementation |
|---------------|---------------|--------------|-------------|------------------------|
| **Categories**: Race, political opinions, religion, health, sexual orientation, criminal records, biometrics, genetics | **Categories**: Similar categories plus trade union membership, philosophical beliefs | Largely overlapping categories | GDPR includes trade unions and philosophical beliefs | Comprehensive sensitive data classification |
| **Processing Conditions**: Explicit consent or other specific lawful grounds | **Processing Conditions**: Explicit consent plus 9 other specific conditions | Similar explicit consent requirement | GDPR more specific alternative conditions | Extended processing condition management |
| **Enhanced Protection**: Additional security measures | **Enhanced Protection**: Higher standard of protection | Both require enhanced protection | Similar protection standards | Enhanced security controls for sensitive data |

**Platform Features**:
- Automated sensitive data classification
- Enhanced consent collection for sensitive data
- Elevated security controls and access restrictions
- Specific lawful basis validation
- Enhanced audit and monitoring capabilities

## Implementation Priority Matrix

### Priority 1: Core Rights (Must Have - Launch Requirement)

| Feature | PDPA Requirement | GDPR Requirement | Implementation Status | Target Date |
|---------|-----------------|------------------|----------------------|-------------|
| **Data Access** | Section 30 | Article 15 | In Development | Q4 2025 |
| **Data Rectification** | Section 31 | Article 16 | In Development | Q4 2025 |
| **Data Erasure** | Section 32 | Article 17 | In Development | Q4 2025 |
| **Data Portability** | Section 33 | Article 20 | In Development | Q4 2025 |
| **Processing Objection** | Section 34 | Article 21 | In Development | Q4 2025 |
| **Consent Management** | Section 7 | Article 6(1)(a) | In Development | Q4 2025 |
| **Breach Notification** | Section 25 | Articles 33-34 | In Development | Q4 2025 |

### Priority 2: Controller Obligations (Should Have - Post-Launch)

| Feature | PDPA Requirement | GDPR Requirement | Implementation Status | Target Date |
|---------|-----------------|------------------|----------------------|-------------|
| **Processing Records** | Section 23 | Article 30 | Planned | Q1 2026 |
| **Security Measures** | Section 24 | Article 32 | Planned | Q1 2026 |
| **Privacy Impact Assessment** | Section 26 | Article 35 | Planned | Q1 2026 |
| **DPO Management** | Section 27 | Article 37 | Planned | Q2 2026 |
| **Processor Agreements** | Various | Article 28 | Planned | Q2 2026 |

### Priority 3: Advanced Features (Could Have - Future Releases)

| Feature | PDPA Requirement | GDPR Requirement | Implementation Status | Target Date |
|---------|-----------------|------------------|----------------------|-------------|
| **Processing Restriction** | Limited | Article 18 | Planned | Q2 2026 |
| **Automated Decision Protection** | Limited | Article 22 | Planned | Q3 2026 |
| **Transfer Impact Assessment** | Sections 39-42 | Chapter V | Planned | Q3 2026 |
| **Children's Data Protection** | Various | Various | Planned | Q4 2026 |
| **Advanced Analytics** | N/A | N/A | Planned | Q4 2026 |

### Implementation Approach

#### Phase 1: Foundation (Q4 2025)
- Implement core data subject rights with unified PDPA/GDPR compliance
- Basic consent management with jurisdiction-specific requirements
- Essential breach notification capabilities
- Multi-tenant architecture with jurisdiction configuration

#### Phase 2: Enhancement (Q1-Q2 2026)
- Advanced controller obligation features
- Comprehensive processor management
- Enhanced security and audit capabilities
- Extended integration and automation features

#### Phase 3: Innovation (Q3-Q4 2026)
- AI-powered compliance assistance
- Predictive risk assessment
- Advanced analytics and reporting
- Ecosystem integration and marketplace

### Compliance Validation Strategy

#### Continuous Compliance Monitoring
- Real-time requirement coverage assessment
- Automated compliance gap detection
- Regulatory change impact analysis
- Compliance score calculation and reporting

#### Regular Compliance Reviews
- Monthly requirement coverage review
- Quarterly compliance assessment
- Annual comprehensive compliance audit
- Ongoing regulatory tracking and updates

#### Stakeholder Validation
- Legal team requirement validation
- Customer compliance feedback
- Regulatory authority engagement
- Industry peer benchmarking

---

## Change Log

### Version 1.0.0 - 2025-09-15
- **Added**: Comprehensive PDPA vs GDPR requirements mapping
- **Added**: Detailed side-by-side comparison of data subject rights
- **Added**: Complete controller and processor obligations mapping
- **Added**: Special situations analysis for children's data and sensitive data
- **Added**: Implementation priority matrix with development timeline
- **Added**: Platform feature specifications for each requirement
- **Type**: Regulatory Mapping Document
- **Author**: Legal Team
- **Rationale**: Provide detailed regulatory requirement comparison to ensure comprehensive compliance coverage in Open PDPA Platform development
