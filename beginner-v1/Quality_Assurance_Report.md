# Quality assurance — Beginner v1.0

Release date: October 31, 2026. Local checks passed. Deployment evidence is recorded separately in `Deployment_Verification.md` after the live site is verified.

## Delivered scope

17 modules, 51 individually authored lessons, six phases, 20 educational simulation types, 51 explanatory knowledge checks, a three-question orientation, matching and sequencing activities, a 12-question final examination, 14 capstone evidence gates, searchable glossary, inline keyboard-accessible term explanations, notes, bookmarks, review reminders, local progress import/export and a separately runnable lab kit. Suggested study/practice workload is 168 hours; it is an estimate, not a promise of qualification.

The HTML embeds CSS, JavaScript, official logo, curriculum and downloadable lab ZIP. No CDN, remote font, model API or external script is required for learning. Source ZIP and release documentation are companion files; keep the complete release folder if using those offline.

## Executed tests

| Check | Observed outcome |
|---|---|
| Python lab suite from a freshly extracted ZIP | 36 tests passed; 0 failures on Python 3.10.6 / Windows |
| Real HTTP behavior | Health, draft creation, stored task ID, repeated request deduplication, caller-supplied identity rejection and cross-origin denial passed |
| Data and security | Tool schema, unknown tool, permission denial, cross-tenant access, changed/expired/missing approval, changed-since-inspection binding and restart checks passed |
| Architectures | Sequential and explicit graph controllers produced matching results |
| Failure recovery | Bounded failure escalated; temporary failures recovered; step exhaustion remained an explicit incomplete state |
| Quality fixtures | 4/4 deterministic evaluation fixtures passed; this is not a real-world accuracy estimate |
| Local load | 20 actual HTTP requests, concurrency 4, zero errors; observed p95 192.53 ms and 55.71 requests/sec on this local run only |
| Backup/restore | Fixture recovered; SQLite integrity check ok; observed restore verification 0.015437 seconds for the small fixture |
| Optional model adapter | Fake-transport contract, incomplete-response rejection and no-evidence/no-network tests passed; no paid inference performed |
| JavaScript/static | 75 assertions passed: simulation arithmetic, security settings, invalid JSON, import filtering, storage-error fallback, embedded dependencies and 51 substantive lesson records |
| Full lesson browser traversal | 51/51 pages rendered all 13 learning sections; each experiment ran and each correct quiz answer produced feedback |
| Responsive DOM | 45 route/viewport combinations at exact CSS widths 320, 390, 768, 1024 and 1440; no horizontal document overflow |
| Accessibility automation | axe-core WCAG 2 A/AA, 2.1 AA and 2.2 AA rules: zero violations in studio, dashboard, roadmap, programming lesson, assessment, setup, labs, glossary and sources; dark dashboard and final mobile assessment also passed |
| Keyboard/manual | Mobile menu and route closure, visible file-input focus, keyboard glossary dialog and return, lesson controls, diagram buttons and semantic radio groups exercised |
| Learning state | Correct answers, studied status, notes and bookmark persisted through reload; export/reimport worked; invalid-version import rejected |
| Assessments | Matching returned 4/4; final examination returned 12/12 with explanations; conceptual results remain separate from practical evidence |
| Downloads | Browser downloaded engineering ZIP, standalone HTML and progress JSON |
| Offline interaction | With networking disabled after loading, navigation and token simulation worked; static inspection confirmed embedded dependencies |
| Runtime errors | No JavaScript error logs observed during exercised browser flows |
| Packaging | Standard-library build and lab setup documented; archives contain runnable source and dependency specifications |

## Defects found and corrected

- Security simulator reversed the enforced/disabled selector mapping. A direct cross-tenant scenario caught it; fixed and retested with expected denial.
- A visually hidden progress file input exceeded small-screen width. Replaced with a visible labeled input, then reran all 45 responsive checks.
- Skip-link routing risked returning to the dashboard. It now focuses current content without replacing the lesson.
- Approval review rejects content changed between inspection and approval. Approval/execution checks use explicit write transactions; a regression test covers changed content.

## Curriculum review

Each lesson has a distinct situation, explanation, analogy limitation, technical detail, walkthrough, practice, expected result, troubleshooting and explanatory check. Foundations precede agent/framework/infrastructure work. Python setup covers Windows, macOS and Linux with complete beginner code and line explanations. Projects have observable artifacts or review criteria. Advanced coverage includes tenancy, durable records, idempotency, deployment, rollback, recovery, queues, costs, evaluation and governance.

The advanced reference course remains at its original repository root. Official LogoPack artwork is embedded unchanged. Sources and exact reference commits are in `Source_Ledger.md`.

## Explicit verification limits

- Browser-tool policy blocks file:// navigation. Direct-from-disk browser launch could not be exercised. Dependency inspection and network-disabled interaction were tested instead; these are not represented as a direct file-mode browser test.
- Automated accessibility checks and keyboard sampling do not establish full WCAG conformance. No screen-reader user study was performed.
- Large emulated screenshot capture showed browser-tool compositing artifacts. Responsive geometry was checked with exact layout measurements; default-view visual inspection was used for interface review.
- The baseline executes real Python, HTTP and SQLite but uses deterministic worker roles and lexical retrieval. It is not live LLM inference, neural embeddings or an MCP server.
- The optional paid-model adapter is implemented and fake-transport tested; live provider behavior and charges are unverified.
- Docker/Kubernetes configurations and guided instructions are supplied but those runtimes were unavailable locally and not executed. Public cloud deployment of the Python service is not claimed; the course itself uses static GitHub Pages.
- macOS/Linux setup was checked against official documentation, not executed on those operating systems.
- The local HTTP service is not internet-hardened; identity/reviewer are fixtures and SQLite audit rows are not tamper-proof. Production needs real identity, representative evaluations, security review, operational ownership and applicable governance.
- Imported evidence is learner-supplied and editable, not independent certification. Completion does not establish professional qualification.

No known release-blocking defect remained in the tested instructional and local-lab scope. These limitations remain explicit follow-on verification work.
