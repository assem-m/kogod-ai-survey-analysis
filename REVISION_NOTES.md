# Revision and verification notes

Portfolio revision prepared November 2, 2026 from the local `Final Notebook-1.ipynb` export. The original is unchanged.

## Revisions

- Credited the project collaborators.
- Changed longitudinal claims to comparisons across survey years because linked participants are not established.
- Used one combined input and the explicit Kogod cohort indicator instead of several missing or ambiguously named CSV files.
- Unified usage groups from reported frequency: 0, 1–7, and 8+; missing remains Unknown.
- Replaced unverified numeric Likert means with labeled response distributions. No numeric remapping was invented.
- Excluded missing Yes/No responses from denominators and reported missing Perplexity usage separately.
- Replaced duplicated qualitative cells with an optional validated annotation section. Themes use nonmissing labels per theme; sentiment uses labeled feedback and reports coverage.
- Removed unused statistical-test imports and unsupported testing claims.
- Removed all stored cell outputs and platform metadata; did not include survey files or respondent-level examples.
- Added setup instructions, input checks, and limitations. No new empirical findings or causal claims were introduced.

## Verification completed

- Executed all 20 code cells sequentially using the local combined survey file and the installed Anaconda Python environment, with chart display redirected to a noninteractive backend. The file contained 609 records, including 491 marked Kogod records; only aggregate counts were inspected.
- Confirmed zero-use and missing-use cases remain distinct from Normal Users.
- Confirmed usage-group classification and that agreement and shortcut percentage distributions sum to 100% where responses exist.
- Validated the Jupyter notebook schema, Python syntax, and absence of saved cell outputs.
- Exercised the optional annotation branch using temporary synthetic validation fixtures, including missing theme/sentiment labels and rejection of nonbinary theme values. These fixtures were not added to the repository.

## Limits

The real annotation workbook is unavailable, so its schema, labels, and empirical qualitative results have not been verified. Survey instrument equivalence, prior cleaning decisions, participant linkage remain undocumented. The published notebook is intentionally output-free and requires authorized local data to reproduce results.
