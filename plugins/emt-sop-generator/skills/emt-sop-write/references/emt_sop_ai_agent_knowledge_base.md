---
title: "EMT SOP AI Agent Knowledge Base"
version: "2.0"
date: "2026-06-05"
purpose: "Language-independent SOP generation blueprint for Emergency Medical Teams of any EMT type"
audience:
  - AI SOP generation agents
  - EMT SOP authors
  - EMT coordination, clinical, operations, logistics, ICT, public-health, and quality leads
scope: "General SOP architecture for WHO Emergency Medical Teams, with EMT-type-specific details provided by the user or mission documents."
status: "Research synthesis / generation blueprint"
---

# EMT SOP AI Agent Knowledge Base

## 0. Purpose

Use this file to generate field-ready Standard Operating Procedures for Emergency Medical Teams. It is generic across EMT types and capability packages. Derive type-specific capability limits from the user-provided EMT type, capability statement, mission documents, or locally approved scope.

The SOP generator must produce procedures that can be used by tired, multilingual, interrupted, time-pressured staff in austere or rapidly changing conditions.

## 1. EMT type and capability controls

Before drafting a complete SOP, identify the EMT type or approved capability package. Ask the user if it is missing.

Common EMT configurations include:

- Type 1 Mobile: mobile outpatient emergency care.
- Type 1 Fixed: fixed-site outpatient emergency care.
- Type 2: inpatient acute care, emergency care, and surgery within the team's approved capability.
- Type 3: referral-level inpatient care with more complex surgical and critical-care capability within the team's approved capability.
- Specialist care team or cell: a defined specialist capability integrated with another EMT or health facility, such as rehabilitation, burns, dialysis, obstetrics, infectious disease, mental health, public health, or logistics support.

For every SOP, define:

- included services;
- excluded services;
- patient groups;
- staffing assumptions;
- site or mobile operating model;
- referral and escalation pathways;
- diagnostics, procedures, medicines, and equipment authorized for the team;
- host-country or mission-approved scope changes.

Do not authorize activities outside the specified EMT type, specialist cell mandate, or locally approved scope.

## 2. Canonical SOP sections

Use these seven canonical sections internally. Translate headings and definitions into the user-specified SOP language for the final output.

