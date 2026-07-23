
# FIPS 199 System Categorization Worksheet

## Orion Government Solutions

### Orion Citizen Services Portal

---

## 1. Document Control

| Field                                      | Details                                  |
| ------------------------------------------ | ---------------------------------------- |
| Organization                               | Orion Government Solutions               |
| System Name                                | Orion Citizen Services Portal            |
| Document Type                              | FIPS 199 System Categorization Worksheet |
| RMF Phase                                  | Categorize                               |
| Version                                    | 1.0                                      |
| Status                                     | Draft                                    |
| Prepared By                                | Junior GRC Analyst                       |
| System Owner                               | To Be Assigned                           |
| Information System Security Officer (ISSO) | To Be Assigned                           |
| Authorizing Official (AO)                  | To Be Assigned                           |
| Date Prepared                              | YYYY-MM-DD                               |
| Next Review Date                           | YYYY-MM-DD                               |

---

# 2. Organization and Business Context

## 2.1 Organization Profile

Orion Government Solutions is a regulated organization with approximately **1200 employees** operating a hybrid technology environment.

The organization's technology environment includes:

* Azure Government cloud infrastructure
* Microsoft 365
* On-premises infrastructure
* Remote workforce capabilities
* Third-party service providers
* Customer and citizen information
* Regulated business processes

The organization relies on interconnected systems to provide citizen-facing services and manage sensitive operational and customer information.

---

## 2.2 System Being Categorized

### System Name

**Orion Citizen Services Portal**

### System Description

The Orion Citizen Services Portal is a citizen-facing web application that enables users to access government-related services and submit or review information associated with their service requests.

The system may interact with:

* Citizen identity information
* Contact information
* Service request information
* Eligibility or benefits-related information
* Supporting documentation
* Internal administrative systems
* Third-party service providers

The system is assumed to operate within Orion's hybrid cloud environment and may utilize Azure Government services for hosting or supporting infrastructure.

---

# 3. System Boundary

## 3.1 In-Scope Components

The following components are considered within the preliminary system boundary:

| Component                            | Description                                   | Included?        |
| ------------------------------------ | --------------------------------------------- | ---------------- |
| Citizen-facing web application       | Public portal used by citizens                | Yes              |
| Application servers                  | Backend application processing                | Yes              |
| Application database                 | Stores system information                     | Yes              |
| Identity and authentication services | Supports user authentication                  | Yes              |
| Azure Government infrastructure      | Cloud-hosted system components                | Yes              |
| Administrative interfaces            | Used by authorized employees                  | Yes              |
| Relevant network components          | Connectivity supporting the system            | Yes              |
| Security monitoring tools            | Monitoring and security logging               | Yes              |
| Relevant third-party integrations    | External services supporting system functions | To Be Determined |

---

## 3.2 Out-of-Scope Components

The following are not automatically considered part of the system boundary unless they directly support the system:

| Component                         | Reason                                                                                         |
| --------------------------------- | ---------------------------------------------------------------------------------------------- |
| Unrelated corporate applications  | Not directly supporting the system mission                                                     |
| Personal employee devices         | Unless formally authorized and used to process system information                              |
| Unrelated Microsoft 365 workloads | Only relevant components are included                                                          |
| Independent third-party systems   | May be external dependencies or interconnected systems rather than part of the system boundary |



---

# 4. Information Types

The following information types have been identified for preliminary categorization.

| Information Type                                  | Description                                                       | Primary System Use                            |
| ------------------------------------------------- | ----------------------------------------------------------------- | --------------------------------------------- |
| Citizen Personally Identifiable Information (PII) | Information that can identify or be associated with an individual | User registration and service delivery        |
| Contact Information                               | Names, email addresses, phone numbers, and mailing information    | Communication and account management          |
| Service Request Information                       | Information submitted by citizens when requesting services        | Service processing                            |
| Benefits or Eligibility Information               | Information used to determine or support service eligibility      | Decision-making and service delivery          |
| Supporting Documentation                          | Documents submitted by citizens                                   | Verification and service processing           |
| Authentication Information                        | Account credentials and authentication-related information        | Identity verification and access control      |
| System Audit Logs                                 | Records of system activity and security events                    | Monitoring, investigation, and accountability |
| Public Service Information                        | Publicly available service information                            | Citizen communication                         |

---

# 5. FIPS 199 Impact Analysis

The system is evaluated against the three security objectives:

1. Confidentiality
2. Integrity
3. Availability

The impact level for each objective is assessed as:

* **Low**
* **Moderate**
* **High**

The final system categorization follows the **high-water-mark principle**:

> The overall system categorization is determined by the highest impact level assigned to Confidentiality, Integrity, or Availability.

---

# 6. Confidentiality Impact

## Impact Level: MODERATE

### Rationale

The Orion Citizen Services Portal processes citizen and customer information, including personally identifiable information and potentially sensitive service-related information.

Unauthorized disclosure could result in:

* Privacy harm to affected individuals
* Identity-related risks
* Loss of public trust
* Regulatory or legal consequences
* Reputational damage to Orion Government Solutions

However, based on the currently available business context, the system is not assumed to process classified national security information or information where unauthorized disclosure would directly result in exceptionally severe organizational or national-level consequences.

Therefore, the preliminary confidentiality impact is assessed as:

> **MODERATE**

### Confidentiality Assessment

| Question                                                | Assessment   |
| ------------------------------------------------------- | ------------ |
| Does the system process PII?                            | Yes          |
| Does it process customer or citizen information?        | Yes          |
| Could unauthorized disclosure harm individuals?         | Yes          |
| Could disclosure create regulatory consequences?        | Yes          |
| Is classified national security information identified? | No           |
| Preliminary Impact Level                                | **Moderate** |

