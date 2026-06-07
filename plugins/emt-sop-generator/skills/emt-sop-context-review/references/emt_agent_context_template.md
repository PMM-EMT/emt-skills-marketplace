# EMT [Type] — Agent Context

<!-- Title format: "EMT [Full Type Name] — Agent Context"
     Examples: EMT Type 1 Mobile, EMT Type 2, EMT Type 3 -->

_Source: WHO Classification and Minimum Standards for EMTs, 2021_

---

## Identity Parameters

<!-- Core deployment specs. All fields are required. Use exact numbers from the WHO Blue Book.
     "Structure" describes the physical facility model (tent, vehicle, modular hospital, etc.) -->

| Parameter | Value |
|---|---|
| Type | <!-- e.g. EMT Type 2 --> |
| Facility model | <!-- e.g. Fixed inpatient surgical facility --> |
| Care level | <!-- e.g. Inpatient surgical and general care --> |
| Min throughput | <!-- e.g. 20 inpatients/day; 7 ORs/week --> |
| Operating hours | <!-- e.g. 24/7 inpatient care --> |
| Deployment readiness | <!-- e.g. Operational within 72 h of arrival --> |
| Min deployment duration | <!-- e.g. 3 weeks --> |
| Structure | <!-- e.g. Modular tent-based surgical hospital --> |

---

## Scope of Care

<!-- Two mandatory subsections: what this team type CAN do, and what must be referred.
     Keep each bullet to one capability cluster. Avoid duplicating the Clinical Capabilities table. -->

**Permitted:**
- <!-- List services, interventions, and care domains in scope -->

**Refer to higher care:**
- <!-- List conditions, procedures, or complexity levels that exceed this team type's scope -->

---

## Explicit Exclusions

<!-- Hard boundaries — what this team type must NEVER be described as providing.
     Start each item with "No" for fast agent parsing. Include optional items with a note. -->

- No <!-- capability -->
- <!-- [OPTIONAL: item] — optional only, not a minimum standard -->

---

## Clinical Capabilities

<!-- Row-per-domain reference table. Use "Not applicable" for domains this type does not cover.
     Use "Not required" for optional/context-dependent items.
     Keep capability text concise — abbreviate where unambiguous (BLS, BVM, RDT, IPC, etc.)
     Standard domain rows are listed below; add rows for type-specific domains as needed. -->

| Domain | Capability |
|---|---|
| Triage | <!-- e.g. Initial + field triage; MCI plan required --> |
| Resuscitation | <!-- e.g. Advanced life support; RSI; point-of-care ultrasound --> |
| Airway | <!-- e.g. Full airway management including surgical airway --> |
| Wounds | <!-- e.g. Surgical wound management; delayed primary closure --> |
| Burns | <!-- e.g. Up to X% TBSA; refer complex/major burns --> |
| Fractures | <!-- e.g. Internal/external fixation; refer complex cases --> |
| Spinal injury | <!-- e.g. Surgical stabilization; or: Assessment, immobilization, transfer --> |
| Communicable disease | <!-- e.g. Isolation, screening, reporting, referral --> |
| NCDs | <!-- e.g. Inpatient chronic disease management --> |
| RMNH | <!-- e.g. Comprehensive emergency obstetric care including C-section --> |
| Paediatrics | <!-- e.g. Inpatient paediatric care and surgery --> |
| Analgesia/anaesthesia | <!-- e.g. General and regional anaesthesia --> |
| Surgery | <!-- e.g. General, orthopaedic, obstetric surgery --> |
| Palliative care | <!-- e.g. Inpatient palliative care --> |
| Rehabilitation | <!-- e.g. Post-surgical rehabilitation --> |
| Laboratory | <!-- e.g. Full blood count, biochemistry, crossmatch, RDTs --> |
| Pharmacy | <!-- e.g. Inpatient drug supply including anaesthetic agents --> |
| Sterilization | <!-- e.g. Steam autoclave; instrument decontamination --> |
| IPC | <!-- e.g. Facility-wide IPC protocols; surgical site IPC --> |
| Imaging | <!-- e.g. X-ray required; ultrasound required; or: Not required --> |
| ICU | <!-- e.g. 4-bed ICU with ventilation; or: Not applicable --> |
| Blood transfusion | <!-- e.g. Whole blood or component transfusion; or: Not applicable --> |

