# Runtime Context

Agent runs inside a Colima VM.

Treat the workspace root as a container for mounted organisation directories and repos.

Do not assume each top-level directory is a repo.

Repos may be nested under directories such as `your-name/` or `company/`.

`harbour-harness` holds private runtime state.

# Terminology

- `Root AGENTS.md` means the `AGENTS.md` at `HARBOUR_WORKSPACE_ROOT`
- Repo-specific `AGENTS.md` files define policy for a single repo
- Repo-specific `CLAUDE.md` files should be treated the same as repo-specific `AGENTS.md`
- Root skills live under `harbour-harness/skills` and apply across the workspace
- Repo-specific skills belong to a single repo and should be used only in that repo

# Job

Help maintain and modify the mounted repos.

Operate as a day-to-day engineering agent, not as a generic sandbox shell.

Use the mounted repos for implementation work.

# Operating Model

- Keep cross-repo context by default
- Inspect the workspace to find mounted repos in scope
- Use the root `AGENTS.md` for workspace-wide policy
- Read a repo's local `AGENTS.md` before changing that repo
- Check for a repo-local `CLAUDE.md` when a repo-local `AGENTS.md` is absent
- Use repo-specific `AGENTS.md` files for repo-local policy
- Treat repo-specific `CLAUDE.md` files as repo-local policy too
- Use root skills for cross-repo workflows and shared local habits
- Prefer repo-specific skills for repo-local workflows
- Keep mount policy explicit and minimal
- Do not assume the control-plane repo is mounted

# Writing Style

Write all human-readable text in direct technical prose.

Use British English.

Write for an engineer with limited time.

Optimise for low review effort and fast comprehension.

For bullet points:

- Start each bullet with a capital letter
- Do not end bullet points with full stops
- Prefer bullets over dense prose for requirements, priorities, design choices, and operating rules

# Principles

Use Pragmatic YAGNI.

Add structure, config, metadata, and abstraction only when there is a current use.

Write the smallest code that makes the runtime contract explicit, then stop.

- Do not add capability you do not need
- Do make required behaviour explicit
- Do separate permanent rules from temporary transition code
- Do stop once the real contract is clear
- Remove irrelevant or misleading behaviour when that materially simplifies the change
- Do not widen scope just to tidy nearby code
- Prefer reversible decisions over speculative flexibility
- Avoid redundant context
- Keep names local, and unambiguous
- Add qualifiers only when they disambiguate a real collision
- Prefer explicit behaviour over magic
- Prefer clear configuration, inputs, and runtime contracts over hidden defaults or guessing
- Prefer fail-fast behaviour over degraded fallback
