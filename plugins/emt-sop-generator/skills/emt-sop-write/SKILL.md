---
name: emt-sop-write
description: Generate and revise Standard Operating Procedures for WHO Emergency Medical Teams of any EMT type, including Type 1 Mobile, Type 1 Fixed, Type 2, Type 3, and specialist care teams or cells. Use when Claude needs to draft field-ready EMT SOPs, adapt SOP content to mission data and team capability, ask for missing required SOP inputs, enforce mandatory SOP sections in the requested output language, maintain defined terms and roles, or enforce EMT capability limits from user-provided team scope.
---

# EMT SOP Write

## Core Contract

Generate Standard Operating Procedures for Emergency Medical Team deployments across EMT types. Default to Markdown output. Do not assume the SOP language: always ask the user to specify the SOP language before drafting a complete SOP.

Use English in internal reasoning, reference names, and skill-maintained terminology. Translate SOP section headings, role labels, terms, and definitions into the user-specified SOP language for the final output. Preserve official acronyms such as EMT, EMTCC, MoH, PHEOC, MDS, IPC, PPE, and SitRep unless the user provides local equivalents.

Treat the seven main SOP sections as nonnegotiable. Use these English canonical section names internally:

1. Scope
2. Goal
3. Roles and responsibilities
4. Terms and definitions
5. Procedure description
6. Appendices
7. Legal and regulatory requirements

In the SOP output, translate these seven headings into the requested language and keep their meaning, order, and separation. Create subsections when they improve clarity. Do not remove, merge, or reorder the main sections.

## Reference Loading

Read `references/emt_high_level_context.md` before drafting, revising, or reviewing a complete SOP. Use it for EMT domain context, EMT types, guiding principles, operating logic, coordination, records, reporting, operational requirements, public health role, operating constraints, terminology, and abbreviations.

Read `references/emt_sop_structure.md` before drafting, revising, or reviewing a complete SOP. Use it for document structure, section format, section purpose, and section-level rules.

For the requested EMT type, ask the user for the team's official capability statement, approved scope, exclusions, staffing model, deployment configuration, and any local authorization that changes the baseline EMT type capability.

For narrow edits to an existing SOP, read only the relevant reference sections when possible. Useful search headings include:

- `EMT Types` in `emt_high_level_context.md`
- `Operating Logic` in `emt_high_level_context.md`
- `Records & Reporting` in `emt_high_level_context.md`
- `Metadata Table` in `emt_sop_structure.md`
- `Procedure Description` in `emt_sop_structure.md`
- `Escalation` in `emt_sop_structure.md`
- `Completion Criteria` in `emt_sop_structure.md`

## Intake Workflow

Before drafting a complete SOP, ask for missing required data instead of inventing it. Always ask for:

- SOP language.
- EMT type or capability package.
- SOP title, SOP ID, version, effective date, review date or review cycle, owner, approver, applicable deployment phase, related SOPs, and related forms.
- SOP topic or workflow, activation trigger, covered site or operational setting, covered hours or shift model, staff groups, patient groups, included services, excluded services, and operational boundaries.
- Named roles and alternates, reporting lines, escalation authority, approval authority, delegation rules, and handover responsibility.
- Coordination recipients such as EMTCC, MoH, PHEOC, referral facilities, local emergency operations structures, mission command, or cluster coordination bodies.
- Required forms, logs, checklists, reports, appendices, evidence artifacts, deadlines, and record locations.
- Legal or regulatory sources where the SOP-specific workflow needs them, plus host-country authorization, clinical scope, credential recognition, medicine and customs rules, waste rules, data protection, confidentiality, liability, and record retention requirements when relevant.

If data is incomplete, ask concise follow-up questions grouped by section. Continue drafting only the parts supported by available data, and mark unresolved items as `To be completed:` only when the user explicitly wants a partial draft.

## Drafting Rules

Keep each SOP bound to one primary workflow and deployment phase. If setup, daily operation, maintenance, shift handover, demobilization, or incident follow-up create different triggers, evidence, roles, or escalation thresholds, split them into separate SOPs or working drafts instead of mixing them into one procedure.

Keep every SOP within the approved capability of the specified EMT type. Derive the permitted boundary from user-provided team documents, not from generic EMT type labels alone. Ask for the team's official capability statement, approved clinical and operational scope, exclusions, staffing model, site or mobile operating model, referral and escalation pathways, authorized diagnostics, procedures, medicines, equipment, services, and host-country or mission-approved scope changes.

Do not authorize clinical services, procedures, admissions, diagnostics, surgeries, critical care, blood products, specialist care, transport, public-health functions, or operational activities unless they are inside the team type, specialist mandate, local authorization, staff competence, equipment, medicine availability, and assigned tasking.

Use role-bound, evidence-backed instructions:

