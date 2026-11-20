# GEMINI.md - Project Agent Guidelines

## 1. Repository Structure
- `README.md`: Project overview and documentation
- `GEMINI.md`: Project agent guidelines for Gemini CLI and Continuous AI workflows
- `feature_list.json`: Task tracking list for multi-session continuity
- `progress.txt`: Session-by-session work log and handoff notes
- `.github/workflows/gemini-continuous-ai.yml`: Automated daily inspection and on-demand `@gemini-cli` workflow

## 2. Build & Test Verification Rules
- Always run relevant build, lint, and test checks before proposing changes.
- Do not mark a task as passing unless all verification steps succeed without errors.
- Document any missing tests or verification gaps in an issue or Draft PR.

## 3. Core Working Principles
- **One Independent Task Per Session**: Focus on a single, self-contained task per session to keep changes small, reviewable, and easy to revert.
- **No Auto-Merge**: Never automatically merge pull requests. All changes require human review and explicit approval.
- **Draft PRs Only**: When proposing code or documentation changes via automation, always create a **Draft Pull Request** targeting `master`.

## 4. Session Continuity (`feature_list.json` & `progress.txt`)
- After completing or pausing any task, update `feature_list.json` with the latest task `status` (`"failing"`, `"in_progress"`, or `"passing"`) and notes.
- Append a dated entry to `progress.txt` summarizing what was done, verification results, and clear handoff notes for the next session.
