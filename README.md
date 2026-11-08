# 🛠️ The GSoC Engineer's Runbook

> **Stop watching roadmaps. Go build a repo locally.**
>
> A no-fluff, evidence-backed engineering runbook for **Google Summer of Code (GSoC)** — built from official Google Open Source statistics, mentor mailing-list discussions, and real maintainer evaluation criteria.

---

## 📂 What's Inside This Runbook

| File | Description |
| :--- | :--- |
| [**`01-org-shortlist-checklist.md`**](./01-org-shortlist-checklist.md) | **The 5-Point Organization Shortlist Checklist & Scoring Matrix** — evaluate and narrow 180+ orgs down to **2 target repositories** you can actually build locally. |
| [**`02-maintainer-message-templates.md`**](./02-maintainer-message-templates.md) | **Maintainer Issue, PR & Chat Templates** — exact templates for public channels (Matrix/Zulip/Discord) and GitHub issues so you never send `"Please assign to me"` spam. |
| [**`03-proposal-skeleton.md`**](./03-proposal-skeleton.md) | **The GSoC Engineering Proposal Skeleton** — structured around your **1–3 meaningful PRs**, technical design, weekly milestones, and anti-AI-spam compliance. |
| [**`04-git-and-local-setup-cheatsheet.md`**](./04-git-and-local-setup-cheatsheet.md) | **Git Rebasing & Codebase Navigation Cheatsheet** — upstream sync, interactive rebase (`git rebase -i`), reading tests first, and tracing unfamiliar repos. |

---

## 📊 The Reality Check (Official Data)

Before writing a single line of a proposal, understand the numbers and how maintainers actually select contributors:

- **2026 Acceptance Rate**: **15,245 applicants** submitted **23,371 proposals** across **184 organizations** — only **1,141 contributors** were accepted (**~7.48% of applicants** / **~4.88% of proposals**, **92.5% rejected**).
- **Beginners Are the Target Audience**:
  - In GSoC 2025, **92.32%** of accepted contributors were doing GSoC for the **very first time**.
  - **43.04%** had **zero prior open-source contributions** before starting their GSoC preparation.
  - Google's official FAQ defines a beginner as someone with **fewer than 10 issues/PRs** across open source.
- **Not an Internship or Recruiting Pipeline**: GSoC is an open-source mentorship program run by **volunteer maintainers and engineers**, not HR recruiters. Your resume, college tier, and LeetCode rating do not get you selected — **working code and clear public communication do**.
- **India Stipends (PPP-Adjusted)**:
  - **Small (~90 hours)**: `$750 USD`
  - **Medium (~175 hours)**: `$1,500 USD`
  - **Large (~350 hours)**: `$3,000 USD`
  - Paid in two installments: **45%** after passing the midterm evaluation + **55%** after passing the final evaluation.

---

## 🚦 The 3 Self-Check Questions (Ask Yourself Today)

Before shortlisting any organization, verify that you can answer **YES** to all three:

1. **Can I build a small project in my primary language without following a step-by-step video tutorial?**
2. **Am I comfortable with Git branching, rebasing (`git rebase`), and resolving merge conflicts?**
3. **Can I dedicate 8–10 focused hours per week consistently from November/December through March?**

> If any answer is **No**, spend **2 focused weeks** fixing that gap first (see [`04-git-and-local-setup-cheatsheet.md`](./04-git-and-local-setup-cheatsheet.md)), then start Step 3 below.

---

## 🗺️ The 5-Step Execution Plan

1. **Lock In 1 Real Tech Stack**: Pick a language/framework you can already write and debug independently. Never learn a brand-new language and a brand-new 100k-line codebase at the same time.
2. **Master Git Workflows**: Practice forks, feature branches, interactive rebasing, and reading test suites.
3. **Shortlist 2 Organizations from the GSoC Archive**: Use [`01-org-shortlist-checklist.md`](./01-org-shortlist-checklist.md) in November/December — **do not wait until the February org announcement** when thousands of applicants flood the chat channels.
4. **Build 1 Target Repository Locally This Week**: Clone the repo, run the test suite, break something intentionally, and trace how the modules connect.
5. **Ship 1–3 Meaningful PRs & Communicate in Public**: Follow [`02-maintainer-message-templates.md`](./02-maintainer-message-templates.md) and draft your proposal early using [`03-proposal-skeleton.md`](./03-proposal-skeleton.md).

---

## 🤖 Rules on Using AI (Don't Get Flagged as Spam)

Maintainers are flooded with LLM-generated proposals and automated PR spam. Follow these boundaries strictly:

| ✅ Smart Engineering Use of AI | ❌ Instant Disqualification (AI Spam) |
| :--- | :--- |
| Explaining unfamiliar files, call graphs, or error stack traces locally | Copy-pasting ChatGPT/Claude to generate or "rephrase" your project idea description |
| Helping you locate which test file covers a module | Submitting automated typo/whitespace PRs or unverified AI-generated diffs you cannot explain |
| Reviewing your own draft for clarity **after** you write the technical design | Violating org-specific AI policies (e.g., SymPy's strict *"No AI used for the application"* rule) |

---

## 🔗 Official Sources & References Referenced in the Video

1. **GSoC 2026 Accepted Contributors & Statistics (`15,245` applicants, `23,371` proposals, `1,141` accepted)**:  
   https://opensource.googleblog.com/2026/04/the-journey-begins-meet-the-2026-gsoc-contributors.html
2. **GSoC 2025 Contributor Statistics (`43.04%` first-time OSS, `92.32%` first GSoC)**:  
   https://opensource.googleblog.com/2025/08/google-summer-of-code-2025-contributor-statistics.html
3. **Official GSoC FAQ (Eligibility, `<10` PRs beginner definition, up to 3 proposals / max 1 accepted)**:  
   https://developers.google.com/open-source/gsoc/faq
4. **Official GSoC Contributor Stipends (PPP table & 45% / 55% evaluation split)**:  
   https://developers.google.com/open-source/gsoc/help/student-stipends
5. **Official GSoC Timeline**:  
   https://developers.google.com/open-source/gsoc/timeline
6. **Google GSoC Mentor Guide — Handling AI-Generated Spam Proposals (`1–3` meaningful PRs)**:  
   https://developers.google.com/open-source/gsoc/resources/spam_proposals
7. **Eclipse `soc-dev` Mentor Call — *"Managing AI Spam and Influx of Applicants"***:  
   https://www.eclipse.org/lists/soc-dev/msg01018.html
8. **SymPy GSoC Mailing List — *"No AI used for the application"* Policy**:  
   https://groups.google.com/g/sympy/c/CY2VTl6Eg48
9. **MediaWiki Talk Page — Why Quality Beats Quantity (`~47 PRs` discussion)**:  
   https://www.mediawiki.org/wiki/User_talk:Pavithraes
10. **Tier-3 MCA Student Selected in GSoC 2026 on 3rd Attempt (Tarun Singh)**:  
    https://dev.to/tarunsinghofficial/how-i-got-into-google-summer-of-code-gsoc-2026-as-a-tier-3-mca-student-4017

---

## 📄 License

Released under the [MIT License](./LICENSE). Feel free to fork this repository and use the checklists and templates to track your GSoC journey!
