# .allstar — honua-io org security policy

Org-wide [OpenSSF Allstar](https://github.com/ossf/allstar) configuration. The Allstar app
is installed across honua-io; these files define which policies it enforces.

- **Strategy:** opt-out — policies apply to every repo except those listed in
  `allstar.yaml` `optOutRepos` (archived/non-dev repos).
- **Action:** `issue` for all policies — Allstar files a tracking issue on drift; it does
  **not** modify repos. Escalate specific policies to `fix` later if desired.

| Policy | File | Checks |
|---|---|---|
| Branch Protection | `branch_protection.yaml` | PR required, ≥1 approval, no force-push |
| Binary Artifacts | `binary_artifacts.yaml` | No checked-in binaries |
| Outside Collaborators | `outside.yaml` | No outside admin/push |
| Security Policy | `security.yaml` | SECURITY.md present (org default via `.github`) |
| Dangerous Workflow | `dangerous_workflow.yaml` | Risky Actions patterns |

Managed as part of the Phase 1 security program (honua-compliance #7).