| Section | Objective | Required content | Writing guidance | Generic EMT example |
|---|---|---|---|---|
| **1. Scope** | Define exactly what the SOP governs, where it applies, when it activates, who must use it, and what it excludes. | SOP title; SOP ID; version; effective date; owner; review cycle; deployment phase; activation trigger; location or mobile area; shift or operating hours; user groups; patient groups; included services; excluded services; interfaces with referral facilities, pharmacy, IPC, logistics, ICT, EMTCC, PHEOC, MoH, and local authorities; dependencies on other SOPs and forms. | Write as a boundary statement. Use present tense and direct verbs: `applies`, `covers`, `excludes`, `activates`, `does not authorize`. Avoid vague phrases such as `all medical activities` unless boundaries are listed. | `This SOP applies to the EMT clinical workflow during the response phase at the approved site or mobile area. It covers activation, staffing confirmation, patient flow, documentation, referral, reporting, and handover. It does not authorize services outside the team capability statement.` |
| **2. Goal** | State the operational end-state the SOP must achieve. Link staff behavior to safety, quality, timeliness, accountability, and coordination. | Purpose statement; intended safety outcome; clinical or operational quality outcome; coordination outcome; documentation/reporting outcome; measurable service targets; trigger-to-action expectations; continuity-of-care goal; referral goal; reporting deadlines. | Use one declarative paragraph followed by 2-5 measurable goal statements. Use active, outcome-focused verbs: `ensure`, `maintain`, `stabilize`, `refer`, `document`, `report`, `handover`. | `The goal of this SOP is to ensure that the EMT delivers care within its approved capability, documents all critical actions, escalates risks promptly, and reports required data to coordination authorities by the agreed deadline.` |
| **3. Roles and responsibilities** | Make command, accountability, task ownership, escalation rights, and handover duties explicit. | Named roles and alternates; activation authority; stop-work authority; escalation thresholds; approval requirements; reporting lines; delegation rules; shift handover responsibilities; signature authority for forms and reports. Common roles may include Team Leader, Deputy or Operations Lead, Clinical Lead, Triage Lead, Registration/Data Lead, MDS or Information Management Focal Point, Referral Focal Point, Pharmacy or Medical Supplies Lead, IPC/Waste Lead, Logistics Lead, ICT/Telecom Lead, Security Focal Point, EMTCC/MoH/PHEOC Liaison, Shift Supervisor, and Handover or Demobilization Owner. | Use role-action format: `Role + must + action`. Keep each responsibility atomic. Avoid diffuse ownership such as `the team ensures`. State alternates. Use RACI-style logic where helpful. | `The Team Leader authorizes activation. The Clinical Lead confirms clinical scope and escalation thresholds. The Information Management Focal Point submits the daily report. The Logistics Lead verifies utilities, equipment, transport, and supply readiness.` |
| **4. Terms and definitions** | Standardize vocabulary so staff and partner agencies interpret the SOP the same way. | Abbreviations expanded on first use; locally binding definitions; WHO EMT typology terms; MoH/PHEOC/EMTCC terminology; patient-category terms; triage terms; referral terms; activation/mobilization/demobilization terms; MDS; PPE; IPC; SitRep; handover; red flag; clinical escalation; local legal or administrative terms. Include translation pairs when SOPs are bilingual. | Keep definitions short. Use one sentence per term. Prefer common emergency-management terminology over local shorthand. Avoid unexplained acronyms, radio codes, slang, and roster-mismatched role names. Define only terms that affect action, interpretation, safety, reporting, or legal compliance. | `EMTCC: Emergency Medical Team Coordination Cell responsible for coordinating EMT support. MDS: EMT Minimum Data Set used for daily operational and clinical reporting. Scope of practice: the clinical activities authorized by the host authority and the EMT leadership for the deployment.` |
| **5. Procedure description** | Provide the step-by-step execution path from trigger to completion. | Prerequisites; trigger; authorization; minimum staffing; required equipment/PPE; site or mobile setup; safety checks; patient or task flow; registration; triage if relevant; clinical or operational sequence; limits; referral criteria; communication; transport or escort rules; pharmacy or supply process; IPC and waste flow; documentation; MDS/SitRep deadlines; incident escalation; contingency actions; handover; demobilization; after-action review. | Use numbered, sequential, imperative steps. Each critical step must identify actor + action + output. Use `If...then...` decision logic. Use `Do not...unless...` for safety boundaries. Keep one action per line where possible. Put explanatory detail in notes or annexes, not in the hot path. | `1. The Team Leader activates the SOP. 2. The Shift Supervisor confirms minimum staffing. 3. The Logistics Lead verifies required resources. 4. The responsible role executes the workflow and records evidence. 5. The designated focal point escalates exceptions. 6. The Information Management Focal Point submits required reports. 7. The Shift Supervisor completes handover.` |
| **6. Appendices** | Convert the SOP from guidance into a field-ready operational package. | Controlled attachments such as activation checklist, contact tree, site or mobile-area checklist, layout or route map, patient-flow diagram, staffing matrix, equipment/cache list, pharmacy stock sheet, cold-chain log, triage aid, patient record form, referral form, MDS tally sheet, daily report template, SitRep template, incident/escalation form, waste segregation chart, PPE card, cleaning schedule, security briefing template, exit report, handover checklist, after-action review template. | Name appendices clearly and reference them directly inside the procedure. Version-control forms. Keep appendices short, operational, printable, and scannable. Do not hide mandatory steps only in appendices. | `Appendix A: Activation checklist. Appendix B: Staffing and role confirmation form. Appendix C: Referral form. Appendix D: EMT MDS tally sheet. Appendix E: Handover checklist.` |
| **7. Legal and regulatory requirements** | Make the SOP legally operable, auditable, and defensible. | Host-country request or authorization; MoH approval; disaster/emergency law; health-facility or mobile-clinic authorization; professional licensing or credential recognition; scope of practice; liability coverage; customs/import rules; medicine and controlled-drug rules; medical-device rules; occupational health and safety; IPC; medical waste; patient confidentiality; data protection; record retention; death reporting; referral documentation; MoUs/MoAs; International Health Regulations obligations; humanitarian principles and medical neutrality where relevant. | Write as a compliance map, not copied legislation. Use `instrument or standard + operational implication + responsible role + evidence`. Use exact names, dates, decree numbers, articles, and local authorities when available. | `Before operations begin, the Team Leader verifies host authorization, clinical credential recognition, customs clearance, medicine controls, waste arrangements, liability coverage, and secure handling of records.` |

## 3. Intake data set

Ask for missing data before drafting. Required intake includes:

