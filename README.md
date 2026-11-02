# Kogod AI Survey Analysis (2024–2026)

A team course project exploring AI adoption, reported academic uses, attitudes, and tool preferences across three years of student survey responses. The revised portfolio notebook focuses on the Kogod cohort and descriptive comparisons between usage groups.

## Research question

How does reported AI usage vary across survey years, and how do respondents with different usage frequencies differ in their reported behaviors and concerns?

## Team and provenance

Course project developed with **Natalie Cope, Victoria Smith, and Esha Teware** for ITEC-400 / 600. The source was a locally saved Deepnote export, `Final Notebook-1.ipynb`; this edition was revised with AI assistance for consistency, privacy, and reproducibility. The original file remains unchanged on the author's computer.

## What the notebook does

- Filters the combined survey file using the existing `is_kogod_major` indicator.
- Compares weekly usage distributions and the share reporting eight or more uses per week.
- Shows agreement-response distributions without imposing an unverified numeric Likert scale.
- Compares reported AI shortcut use, preferred tools, and tool-choice factors.
- Optionally summarizes precomputed LLM concern, desired-skill, and feedback-sentiment annotations when the separate annotation workbook is available.

User groups are consistent throughout: **Non-user = 0**, **Normal User = 1–7**, **Power User = 8+** uses/week. Missing usage remains Unknown and is excluded from usage-based comparisons. No inferential or causal claims are made.

## Run locally

Python 3.10+ is recommended. Install the notebook dependencies:

```sh
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open `kogod_ai_survey_analysis.ipynb`. Put an authorized copy of `cleaned_master_all_years.csv` in `data/`, or set `KOGOD_DATA_DIR` to its directory before launching Jupyter. The file must contain `year`, `usage_bucket`, `is_kogod_major`, the five agreement items, `ai_shortcut`, `model_favor`, `model_factor`, and `perplexity_usage`. The notebook validates required columns and expected usage categories.

The optional `AI_Survey_LLM_Analysis.xlsx` must have a `Full_Data` sheet with the same cohort/year/usage indicators, response-presence fields (`ai_concern_open`, `desire_ai_skill`, `perplexity_feedback`), binary concern/skill labels, and `perplexity_sentiment`. Optional schema checks are described in the notebook. Missing annotation files produce an explicit skip message.

## Data and privacy

**No respondent data, respondent previews, or saved cell outputs are distributed.** CSV/Excel inputs, local data, generated outputs, and environment files are ignored. Survey data require their own sharing authorization; this repository does not grant access to them. No real observations have been replaced with fabricated data.

## Interpretation

The original export called the study longitudinal. This edition uses **survey-year comparisons** because respondent linkage across years is not established. Changes can reflect different samples, nonresponse, or survey instruments. Respondents are not necessarily representative of all Kogod students. Numeric precomputed agreement scores are not reused because their coding merges response labels and a verified survey codebook is unavailable.

LLM annotations are supplied inputs; generation prompts, model details, and validation are not available. Theme percentages use nonmissing labels per theme; multi-label percentages need not sum to 100%. Missing sentiment labels and missing Yes/No answers are not treated as negative responses. The upstream cleaning pipeline and coding decisions cannot be reconstructed fully from the saved files.

## Verification

See `REVISION_NOTES.md` for the changes and exact verification scope. Data are intentionally excluded, so a fresh clone needs authorized inputs for execution. No team-wide reuse license has been assigned.
