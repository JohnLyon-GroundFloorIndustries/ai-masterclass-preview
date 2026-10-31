# Curriculum and learning path — Beginner v1.0

Audience: adults who can use a computer and have asked ChatGPT questions. No programming knowledge assumed.

17 modules, 51 lessons, six phases. Suggested workload: 168 hours, including practice. At 5 hours/week allow approximately 34 weeks; pace is a planning estimate, not a promise.

Weekly rhythm: two 60-minute reading/simulation sessions, one 2-hour real exercise, one hour of retrieval practice and troubleshooting. Pause to reproduce a result before advancing. Allow extra time for capstone changes and independent review.

All lessons contain outcome, relevance, plain explanation, bounded analogy, technical explanation, clickable visual, steps, practice, expected output, troubleshooting, explanatory check, ability recap and a connection forward.

Prerequisite chain: each lesson builds on the preceding lesson; Module 0 starts from the stated audience knowledge. Modules 0–2 need only a browser. Module 3 introduces terminal and Python setup before code execution. Modules 4–6 introduce agents/tools/retrieval before frameworks. Infrastructure follows real local programs; production topics follow deployment and reliability.

Completion, correct concept checks, attempted exercises, successful educational simulations and learner-supplied executable evidence are recorded separately. No professional qualification is implied.

## Phase 1: Understanding AI and computers

### Module 0: Welcome to the world of AI — 4 hours
Prerequisite: basic computer use.
Project: Classify three everyday tasks and choose where a person must remain in charge.
- 0.1 Your first map of AI: Distinguish the application you use from the model behind it.
  Practice: Use the comparison simulator. Write one task that needs only text and one that requires changing another system.
  Success indicator: Drafting produces text. Creating a task changes a system and needs a permitted tool.
- 0.2 Helpful does not mean dependable: Separate a useful draft from a verified fact.
  Practice: Use the retrieval simulator to ask an unsupported question. Choose to withhold an answer when no source matches.
  Success indicator: The system says evidence is insufficient instead of inventing a policy.
- 0.3 Choose the simplest useful system: Choose between a chatbot, a fixed workflow and an agent.
  Practice: Compare chatbot, workflow and agent modes for a support request. Explain why a fixed triage rule may be enough.
  Success indicator: Your design names a human owner, an allowed action and a clear stopping point.

### Module 1: How AI actually works — 5 hours
Prerequisite: Modules 0–0.
Project: Measure the effects of limited context and compare model choices using a small task set.
- 1.1 Learning before answering: Explain training and inference without confusing them.
  Practice: Change the variation setting and compare the resulting continuations. Describe why plausible text is not a factual check.
  Success indicator: Higher variation offers more varied example continuations. No real model runs in the page.
- 1.2 Tokens and the working space: Explain why long conversations can lose useful details.
  Practice: Find a capacity at which the example fits, then add irrelevant text until it does not.
  Success indicator: The overflow warning changes as input and reserved output compete for capacity. Counts are explicitly estimates.
- 1.3 Reasoning, speed and cost: Choose a model based on measured task results.
  Practice: Create three test tasks: a summary, a calculation and an evidence-based policy question. Define what a correct answer needs.
  Success indicator: A comparison sheet includes quality criteria as well as time and estimated expense.

### Module 2: Computers, software and the internet — 5 hours
Prerequisite: Modules 0–1.
Project: Trace a browser request and locate where data lives.
- 2.1 The computer beneath the application: Distinguish hardware, operating systems, files and programs.
  Practice: Draw a folder tree with the lab folder, a Python source file and an output file.
  Success indicator: You can explain that the program creates output; the folder only organizes it.
- 2.2 From a button to a server: Trace a request and distinguish local from remote work.
  Practice: Explain which computer performs each step and why refreshing cannot repair an unavailable database.
  Success indicator: The trace separates browser, network, application server and database.
- 2.3 Where information is stored: Distinguish a database, file storage and cloud services.
  Practice: Use the memory simulator to compare a temporary conversation with a saved record, then clear working context.
  Success indicator: Saved records remain in the simulation when working context is cleared. Browser course progress has its own export control.

### Module 3: Introduction to programming and APIs — 12 hours
Prerequisite: Modules 0–2.
Project: Run hello.py and make a real HTTP request to a safe local mock API.
- 3.1 Your first real Python program: Install an interpreter, open a terminal and run a file.
  Practice: Run the real hello.py file. Change the list from two tasks to three and predict the new count.
  Success indicator: The original program prints “Hello, learner”, two numbered tasks, and “Ready: 2 tasks”.
