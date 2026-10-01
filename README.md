# Security Risk Assessment (GRC) | NIST CSF 2.0

A security risk assessment for CloudCart, a fictional small e-commerce business. It combines a qualitative risk register with proportionate controls and proposed governance arrangements mapped to the NIST Cybersecurity Framework (CSF) 2.0.

## What This Is

This portfolio case study shows how a GRC analyst can turn business risks into treatment priorities, management decisions and evidence requirements. The assessment identifies eight risks, rates likelihood and impact, and connects operational safeguards to the policies, ownership and oversight needed to sustain them.

The recommendations are proposed actions for a fictional business. Control implementation, effectiveness and residual risk have not been verified. The assessment does not claim a complete CSF Organizational Profile, a CSF Tier or regulatory compliance.

## The Business

**CloudCart** (fictional): a small e-commerce business, approximately 15 employees, selling homeware online. Handles customer payment data, has a small in-house IT/development team, and works with a couple of third-party vendors (a payment processor and a hosting provider).

## Methodology

1. Establish the business context: customer data, online trading, internal IT capacity and supplier dependencies. Management should confirm applicable legal and contractual requirements, including the scope of payment-data obligations, before approving treatment priorities.
2. Assess each scenario using qualitative **Likelihood** (probability of occurrence) and **Impact** (consequences for customers, operations, finances and reputation). Low, Medium and High are relative judgements for this case study, with no numerical probability or loss estimate.
3. Combine likelihood and impact into **Overall Risk** using the matrix below. This matrix defines the scoring convention for the register. CSF 2.0 supplies the outcome taxonomy, not this scoring matrix.
4. Select proportionate treatments and map them to relevant CSF 2.0 outcomes. A recommendation can support more than one Function; a mapping indicates relevance, not proof that an entire outcome has been achieved.
5. Propose accountable owners, evidence and review arrangements. After implementation, validate effectiveness and reassess residual risk before management accepts any remaining exposure.

| Likelihood / Impact | Low impact | Medium impact | High impact |
|---|---|---|---|
| Low likelihood | Low | Low | Medium |
| Medium likelihood | Low | Medium | High |
| High likelihood | Medium | High | High |

CSF 2.0 has six Functions: **Govern, Identify, Protect, Detect, Respond and Recover**. Govern informs decisions across the other Functions through business context, risk strategy, accountability, policy, oversight and supply chain risk management. The Functions operate together rather than as sequential lifecycle stages.

## Risk Register

| # | Risk | Likelihood | Impact | Overall Risk |
|---|---|---|---|---|
| 1 | Customer payment data breach | Medium | High | High |
| 2 | Phishing attack against employees | High | Medium | High |
| 3 | Ransomware infection | Medium | High | High |
| 4 | Weak or reused employee passwords | High | Medium | High |
| 5 | Unpatched software or systems | Medium | Medium | Medium |
| 6 | Lost or stolen employee laptop | Medium | Medium | Medium |
| 7 | Third-party vendor (payment processor) compromise | Low | High | Medium |
| 8 | Insider data theft or misuse | Low | Medium | Low |

## Recommended Controls Mapped to CSF 2.0

These proposed safeguards address the eight risks. The mappings distinguish supplier governance, preventive protection and monitoring. Additional governance and incident recommendations follow separately.

| Risk | Recommended control | CSF 2.0 mapping and rationale |
|---|---|---|
| Payment data breach | Encrypt payment data at rest and in transit; restrict access to only staff who need it (least privilege) | Protect: PR.DS-01/02 for stored and transmitted data; PR.AA-05 for access permissions |
| Phishing | Security awareness training; email filtering and anti-phishing gateway | Protect: PR.AT-01 for staff awareness; PR.PS for platform safeguards such as email filtering |
| Ransomware | Offline or immutable backups tested regularly; endpoint detection and response (EDR) | Protect: PR.DS-11 for backup protection and testing; Detect: DE.CM-09 for endpoint monitoring. Response and restoration actions are specified below |
| Weak passwords | Enforce MFA account-wide; adopt a password manager | Protect: PR.AA-01/03 for credential management and authentication |
| Unpatched software | Formal patch management schedule; regular vulnerability scanning | Identify: ID.RA-01 for vulnerability identification; Protect: PR.PS-02 for software maintenance |
| Lost or stolen laptop | Full-disk encryption; remote wipe capability | Protect: PR.DS-01 for stored-data protection. Remote wipe supports limiting exposure where the device remains reachable |
| Vendor compromise | Vendor security review before onboarding; contractual security requirements | Govern: GV.SC-06 for due diligence and GV.SC-05 for contractual requirements; Identify: ID.RA-10 for assessment of critical suppliers |
| Insider misuse | Access logging and monitoring; role-based access control | Protect: PR.PS-04 for logging and PR.AA-05 for permissions; Detect: DE.CM-03 for monitoring staff activity |

### Incident Response and Recovery

