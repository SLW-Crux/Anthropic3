# Photonics & Enabling Supply Chain — PE Investment Research Prompts (v2)

## Purpose
A staged research programme to develop an evidence-backed, executable private equity investment thesis — not a general photonics market overview. Written for **Claude with web search**.

## Files (run in this order)

| File | Stage | Purpose |
|---|---|---|
| `00_MASTER_INSTRUCTIONS.md` | all | Mandate, scope, Fund Mandate block, evidence system, handoff template. Standing instructions for every session. |
| `01_EVIDENCE_AUDIT.md` | 1 | Triage all 100 sources, verify the 20–30 claims that matter, quantify the catalog's bias, define gaps. |
| `02A_VALUE_CHAIN_AND_DEMAND.md` | 2A | Value chain, end markets, architectures, adoption and demand scenarios. |
| `02B_SEGMENT_ECONOMICS.md` | 2B | Segment economics, profit pools and bottleneck durability. |
| `03_PE_OPPORTUNITIES.md` | 3 | Generate, screen and score competing PE theses; shortlist up to three. |
| `04_THESIS_UNDERWRITING.md` | 4 | Archetype models, break-even conditions, stress tests, exits. |
| `05_TARGETS_AND_EXECUTION.md` | 5 | Real company universe, tiered targets, origination, diligence and value creation. |
| `06_RED_TEAM_AND_IC.md` | 6A, 6B | Independent red team in a fresh session, then the final IC package. |

## Setup in Claude

1. Create a **Project**. Upload `00_MASTER_INSTRUCTIONS.md` to the project files (it is too long for the instructions box) and paste this into the project instructions:

   > Before doing anything in any chat, read the project file 00_MASTER_INSTRUCTIONS.md in full and follow it throughout. It sets the mandate, scope, Fund Mandate rules, evidence system and handoff template for this research programme. Begin each chat with the capability declaration it requires. If you cannot read that file, stop and say so.
2. Add the workbook `photonics_pe_evidence_review_100_2026-11-12.xlsx` to the project knowledge. **The workbook is not included in this ZIP.**
3. Turn on **web search** and **code execution / file creation** so Claude can read the workbook and produce CSV/XLSX ledgers and models. Use Research mode for the heavier stages (1, 2A, 2B, 5) if available.
4. The **Fund Mandate** table in the master instructions has target geography set: Asia Pacific, excluding China and any company with Chinese shareholding, manufacturing in China, or manufacturing with Chinese companies (joint ventures or Chinese contract manufacturers). "China" includes Hong Kong and Macau; Taiwan is in scope. Chinese customers and Chinese material or component suppliers are flagged but do not exclude a company; edit the geography rule if you intend otherwise. The master instructions also require every stage to examine the **manufacturing-partner opportunity**: Asia Pacific ex-China companies manufacturing European or US photonics solutions. Two further rules are set: **every level of the value chain is in scope** (materials, IP, manufacturing, distribution, services), and **no venture risk**, defined as an unproven market and/or unproven solution. Established businesses are investable, and so are minority stakes in new-build manufacturing companies where the market is proven and the solution is evidenced; technology developers themselves are never targets. The other rows are optional. Any row left as NOT PROVIDED is handled by presenting results across bands and listing the conclusions that depend on it; Claude is instructed not to invent a value.

## How to run

1. Start a **new chat for each stage**, set the model (see below), attach `00_MASTER_INSTRUCTIONS.md` to the first message and paste that stage's prompt.
2. Claude opens with a capability declaration. If it reports it cannot search the web or read the workbook, fix the settings before continuing.
3. A stage may take several responses. Reply `CONTINUE STAGE N` until Claude reports nothing remains.
4. Each stage ends with a **gate self-assessment** against the pass criteria in the prompt. Review it, check any "Partly met" or "Not met" items, and use `REVISE STAGE N` if needed.
5. Download the stage's files (ledgers, registers, models) and its **Stage Handoff**. Attach them to the next stage's chat, or add them to the project knowledge.
6. **Stage 6A must be independent.** Run it in a chat **outside the project** (so it cannot draw on earlier chats), attach the master instructions, paste the 6A prompt, and attach only the handoffs and files — no transcripts. Then review its objections before sending `ADVANCE TO STAGE 6B`.

## Which model to use

Set the model in the picker before sending each stage prompt. Fable 5.2 is used where judgement matters most; Sonnet 5.5 is enough elsewhere and uses less of your allowance. Do not use Haiku.