- Put the responsible role before each safety-critical action.
- Define the trigger, action, output or evidence, form or appendix, escalation path, and completion criterion for each critical workflow.
- Select evidence artifacts that match the workflow and documentation system, such as activation logs, readiness checklists, rosters, patient records, triage tags, referral forms, pharmacy logs, stock cards, cold-chain logs, waste logs, daily reports, incident reports, handover checklists, and demobilization records.
- Use numbered steps in `Procedure description`.
- Use `If...then...` decision logic for thresholds and exceptions.
- Use `Do not...unless...` for safety boundaries.
- Use tables for role ownership, legal matrices, forms, escalation thresholds, and appendices.
- Keep operational steps focused on action, testing, recording status, and documenting results. Put repeated escalation/reporting paths in the escalation subsection instead of duplicating them in setup steps, checks, role descriptions, appendices, or handover text.
- For each escalation threshold, identify the triggering condition, responsible role, escalation recipient, required evidence, and immediate operational limit or workaround.
- Match escalation thresholds to the SOP phase. Setup SOPs should escalate setup limitations and readiness blockers; maintenance or operations SOPs should carry broader degradation, outage, incident follow-up, and shift handover escalation policies.
- Avoid vague terms such as `appropriate staff`, `if necessary`, `regularly`, or `according to local procedures` unless the role, threshold, frequency, authority, or source is named.

## Terms And Roles Discipline

Maintain unambiguous vocabulary throughout the SOP.

- Define every acronym, role, locally binding term, patient category, report name, authority, coordination body, form, and operational status that affects action, safety, interpretation, reporting, or legal compliance.
- Reference defined terms and role names exactly as written in `Terms and definitions` and `Roles and responsibilities`, translated consistently into the SOP language.
- If a new term, acronym, authority, form, or role appears while drafting a later section, add it to the appropriate definitions or roles section before finalizing.
- Do not use informal synonyms for defined roles. For example, if `Clinical Lead` is defined, keep using `Clinical Lead`; do not switch to `clinical supervisor`, `medical lead`, or `lead doctor` unless those are separately defined.

## Source And Appendix Discipline

Use source material and appendices deliberately.

- Capture baseline assumptions from user-provided source material before drafting, including team type, staffing model, operating model, minimum equipment or systems, redundancy assumptions, local authorization dependencies, and known exclusions.
- When a technical, clinical, security, logistics, or legal requirement comes from a source pack or guidebook, convert it into concise field actions, parameters, evidence, or appendix rows. Do not bury source-derived controls in long explanatory paragraphs.
- Keep main SOP procedures concise. Move long resource lists, detailed technical controls, logs, checklists, contact templates, handover tools, and source-backed requirement tables into appendices.
- Order appendices by first use in the main SOP, keep appendix letters and file names synchronized, and update every in-text reference when appendix order changes.
- Do not hide mandatory actions only in appendices. The main procedure must tell staff when to use each appendix.
- Use generic system names when product names or local tools are not essential, such as `local servers running approved team applications`; use product names only when the SOP specifically depends on that product, authorization, configuration, or test.

## Coordination And Contact Discipline

Make coordination and contact requirements operational.

- Define coordination bodies, technical coordination structures, diplomatic contact points, and local authorities when they appear in the SOP, including mission-specific bodies such as EMTCC, ETC, UCPMT, MoH, EOC, embassies, EU delegation, or equivalent local structures.
- Add contact placeholders when the procedure depends on reaching coordination, referral, security, emergency, or diplomatic contacts.
- Keep contact templates in appendices unless a small contact list is essential in the procedure hot path.

## Segmentation And Security Pattern

For ICT, data, communications, or other system workflows, separate high-level operational requirements from detailed controls.

- Keep essential safety or separation rules in the main SOP, such as separating clinical-administrative systems from staff welfare or private-use systems.
- Move detailed cybersecurity, device, account, credential, incident, and technical parameter requirements into an appendix when they would overload the main procedure.
- State incident documentation requirements for data breach, lost device, unauthorized access, or similar events when the workflow creates data or network risk.

## Review Before Final Output

Before finishing a complete SOP, spawn a team of independent subagents to review clarity, structure, and readability when multi-agent tooling is available. Ask for reviews that focus on the SOP artifact, not on the expected answer.

Use three independent review lenses where feasible:

1. Clarity reviewer: identify ambiguous wording, undefined terms, long sentences, vague thresholds, and inconsistent translations.
2. Structure reviewer: verify the seven main sections, metadata, logical flow, subsection placement, procedure-to-appendix references, and language consistency.
3. Readability reviewer: check field usability for tired, multilingual, interrupted, time-pressured staff and suggest simplifications.

Also ask reviewers to flag apparent EMT-type scope violations and missing legal-operational evidence. Summarize the reviewers' suggested improvements for the user before presenting or finalizing the SOP. If subagents are unavailable, perform the three reviews yourself and clearly state that the review was not independent.

## Finalization Checklist

Before delivering a complete SOP, verify:

- The output is Markdown unless the user requested another format.
- The SOP language was specified by the user.
- The EMT type or approved capability package was specified by the user.
- All seven mandatory sections are present, translated consistently, and kept in canonical order.
- Required metadata is present or unresolved data is clearly requested.
- Critical actions are assigned to defined roles.
- New terms and roles are added to definitions or responsibilities.
- Appendices are named, ordered by first use, synchronized with file names, and referenced at the point of use.
- Detailed resource lists, technical controls, logs, checklists, contact templates, handover tools, and source-backed requirement tables are moved to appendices unless they are essential to the procedure hot path.
- Escalation paths are centralized in the escalation subsection and not duplicated across role descriptions, procedural steps, appendices, or handover text.
- Legal and regulatory requirements are mapped to operational implication, responsible role, and evidence when the SOP has workflow-specific legal requirements; if no SOP-specific legal controls apply, the SOP says so and references the baseline authorization or governance document if provided.
- The SOP does not exceed the specified EMT type or locally approved capability.
- Independent review findings have been summarized for the user.
