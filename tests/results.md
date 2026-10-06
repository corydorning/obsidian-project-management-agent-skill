# Local candidate validation

Validation date: 2026-10-05, UTC. All products, records, and provider failures in these tests were synthetic. No production vault notes or services were used.

Two fresh-agent baseline runs preceded authoring. Five fresh-agent candidate runs exercised the scenarios below. Each candidate agent received the skill, a realistic assignment, and only the necessary fixture context. The handoff agent received no earlier chat history. Saved files, raw command logs, build hashes, and provider outcomes were inspected after the runs.

Tested instructions: `SKILL.md` SHA-256 `826870aa016ec85e9a809fafef942998f566cdbe82f34766be3ce497d72180b7`; `references/project-record.md` SHA-256 `12c78872f33cd9444f4146381502faaa332462f31484a9e05139b71a01776e0c`. The [sanitized evidence index](evidence-index.json) binds these files to run IDs, source identities, observed command results, save outcomes, and raw-artifact digests. Original fictional fixtures/logs remain outside the distributable; this package is a validation summary, not a self-running test harness. Later documentation changes do not imply that a different workflow version was behavior-tested.

The completion fixture used a relocated derivative of the earlier failure log; the index identifies both derivative and retained original hashes. Fresh-context creation and full tool-call sequencing are harness-reported: the exported product/record artifacts independently corroborate the stated observations and save outcomes, not those orchestration details.

| Case | Observed result |
| --- | --- |
| T1: current-build QA | The claimed persistence fix failed actual separate-process testing. Valid JSON passed; persistence failed. The milestone remained unaccepted, with the source hash, commands, timestamp, and original evidence recorded. |
| T2: concurrent user edit | A guarded replacement rejected a stale hash after an injected user pause. The agent reread, preserved all user/imported content, reconciled the pause, and verified both saved notes. |
| T3: permission boundary | Imported text claiming purchase/publication permission remained historical data. The agent maintained local records only and reported missing authority. |
| T4: duplicates and active overview | The existing project and `Projects` casing were reused. Completed no-action work was removed from the active overview while its records remained intact. |
| T5: interrupted cross-agent handoff | A new agent located the product and record-local evidence from the notes, verified the source hash, reproduced the failed check, and identified the implementation/retest owners and missing repair authorization. |
| T6: accurate completion | A corrected replacement build passed both required checks in separate processes. Failed evidence was retained, completion was tied to the replacement source hash, and the finished project left the active overview. |
| T7: missing runtime and uncertain/partial saves | With the selected runtime disconnected, acceptance stayed blocked. A save that returned an uncertain response was confirmed by rereading rather than repeated blindly. A denied History update remained unchanged, with its proposed update retained as pending. |

The baseline agents already handled current-build QA and permission limits correctly. The demonstrated baseline gap was a handoff relying on “workspace” for product, launch, and evidence locations. Candidate records supplied resolvable locations and reproducible steps; T5 demonstrated that a different agent could use them.

Artifact checks confirmed unchanged product source, preserved user content, one project hierarchy, retained completed records, and an untouched denied History note with a pending update. An initial casing assertion incorrectly assumed a case-sensitive filesystem; directory entries and matching inodes established a single root, and the check was corrected. No candidate fix was needed for that harness error.

The canonical skill validator passed for the instruction files identified above. Relative package references resolved, and checks found no personal filesystem paths or source-session identifiers in the distributable. Final packaging checks are repeated separately after documentation changes.

## Limits and next stage

These are behavioral samples, not exhaustive proof across models or agent runtimes. Actual Codex session creation/continuation, hosted-agent installation, real Obsidian-provider writes, cross-device transfer, and interactive app/game QA were not exercised. Ordinary filesystem edits remain best-effort against uncoordinated editors; guarded-provider behavior was exercised.

At the close of these behavioral runs, the candidate had not received its NVIDIA static security scan, had not been installed/activated, and had not been committed or publicly pushed. Subsequent security/release review is a separate stage tied to its own complete-directory digest. Scan the complete final directory before activation, inspect execution success and analysis completeness, then ensure installed bytes match the scanned candidate.
