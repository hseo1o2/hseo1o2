<div align="center">

# Jang Hyeonseo

### AI & Backend Engineer

**Document Intelligence · Financial Data Agents · Production Backend Systems**

I build systems that turn unstructured documents and operational data into
traceable decisions—and make those systems reliable enough to run in production.

[![Email](https://img.shields.io/badge/Email-0102jhshs%40ewha.ac.kr-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:0102jhshs@ewha.ac.kr)
[![GitHub](https://img.shields.io/badge/GitHub-hseo1o2-181717?style=flat-square&logo=github)](https://github.com/hseo1o2)

</div>

## About

- Computer Science student at Ewha Womans University
- 1st Place, Upstage AI Workflow Hackathon
- Interested in document intelligence, evidence-grounded agents, multimodal AI, and production backend engineering
- UMC 9th President · UNIS 7th President

## Selected Work

### [gongsiri — Financial Disclosure Risk Agent](https://github.com/GoBeromsu/gongsiri)

Built the AI risk-analysis layer for an agent that interprets corporate disclosures
and answers questions against collected evidence.

- Replaced a placeholder text-composition flow with a production-oriented **Solar Pro risk-analysis engine**
- Designed a two-stage analysis path: quantitative disclosure checks followed by contextual LLM interpretation
- Added evidence-grounded Q&A, structured risk explanations, JSON recovery, and graceful fallback that preserves deterministic results when the model fails
- Extended the analyzer into a deployable service with frontend and cloud deployment configuration

Evidence: [Solar risk engine PR #14](https://github.com/GoBeromsu/gongsiri/pull/14) · [Authored PRs](https://github.com/GoBeromsu/gongsiri/pulls?q=is%3Apr+author%3Ahseo1o2)

### [PitchCoach — Document & Multimodal AI Coaching](https://github.com/Capstone-POKI/Pitchcoach-AI)

Led the AI pipeline and backend integration for a service that analyzes program
notices, IR decks, rehearsal audio, and Q&A responses.

- Stabilized a **Document AI → Gemini structured extraction** pipeline and implemented evidence-aware fallback rules for evaluation criteria and scoring
- Connected notice requirements to IR-deck analysis, adding slide classification, OCR cleanup, criterion-level scores, explanations, and report generation
- Built FastAPI flows for asynchronous deck analysis, Whisper-based rehearsal analysis, and Gemini-based Q&A evaluation
- Implemented the NestJS integration layer for AI job polling, result persistence, version comparison, failure states, authentication, and EC2/Docker deployment

Evidence: [Document pipeline #9](https://github.com/Capstone-POKI/Pitchcoach-AI/pull/9) · [IR analysis #19](https://github.com/Capstone-POKI/Pitchcoach-AI/pull/19) · [Voice analysis #21](https://github.com/Capstone-POKI/Pitchcoach-AI/pull/21) · [Backend AI sync #12](https://github.com/Capstone-POKI/Pitchcoach-BACK/pull/12)

### [IDly — AI Email Security Backend](https://github.com/IDlyProject/IDly-Back)

Owned major parts of the backend flow from Gmail ingestion and AI analysis to
security actions and production stabilization.

- Implemented consent-aware Gmail onboarding, analysis persistence, evidence deduplication, and Solar-powered security reports
- Designed a deterministic **Action Assistant state machine** where the LLM explains actions but cannot invent official URLs, change risk levels, or mark actions complete
- Hardened authentication and privacy with refresh-token rotation, ownership checks, rate limits, secret detection, log redaction, and LLM-context masking
- Reworked large-mailbox ingestion into disk streaming and added retry, cooldown, memory caps, and schema validation to prevent production OOM and overlapping analysis

Evidence: [Core backend flow #3](https://github.com/IDlyProject/IDly-Back/pull/3) · [Action Assistant #11](https://github.com/IDlyProject/IDly-Back/pull/11) · [Security hardening #18](https://github.com/IDlyProject/IDly-Back/pull/18) · [Streaming OOM fix #29](https://github.com/IDlyProject/IDly-Back/pull/29) · [Stability & AI mapping #45](https://github.com/IDlyProject/IDly-Back/pull/45)

### [Enterprise Due Diligence — Data-Grounded BI Agent](https://github.com/1eehvunzin/dive2026)

Built a data-contract-first backend for company due diligence, candidate
comparison, and evidence-grounded decision support.

- Combined financial, employment, patent, NTIS, support-history, and industry benchmark data for **2,886 companies**
- Prevented time leakage, separated missing values from zero, normalized units, and replaced random similarity with cohort-based distance
- Built a **Document Parse → Solar Pro** pipeline that extracts program requirements with source pages, original text, and review status
- Restricted agent answers to report fields and evidence IDs; added regression checks for generated-score errors and historical-data leakage

Evidence: [Backend & data contracts #1](https://github.com/1eehvunzin/dive2026/pull/1) · [Due-diligence report refinement #2](https://github.com/1eehvunzin/dive2026/pull/2)

### [upstage-research-cli — Research-to-Evaluation CLI](https://github.com/hseo1o2/upstage-research-cli)

Created a CLI that turns AI research papers into reusable implementation and
evaluation workflows.

- Parses papers with Upstage Document Parse and identifies reproducible method components
- Generates evaluation code and normalized metric definitions from paper evidence
- Packages the workflow as reusable Agent Skills with regression fixtures and structured outputs

### [LOOPy — Location-Based Challenge & Stamp Backend](https://github.com/Organization-LOOPy/LOOPy-BE)

Served as a core backend contributor for the challenge, stamp, notification, and
deployment flows of a location-based cafe service.

- Implemented and evolved challenge participation, stamp books, history, redemption, phone/QR accumulation, and owner/admin operations
- Refactored large controllers into domain services and shared validation/date utilities while preserving frontend response contracts
- Tightened cafe-search filters and notification authorization around ownership and user opt-in settings
- Unified deployment on Docker Compose, removed port conflicts, and made CI fail when the production deployment actually fails

Evidence: [Challenge domain #20](https://github.com/Organization-LOOPy/LOOPy-BE/pull/20) · [Stamp domain #66](https://github.com/Organization-LOOPy/LOOPy-BE/pull/66) · [Domain refactor #282](https://github.com/Organization-LOOPy/LOOPy-BE/pull/282) · [Deployment stability #299](https://github.com/Organization-LOOPy/LOOPy-BE/pull/299)

## Engineering Focus

| Area | Experience |
|---|---|
| AI & LLM | Document intelligence, structured extraction, RAG, evidence-grounded agents, Gemini, Upstage Solar, Whisper |
| Backend | Python, FastAPI, TypeScript, NestJS, Express, REST API design, asynchronous jobs |
| Data | PostgreSQL, Prisma, SQLite, schema design, data validation, leakage prevention, evaluation datasets |
| Production | Docker, GitHub Actions, AWS EC2/S3, Render, retries, observability, memory and failure handling |

## How I Work

I care about the boundary between an AI model and the surrounding software:
what must remain deterministic, what evidence should be retained, how failures
degrade safely, and how an experimental pipeline becomes an operable product.
