---
name: emt-sop-readability-review
description: Review Emergency Medical Team SOP readability for field usability by tired, multilingual, interrupted, and time-pressured staff. Use when Claude needs to calculate supported language-specific readability scores, identify hard-to-read SOP sections, and suggest clearer field-ready wording.
---

# EMT SOP Readability Review

## Core Contract

Review SOP readability for field usability. Focus on whether tired, multilingual, interrupted, time-pressured staff can scan and act on the SOP.

When the user asks for a readability score or quantitative readability check, first identify the SOP language. Use only the script for that language. If the SOP language is missing, mixed, or not listed below, do not run a scoring script because the result may be invalid; apply only the generic review rules.

## Language-Specific Scoring Scripts

| SOP language | Script | Algorithm | Score interpretation |
| --- | --- | --- | --- |
| English | `scripts/flesch_reading_ease.py` | Flesch Reading Ease | `0-100`; higher = easier. |
| German | `scripts/wiener_sachtextformel_1.py` | Wiener Sachtextformel 1 | `4-15`; lower = easier. `4-5` very easy, `6-7` easy, `8-10` average, `11-12` difficult, `13-15` very difficult. |
| Spanish | `scripts/flesch_szigriszt.py` | Flesch-Szigriszt / Indice de Perspicuidad | `0-100`; higher = easier. `<40` very difficult, `40-55` difficult, `55-65` normal, `65-80` easy, `>80` very easy. |
| Italian | `scripts/gulpease_index.py` | Gulpease Index | `0-100`; higher = easier. `<40` difficult for high-school readers, `<60` difficult for lower-secondary readers, `<80` difficult for elementary readers. |
| Polish | `scripts/jasnopis_readability.py` | Jasnopis readability class | `1-7`; lower = easier. `1` primary grades 1-3, `2` primary grades 4-6, `3` lower secondary, `4` high school, `5` undergraduate, `6` graduate, `7` expert. |
| French | `scripts/kandel_moles.py` | Kandel-Moles | `0-100`; higher = easier. `90-100` very easy, `60-70` standard, `30-50` difficult, `<30` very difficult. |

All scripts use only the Python standard library and accept the same interface:

Run:

```bash
python3 scripts/<script_name>.py path/to/sop.md
```

Or:

```bash
python3 scripts/<script_name>.py --text "Plain text to score."
```

Each script reports the algorithm score plus the input metrics needed for that formula, such as:

- sentence count;
- word count;
- syllable count;
- letter count, when required;
- average sentence length;
- average syllables per word;
- algorithm-specific percentages, when required.

## Script Selection Rules

- Use `scripts/flesch_reading_ease.py` only for English SOPs. Treat an English SOP as easy to read when its Flesch Reading Ease score is between `70.0` and `60.0` or above.
- Use `scripts/wiener_sachtextformel_1.py` only for German SOPs.
- Use `scripts/flesch_szigriszt.py` only for Spanish SOPs.
- Use `scripts/gulpease_index.py` only for Italian SOPs.
- Use `scripts/jasnopis_readability.py` only for Polish SOPs.
- Use `scripts/kandel_moles.py` only for French SOPs.
- If the SOP language is unsupported, unknown, or substantially mixed-language, state that no validated script is available for that language and do not calculate a score.
- Use quantitative scores as signals, not final judgments. Syllable counting is heuristic and can be affected by acronyms, medicine names, role names, local place names, and legal terms.

## Review Rules

- Flag long sentences, dense paragraphs, vague thresholds, passive voice in critical steps, and undefined acronyms.
- Prefer short action statements with responsible role, trigger, action, evidence, escalation path, and completion criterion.
- Suggest concrete simplifications, but do not remove legal, safety, scope, or evidence requirements.