- 3.2 Values, decisions and repetition: Read variables, types, conditions, loops and functions.
  Practice: Add a function called double that returns its input multiplied by two. Call it with 4 and then with 0.
  Success indicator: The function returns 8 and 0. The empty task list takes the “No tasks yet” branch.
- 3.3 JSON and a real local API: Send structured information to a local service and interpret its response.
  Practice: In the API simulator send valid JSON, then remove a closing brace, then replace the numeric amount with text.
  Success indicator: The local client prints status 200 and total 12. The simulator distinguishes malformed JSON from an invalid field type.

## Phase 2: From chatbots to agents

### Module 4: Understanding AI agents — 7 hours
Prerequisite: Modules 0–3.
Project: Run a bounded task agent and explain every action in its trace.
- 4.1 Goals, tools and autonomy: Turn a vague request into a bounded assignment.
  Practice: Run the agent simulator with step limits of one and four. Compare partial and completed work.
  Success indicator: One step stops before completion; four permits retrieval, drafting and review. No external actions occur.
- 4.2 The agent loop: Follow observation, decision, action and verification.
  Practice: Run python workflow.py --scenario failure in the external lab after the setup exercises.
  Success indicator: The trace contains bounded attempts and an escalated status. No task is marked approved.
- 4.3 Oversight as part of the design: Choose when to ask a human and what information they need.
  Practice: Write a review card for a sample task with proposed action, source and a clear reject option.
  Success indicator: The action cannot proceed on rejection or after the approved content changes.

### Module 5: How agents use tools — 8 hours
Prerequisite: Modules 0–4.
Project: Validate calculator, document-search and task-tool requests before execution.
- 5.1 Function calling and contracts: Explain how generated tool arguments become real operations.
  Practice: Send valid and invalid calculator inputs in the API simulator. Explain why the invalid request never reaches arithmetic.
  Success indicator: A valid 5 plus 7 returns 12. Strings, unknown operations and excessive inputs are rejected.
- 5.2 MCP and tool discovery: Explain a common tool connection protocol without mistaking it for trust.
  Practice: Use the tool simulator to choose a known tool and an unknown tool. Explain what discovery can establish and what still needs authorization.
  Success indicator: Unknown tools are rejected. Discovery reveals a contract but grants no permission.
- 5.3 Errors and safe side effects: Handle failures without duplicating changes.
  Practice: Set duplicate delivery in the retry simulator and compare idempotency on and off.
  Success indicator: With deduplication, repeated delivery creates one task. Without it, duplicate effects are visible.

### Module 6: Memory and knowledge — 9 hours
Prerequisite: Modules 0–5.
Project: Build permission-filtered document retrieval and cite the selected evidence.
- 6.1 Memory is a design choice: Separate conversation context from durable records.
  Practice: Design a memory record with text, source, owner and expiry. Explain when it should be deleted.
  Success indicator: The record can be traced to its source and is not confused with the model’s training.
- 6.2 Retrieval before generation: Build an answer from accessible evidence and recognize missing support.
  Practice: Ask “How do I reset access?” in the retrieval simulator, then ask “What is the refund deadline?”
  Success indicator: The first query finds the access policy. An unsupported policy claim is withheld.
- 6.3 Embeddings, vectors and relationships: Choose between exact search, similarity and graph relationships.
  Practice: Write three query/document pairs that a lexical retriever misses. Propose a labeled evaluation set before adding embeddings.
  Success indicator: Your test set includes relevant and irrelevant matches and a tenant boundary case.

## Phase 3: Building practical agent systems

### Module 7: Designing an AI agent — 10 hours
Prerequisite: Modules 0–6.
Project: Implement a source-backed draft workflow with explicit state and stopping rules.
- 7.1 Instructions and structured results: Write a contract that separates goals, data and output requirements.
  Practice: Add a new required field to a copy of the result contract and write a test that fails when it is missing.
  Success indicator: The test catches the missing field; a supported result has at least one permitted source.
- 7.2 Planning and checking: Compare ReAct, plan-and-execute and reflection.
  Practice: Compare python workflow.py --approach sequential with --approach graph. Save both outputs and explain their state transitions.
  Success indicator: Both approaches produce the same supported draft; the graph makes transitions explicit.
- 7.3 Predictability under failure: Enforce deadlines, budgets and terminal states.
  Practice: Change max_steps in a copy of the lab configuration to one. Explain why budget exhaustion is not success.
  Success indicator: The run stops with an explicit bounded outcome and a trace of completed steps.

