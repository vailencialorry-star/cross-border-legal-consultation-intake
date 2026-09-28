---
name: cross-border-legal-consultation-intake
description: Classify and restructure all legal questions in a client brief or Word/PDF document, then produce a lawyer-style preliminary cross-border legal and tax consultation report with China-law sections, jurisdiction research, issue matrices, go/no-go decisions, and a source-to-output coverage index. Use when a user provides a transaction, platform, marketplace, logistics, warehouse, payment, tax, customs, AML, data, or multi-jurisdiction business brief and asks to classify legal issues, prepare consultation questions, identify workstreams, or give preliminary advice under Chinese law and foreign/treaty rules.
---

# Cross-Border Legal Consultation Intake

## Purpose

Turn an unstructured client brief into a complete, traceable legal work plan and preliminary research memorandum. Preserve every original question, separate legal domains and jurisdictions, research current official authorities, and convert abstract legal risks into product, contract, system, document, and licensing actions.

This skill prepares an **intake and preliminary research deliverable**, not a formal local-law opinion. State this boundary in the report.

## Required companion skills

Before planning, read and follow:

1. `/home/ubuntu/skills/legal-expert/SKILL.md` for legal reasoning, source authority, and risk assessment.
2. `/home/ubuntu/skills/technical-writing/SKILL.md` for report structure and citations.
3. `/home/ubuntu/skills/deep-research/SKILL.md` when the user requests current law, treaties, or substantive preliminary advice.
4. `/home/ubuntu/skills/workflow-composer/SKILL.md` when researching three or more independent jurisdictions or comparable legal workstreams.

## Inputs and default outputs

Accept `.docx`, `.pdf`, `.md`, `.txt`, or pasted text. Read the entire source, including appendices and tables.

Default outputs:

- A complete Markdown report.
- A `.docx` version when the source is Word, the document is client-facing, or the user requests Word.
- No PDF unless requested.

Use the report skeleton in `templates/legal-consultation-report-template.md`. Adapt section names to the transaction, but retain traceability, preliminary advice, a decision matrix, and a source index.

## Workflow

### Step 1 — Extract every proposed consultation item

Read the source once in full. If extraction is truncated, read the saved text extraction or remaining page ranges before analysis.

Create an internal **coverage ledger** with these fields:

| Field | Required content |
|---|---|
| Source location | Section, page, paragraph, bullet, or question number |
| Original issue | Faithful short restatement; do not change legal substance |
| Facts/premises | Business facts assumed by the question |
| Jurisdiction | China, foreign state, international/treaty, or multiple |
| Legal domain | Contract/property, tax, customs, licensing, payment, AML, criminal, data, consumer, dispute, etc. |
| Normalized issue ID | Stable code used in the report |
| Duplicate/linked issues | Other source questions that overlap or depend on it |

Do not draft conclusions until all questions have been captured. Merge duplication only after preserving the original source references.

### Step 2 — Build the issue architecture

Read `references/classification-framework.md` and classify the ledger. Use six default workstreams unless the facts justify a different structure:

1. Transaction structure, contract, title, platform and warehouse roles.
2. China tax, customs, import and invoice compliance.
3. Criminal compliance, AML, payments and foreign exchange.
4. Foreign-jurisdiction operations, licensing, local tax and customs.
5. Identity, data protection and evidence chain.
6. Group structure, treaties, conflict of laws and dispute resolution.

Separate concepts that are often wrongly combined:

- Contract obligations vs. proprietary title/possession.
- Platform service provider vs. agent vs. principal/seller.
- Taxable supply vs. physical import/export.
- PSP obligations vs. platform obligations.
- Statutory AML duties vs. prudent risk controls.
- Platform suspension vs. PSP freeze vs. warehouse lien vs. official seizure.
- Personal-use import vs. e-commerce retail import vs. commercial import.

Assign priorities:

- **P0:** blocks launch or creates material criminal, licensing, customs, client-money, or title risk.
- **P1:** must be resolved before scale, local operation, or higher-risk functions.
- **P2:** optimization, future product, or governance issue.

### Step 3 — Plan jurisdiction research

Read `references/research-protocol.md` before legal research.

For three or more jurisdictions, use `workflow/run` with:

- One agent per jurisdiction.
- One separate agent for conflict rules, treaties, and cross-border execution.
- Shared structured output fields: bottom line, issue matrix, authorities, application, risk, actions, unresolved items, and source URLs.
- One reducer agent for comparative synthesis.

Give every researcher the full transaction facts and source document. Require official or first-party sources and a current-law note. Do not let researchers treat search snippets, legal blogs, or machine translations as conclusive law.

### Step 4 — Research in the correct legal order

Analyze each transaction path in this order:

