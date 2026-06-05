---
description: Generate, revise, and quality-check Standard Operating Procedures for WHO Emergency Medical Teams of any EMT type, including Type 1 Mobile, Type 1 Fixed, Type 2, Type 3, and specialist care teams or cells. Use when Claude needs to draft field-ready EMT SOPs, adapt SOP content to mission data and team capability, ask for missing required SOP inputs, enforce mandatory SOP sections in the requested output language, maintain defined terms and roles, enforce EMT capability limits from user-provided team scope, or review SOP clarity, structure, readability, legal-operational mapping, and scope boundaries.
---

# EMT SOP Generator

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

Read `references/emt_sop_ai_agent_knowledge_base.md` before drafting, revising, or reviewing a complete SOP. Use it for generic EMT SOP architecture, required metadata, language-independent section definitions, writing rules, evidence artifacts, escalation logic, legal-operational mapping, and validation.

For the requested EMT type, ask the user for the team's official capability statement, approved scope, exclusions, staffing model, deployment configuration, and any local authorization that changes the baseline EMT type capability.

For narrow edits to an existing SOP, read only the relevant reference sections when possible. Useful search headings include:

- `Canonical SOP sections`
- `Intake data set`
- `Procedure step template`
- `Evidence-of-action rule`
- `Legal-operational rule`
- `Validation checklist`
- `EMT type and capability controls`

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

Keep every SOP within the approved capability of the specified EMT type. Do not authorize clinical services, procedures, admissions, diagnostics, surgeries, critical care, blood products, specialist care, transport, or public-health functions unless they are inside the team type, specialist cell mandate, or locally approved scope provided by the user.

Use role-bound, evidence-backed instructions:

- Put the responsible role before each safety-critical action.
- Define the trigger, action, output or evidence, form or appendix, escalation path, and completion criterion for each critical workflow.
- Use numbered steps in `Procedure description`.
- Use `If...then...` decision logic for thresholds and exceptions.
- Use `Do not...unless...` for safety boundaries.
- Use tables for role ownership, legal matrices, forms, escalation thresholds, and appendices.
- Avoid vague terms such as `appropriate staff`, `if necessary`, `regularly`, or `according to local procedures` unless the role, threshold, frequency, authority, or source is named.

## Terms And Roles Discipline

Maintain unambiguous vocabulary throughout the SOP.

- Define every acronym, role, locally binding term, patient category, report name, authority, coordination body, form, and operational status that affects action, safety, interpretation, reporting, or legal compliance.
- Reference defined terms and role names exactly as written in `Terms and definitions` and `Roles and responsibilities`, translated consistently into the SOP language.
- If a new term, acronym, authority, form, or role appears while drafting a later section, add it to the appropriate definitions or roles section before finalizing.
- Do not use informal synonyms for defined roles. For example, if `Clinical Lead` is defined, keep using `Clinical Lead`; do not switch to `clinical supervisor`, `medical lead`, or `lead doctor` unless those are separately defined.

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
- Appendices are named and referenced where used.
- Legal and regulatory requirements are mapped to operational implication, responsible role, and evidence when the SOP has workflow-specific legal requirements.
- The SOP does not exceed the specified EMT type or locally approved capability.
- Independent review findings have been summarized for the user.