---

## Facility Layout

<!-- Physical zones and patient flow requirements specific to this team type.
     List only zones that are required minimums — do not include optional/contextual zones. -->

- <!-- Entry point and patient identification -->
- Required zones: <!-- zone · zone · zone -->
- <!-- Any dedicated areas required (e.g. OR, ICU, isolation, maternity) -->
- <!-- Infection control / patient separation requirements -->
- <!-- Accessibility and dignity requirements -->

---

## Triage Requirements

<!-- Triage system, staffing, and MCI planning obligations.
     Most of these are consistent across types; adjust only where the WHO Blue Book differs. -->

- Established triage system for both daily care and mass casualty incidents (MCI)
- Includes infectious disease screening at triage
- Dedicated triage staff member per shift
- MCI management plan must be validated and rehearsed
- Waiting patients reassessed when clinical condition may change

---

## Referral and Transfer

<!-- Referral obligations. The first four bullets are standard across all EMT types.
     Adjust the first bullet to name this team type correctly.
     Add type-specific referral obligations (e.g. ICU overflow, specialist transfer) as needed. -->

- Referral is a central [Type Name] function; written protocols required
- Communicate with receiving facility before transfer where possible
- Stabilize using ABCDE and manage pain before transport
- Obtain informed consent; provide written clinical summary with each transfer
- Responsibility remains with transferring team until formal handover to receiving facility
- <!-- Any additional type-specific transfer obligations -->

---

## Operational Parameters

<!-- Numeric specifications. Use exact figures from the WHO Blue Book.
     Add or remove rows to match what is specified for this team type.
     The "Additional" line below is for non-tabular requirements (accessibility, hygiene, etc.) -->

| Resource | Specification |
|---|---|
| Power | <!-- e.g. 30–60 kVA --> |
| Water — staff | <!-- e.g. 40–60 L/person/day --> |
| Water — inpatients | <!-- e.g. 40–60 L/patient/day --> |
| Water — outpatients | <!-- e.g. 5 L/outpatient/day; omit if not applicable --> |
| Toilets — staff | <!-- e.g. 1 per 20 persons --> |
| Toilets — patients | <!-- e.g. 1 per 10 inpatients --> |
| Infectious waste | <!-- e.g. Min X kg/day treatment capacity; Y L hazard containment --> |
| Mortuary | <!-- e.g. X bodies in dedicated tent/space --> |
| Communications | <!-- e.g. 1 primary + 1 backup; SIM + satellite; voice and data --> |

Additional: <!-- any non-tabular operational requirements specific to this type -->

---

## Staffing

<!-- Minimum staffing composition per the WHO Blue Book.
     List by role and required minimum count.
     Note any 24/7 supervision or specialist on-call obligations. -->

- Minimum <!-- N --> <!-- role(s) -->
- <!-- Medical supervision model: 24/7 physical presence / on-call system -->
- Structured clinical handover between shifts required

---

## Coordination and Reporting

<!-- These rules are consistent across all EMT types. Do not modify unless the
     WHO Blue Book specifies a deviation for this team type. -->

- Deploy only when formally accepted and tasked by the relevant authority
- Register on arrival per national or EMT coordination procedures
- Operate under the national health emergency management authority and/or EMT Coordination Cell
- Report using national forms; use EMT Minimum Data Set if national forms are unavailable
- Maintain confidential patient records; provide each patient with a discharge or referral document
- Coordinate referrals, transfers, public health reporting, and exit planning with local authorities
- No research without patient consent, national authority approval, and ethical approval
