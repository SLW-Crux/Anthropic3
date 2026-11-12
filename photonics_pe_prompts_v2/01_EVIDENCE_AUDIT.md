# Stage 1 — Evidence validation and research foundations

**Required context:** `00_MASTER_INSTRUCTIONS.md` and the original 100-source workbook. Start with the capability declaration.

**Recommended model:** Sonnet 5.5 for Tier 1 and the sample check; Fable 5.2 from Tier 2 onwards. You cannot change your own model, so the prompt includes a pause where the user switches.

## Mandate
Establish what the existing research actually demonstrates, what is repeated or promotional, what has not been verified, how the catalog itself is skewed, and what additional evidence a PE decision would need. **Do not propose or rank investment theses.**

The work has two tiers because verifying 100 articles in depth is neither feasible nor useful: most of the investment case will rest on a few dozen claims. Triage everything lightly; verify the important claims properly.

## Tier 1 — Triage all 100 rows
Build on the workbook's existing columns; do not re-create them. Add only:
1. **Duplicate family** — group rows that report the same underlying event or the same company narrative.
2. **Normalised segment** — the workbook's `Segment` column is free text with dozens of one-off values. Map each row to a short fixed taxonomy (about 10–14 value-chain segments, which you define and which Stage 2 will reuse) plus an **end-market tag**.
3. **Maturity of what is reported** — demonstration / prototype / design win / qualification / contracted / in production; or for deals, announced / agreed / closed.
4. **Verification level and grade** under the master evidence system. Checks inherited from the catalog are V1 unless you repeat them.
5. **PE relevance** — high / medium / low, with a one-line reason.
6. **Flag** — outdated, promotional, misleading date, unsupported assertion, or none.

Do not open all 100 links. Instead open a random sample of at least 10 rows to test whether the catalog's "Publisher page opened" and "Corroborating source" columns are reliable, and report the result.

Work in batches of 25 rows if needed, and continue until all 100 are done.

## Pause between tiers
When Tier 1 and the sample check are complete, save the Tier 1 ledger file, then stop and reply **"TIER 1 COMPLETE – READY FOR TIER 2"**, listing anything in Tier 1 that is unfinished or uncertain. Do not start Tier 2 until the user sends `CONTINUE STAGE 1`. The user will switch model at this point.

## Tier 2 — Deep verification of critical claims
1. Assemble the 20–30 claims most likely to change an investment conclusion (`C-001…`). Start with every row of the `Investment Evidence - Critical` sheet, then add the highest-consequence claims from Tier 1: commercial adoption, volumes, yield, capacity actually installed, pricing, completed acquisitions and their valuations, reported financial performance.
2. For each, open the best primary or independent source in this session and record: what the source actually says, verification level reached, grade, contradicting evidence found, and what remains unverified.
3. Where a claim cannot be verified, say so and name the source that would settle it.

## Catalog bias — report as findings
1. **Publisher concentration.** Compute the share of rows per publisher and per source class. State plainly how much of the catalog comes from trade press repeating company announcements, and what that means for its reliability.
2. **Selection bias.** Review the `Rejected and Replaced` sheet. Note any sources removed for being peripheral to one thesis rather than for quality, and what kinds of business the catalog under-covers as a result.
3. **Coverage map.** Rows by normalised segment, end market and **company geography**, showing where coverage is thin or absent relative to the master scope. In particular, state how many rows concern companies that could qualify under the Fund Mandate geography rule (Asia Pacific outside China), since the catalog may be weighted towards US and European names.

## Targeted new research
Run new research on the highest-impact gaps, prioritising (a) primary and independent sources for Tier 2 claims, (b) negative and counter-evidence, (c) end markets the catalog under-covers, (d) Asia Pacific ex-China photonics companies, clusters and transactions, (e) evidence for or against the manufacturing-partner opportunity — European and US photonics companies placing, moving or licensing production in Asia outside China, (f) completed PE and strategic transactions with disclosed terms. Record new sources as `N-…`, separately from the original 100. Aim for quality over volume; a few dozen well-chosen sources is enough at this stage.

## Required deliverables
A. **Workbook integrity and bias summary:** sheet structure, counts, date range, publisher and source-class concentration, selection bias, coverage map, sample-check result.

B. **Tier 1 ledger (file):** `S-ID`, the added columns above, and a corrective note where needed.

C. **Critical claims register (file plus summary table):** `C-ID`, claim, source IDs, what was checked, verification level, grade, contradicting evidence, implication for PE.

D. **Evidence gap register:** `G-ID`, question, importance, what exists, what is missing, best source or approach, blocking or not.

E. **New source list** (`N-…`) with grade and the gap each addresses.

F. **Stage 2 research agenda:** prioritised questions, and the segments and end markets that deserve deep work versus a light scan.

G. **Gate self-assessment and Stage Handoff.**

## Gate pass criteria
- All 100 rows triaged, with segment taxonomy and duplicate families assigned.
- Every row of the Critical sheet re-verified in this session, or marked not verifiable with a reason.
- At least 20 critical claims carry an explicit verification level and grade.
- Catalog bias quantified and its consequences stated, including coverage of Asia Pacific ex-China companies.
- Every gap marked blocking or non-blocking.
- No thesis has been proposed or ranked.

**Stop after Stage 1.**
