# Harbour context skeleton

Template repo for your private `harbour-context`.

This skeleton is intended to be edited.

Replace the placeholder paths, add your own skills, and commit the result as your own private context repo.

It is intentionally unopinionated. Keep what fits your workflow and change what does not.

Keep this harness inside the work directory you want Harbour to mount.

## Getting started

1. Fork `harbour-context-skeleton`

2. Clone your fork

```sh
git clone --depth 1 git@github.com:your-user/harbour-context-skeleton.git my-harbour-context
```

3. Update `AGENTS.md`

4. Keep the harness directory under the workspace path you will mount with Harbour

5. Remove `skills/example-skill/`

6. Add your own skills under `skills/`

7. Run `harbour provision`

Harbour will prompt for:

- `workspace_path`
- `harness_path`
- `codex` or `claude`
- The default `harbour` command
