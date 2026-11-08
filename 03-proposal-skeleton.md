# 📝 The GSoC Engineering Proposal Skeleton (Anti-AI-Spam Edition)

> **Why Most Proposals Get Rejected**:
> As Google's official [Mentor Guide on AI Spam Proposals](https://developers.google.com/open-source/gsoc/resources/spam_proposals) notes:
> *"Most of the AI generated spam just rephrases the project description from your idea list."*
>
> A winning proposal reads like an **Engineering RFC (Request for Comments)** written by someone who has already built the codebase locally, read the exact source files, and shipped **1–3 meaningful PRs**.

---

## 📌 Proposal Structure (Copy & Customize)

# [Project Title]: [Specific, Measurable Engineering Outcome]

- **Organization**: `[Organization Name]`
- **Project Size**: `Small (~90 hrs) / Medium (~175 hrs) / Large (~350 hrs)`
- **Primary Mentor(s)**: `[Mentor Name(s)]`
- **Contributor**: `[Your Name]`
- **GitHub / GitLab**: `https://github.com/your-username`
- **Email & Timezone**: `you@example.com` (`UTC+05:30 / IST`)

---

## 1. Proof of Codebase Readiness (Put Your PRs First!)

> *Maintainers check this table before reading anything else. Put it on Page 1.*

### 1.1 Merged & Open Pull Requests in `[Organization]`

| PR / Issue | Title & Scope | Files Modified | Status |
| :--- | :--- | :--- | :---: |
| **[PR #1234](https://github.com/...)** | Fix race condition in worker queue shutdown | `src/worker/pool.py`, `tests/test_pool.py` | ✅ **Merged** |
| **[PR #1256](https://github.com/...)** | Add schema validation for v2 config loader | `src/config/schema.py`, `tests/test_config.py` | 🔍 **In Review** |
| **[Issue #1270](https://github.com/...)** | Reproduced & root-caused memory leak in stream parser | `src/parser/stream.py` | 💬 **Triaged** |

### 1.2 Local Prototype / Proof of Concept (If Applicable)
- Summarize any small spike or benchmark you already ran locally to validate that your proposed approach works on the real codebase.

---

## 2. Problem Statement & Current Architecture Limitations

*(Do NOT copy-paste the org's project idea paragraph. Explain the problem by referencing actual file paths, classes, and functions in the repository.)*

- **How it works today**: Currently, in `path/to/module.ext` (`ClassName.method_name()`, lines `XX–YY`), the system handles `[X]` by doing `[Y]`.
- **Where it breaks / bottleneck**: When `[condition Z]` happens, `[specific limitation, bug, or missing capability]`.
- **Why this matters to users/maintainers**: `[1–2 sentences on concrete impact]`.

---

## 3. Proposed Technical Design & Implementation Plan

### 3.1 Architecture Overview
*(Include a simple ASCII diagram or Mermaid flowchart showing how your new module/changes plug into the existing codebase.)*

```text
[Existing Caller: src/api/handler.py]
          │
          ▼
[New Interface: src/core/adapter.py]  ◄── Unit Tests: tests/unit/test_adapter.py
          │
          ▼
[Existing Storage: src/db/store.py]
```

### 3.2 Concrete File-Level Changes
1. **`src/path/file_a.ext`**:
   - Introduce `NewClass / function_signature(arg1, arg2) -> ReturnType`.
   - Handle edge cases: `[Edge case 1]`, `[Edge case 2]`.
2. **`src/path/file_b.ext`**:
   - Refactor `existing_function()` to delegate `[sub-task]` while maintaining backward compatibility for existing callers.
3. **Backward Compatibility & Migration**:
   - Explain how existing APIs/configs continue to work without breaking current users.

---

## 4. Testing, CI & Documentation Strategy

- **Unit Tests**: New test cases in `tests/unit/...` covering normal paths and failure modes.
- **Integration / E2E Tests**: How the feature will be verified end-to-end in CI (`.github/workflows/...`).
- **Documentation**: Which docs (`docs/...`) and docstrings will be added or updated.

---

## 5. Week-by-Week Deliverables & Timeline (With Buffer!)

> *Include explicit deliverables (PRs) for every week, and always include a buffer week for code review iterations.*

| Period | Milestone & Concrete Deliverable | Expected PR(s) |
| :--- | :--- | :--- |
| **Community Bonding** | Finalize interface design with mentors; set up test fixtures & benchmark baseline | RFC Issue / Draft PR #1 |
| **Weeks 1–2** | Implement core data structures & parser in `src/...` + unit tests | PR #2 (Core module) |
| **Weeks 3–4** | Wire up API integration & CLI flags + error handling | PR #3 (Integration) |
| **Week 5** | **Buffer & Code Review Polish** — address mentor review feedback from PRs #2–#3 | — |
| **Week 6 (Midterm)** | **Midterm Evaluation Deliverable**: Working end-to-end core pipeline passing CI | Midterm Demo & Docs |
| **Weeks 7–8** | Implement `[Phase 2 feature / optimization]` + edge-case test suite | PR #4 |
| **Weeks 9–10** | End-to-end integration tests, performance benchmarks, and user documentation | PR #5 (Docs & Benchmarks) |
| **Week 11** | **Buffer Week** — bug fixes, edge cases, and mentor review cleanup | — |
| **Week 12 (Final)** | Final evaluation report, release notes, and handoff documentation | Final Submission |

---

## 6. Availability, Commitments & AI Disclosure

- **Weekly Availability**: `XX hours/week` (`start date` to `end date`).
- **Academic / Exam Schedule**: List any university exam dates upfront and how you have buffered for them.
- **AI Usage Disclosure**:
  - *"This proposal and all architectural designs were written by me after building and testing the repository locally. I adhere strictly to `[Organization Name]`'s AI policy."*
