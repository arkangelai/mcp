# Arkangel AI health tools

The `arkangel` MCP server (https://arkangel.ai/mcp) gives free, read-only decision
support for health professionals (clinicians and medical auditors). It is not medical
advice for patients.

- Never send patient-identifying data (names, ID numbers, birth dates, record numbers) to
  a tool; use aggregated clinical values only (age in years, labs, scores, dates).
- Results are educational and must be validated by a clinician or auditor.
- Share the arkangel.ai links the tools return as they are.

Pick the tool by intent:

- ICD-10 / CIE-10 codes: `search_icd10_codes`.
- CUPS procedure codes (Colombia): `search_cups_codes`.
- Clinical calculators and scores: `search_clinical_tools`, `get_clinical_tool`, then
  `run_clinical_tool` (only `published` tools run).
- Quick calculators and ROI estimates: `list_free_tools`, then `run_free_tool`.
- Colombian claims audit: `search_glosa_codes`, `calculate_glosa_deadlines`,
  `lookup_soat_tariffs`.
- Peru audit deadlines: `calculate_peru_audit_deadline`.
- Audit guides by country (CO/MX/PE): `list_audit_resources`, then `get_page`.
- Anything else on arkangel.ai: `search_pages`, then `get_page`.