---

# 7. Integrity Impact

## Impact Level: HIGH

### Rationale

The system may process information that influences citizen services, eligibility, administrative decisions, or other service outcomes.

Unauthorized modification, destruction, or manipulation of system information could result in:

* Incorrect service decisions
* Incorrect eligibility or benefits outcomes
* Fraudulent changes to citizen information
* Incorrect administrative actions
* Significant harm to affected individuals
* Loss of confidence in government services

Because the accuracy and trustworthiness of the information may directly affect citizen services and operational decisions, a compromise of integrity could have a severe impact.

Therefore, the preliminary integrity impact is assessed as:

> **HIGH**

### Integrity Assessment

| Question                                                 | Assessment  |
| -------------------------------------------------------- | ----------- |
| Could incorrect data affect citizen services?            | Yes         |
| Could unauthorized modification create significant harm? | Yes         |
| Could inaccurate data affect eligibility or decisions?   | Yes         |
| Could manipulation enable fraud?                         | Potentially |
| Preliminary Impact Level                                 | **High**    |

---

# 8. Availability Impact

## Impact Level: HIGH

### Rationale

The Orion Citizen Services Portal supports access to government-related services.

A prolonged outage could:

* Prevent citizens from accessing services
* Delay service requests
* Disrupt critical operational processes
* Create significant service backlogs
* Affect individuals who depend on timely access to services
* Cause substantial operational and reputational impact

Because availability may directly affect access to important citizen services, a prolonged disruption could result in significant harm.

Therefore, the preliminary availability impact is assessed as:

> **HIGH**

### Availability Assessment

| Question                                   | Assessment |
| ------------------------------------------ | ---------- |
| Is the system citizen-facing?              | Yes        |
| Would prolonged downtime disrupt services? | Yes        |
| Could citizens be materially affected?     | Yes        |
| Are continuity and recovery important?     | Yes        |
| Preliminary Impact Level                   | **High**   |

---

# 9. Overall System Categorization

## High-Water-Mark Analysis

| Security Objective | Impact Level |
| ------------------ | ------------ |
| Confidentiality    | Moderate     |
| Integrity          | High         |
| Availability       | High         |

---

## Overall Categorization: HIGH

### Categorization Statement

Based on the preliminary assessment of the system's information types, mission, and potential impact of security compromises, the Orion Citizen Services Portal is categorized as:

# HIGH

The categorization is determined using the highest impact level assigned to the three security objectives:

```text
Confidentiality = Moderate
Integrity       = High
Availability    = High

Overall System Categorization = HIGH
```

---

# 10. Categorization Rationale

The Orion Citizen Services Portal receives an overall **High** categorization because compromises to the integrity or availability of the system could result in significant harm to citizens and disruption of important government-related services.

The system processes sensitive citizen and customer information, creating a meaningful confidentiality impact. However, the potential consequences of inaccurate information or prolonged service disruption are assessed as more severe.

The primary drivers of the High categorization are:

1. **Integrity**

   Incorrect or manipulated citizen, service, eligibility, or benefits-related information could result in serious harm and incorrect service outcomes.

2. **Availability**

   Extended unavailability could prevent citizens from accessing important services and create significant operational disruption.

---

# 11. Categorization Assumptions

This preliminary categorization is based on the following assumptions:

| ID    | Assumption                                                                              |
| ----- | --------------------------------------------------------------------------------------- |
| A-001 | The system processes personally identifiable information                                |
| A-002 | The system supports citizen-facing services                                             |
| A-003 | The system may process information related to service eligibility or benefits           |
| A-004 | The system operates in a regulated environment                                          |
| A-005 | Azure Government may host or support system components                                  |
| A-006 | The system has dependencies on identity, network, monitoring, and third-party services  |
| A-007 | The system is not currently assumed to process classified national security information |

> These assumptions must be validated by the System Owner and relevant information owners before final categorization approval.

---

# 12. Categorization Limitations

This is a **preliminary categorization** based on the available business profile.

The following information should be confirmed before final approval:

* Exact information types processed
* Applicable legal and regulatory requirements
* Specific citizen data categories
* System availability requirements
* Maximum tolerable downtime
* Recovery Time Objective (RTO)
* Recovery Point Objective (RPO)
* Data classification requirements
* System interconnections
* Third-party dependencies
* Whether any information requires a higher impact categorization

---

# 13. Review and Approval

| Role                 | Name   | Decision            | Date | Signature |
| -------------------- | ------ | ------------------- | ---- | --------- |
| System Owner         | [Name] | Reviewed            |      |           |
| Information Owner    | [Name] | Reviewed            |      |           |
| ISSO                 | [Name] | Recommended         |      |           |
| Authorizing Official | [Name] | Approved / Rejected |      |           |

---

# 14. Categorization Review Triggers

The categorization should be reviewed when:

* [ ] The system processes new information types
* [ ] The system's mission changes
* [ ] The system boundary changes
* [ ] A new major system interconnection is introduced
* [ ] A significant change occurs in system architecture
* [ ] A new regulatory requirement applies
* [ ] The potential impact of a security compromise changes
* [ ] A major incident reveals previously unidentified impact
* [ ] The system begins processing higher-sensitivity information

---

# 15. RMF Next Step

The categorization result is used as the foundation for the next RMF activity:

> **Select appropriate security and privacy control baselines and tailor them to the system.**

The output of this worksheet therefore feeds into:

```text
CATEGORIZE
     ↓
HIGH SYSTEM CATEGORIZATION
     ↓
SELECT
     ↓
CONTROL BASELINE SELECTION
     ↓
TAILORING
     ↓
SYSTEM SECURITY PLAN
```



