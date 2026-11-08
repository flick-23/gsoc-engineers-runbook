# 📋 The 5-Point GSoC Organization Shortlist Checklist

> **Goal**: Narrow down 180+ organizations from the [Official GSoC Archive](https://summerofcode.withgoogle.com/archive) to **2 target organizations** (and **1 primary repository**) that fit your existing skills.

---

## 🔍 Step 1: The 5-Filter Elimination Checklist

Run every candidate organization through these 5 filters in strict order. If an organization fails **any** filter, drop it immediately and move to the next one.

### Filter 1 — Tech Stack Match (Non-Negotiable)
- [ ] Does this repository use a programming language and framework I can **already write and debug without a tutorial**?
- [ ] *Rule*: **Never learn a new language and a new codebase at the same time.** If you write JavaScript/TypeScript or Python daily, do not pick a C/Rust kernel project just for the brand name.

### Filter 2 — Active Repository Pulse (Last 14 Days)
- [ ] Open the target GitHub/GitLab repository -> click **Pull Requests** -> filter by `is:pr is:merged`.
- [ ] Have **at least 3–5 PRs been reviewed and merged in the last 14 days**?
- [ ] Are maintainers actively replying to issues or reviewing community PRs? (Avoid dead/archived sub-repos where PRs sit unreviewed for 3+ months.)

### Filter 3 — GSoC Track Record (Consistency)
- [ ] Search the organization in the [GSoC Past Programs Archive](https://summerofcode.withgoogle.com/archive).
- [ ] Has this organization participated in GSoC for **at least 2–3 of the last 4 years**?
- [ ] Returning organizations have established onboarding docs, experienced mentors, and a high probability of being accepted again in February.

### Filter 4 — The 48-Hour Local Build Test
- [ ] Can I clone the repository, install dependencies, build the project, and run the existing unit test suite on my machine within **48 hours**?
- [ ] Does the repo have a `CONTRIBUTING.md`, `DEVELOPMENT.md`, or Docker/DevContainer setup?
- [ ] *Reality check*: Over 80% of applicants never get past building the repository locally. Once your local tests pass, you are already ahead of most of the applicant pool.

### Filter 5 — Public Communication Health
- [ ] Join their official public communication channel (Matrix, Zulip, Discord, Slack, Discourse, or Mailing List).
- [ ] Read the last **2 weeks of messages** before typing a single word.
- [ ] Are mentors answering technical questions with specific pointers?
- [ ] What is their explicit **AI Policy**? (Check their GSoC wiki page / mailing list for strict rules like SymPy's *"No AI used for the application"*.)

---

## 📊 Step 2: Organization Comparison Matrix (Copy & Fill In)

Score 3–5 initial candidates from `1` (Poor) to `5` (Excellent), then commit to your **Top 2**:

| Criterion (1–5) | Org 1: `__________` | Org 2: `__________` | Org 3: `__________` |
| :--- | :---: | :---: | :---: |
| **1. Tech Stack Familiarity** | `/5` | `/5` | `/5` |
| **2. Repo Merge Activity (Last 14d)** | `/5` | `/5` | `/5` |
| **3. Past GSoC Years (3+ yrs ideal)** | `/5` | `/5` | `/5` |
| **4. Local Build & Test Speed** | `/5` | `/5` | `/5` |
| **5. Maintainer Responsiveness** | `/5` | `/5` | `/5` |
| **TOTAL SCORE (`/25`)** | **`/25`** | **`/25`** | **`/25`** |
| **Target Repo URL** | | | |
| **Chat Channel Link** | | | |
| **AI Policy Noted?** | `Yes / No` | `Yes / No` | `Yes / No` |

---

## 🎯 Step 3: Your 1–3 Meaningful PR Tracker

Remember Google's official Mentor Guide: maintainers look for **1 to 3 meaningful, well-understood pull requests**, not 40+ typo fixes.

| PR # | Organization / Repo | Issue / Bug Addressed | What Root Cause Did I Fix & Test? | Status (`Open` / `Reviewed` / `Merged`) | Link to PR |
| :---: | :--- | :--- | :--- | :---: | :--- |
| **1** | | | | | |
| **2** | | | | | |
| **3** | | | | | |
