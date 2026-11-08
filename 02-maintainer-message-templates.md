# 💬 Maintainer Issue, PR & Public Chat Templates

> **Core Principle**: Maintainers are unpaid volunteer engineers reviewing code after work. Every message you send should **save them time**, prove you did your homework, and stay **100% in public channels**.

---

## 🚫 The 4 "Never Do This" Rules

1. **NEVER comment `"Hi, I am interested in this issue for GSoC, please assign this to me."`**  
   In open source, you don't ask for permission to read code. Reproduce the bug locally, find the root cause, and share your findings or open a draft PR.
2. **NEVER DM maintainers privately** on LinkedIn, X/Twitter, personal email, or private Discord/Matrix DMs unless the organization explicitly asks you to.
3. **NEVER paste a raw 200-line stack trace** asking *"Why is my build failing?"* without showing what you already investigated.
4. **NEVER use ChatGPT to write your chat messages or issue comments.** Maintainers spot LLM-generated paragraphs (`"I would love to delve into..."`, `"Thank you for your valuable insights..."`) in two seconds. Write plain, direct engineering English.

---

## ✅ Template 1: Claiming / Investigating a Bug on a GitHub Issue

Instead of asking *"Can I work on this?"*, post a root-cause investigation comment after reproducing the issue locally:

```markdown
Hi @maintainer-handle — I reproduced this issue locally on `main` (commit `abc1234`, OS/Python/Node version).

**Root Cause Found:**
In `src/module/parser.ts` (lines 142–156), `parseConfig()` assumes `options.timeout` is always defined, which throws a `TypeError` when `options` is passed as `{}` from the CLI flag parser.

**Proposed Fix:**
1. Default `timeout` in `normalizeOptions()` before reaching `parseConfig()`.
2. Add a regression unit test in `tests/parser.test.ts` covering empty CLI flag objects.

I have this working and passing existing tests locally — I'll open a PR shortly referencing this issue unless you prefer a different approach.
```

---

## ✅ Template 2: Asking for Help When Blocked on Local Setup

Only post this **after** you have read `CONTRIBUTING.md`, searched closed issues/chat history, and spent at least 60–90 minutes debugging the error yourself:

```markdown
Hi everyone — I'm setting up `repo-name` locally by following `CONTRIBUTING.md` and hit a test failure I couldn't find in prior chat threads.

**Environment:**
- OS: Ubuntu 24.04 / WSL2 (or macOS / Windows)
- Runtime: Python 3.12.4 / Node 22.4.0
- Branch: `main` (`git rev-parse --short HEAD` -> `8f4e2a1`)

**Command Run & Exact Error:**
Running `pytest tests/unit/test_storage.py` fails at `test_sqlite_migration` with:
`OperationalError: no such table: schema_migrations`

**What I Already Tried:**
1. Ran `alembic upgrade head` prior to running pytest.
2. Checked `conftest.py` and noticed `temp_db_fixture` skips migration scripts when `FAST_TESTS=1` is set, but `FAST_TESTS` is unset in my shell.

Is there an initialization step required before running `test_storage.py` standalone?
```

---

## ✅ Template 3: First Message in the Public GSoC Channel (After Merging/Opening 1st PR)

Do **not** post a 5-paragraph biography with your college name, CGPA, and resume link. Introduce yourself through **code**:

```markdown
Hi team — I've been exploring `repo-name` over the past week, got the local dev environment and test suite running, and opened PR #1234 fixing Issue #1210 (handling null pagination cursors in the API client).

I'm interested in the **[Project Idea Name]** project for GSoC and have been reading through `src/ subsystem /` to understand how `[Current Component]` works today.

Before I draft my technical design for `[specific sub-problem]`, is `[File/Module X]` still the intended place where the new interface should live, or is that being refactored in another branch?
```

---

## ✅ Template 4: Requesting Early Mentor Feedback on Your Proposal Draft

Share your draft **7–10 days before the deadline** (never on the final day):

```markdown
Hi @mentor-handle — following our discussion on `[topic/PR #1234]`, I've put together a concise technical draft for **[Project Title]**:
[Link to Google Doc / GitHub Gist with comment access enabled]

Specifically, I'd appreciate your pushback on two sections when you have a moment:
1. **Section 2.2 (Architecture)**: Whether extending `BaseRunner` vs. creating a standalone adapter fits the roadmap better.
2. **Section 4 (Weekly Milestones)**: Whether Weeks 3–5 give enough buffer for integration testing.

Thank you for your time!
```
