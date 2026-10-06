# Obsidian Project Management Agent Skill

A portable skill for taking an authorized software, app, or game project from an agreed outcome through milestones, implementation, actual-product QA, and repair/retest loops. Obsidian Markdown records provide continuity across agents and sessions.

The core works with ordinary authorized product and Markdown tools. Dot/Codex session creation and reuse are covered by an optional adapter. Missing tools or write access are reported as limitations; the skill does not provide them.

## Package

- `SKILL.md`: project-management workflow.
- `references/project-record.md`: current contract, history, evidence, and resume format.
- `references/codex.md`: optional session coordination.
- `tests/scenarios.md`: synthetic behavioral validation cases.
- `tests/results.md`: observed local validation results and limits.
- `tests/evidence-index.json`: tested instruction hashes and sanitized synthetic-run evidence.

## Use

Install the complete folder through your agent's supported skill route after reviewing and scanning it. Invoke `obsidian-project-management-agent-skill` with the intended outcome, existing project or repository, chosen environment, and authorized vault destination.

Example: “Manage my offline checklist project through its agreed acceptance checks. Reuse its existing records and implementation owner, test the current product, and keep its Obsidian notes ready for another agent to resume.”

The agent inspects the actual folder casing and existing projects first. New projects use `Projects/<project-name>/Project.md` and `History.md` unless the vault already has a different established destination.

Local Codex installation and another agent's hosted Skills workspace are separate operations. Installing in one does not confirm installation in the other.

This package uses independently written instructions and templates and is released under the [MIT License](LICENSE).

## Validation and limits

Behavioral validation used fictional projects only. The [results](tests/results.md) and [evidence index](tests/evidence-index.json) describe cross-agent resume, interrupted work, duplicate avoidance, actual-build QA/retesting, guarded concurrent edits, partial saves, and permission boundaries. They are a validation summary, not a publicly reproducible test suite.

Release review on 2026-10-06 used the existing owner-maintained NVIDIA SkillSpector 2.12.0 with local repairs and `--no-llm`. Static execution succeeded and inspected all bundled files, with no analyzer failures. The result remains **CAUTION**, score **11 / LOW**, with two **MEDIUM** entries for the same pattern and **partial overall completeness**. The entries match “without confirmation” in this summary and inside the adapter's prohibition on unsupported claims. The completeness exception treats a runtime project-note output path as an absent bundled file. These were reviewed as benign in context and remain unsuppressed. Semantic/LLM analysis was not run. These results do not guarantee safety; scan the complete version you intend to install and inspect its own report.

Independent review found no material workflow or privacy defect and matched the reported synthetic evidence. Live Obsidian writes, Codex session creation/continuation, hosted-agent installation, cross-device transfer, and interactive app/game QA remain untested. The skill supplies neither service access nor additional permissions.