| Stage | Model |
|---|---|
| 1 — Tier 1 triage and sample check | Sonnet 5.5 |
| 1 — Tier 2 onwards (Claude pauses and says "TIER 1 COMPLETE – READY FOR TIER 2"; switch model, then send `CONTINUE STAGE 1`) | Fable 5.2 |
| 2A, 2B | Sonnet 5.5 |
| 3 | Fable 5.2 |
| 4 | Fable 5.2 |
| 5 | Sonnet 5.5 |
| 6A | Fable 5.2 |
| 6B | Sonnet 5.5 (or stay on Fable 5.2) |

## Operating guidance

- Do not ask Claude to run several stages at once.
- Spot-check citations yourself at each gate, especially anything graded A. URLs marked `(not retrieved)` were not opened by Claude.
- Source quality and evidence confidence are separate from investment attractiveness.
- Company valuations, ownership, transaction availability and financial performance must never be invented; expect and accept "Unknown".
- Models in Stage 4 describe an archetype, not a real company. Read the break-even conditions, not the point returns.
- Preserve negative evidence and rejected ideas between stages.

## Commands

- `CONTINUE STAGE N` — finish remaining work in that stage (N = 1, 2A, 2B, 3, 4, 5, 6A, 6B).
- `REVISE STAGE N` — revisit specified findings and regenerate the handoff.
- `ADVANCE TO STAGE N` — begin the next stage using the approved prior outputs.

## Changes from v1

1. **Fund Mandate block** added, with defined behaviour when parameters are not provided.
2. **Capability declaration** at the start of every session; unopened URLs are marked.
3. **One evidence system:** claim labels, verification levels V0–V4, grades A–D, and a mapping from the workbook's `Source class`.
4. **Stable ID scheme** for sources, claims, gaps, theses, kill criteria and companies.
5. **Stage 1 in two tiers:** light triage of all 100 rows, deep verification of the critical claims.
6. **Catalog bias** (publisher concentration, selection towards AI data-centre optics) is reported as a finding and corrected by new research.
7. **Stage 2 split** into 2A and 2B, each with its own gate.
8. **Scope defined**, broad through Stage 3, with non-communications end markets explicitly included.
9. **Rule for paywalled market research** quoted second-hand.
10. **Stage 3:** pass/fail screen, anchored 1–5 scoring rubric, five to eight candidates without padding.
11. **Stage 4:** tagged inputs, dated comparables, no-multiple-expansion case, break-even conditions, AI-capex-pause stress test.
12. **Stage 5:** sourced-or-Unknown rule, capped universe, evidence thresholds for target tiers.
13. **Stage 6 split:** independent red team (6A) in a fresh session, then the IC package (6B).
14. **Gate pass criteria** in every stage.
15. **Fixed handoff template** with a length cap; ledgers travel as files.
16. Workbook filename corrected; run instructions rewritten for Claude.
17. **Target geography set to Asia Pacific ex-China, with no Chinese shareholding and no manufacturing in China or with Chinese companies:** hard constraint on targets, a three-test China screen on every company in Stage 5, global analysis retained for demand, comparables and competitors, and the red team reports the cost of the constraint.
18. **Manufacturing-partner opportunity added:** Asia Pacific ex-China companies manufacturing European or US photonics solutions (contract, licence, joint venture or carved-out plant) is examined at every stage, must appear as a candidate thesis in Stage 3, and is challenged specifically by the red team.
19. **All value-chain levels and no venture capital:** scope names every level of participation including distribution and IP licensing; venture-stage companies are excluded as targets by a hard rule in the master instructions and the Stage 3 screen.
20. **Model guidance and setup fix:** each stage names its recommended model (Fable 5.2 or Sonnet 5.5); Stage 1 pauses between Tier 1 and Tier 2 for the model switch; the master instructions are uploaded as a file with a short pointer in the instructions box.
21. **Source logging rule:** every opened source is written to a log file immediately and work is saved in small batches, so that long chats do not lose source records.
22. **Venture rule redefined and new-build investments allowed:** "venture" now means an unproven market and/or solution. Minority stakes in new manufacturing companies in the region are permitted where the market is proven and the solution is evidenced; they are assessed as a separate class with their own tests in Stages 3 to 6A.
23. **China screen results refined:** carve-outs are tested on the business being acquired; a wholly owned China plant with no Chinese partner is recorded as "fails today – remediable", a second-tier result reported separately from passes.
24. **Cheque size set:** up to US$500m equity per investment, with a working ceiling of about US$1bn enterprise value for whole-company targets, to be confirmed.
