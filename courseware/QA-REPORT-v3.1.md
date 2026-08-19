# Courseware QA Report — v3.1

**Course:** Electrostatic Discharge (ESD) Control for Lab and Factory Engineers and Managers

**Course code:** TGS-2024051412

**QA date:** 20 August 2026

**Overall pre-publication verdict:** PASS

## A. PowerPoint Quality Audit — PASS

- Final deck: 129 slides, rebuilt in a logical sequence from electrostatic physics and discharge models through defects, reliability, prevention, standards, verification, auditing, incident response and management review.
- No standalone legacy-picture gallery, provenance page, corporate cartoon, QR/OTP image or other irrelevant legacy image remains.
- Four relevant legacy technical figures are retained only beside the concepts they explain: HBM, CDM, discharge-path/model comparison and device-level protection.
- Four photorealistic ESD workplace scenes are blended into the matching EPA, safe-handling, compliance-verification and incident-analysis lessons.
- Content explicitly covers HBM, legacy MM and CDM; catastrophic, latent and cumulative defects; device-level protection; EPA controls; grounding/bonding; personnel grounding; ionisation; shielding; packaging; qualification; verification; audit evidence; CAPA; and reliability metrics.
- Standards coverage identifies ANSI/ESD S20.20-2021 and IEC 61340-5-1:2024 while directing exact limits and methods to current controlled copies.
- Detailed step-by-step procedures do not appear in the slides; they are confined to the Learner Guide and activity packs.
- No practice exam is included, as explicitly directed for this course.
- Independent full-deck visual review passed after correction of two title clips and one wrist-strap contact ambiguity. Final review found no clipping, overlap, broken flow or strange standalone page.
- The PowerPoint structural validator passed all checks.

## B. Assessment Quality Audit — PASS

- Assessment structure mirrors the existing course instrument: four-question Written Assessment (SAQ) plus two-task Case Study; no practice examination was created.
- All questions and tasks are open-ended. Timings are one hour for the WA and one hour for the Case Study, open book.
- Candidate papers use the required sequence: cover, candidate instructions and grading, then questions/tasks.
- All four assessment DOCX files rendered without clipping, overflow or stray pages.
- Live Google Drive viewer checks confirmed correct cached page totals (`2 of 4` for WA, `2 of 5` and `5 of 5` for Case Study) and intact answer boxes; this closes the Google-viewer pagination risk that a PDF-only check cannot detect.

| Criterion | Assessment item | Coverage evidence |
|---|---|---|
| K1 | WA Question 1 | Charge generation, discharge paths, HBM/MM/CDM and defect consequences |
| K2 | WA Question 2 | ESD control-programme requirements and standards-based controls |
| K3 | WA Question 3 | Verification instruments, test discipline and defensible records |
| K4 | WA Question 4 | Prevention, competence, incident response and reliability improvement |
| A1 | Case Study Task 1 | Select, justify and implement control measures |
| A2 | Case Study Task 2 | Monitor effectiveness with evidence and defined indicators |
| A3 | Case Study Task 2 | Recommend follow-up action, CAPA and management decisions |

## C. Lesson Plan — PASS

- WSQ cover, v3.1 version-control row and populated static table of contents are present.
- The two-day schedule maps all four modules, eight activities and the two-hour assessment.
- Activity and module references are generated from the final 129-slide map.
- Final five-page render has no orphaned row or sparse spill page.

## D. Learner Guide — PASS

- WSQ cover, v3.1 version-control row and a 122-entry, page-numbered static table of contents are present.
- The guide follows the same four-module progression as the deck and expands each concept with decision takeaways and source alignment.
- All eight activities contain scenario, detailed step-by-step procedure, scenario questions, evidence requirements and acceptance criteria.
- Markdown, DOCX and 26-page PDF editions are present and aligned.

## E. Activities and Cross-Artifact Alignment — PASS

- Eight activities are stored in eight individual, self-contained folders.
- Each folder contains its own README, scenario, worksheet, evidence and checklist in Markdown and PDF; Activity 5 also contains simulated measurement data.
- Markdown/PDF parity is 41/41.
- Slide map, Learner Guide, Lesson Plan, activity numbering and assessment criteria are mutually aligned.

## F. Files and Distribution Boundary — PASS

- Current PPTX/PDF, Learner Guide DOCX/PDF/Markdown, Lesson Plan DOCX/PDF, activity packs, source coverage and asset register are present.
- Assessment papers and answer keys are stored in the private `assessment/` folder and excluded from GitHub.
- Candidate papers may be linked for learners; answer keys must remain trainer-only and must not be linked in LMS-TMS.
- Reference files, generated image assets, build tooling, QA renders, archives and `.env` are excluded from the public repository.

## Publication gate

The package may be published only after Drive folder identity verification, dry-run, upload readback, answer-key permission audit, LMS-TMS readback and local-to-remote Git SHA comparison.