### Module 8: Multi-agent systems — 10 hours
Prerequisite: Modules 0–7.
Project: Run researcher, drafter and reviewer roles and justify their boundaries.
- 8.1 When a team helps: Decide whether distinct roles justify added complexity.
  Practice: Use the delegation simulator with one and three workers. Compare coordination overhead and result checks.
  Success indicator: The research pipeline preserves source IDs through each role and stops for human review.
- 8.2 Handoffs and shared state: Pass the minimum necessary information between roles.
  Practice: Sequence the handoff stages in the assessment studio: request, research, draft, review, human decision.
  Success indicator: The review step can trace every supported claim to permitted source material.
- 8.3 Coordination failures: Handle missing workers, duplicate messages and conflicting results.
  Practice: Write a recovery decision for a missing optional summary versus missing required evidence.
  Success indicator: Missing evidence blocks the answer; missing optional formatting can produce a clearly labeled partial result.

### Module 9: Frameworks and orchestration — 9 hours
Prerequisite: Modules 0–8.
Project: Implement one workflow as sequential Python and as an explicit graph.
- 9.1 Plain Python before a framework: Recognize the architecture hidden beneath library features.
  Practice: Add a validation step to both copies and run parity tests.
  Success indicator: The supported answer and sources match across approaches; the failure branch remains explicit.
- 9.2 Compare framework approaches: Choose a framework using requirements and maintenance evidence.
  Practice: Create an architecture decision record choosing plain Python or a framework and include one rejected alternative.
  Success indicator: The decision cites requirements and a small proof of behavior, not popularity alone.
- 9.3 Trace and debug execution: Locate the first divergence from expected behavior.
  Practice: Use the monitoring simulator to distinguish a slow model from a failed retrieval step.
  Success indicator: Your diagnosis names the failing stage, its observed evidence and a testable next action.

## Phase 4: Understanding AI infrastructure

### Module 10: Infrastructure fundamentals — 8 hours
Prerequisite: Modules 0–9.
Project: Draw a deployable topology and explain every box and connection.
- 10.1 Compute and model hosting: Distinguish running your application from running a model.
  Practice: Use the architecture simulator to toggle a hosted model and local application. Explain why a GPU is not mandatory for the core lab.
  Success indicator: The free lab runs on a CPU using deterministic logic; hosted inference is an optional separate extension.
- 10.2 Storage, queues and caches: Choose infrastructure components by the job they perform.
  Practice: Add a queue and a tenant-aware cache to your architecture diagram, labeling what each stores.
  Success indicator: The queue stores pending work; the database remains authoritative; cache expiry is explicit.
- 10.3 Networks and topology: Map trust boundaries and failure dependencies.
  Practice: Use the architecture simulator to inspect each component, then save an architecture decision explaining what you deliberately omitted.
  Success indicator: Every box has a responsibility, owner, access rule and failure behavior.

### Module 11: Deploying AI applications — 12 hours
Prerequisite: Modules 0–10.
Project: Run the local service, package it and rehearse a rollback with evidence.
- 11.1 Version control and environments: Save reproducible changes and separate practice from real users.
  Practice: Explain where this HTML runs versus where python server.py runs.
  Success indicator: The course runs in the browser. The Python service runs in a local process and needs separate hosting for remote use.
- 11.2 Containers and orchestration: Explain an image, container and Kubernetes deployment.
  Practice: Inspect the supplied Kubernetes manifest and identify image, replicas, resource limits and health probes before trying the optional local-cluster exercise.
  Success indicator: The Python health endpoint returns status ok. Container and cluster steps require their own installed tools and local verification.
- 11.3 Pipelines, infrastructure as code and rollback: Design a release with a tested recovery path.
  Practice: Write a release gate that blocks deployment when tenant-isolation or approval tests fail. Record the exact version and rollback command.
  Success indicator: A failed gate prevents promotion; rollback names a version instead of “use whatever worked before.”

### Module 12: Reliability, performance and cost — 10 hours
Prerequisite: Modules 0–11.
Project: Measure a workload, inject failures and demonstrate bounded recovery.
- 12.1 Latency, throughput and concurrency: Explain how a workload creates bottlenecks.
  Practice: Run python load_test.py against the local service and inspect request count, error count and p95 latency.
  Success indicator: The report contains measured local results rather than claims about cloud scale.
- 12.2 Retries and recovery: Use bounded backoff and idempotency together.
  Practice: Run the lab’s recovery and duplicate tests. Explain which errors are retried and why.
  Success indicator: Temporary failure can recover within budget; exhausted or permanent failure escalates. Duplicate effects remain suppressed.
- 12.3 Budget-aware architecture: Calculate total expense and enforce a stopping budget.
  Practice: Document a per-run budget and a global daily budget, including behavior when either is exhausted.
  Success indicator: Your design refuses or queues new work at its budget boundary and records the reason.

