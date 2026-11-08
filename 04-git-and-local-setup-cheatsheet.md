# 🔧 Git Rebasing & Large Codebase Navigation Cheatsheet

> **Step 2 & Step 4 of the Action Plan**: How to navigate a 100,000-line repository without getting overwhelmed, and the exact Git workflow maintainers expect on every Pull Request.

---

## 🧭 Part 1: How to Read a Large Unfamiliar Codebase in 60 Minutes

Do **not** try to read a repository from top to bottom. Use this 4-step surgical loop:

1. **Run the Test Suite First**:
   - Tests are executable documentation. Run a single test file with verbose output (`pytest -v tests/test_xyz.py` or `npm test -- test_xyz`) to see how objects are initialized and called.
2. **Search by UI String, CLI Flag, or Error Message (`git grep` / `rg`)**:
   - Find the exact entry point for an issue in 2 seconds:
     ```bash
     git grep -n "exact_error_or_flag_name"
     ```
3. **Add a Intentional Breakpoint or `print` / `console.log`**:
   - Change 1 line in the suspected function, re-run the single test, and watch it fail. Now you have 100% proof that your local code path is active.
4. **Read `git log -p -n 5 <file>`**:
   - See the last 5 commits that touched that file and which PRs they belonged to. Copy the coding style, test style, and commit message convention of those merged PRs.

---

## 🌿 Part 2: The Clean Open-Source Git Workflow

### 1. Fork, Clone & Add `upstream`
```bash
# Clone your fork
git clone https://github.com/<your-username>/<repo>.git
cd <repo>

# Add the official organization repo as 'upstream'
git remote add upstream https://github.com/<org-name>/<repo>.git
git remote -v
```

### 2. Never Work on `main` — Create a Focused Branch
```bash
git fetch upstream
git checkout -b fix/issue-1234-null-cursor upstream/main
```

### 3. Keep Your Branch Clean with `git rebase` (No Messy Merge Commits)
When `upstream/main` moves forward while your PR is open, rebase your branch cleanly instead of creating `"Merge branch 'main' into..."` commits:
```bash
git fetch upstream
git rebase upstream/main
```
If a conflict occurs:
```bash
# 1. Open the conflicted file(s) and resolve the conflict markers
# 2. Stage the resolved file(s):
git add <resolved-file>
# 3. Continue the rebase:
git rebase --continue
# (Or abort safely at any time with: git rebase --abort)
```

### 4. Squash WIP Commits Before Requesting Review (`git rebase -i`)
Maintainers do not want to see 12 commits named `"wip"`, `"fix typo"`, `"try again"`. Squash them into 1 atomic commit:
```bash
git rebase -i upstream/main
# Keep 'pick' on the first commit, change subsequent WIP commits to 'squash' (or 's'), and write a clean commit message.
git push --force-with-lease origin fix/issue-1234-null-cursor
```

---

## ✅ Pre-PR Self-Review Checklist

Before clicking **Create Pull Request**, verify every box:

- [ ] Does `git diff upstream/main` contain **only** the lines needed for this fix (zero stray formatting changes, zero `.env` or IDE config files)?
- [ ] Did I add or update a unit test that **fails without my fix** and **passes with my fix**?
- [ ] Did I run the linter/formatter required by `CONTRIBUTING.md`?
- [ ] Can I explain every single line of my diff in plain English if a mentor asks why I wrote it that way?