- SOP language.
- EMT type or specialist capability package.
- SOP title, SOP ID, version, effective date, review date or review cycle, owner, approver, deployment phase, related SOPs, and related forms.
- Workflow topic, activation trigger, covered site or mobile area, operating hours, staff groups, patient groups, included services, excluded services, and operational boundaries.
- Named roles and alternates, reporting lines, escalation authority, approval authority, delegation rules, and handover owner.
- Coordination recipients such as EMTCC, MoH, PHEOC, referral facilities, local emergency operations structures, mission command, or cluster coordination bodies.
- Required forms, logs, checklists, reports, appendices, evidence artifacts, deadlines, and record locations.
- Legal and regulatory sources where the workflow needs SOP-specific legal controls; host-country authorization, scope of practice, credential recognition, customs/import rules, medicine and controlled-drug rules, waste rules, data protection, confidentiality, liability, and record retention requirements when relevant.

## 4. Language and translation rules

The agent must not assume the SOP language. Ask the user to specify it.

Use English as the canonical internal language for section names, terms, and role concepts. Translate the final SOP into the requested language. Keep translations consistent across sections.

Rules:

- Expand acronyms on first use in the SOP language when appropriate.
- Preserve official acronyms unless a local official equivalent is provided.
- Use one translated role name consistently.
- If bilingual output is requested, provide term pairs in `Terms and definitions`.
- Avoid mixing languages inside operational steps unless the term is an official role, form, report, or acronym.

## 5. Procedure step template

Use this step-by-step structure for `Procedure description`. Adapt subsection names to the workflow, but keep the sequence actionable from trigger to completion.

```markdown
### 5.1 Trigger

The procedure starts when [role/authority] [activation event].

### 5.2 Preconditions

Before starting, [responsible role] must verify:

- [condition 1]
- [condition 2]
- [condition 3]

### 5.3 Required resources

[Responsible role] must confirm that the following resources are available before the workflow starts:

| Resource type | Required resource | Minimum quantity / condition | Responsible role | Evidence |
|---|---|---|---|---|
| Human resources | [role / staff category] | [minimum number, competency, credential, or availability] | [role] | [roster / briefing record / credential file] |
| Tools and equipment | [tool / device / kit / PPE / ICT item] | [minimum quantity, readiness state, calibration, power, connectivity, or sterility requirement] | [role] | [checklist / log / inspection record] |
| Forms and records | [form / checklist / log / report] | [current version and location] | [role] | [document-control record / completed form] |
| Supplies and medicines | [supply / medicine / consumable] | [minimum stock or threshold] | [role] | [stock card / pharmacy log] |

### 5.4 Step-by-step procedure

1. [Role] must [action] using [tool/form] and record [evidence].
2. [Role] must [action] before [condition/deadline].
3. If [risk/threshold], then [role] must [escalation action] to [recipient].
4. Do not [prohibited action] unless [approval/condition].
5. [Role] must complete [form/checklist] and file it in [location/system].

### 5.5 Escalation

Escalate immediately to [role/authority] if:

- [threshold 1]
- [threshold 2]
- [threshold 3]

### 5.6 Completion criteria

The procedure is complete when:

- [output 1] is completed;
- [output 2] is submitted;
- [handover/reporting] is confirmed.
```

## 6. Writing rules for emergency environments

Use:

- short sentences;
- active voice;
- actor-before-action wording for safety-critical steps;
- numbered steps for procedures;
- bullets for requirements, equipment, risks, and exclusions;
- tables for role ownership, legal matrices, forms, and escalation thresholds;
- `If...then...` decision rules;
- `Do not...unless...` for hard safety boundaries;
- mandatory verbs such as `must` or `shall` for requirements;
- `should` for recommendations;
- `may` only for optional actions;
- direct verbs such as `verify`, `record`, `notify`, `escalate`, `refer`, `isolate`, `clean`, `handover`, `submit`, `secure`, and `dispose`.

Avoid:

- unexplained acronyms;
- passive voice in safety-critical instructions;
- long paragraphs in the operational path;
- multiple actions in one sentence when timing, safety, or accountability matters;
- `as appropriate` without criteria;
- `if necessary` without a decision threshold;
- `relevant staff` without a named role;
- `properly`, `adequately`, `timely`, or `regularly` without measurable meaning;
- long legal quotations.

## 7. Evidence-of-action rule

For every critical step, identify the evidence artifact.