## Phase 5: Production-grade systems

### Module 13: Security, privacy and human oversight — 12 hours
Prerequisite: Modules 0–12.
Project: Prove isolation, approval binding and safe failure with executable tests.
- 13.1 Identity, permissions and secrets: Separate who is asking from what they may do.
  Practice: Use the security simulator to request another tenant’s document with enforcement enabled and disabled.
  Success indicator: The enforced boundary blocks cross-tenant access regardless of the request wording.
- 13.2 Prompt injection and isolation: Treat external text as evidence rather than authority.
  Practice: Add an attack fixture that requests a forbidden tool without using the phrase “ignore instructions.”
  Success indicator: The tool allowlist rejects it because of the requested operation, not because of a keyword match.
- 13.3 Approval, privacy and audit: Make consequential actions reviewable and reconstructable.
  Practice: Create a privacy inventory listing each stored field, purpose, access owner, retention and deletion method.
  Success indicator: Changed content invalidates approval; the audit records the attempted decision and outcome.

### Module 14: Monitoring, testing and evaluation — 11 hours
Prerequisite: Modules 0–13.
Project: Produce test results, a load report and an incident diagnosis.
- 14.1 Tests and evaluations answer different questions: Build checks for code behavior and answer quality.
  Practice: Add a new evaluation case before modifying retrieval. Record whether your change improves it without breaking earlier cases.
  Success indicator: The test suite reports individual checks; evaluation reports supported-answer and refusal outcomes.
- 14.2 Logs, metrics, traces and alerts: Choose signals that reveal user-facing failures.
  Practice: Define one alert with its signal, threshold, evaluation window, owner and first diagnostic action.
  Success indicator: The alert points to a concrete runbook and measured user impact.
- 14.3 Incident response and runbooks: Diagnose, contain and recover from a failure.
  Practice: Write an incident note with impact, evidence, containment, recovery verification and one preventive test.
  Success indicator: The note distinguishes observations from hypotheses and includes a reproducible recovery check.

### Module 15: Enterprise and advanced architectures — 12 hours
Prerequisite: Modules 0–14.
Project: Document operational decisions and perform a local backup-and-restore drill.
- 15.1 Enterprise integration and tenancy: Integrate business systems without erasing their authority.
  Practice: Write an integration contract with field mapping, owner, permission, rate limit and failure behavior.
  Success indicator: Each field has one authoritative source and conflicts have a documented resolution path.
- 15.2 Durability and disaster recovery: Recover work and data after a process or machine fails.
  Practice: Set an example RPO and RTO for a noncritical training service and compare them with your measured restore drill.
  Success indicator: The restored record matches and the report includes measured recovery time.
- 15.3 Advanced capabilities with evidence boundaries: Evaluate multimodal, computer-use and adaptive designs responsibly.
  Practice: Write an architecture decision rejecting an unnecessary advanced capability, with conditions under which you would revisit it.
  Success indicator: The decision includes measurable acceptance criteria and explicitly marks untested behavior.

## Phase 6: Build your own infrastructure

### Module 16: Production capstone — 24 hours
Prerequisite: Modules 0–15.
Project: Deliver a working support-draft service, tests, recovery evidence and an honest readiness review.
- 16.1 Build the smallest useful agent: Define a problem and deliver a functioning first slice.
  Practice: Change one fictional policy and add a matching evaluation case. Demonstrate the new answer with its source identifier.
  Success indicator: A real Python process returns a draft with permitted source evidence and awaiting_review status.
- 16.2 Add controls and prove recovery: Build practical evidence for security, reliability and operations.
  Practice: Import the generated evidence JSON into the course dashboard. Then write a short explanation of one failing test you intentionally created and fixed.
  Success indicator: The dashboard records a lab-suite report separately from lesson completion and quiz scores. Imported reports are learner-supplied, not independent certification.
- 16.3 Demonstrate and defend the system: Present a working system and explain its limits.
  Practice: Have a reviewer reproduce the setup and challenge a tenant boundary, changed approval and unsupported question. Record the observed outcomes.
  Success indicator: The handoff includes runnable files and actual evidence; unexecuted cloud or model work is labeled pending.

## Practical review rubric
For each of the 14 capstone gates: 0 absent; 1 explained; 2 executed with reproducible evidence; 3 independently reproduced and challenged. Do not add points for opening lessons. Submit source, tests, evaluation, architecture, access controls, approval evidence, recovery, measured load and runbooks. Live model/cloud/container work remains separately verified.