1. **Actors and roles:** actual seller, buyer, platform, agent, warehouse/bailee, PSP, carrier, exporter, importer/IOR, tax invoice issuer.
2. **Contract and title:** contract formation, governing law, title transfer, possession/delivery, third-party effectiveness, insolvency and seizure.
3. **Licensing and conduct:** platform, telecom/e-commerce, auction, secondhand goods, warehouse, payment, consumer and advertising rules.
4. **Tax and invoice:** revenue principal/agent, VAT/GST/consumption tax, income tax, barter valuation, invoice/credit note, reporting.
5. **Customs:** personal vs. commercial route, classification, valuation, origin, permits, importer/exporter and evidence.
6. **AML and criminal:** legal status, CDD/STR, suspicious-property rules, proceeds of crime, stolen goods, sanctions, tipping-off, customs and invoice offences.
7. **Data and evidence:** KYC/KYB, cross-border transfer, retention, electronic signatures, immutable audit trail.
8. **Treaties and disputes:** conflict of laws, CISG, customs/origin agreement, tax treaty/PE, arbitration and enforcement.

For every conclusion, distinguish:

- Current rule.
- Application to stated facts.
- Risk level.
- Operational action.
- Assumption or unresolved fact.
- Local opinion, ruling, licence, or regulator/PSP confirmation still required.

### Step 5 — Convert research into actionable advice

Use three decision labels:

- **Launchable:** legally supportable under the stated minimum controls.
- **Conditionally launchable:** permitted only after specified documents, licences, local opinions, or system controls.
- **Defer / prohibit:** do not offer until a material blocker is removed, or never offer in the proposed form.

Avoid vague endings such as “may involve” or “consult a lawyer.” If uncertainty remains, name the exact decision-maker and requested deliverable, for example:

- Customs classification or valuation ruling for a representative sample.
- Local property-law opinion on warehouse attornment and insolvency effectiveness.
- PSP written confirmation of merchant, countries, currencies, settlement, reserve, refund and freeze scope.
- Tax adviser principal/agent and invoice matrix.
- Data transfer impact assessment and recipient agreement.

Translate legal conclusions into:

- Product rules and prohibited functions.
- Contract clauses and agreement stack.
- Identity and document requirements.
- Manual-review and escalation rules.
- Required licence or filing.
- Evidence and retention fields.
- External confirmation gates.

### Step 6 — Draft the report

Follow `templates/legal-consultation-report-template.md`. Include at minimum:

1. Scope, assumptions, date, and preliminary-opinion disclaimer.
2. Executive summary.
3. Consolidated workstream table with priority and responsible adviser.
4. Reclassified issue list with stable issue IDs and original source mapping.
5. China-law sections covering tax, contract/property, criminal and AML/payment compliance when relevant.
6. Foreign and treaty preliminary advice.
7. Route Legal Matrix or equivalent path matrix.
8. Launchable / Conditional / Defer-Prohibit table.
9. Standard launch path that can become product rules and contract flow.
10. Recommended external written opinions in priority order.
11. Missing facts.
12. Full source-coverage index.
13. Numeric reference list using official sources.

Use complete paragraphs for analysis and tables for comparisons. Clearly label preliminary and jurisdiction-limited conclusions. Never state that an overseas lawyer opinion, customs ruling, licence, tax treatment, or PSP approval exists unless verified.

### Step 7 — Validate and deliver

Read `references/quality-checklist.md` and complete every applicable check.

At minimum verify:

- Every source question maps to at least one normalized issue or report section.
- Every conclusion identifies jurisdiction and legal domain.
- Every numeric citation has one matching reference definition.
- Official sources have been opened, not merely found in snippets.
- Effective dates and amendments are addressed.
- Contract, title, tax, customs, payment, AML, criminal, data and treaty issues are not conflated.
- Go/no-go decisions state conditions and reasons.
- The Markdown file exists and is complete.
- Any generated Word file opens, renders Chinese text, and contains the full report.

When converting Markdown to Word, use `pandoc --from=gfm --to=docx --toc --toc-depth=3` when available. Visually inspect several opening pages and extract the Word text to confirm completeness.

## Guardrails

- Do not give a formal local-law opinion while lacking final facts, engagement, or local counsel review.
- Do not call an operational preference a statutory rule.
- Do not assume a third-party PSP's licence covers the proposed platform flow.
- Do not treat a platform ledger as a statutory title register.
- Do not treat a tax treaty as eliminating VAT/GST, customs, licensing, data, payment, or consumer rules.
- Do not assume storage, grading, resale, or export country creates origin under a trade agreement.
- Do not recommend grey customs clearance, false declarations, personal-use disguises, invoice fabrication, transaction splitting, wallet workarounds, or AML evasion.
- Do not omit apparently repetitive questions; preserve them in the coverage index.

## Resource navigation

- Read `references/classification-framework.md` when normalizing and coding issues.
- Read `references/research-protocol.md` before multi-jurisdiction research or treaty analysis.
- Read `references/quality-checklist.md` before finalizing any deliverable.
- Copy and adapt `templates/legal-consultation-report-template.md` for the report.
