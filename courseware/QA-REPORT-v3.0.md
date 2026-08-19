# Courseware QA Report — v3.0

**Course:** Electrostatic Discharge (ESD) Control for Lab and Factory Engineers and Managers  
**Course code:** TGS-2024051412  
**QA date:** 19 August 2026  
**Overall pre-publication verdict:** PASS

## A. PowerPoint Quality Audit — PASS

- Final deck: 205 slides; version v3.0 appears once on the cover.
- Two separate visual trainer profiles are present.
- Course-material access and LMS download guidance use visual flow layouts.
- Assessment Flow maps attendance, WA, Case Study, LMS submission and sign-off.
- The end block is Assessment reminder → Assessment Flow → Digital Attendance → Thank You.
- No practice exam is included, as explicitly directed for this course.
- Independent rendered-slide review found no remaining critical/high visual defects.
- Automated bounds inspection found zero off-slide shapes.
- All 88 old-PPT picture instances are imported one-per-slide with source-slide provenance. Tall technical scans use readable zoom panels; three sideways tables are rotated upright.

## B. Assessment Quality Audit — PASS

- Instrument structure mirrors the live TMS assessment: four-question Written Assessment (SAQ) plus two-task Case Study.
- The Case Study instrument type was preserved.
- All questions/tasks are open-ended.
- Question papers use the required page order: cover on page 1, trainee instructions and grading on page 2, content from page 3.
- All four assessment DOCX files passed the structural verifier and rendered without clipping.
- Timings: WA 1 hour; Case Study 1 hour; open book.

| Criterion | Assessment item | Learning activity alignment |
|---|---|---|
| K1 | WA Question 1 | Activities 1–2; ESD fundamentals and failure triage |
| K2 | WA Question 2 | Activities 3–4; EPA controls and equipment selection |
| K3 | WA Question 3 | Activity 5; verification instruments and monitoring |
| K4 | WA Question 4 | Activities 6–8; audit, incident response and management controls |
| A1 | Case Study Task 1 | Activities 3–4; implement and justify control measures |
| A2 | Case Study Task 2 | Activities 5–7; monitor effectiveness and investigate evidence |
| A3 | Case Study Task 2 | Activities 6–8; recommend follow-up action and programme improvement |

## C. Lesson Plan — PASS

- WSQ cover, v3.0 version-control row and static page-numbered TOC are present.
- Activity and module slide references were generated from the final 205-slide map.
- The two-day schedule and two-hour assessment align with the deck and Learner Guide.

## D. Learner Guide — PASS

- WSQ cover, v3.0 version-control row and 118-entry static page-numbered TOC are present.
- All eight activities contain detailed procedures, scenario questions, evidence and acceptance criteria.
- Markdown, DOCX and PDF editions are present and aligned.

## E. Activities and Cross-Artifact Alignment — PASS

- Eight activities are stored in eight individual folders.
- Each folder contains README, scenario, worksheet, evidence and checklist Markdown files with same-basename PDFs.
- Markdown/PDF parity: 41/41.
- Activity 5 also includes simulated measurement data for analysis.

## F. Files and Distribution Boundary — PASS

- Current PPTX/PDF, LG DOCX/PDF/Markdown and LP DOCX/PDF are present.
- Assessment and answer-key files are excluded from GitHub.
- Reference PPT, build tooling, generated assets, QA renders and `.env` are excluded from GitHub.
- Assessment question papers are intended for learner-accessible Drive/LMS links; answer keys are trainer-only on Drive and never linked on LMS.

## Published-checklist note

The current published house page lists six assessment audit points, including the page-order check. Those six points were applied. Its generic practice-exam item was not applied because the course owner explicitly instructed that no practice exam be added.
