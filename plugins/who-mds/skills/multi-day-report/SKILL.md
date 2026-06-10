---
name: multi-day-report
description: Generate and review multi-day WHO Emergency Medical Team Minimum Data Set (MDS) periodic reports from daily MDS CSV exports. Use when Claude needs to aggregate WHO EMT MDS files across several days or facilities, calculate MDS totals and trends, render the bundled A4 HTML periodic report template, prepare restricted-trigger summaries, or explain data quality issues in MDS report inputs.
---

# WHO MDS Multi-Day Report

## Core Contract

Generate multi-day WHO EMT Minimum Data Set periodic reports from one or more daily MDS CSV exports. Keep the main report aggregated. Do not include patient identifiers, clinical narratives, or protection details in the public report. Restricted-trigger details may appear only in a separate restricted appendix.

## Reference Loading

Read `references/who_emt_mds_periodic_report_structure.md` before changing report structure, page order, placeholder behavior, confidentiality handling, or MDS calculation rules.

Use `assets/html-report-templates/` as the canonical HTML template asset. The templates use Mustache-style placeholders and A4 portrait print styling.

## Generator Script

Use `scripts/generate_multi_day_report.py` for deterministic CSV aggregation and HTML rendering.

Run:

```bash
python scripts/generate_multi_day_report.py <csv-file-or-directory> --output report.html
```

Useful options:

```bash
python scripts/generate_multi_day_report.py <input> \
  --start-date 2024-05-07 \
  --end-date 2024-05-14 \
  --organization "Polish Medical Mission" \
  --team-name "PMM EMT" \
  --emt-type "Type 1 Fixed" \
  --output public-report.html \
  --restricted-output restricted-appendix.html
```

The script accepts multiple CSV files and directories. Directories are scanned recursively for `*.csv`.

## Workflow

1. Confirm the requested reporting period, organization/team name, EMT type, and whether a restricted appendix is authorized.
2. Run the generator on the provided CSV files or directory.
3. Validate the public report: check for unresolved `{{placeholder}}` markers, unexpected missing dates, unintended multiple-facility aggregation, data-quality warnings, and public exposure of restricted details.
4. If validation fails, fix the cause before finalizing: correct source file selection or date range, add missing metadata overrides, repair template placeholders, or adjust source data handling. Re-run the generator and repeat validation until the report is internally consistent or the remaining limitation is explicitly documented.
5. If restricted triggers exist, generate or advise creating the restricted appendix separately and share it only through the locally approved confidential pathway.
6. When editing the template manually, preserve the page order and confidentiality rules from the reference structure.

## Calculation Rules

- Treat each CSV row as one consultation unless the user provides a different official aggregation rule.
- Use `h` as the activity date when available.
- Use `MDSa`, `Age`, and `M/Y` to derive age group and under-5 or 5-plus totals.
- Use `MDS1-3` as the sex category: `1` male, `2` female non-pregnant, `3` female pregnant.
- Treat `MDS4` through `MDS65` as binary checkbox-style fields. Values of `1`, `true`, `yes`, `y`, or `x` count as selected.
- For MDS4-MDS35, calculate under-5 and 5-plus counts when age can be derived.
- For MDS36-MDS65, calculate total counts and percentages against consultations when appropriate.
- Use source metadata fields `a`, `b`, `d`, `e`, `f`, `g`, `h`, `i`, `j`, `k`, `l`, `m`, `n`, `ToolVer`, and `Ver` when available.

## Output Rules

- Use exact numbers for all calculated values.
- Mark missing required source fields as `Field not available in source data.`
- Mark empty standard sections as `No data available for the selected reporting period.`
- Do not infer epidemiological conclusions beyond calculated values.
- Keep protection indicators and restricted triggers aggregated in the public report.