| Critical workflow | Evidence artifact |
|---|---|
| Activation | Activation log / command message / deployment order |
| Opening of site or mobile service | Site-opening checklist / mobile-team readiness checklist |
| Staff readiness | Shift roster / briefing record |
| Patient registration | Patient record / registration log |
| Triage | Triage tag / triage register / patient record |
| Clinical care | Patient record / clinical note / treatment log |
| Referral or transfer | Referral form / receiving-facility confirmation |
| Medicine dispensing | Pharmacy log / prescription record |
| Stock change | Stock card / inventory sheet |
| Cold chain | Temperature log / excursion report |
| Waste disposal | Waste log / sharps container check |
| Daily reporting | MDS tally sheet / daily report / SitRep |
| Incident escalation | Incident report / command log |
| Shift change | Handover checklist |
| Demobilization | Exit report / asset reconciliation / handover protocol |

## 8. Escalation rule

Every SOP must define escalation thresholds where relevant. Examples include:

- patient or workload exceeds team capability;
- surge exceeds triage, treatment, bed, theatre, referral, or transport capacity;
- referral pathway is unavailable;
- critical medicine or consumable stock falls below minimum threshold;
- cold chain fails;
- water, power, sanitation, oxygen, sterilization, or waste service fails;
- security threat affects operations;
- data breach or loss of patient records occurs;
- infectious disease cluster is suspected;
- staff injury, exposure, fatigue, credential issue, or safeguarding concern affects safe operation;
- legal authorization, customs clearance, or host-country permission is unclear.

## 9. Legal-operational rule

Not every SOP requires detailed legal or regulatory content beyond the team's baseline authorization and governance. Ask whether the workflow has SOP-specific legal, regulatory, licensing, data, medicine, customs, waste, insurance, or record-retention requirements. If none apply, state that no additional SOP-specific legal controls were identified and reference the baseline authorization or governance document if provided.

When legal or regulatory controls apply, map obligations into field actions. The rows below are examples, not a mandatory list for every SOP.

Use this structure:

| Legal / regulatory source | Operational implication | Responsible role | Required evidence |
|---|---|---|---|
| Host-country authorization | Team may operate only after authorization is confirmed | Team Leader | Authorization letter / email / coordination-cell record |
| Credential recognition | Staff may work only within recognized scope | Team Leader + Clinical Lead | Credential file / recognition list |
| Scope of practice | Services must remain within approved team capability | Clinical Lead | Scope document / approved service list |
| Customs clearance | Imported cache, medicines, and devices must be cleared before use | Logistics Lead | Customs documents / import list |
| Medicine and controlled-drug rules | Medicines must be stored, prescribed, dispensed, and reconciled under applicable rules | Pharmacy/Medical Supplies Lead | Stock records / controlled-drug register |
| Medical waste law | Waste must be segregated, stored, transferred, and documented | IPC/Waste Lead | Waste log / disposal agreement |
| Patient confidentiality / data protection | Patient records must be stored and transmitted securely | Data/MDS Focal Point | Record-control log / secure storage procedure |
| Liability and insurance | Staff and services must be covered before operations | Team Leader | Insurance or indemnity confirmation |

## 10. Validation checklist

Before final output, verify:

- The SOP language was specified by the user.
- The EMT type or capability package was specified by the user.
- All seven canonical sections are present in translated form.
- Required metadata is present.
- Included and excluded services match the approved capability.
- The SOP defines activation trigger, responsible roles, minimum readiness conditions, ordered steps, escalation thresholds, completion criteria, and handover or closure actions.
- Every critical workflow has a form, checklist, log, or report.
- Appendices are named and referenced in the procedure.
- Patient, operational, and reporting documentation requirements are explicit.
- Reporting deadlines and recipients are explicit.
- Terms, roles, acronyms, forms, and authorities are defined and used consistently.
- Legal obligations are mapped to operational actions, responsible roles, and evidence when SOP-specific legal controls apply; otherwise, the legal section states that no additional workflow-specific legal controls were identified.
- The SOP avoids vague qualifiers, unexplained acronyms, and dense operational paragraphs.

## 11. Source map

The architecture and rules are based on general SOP, emergency management, EMT coordination, and humanitarian response guidance, including WHO SOP-writing guidance, WHO EMT classification and standards, WHO EMT strategy, EMT Minimum Data Set guidance, IFRC emergency response frameworks, ASEAN EMT coordination SOPs, FEMA/NIMS planning doctrine, CDC plain-language guidance, field-hospital operational guidance, disaster-law analysis for EMTs, International Health Regulations, and WHO data-policy principles.