CloudCart should establish and exercise an incident plan with escalation contacts and supplier involvement (**Identify: ID.IM-04; Govern: GV.SC-08**). For declared incidents, proposed actions include triaging reports and coordinating the response (**Respond: RS.MA-01/02**), containing affected endpoints or accounts (**RS.MI-01**) and notifying relevant stakeholders according to applicable obligations (**RS.CO-02**).

For ransomware or service disruption, verify backup integrity before restoration (**Recover: RC.RP-03**), then restore affected services and validate normal operation (**RC.RP-05**). Retain exercise and restoration results to identify improvements (**Identify: ID.IM-02**). Maintaining and testing backups is mapped to Protect; executing incident restoration provides the Recover coverage.

## Governance Recommendations Mapped to Govern

These proposed arrangements apply across the register. For a business of around 15 employees, existing management and IT roles can fulfil them without creating a separate governance department. Role assignments and review frequencies below are recommendations, not established CloudCart practices.

| Govern category | Proposed application to CloudCart | Evidence to retain |
|---|---|---|
| Organizational Context (GV.OC) | Record customer-data obligations, critical online services and dependencies on the payment processor and hosting provider | Requirements and dependency record, with payment-data scope confirmed |
| Risk Management Strategy (GV.RM) | Management should agree risk tolerance, treatment priorities and criteria for accepting exceptions; use this matrix consistently | Approved risk criteria and documented treatment or acceptance decisions |
| Roles, Responsibilities, and Authorities (GV.RR) | Assign an accountable management owner to each risk and an operational owner to each treatment; specify who can approve exceptions | Ownership register, decision authority and escalation contacts |
| Policy (GV.PO) | Approve concise policies covering access/MFA, data protection, patching, backups, acceptable use and supplier security; communicate and review them after material changes | Approved policy versions, staff communication and exception records |
| Oversight (GV.OV) | Review high-risk actions monthly and the full register quarterly, using evidence to challenge overdue actions and adjust priorities | Review minutes, action status, MFA coverage, patch reports and restoration-test results |
| Cybersecurity Supply Chain Risk Management (GV.SC) | Apply onboarding reviews and security clauses to suppliers; prioritise critical providers, reassess during the relationship and coordinate incident responsibilities | Supplier assessments, agreed security/notification terms, review dates and incident contacts |

Encryption, MFA and EDR retain their operational mappings. Govern applies to the decisions, responsibilities and assurance around those safeguards. Vendor compromise remains **Medium** in this register, while its **High impact** justifies supplier oversight and clear contractual responsibilities.

### Treatment Follow-Up and Assurance

For each risk, management should record the selected response (mitigate, avoid, transfer/share or accept), accountable owner, action owner, target date, status and evidence. The controls above principally propose mitigation. Supplier contracts clarify responsibilities but do not remove CloudCart's need to manage its own exposure.

Examples of closure evidence include MFA coverage and exception records, encryption/access checks, patch compliance, training completion, reviewed monitoring alerts and successful restoration tests. Reassess likelihood and impact using this evidence, record residual risk separately, and document management approval and a review date for accepted risks. Reopen the assessment after significant incidents, supplier changes or changes in payment-data handling.

## Prioritization Summary

Four risks are **High**: payment data breach, phishing, ransomware and weak passwords. Prioritise their safeguards and assign owners so management can track progress and resolve resource constraints.

Three risks are **Medium**: unpatched software, lost or stolen devices and vendor compromise. Set documented treatment dates and monitor progress; new evidence of exploitation or exposure may require escalation regardless of the original rating.

Insider data theft remains **Low**, reflecting the case study's lower-likelihood judgement for a small organisation. Keep proportionate access restrictions and monitoring, and revisit that judgement when staffing, privileges or evidence changes.

## What This Demonstrates

- Qualitative risk assessment with an explicit scoring matrix and treatment priorities linked to a specific business context.
- Practical use of CSF 2.0, including Govern mappings for policy, accountability, oversight and third-party risk, alongside operational security outcomes.
- Governance design that separates management accountability, control delivery and evidence-based review.
- Supplier risk reasoning that connects due diligence and contracts to ongoing monitoring and incident coordination.
- Assurance discipline: distinguishing recommendations from verified implementation, and planning residual-risk review and documented acceptance.
- Clear communication of business exposure and proportionate actions to technical and non-technical stakeholders.

## Deliverable

Full assessment: [CloudCart-Risk-Assessment.docx](CloudCart-Risk-Assessment.docx)

![CloudCart CSF 2.0 risk assessment preview](screenshots/risk-assessment-preview.jpg)

## Tools and References

| Tool or reference | Purpose |
|---|---|
| [NIST Cybersecurity Framework 2.0 (NIST CSWP 29)](https://doi.org/10.6028/NIST.CSWP.29) | Framework basis; Appendix A contains the Function, Category and Subcategory identifiers used here |
| [NIST CSF resources](https://www.nist.gov/cyberframework) | Official framework guidance and supporting resources |
| Microsoft Word | Assessment report |

## Full Portfolio

See the complete project index: [cybersecurity-portfolio](https://github.com/RaheemC4/cybersecurity-portfolio)
