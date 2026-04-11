# Harbour harness template

Template repo for your private `harbour-harness`.

This template is intended to be edited.

Replace the placeholder paths, add your own skills, and commit the result as your own private harness repo.

It is intentionally unopinionated. Keep what fits your workflow and change what does not.

## Getting started

1. Fork `harbour-harness-template`

2. Clone your fork

```sh
git clone --depth 1 git@github.com:your-user/harbour-harness-template.git my-harbour-harness
```

3. Update `AGENTS.md`

4. Update `repos.yaml` with the repo `host_path` entries you want mounted

   Example:

   ```yaml
   repos:
     - host_path: ./your-org/frontend
     - host_path: ./your-org/backend
     - host_path: ./your-org/lambdas
   ```

   Relative `host_path` values are resolved from the `workspace_root` you enter during `harbour provision`

5. Remove `skills/example-skill/`

6. Add your own skills under `skills/`

7. Run `harbour provision`

Harbour will prompt for:

- Path to your harness
- Workspace root
- Agent to provision
- The default `harbour` command
