---
name: emt-sop-readability-review
description: Review Emergency Medical Team SOP readability for field usability by tired, multilingual, interrupted, and time-pressured staff. Use when Claude needs to calculate Flesch Reading Ease, identify hard-to-read SOP sections, and suggest clearer field-ready wording.
---

# EMT SOP Readability Review

## Core Contract

Review SOP readability for field usability. Focus on whether tired, multilingual, interrupted, time-pressured staff can scan and act on the SOP.

Use `scripts/flesch_reading_ease.py` when the user asks for Flesch Reading Ease (FRE), a readability score, or a quantitative readability check.

## FRE Script

Run:

```bash
python3 scripts/flesch_reading_ease.py path/to/sop.md
```

Or:

```bash
python3 scripts/flesch_reading_ease.py --text "Plain text to score."
```

The script uses only the Python standard library. It reports:

- Flesch Reading Ease score;
- sentence count;
- word count;
- syllable count;
- average sentence length;
- average syllables per word.

## FRE Interpretation

Treat an SOP as easy to read when its Flesch Reading Ease score is between `70.0` and `60.0` or above. This corresponds to plain English, normally understandable by 8th- and 9th-grade readers, or roughly 13- to 15-year-old students.

## Review Rules

- Use FRE as a signal, not a final judgment. SOPs with role names, acronyms, medicine names, or legal terms may score lower even when operationally clear.
- Flag long sentences, dense paragraphs, vague thresholds, passive voice in critical steps, and undefined acronyms.
- Prefer short action statements with responsible role, trigger, action, evidence, escalation path, and completion criterion.
- Suggest concrete simplifications, but do not remove legal, safety, scope, or evidence requirements.
