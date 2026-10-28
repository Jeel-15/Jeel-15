# RESUME_PROJECTS

**Generated on:** October 28, 2026

## Executive Summary
After reviewing repository structure, implementation files, and configs (not just repo names), the strongest resume-ready work appears to be:
1. **Eyenosis (Laravel HMS SaaS)** for large multi-tenant product scope and backend architecture depth.
2. **eye_care_tab (Flutter)** for broad mobile/tablet product implementation across many modules.
3. **vyaparAI (FastAPI + AI platform)** for ambitious AI-enabled platform architecture and domain modeling.
4. **report_generation (Flask + MongoDB)** for practical production-style APIs, auth, and report workflow logic.
5. **AI-Mock-Interview (Next.js + Django + LangChain/Whisper)** for applied LLM product integration.

These five provide the best balance of scope, technical depth, and interview value.

---

## Ranked Shortlist (Top Resume Candidates)

| Rank | Project | Why included | Confidence / evidence note |
|---|---|---|---|
| 1 | **Eyenosis** ([repo](https://github.com/Jeel-15/eyenosis)) | Large Laravel SaaS codebase with platform/superadmin/hospital flows, rich routing, and many controllers/services. | **High** — strong evidence in `routes/web.php`, `app/Http/Controllers/SuperAdmin/*`, `Platform/RegisterController.php`, and dependency/config files. |
| 2 | **eye_care_tab** ([repo](https://github.com/Jeel-15/eye_care_tab)) | Very broad Flutter implementation with many screens/services indicating real product scale. | **High** — `lib/screens/*` and `lib/services/*` are extensive; auth/session logic is detailed in `auth_service.dart`. |
| 3 | **vyaparAI** ([repo](https://github.com/Jeel-15/vyaparAI)) | Multi-module FastAPI platform with RBAC, marketplace, rentals, health/readiness, and vector-index bootstrapping. | **Medium-High** — rich implementation in `src/ai_platform/*`; README is empty, so confidence relies on code structure and files. |
| 4 | **report_generation** ([repo](https://github.com/Jeel-15/report_generation)) | End-to-end Flask backend with JWT auth, role-based routes, report workflows, and MongoEngine models. | **Medium-High** — strong route-level implementation; repository hygiene is mixed (committed `.env`/venv artifacts). |
| 5 | **AI-Mock-Interview** ([repo](https://github.com/Jeel-15/AI-Mock-Interview)) | Full-stack AI app combining interview simulation, LLM chains, and speech transcription. | **Medium** — meaningful implementation exists, but some architecture/quality concerns (heavy view logic, model loading patterns). |

---

## Detailed Project Notes (Resume-Ready)

## 1) Eyenosis — Multi-Tenant Eye Hospital SaaS Platform
- **Repository:** https://github.com/Jeel-15/eyenosis
- **One-line impact summary:** Built a multi-tenant hospital SaaS platform with public onboarding, superadmin governance, and hospital operations routing.
- **Problem/domain:** Healthcare operations + SaaS tenant lifecycle management.

### Major implemented features
- Public registration, pricing, slug/code validation, and onboarding flows.
- Superadmin module for tenant lifecycle (approve/reject/activate/suspend/extend/reseed).
- Master-data and platform management routes (locations, medicines, diagnosis, subscriptions, payments, notifications, audit logs).
- Path-based hospital routing design (`/{slug}` strategy).

### Architecture / data flow
- Laravel MVC app with route groups for public and superadmin concerns.
- Controller-driven orchestration using services (e.g., `TenantService`, `PlatformPricingService`).
- Validation-heavy request handling and audit logging patterns in superadmin flows.

### Technology stack
- PHP 8.3, Laravel 13, Sanctum, Redis (Predis), Laravel Boost, DOMPDF, Laravel Excel.

### Engineering strengths demonstrated
- Large-route surface design and modular controller organization.
- Tenant/account lifecycle logic and admin tooling depth.
- Input validation rigor and operational workflow thinking.

### Honest limitations / gaps
- README is still default Laravel boilerplate (weak external presentation).
- Need clearer architecture documentation and deployed demo evidence before strong public resume claims.

### Resume bullet options
- Built a **multi-tenant Laravel SaaS** for hospital operations with public onboarding and superadmin lifecycle workflows.
- Implemented **tenant governance flows** (approval, suspension, reactivation, grace extension, reseeding) with audit logging.
- Designed path-based hospital routing and platform admin APIs covering subscriptions, payments, and master data modules.

---

## 2) eye_care_tab — Flutter Tablet App for Eye-Care Operations
- **Repository:** https://github.com/Jeel-15/eye_care_tab
- **One-line impact summary:** Developed a large Flutter tablet app spanning clinical, OT, patient, platform-admin, and billing workflows.
- **Problem/domain:** Clinical operations + role-based healthcare workflow execution on tablet/mobile UI.

### Major implemented features
- Extensive screen coverage (patient lifecycle, OT workflows, reports, billing, platform admin).
- Rich service layer for domain modules (`ot_*`, `platform_*`, auth, permissions, history/report services).
- Session/auth restoration and permission-refresh logic in app services.

### Architecture / data flow
- Flutter UI layer (screens/widgets) + service layer abstraction for HTTP/business logic.
- Auth service handles hospital discovery, login, token storage, session refresh, and permission contract synchronization.
- API interactions grouped per domain service for maintainability.

### Technology stack
- Flutter/Dart, HTTP client, secure storage, shared preferences, timezone package.

### Engineering strengths demonstrated
- Strong modularization across many real-world workflows.
- Stateful auth/session and permission handling beyond basic login.
- Product-scale UI/service separation and domain naming consistency.

### Honest limitations / gaps
- README is still template-style; portfolio narrative is missing.
- Need concise architecture docs + screenshots + feature matrix for recruiters/interviewers.

### Resume bullet options
- Built a **large-scale Flutter tablet application** for eye-care operations with modules for OT, patient flow, billing, and reports.
- Implemented robust **authentication/session restoration and permission synchronization** for role-based access.
- Structured app into modular services and domain screens to support complex multi-role healthcare workflows.

---

## 3) vyaparAI — FastAPI AI Commerce/Operations Platform
- **Repository:** https://github.com/Jeel-15/vyaparAI
- **One-line impact summary:** Engineered a multi-module FastAPI platform combining AI-ready architecture with marketplace, rentals, and operations APIs.
- **Problem/domain:** B2B commerce + rentals + AI workflow platformization.

### Major implemented features
- Multi-router API surface (marketplace, rentals, telematics, storefront, buyer, billing/support/admin).
- Role-based permission system with permission mapping and limits (`rbac.py`).
- Operational endpoints for health/readiness, resilience status, provider readiness.
- Domain-rich marketplace and rental workflows with pricing/OTP/logbook logic.

### Architecture / data flow
- FastAPI app with startup bootstrap, router composition, and CORS config.
- Domain repositories for persisted entities + service-like route handlers.
- Readiness checks include storage and vector index considerations.

### Technology stack
- Python 3.12, FastAPI, Pydantic, SQLAlchemy/Alembic, Qdrant client, psycopg, JWT, Next.js frontend folder.

### Engineering strengths demonstrated
- Ambitious platform-level API design and domain modeling.
- Practical RBAC modeling and operational health mindset.
- Multi-domain decomposition (marketplace + rentals + support + admin).

### Honest limitations / gaps
- README is empty (major portfolio weakness).
- Some modules appear ambitious/simulated; claims of production usage or scale should not be made without deployment/runtime proof.

### Resume bullet options
- Built a **modular FastAPI platform** with RBAC, multi-domain routers, and operational health/readiness endpoints.
- Implemented business workflows for marketplace discovery and equipment-rental booking/logbook verification.
- Designed permission-mapping and role-limit enforcement patterns for scalable API authorization.

---

## 4) report_generation — Internship Report Generation Backend
- **Repository:** https://github.com/Jeel-15/report_generation
- **One-line impact summary:** Developed a Flask + MongoEngine backend for authenticated student/admin workflows and structured report-generation APIs.
- **Problem/domain:** Educational/internship reporting automation with profile/report lifecycle handling.

### Major implemented features
- JWT-based authentication and role-protected routes.
- Modular Flask blueprints (`auth`, `admin`, `student`, `reports`, `upload`, `internship-types`).
- Report content sanitization/normalization utilities and structured entity serialization.
- Health endpoint and static/upload serving support.

### Architecture / data flow
- Flask app factory-style setup with blueprint registration.
- MongoEngine models and route-level orchestration of profile/report workflows.
- Support for report-section image workflows and PDF-oriented report logic.

### Technology stack
- Python, Flask, MongoEngine, PyJWT, Flask-Limiter, requests.

### Engineering strengths demonstrated
- Practical API decomposition and auth-protected workflow design.
- Data cleaning/sanitization awareness in text-heavy report sections.
- Business-rule implementation in student/profile/report flows.

### Honest limitations / gaps
- Repo hygiene concerns: committed `.env`, `venv`, and binary artifacts should be cleaned.
- Needs clearer docs, test strategy, and deployment instructions.

### Resume bullet options
- Built a **Flask REST backend** for report generation workflows with JWT auth and role-based access control.
- Designed modular route architecture for student/admin/report/upload domains with MongoDB-backed models.
- Implemented report text normalization and serialization logic to improve consistency of generated outputs.

---

## 5) AI-Mock-Interview — LLM-Assisted Interview Practice Platform
- **Repository:** https://github.com/Jeel-15/AI-Mock-Interview
- **One-line impact summary:** Created a full-stack interview simulator that generates dynamic questions, evaluates answers, and supports voice input.
- **Problem/domain:** Interview preparation with LLM-enhanced feedback.

### Major implemented features
- Session-based interview flow with adaptive difficulty and progress tracking.
- Endpoints for company research, role analysis, common questions, and prep guide generation.
- Voice-answer handling through Whisper transcription path.
- Next.js chat-style frontend with multi-tab assistant modules.

### Architecture / data flow
- Django backend endpoints orchestrate LangGraph/LangChain workflows.
- Next.js frontend starts sessions, submits answers/audio, and displays feedback/results.
- Persistence via Django models for sessions and cached AI outputs.

### Technology stack
- Django, Next.js/TypeScript, LangGraph/LangChain, Whisper, SQLite.

### Engineering strengths demonstrated
- End-to-end AI feature integration across backend and frontend.
- Multi-capability interview assistant design beyond simple Q&A.
- Session and progression mechanics for iterative user workflows.

### Honest limitations / gaps
- Heavy logic concentrated in single view file; would benefit from service-layer extraction.
- Model loading/transcription path may need optimization and production hardening.

### Resume bullet options
- Built a **full-stack AI mock interview platform** using Django + Next.js with dynamic question generation and feedback loops.
- Integrated **LLM and speech workflows** (LangChain/LangGraph + Whisper) for text and voice interview responses.
- Implemented interview session tracking, adaptive difficulty updates, and role/company preparation modules.

---

## Promising Projects (Improve Before Resume)

### 1) enterprise_AI ([repo](https://github.com/Jeel-15/enterprise_AI))
- **Why promising:** Appears to be same/similar substantial codebase lineage as Eyenosis.
- **Why not separate top pick now:** README is empty/boilerplate and overlap with Eyenosis can look duplicate on resume.

### 2) eye_care_app ([repo](https://github.com/Jeel-15/eye_care_app))
- **Why promising:** Large Flutter codebase similar to eye_care_tab with many modules.
- **Why not separate top pick now:** Very high overlap with eye_care_tab; better present one primary variant plus a note.

### 3) jewelry-size-plugin ([repo](https://github.com/Jeel-15/jewelry-size-plugin))
- **Why promising:** Clear product concept + FastAPI architecture scaffold + domain-specific CV angle.
- **Gap:** README explicitly states **Phase 0**; core business routes are still commented in `app/main.py`.

### 4) vehicle_price_prediction ([repo](https://github.com/Jeel-15/vehicle_price_prediction))
- **Why promising:** Good ML pipeline patterns (training, CV search, metadata artifacts, Streamlit app).
- **Gap:** Needs stronger dataset provenance notes, model evaluation narrative, and cleaner project storytelling.

### 5) eCourts-Cause-List-Scraper ([repo](https://github.com/Jeel-15/eCourts-Cause-List-Scraper))
- **Why promising:** Useful automation/data extraction workflow with Selenium + Streamlit + PDF conversion.
- **Gap:** Appears mostly single-script implementation; needs modularization/tests for stronger resume signal.

### 6) iv-studio ([repo](https://github.com/Jeel-15/iv-studio))
- **Why promising:** Broad feature scope in Flask app with project/media generation flows.
- **Gap:** Highly monolithic single-file backend and repo organization issues reduce interview readability.

### 7) DjandoBnB ([repo](https://github.com/Jeel-15/DjandoBnB))
- **Why promising:** Full-stack Django + Next.js intent.
- **Gap:** Current implementation appears early/starter-level in sampled backend files (minimal serializers/views depth).

---

## Skills Matrix (Demonstrated in Repositories)

| Skill / Technology | Evidence Repositories |
|---|---|
| Laravel multi-tenant backend architecture | `eyenosis`, `enterprise_AI` |
| Superadmin/tenant lifecycle operations | `eyenosis` |
| Flutter app modularization at scale | `eye_care_tab`, `eye_care_app` |
| Auth/session/permission handling (mobile) | `eye_care_tab`, `eye_care_app` |
| FastAPI API design & modular routers | `vyaparAI`, `jewelry-size-plugin` |
| RBAC design patterns | `vyaparAI`, `report_generation` |
| LLM application integration | `AI-Mock-Interview`, `vyaparAI` |
| Speech pipeline integration | `AI-Mock-Interview` |
| Flask API development | `report_generation`, `iv-studio` |
| MongoDB/MongoEngine patterns | `report_generation` |
| Web scraping/browser automation | `eCourts-Cause-List-Scraper` |
| ML pipeline training/evaluation | `vehicle_price_prediction` |
| Streamlit app delivery | `vehicle_price_prediction`, `eCourts-Cause-List-Scraper` |

---

## Suggested Resume Project Selection by Target Role

### A) AI/ML Engineer
**Primary picks:**
1. `AI-Mock-Interview`
2. `vehicle_price_prediction`
3. `vyaparAI`

**Optional 4th:** `report_generation` (for applied backend + workflow reliability).

### B) Backend / Full-Stack Engineer
**Primary picks:**
1. `eyenosis`
2. `vyaparAI`
3. `report_generation`

**Optional 4th:** `AI-Mock-Interview` (full-stack + AI integration angle).

### C) Flutter / Mobile Engineer
**Primary picks:**
1. `eye_care_tab`
2. `eye_care_app`
3. `eyenosis` (as backend counterpart integration narrative)

### D) Automation / Data Engineer
**Primary picks:**
1. `eCourts-Cause-List-Scraper`
2. `vehicle_price_prediction`
3. `report_generation`

**Optional 4th:** `vyaparAI` (data/API workflow orchestration angle).

---

## Interview Talking Points & Likely Questions (Top Projects)

## Eyenosis
**Talking points**
- Multi-tenant design choices (tenant lifecycle, role segregation, routing strategy).
- How superadmin controls operational integrity (approval/suspension/audit).
- Validation and data-quality safeguards in onboarding/admin actions.

**Likely questions**
- How did you isolate tenant data and avoid cross-tenant leaks?
- Why path-based tenant routing instead of subdomains?
- Which part of tenant onboarding was hardest and how did you de-risk it?

## eye_care_tab
**Talking points**
- Managing complexity across many role-specific healthcare workflows.
- Service-layer organization and API contract handling in Flutter.
- Session persistence, permission refresh, and secure token handling.

**Likely questions**
- How did you keep screen/service complexity maintainable?
- How do you handle auth expiration and permission changes mid-session?
- What trade-offs did you make for tablet UX vs phone UX?

## vyaparAI
**Talking points**
- API modularization across independent product modules.
- RBAC permission-mapping strategy and role-limit checks.
- Operational readiness endpoints and startup bootstrapping behavior.

**Likely questions**
- How do you keep large router-based APIs cohesive over time?
- How would you productionize the current repository-backed domain stores?
- What is your fallback strategy when AI/vector dependencies degrade?

## report_generation
**Talking points**
- End-to-end authenticated workflow design for report generation.
- Text sanitization and structured serialization approach.
- Balancing API flexibility with input validation and safety.

**Likely questions**
- How did you design role boundaries between admin and student actions?
- Where did data normalization matter most for PDF/report quality?
- What would you refactor first for scale/readability?

## AI-Mock-Interview
**Talking points**
- Coordinating frontend chat UX with backend LLM workflow state.
- Difficulty adaptation logic and interview session tracking.
- Integrating speech transcription and handling async user flows.

**Likely questions**
- How do you control prompt/response consistency across features?
- What are failure points in audio transcription and how do you recover?
- How would you split current Django view logic into cleaner layers?

---

## Truthfulness Checklist (Verify Before Final Resume Submission)

Only claim these if you can independently verify them:

- [ ] **Production deployment status** (live URL, uptime, hosting environment).
- [ ] **Real user count / active usage** for any project.
- [ ] **Performance benchmarks** (latency, throughput, concurrency).
- [ ] **Model quality metrics** (accuracy/RMSE/F1/confidence distributions) with reproducible runs.
- [ ] **Business impact numbers** (revenue saved, time saved, conversion uplift, etc.).
- [ ] **Team size / ownership split** if these were collaborative projects.
- [ ] **Security/compliance claims** (HIPAA/GDPR/ISO) unless explicitly implemented and audited.
- [ ] **Exact cloud architecture claims** (K8s, autoscaling, distributed queues) unless present and verified.

Safe claims from current repository evidence:
- Technology stacks used.
- Implemented modules/routes/services visible in source.
- Architectural patterns directly observable in code structure.

---

## Evidence Basis (What was reviewed)
This document was based on repository READMEs, dependency/configuration files, directory structures, and representative implementation files across the listed candidate repositories (including routing/controllers/services/model files where available).
