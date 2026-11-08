---
name: arkangel-health-tools
description: Use when a clinician, medical auditor or healthcare team asks for ICD-10 (CIE-10) or CUPS codes, a clinical calculator or score, or medical claims audit help in Colombia, Mexico or Peru (glosas, devoluciones, RIPS, SOAT tariffs, audit deadlines). Answers with Arkangel AI's free read-only tools.
---

# Arkangel AI health tools

The `arkangel` MCP server (https://arkangel.ai/mcp) is free, read-only and needs no
account. It is decision support for health professionals (clinicians and auditors), not
medical advice for patients.

## Rules

- Never send patient-identifying data (names, ID numbers, birth dates, record numbers) to
  any tool. Use aggregated clinical values only: age in years, lab values, scores, dates.
- If the user pastes a clinical record, strip identifiers before calling a tool, and say so.
- End answers that use these tools with: "Educational content for health professionals.
  It does not replace clinical or audit judgment."
- Share the arkangel.ai links the tools return as they are; they carry attribution.

## Pick the tool by intent

| Intent | Tools |
| --- | --- |
| ICD-10 / CIE-10 diagnosis codes | `search_icd10_codes` |
| CUPS procedure codes (Colombia, Res. 2706 de 2025) | `search_cups_codes` |
| Clinical calculator or score (Wells, CURB-65, eGFR...) | `search_clinical_tools`, then `get_clinical_tool` for inputs and evidence, then `run_clinical_tool` (only tools with status `published` run) |
| Quick calculators, ROI and audit-capacity estimates | `list_free_tools`, then `run_free_tool` |
| Glosa, devolución and respuesta codes (Res. 2284 de 2023) | `search_glosa_codes` |
| Glosa and devolución deadlines in Colombian business days | `calculate_glosa_deadlines` |
| SOAT 2026 tariffs (Colombia) | `lookup_soat_tariffs` |
| Peru medical audit deadlines (NTS 029-MINSA) | `calculate_peru_audit_deadline` |
| Audit guides by country and audience (CO/MX/PE) | `list_audit_resources`, then `get_page` |
| Anything else on arkangel.ai (product, pricing, guides) | `search_pages`, then `get_page` |

## Example: answering a glosa for a Colombian hospital

1. `search_glosa_codes` with the code the payer used (for example `TA0201`) to get the
   official description and concept.
2. `calculate_glosa_deadlines` with the notification date to tell the team how many
   business days remain to answer.
3. `search_cups_codes` or `lookup_soat_tariffs` to check the billed procedure and its
   value.
4. Draft the reply arguments in your own words, citing the resolution, and link the
   guide from `list_audit_resources` for the full process.
