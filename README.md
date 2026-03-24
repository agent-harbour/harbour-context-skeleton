# harbour-context-skeleton

Template repo for your private `harbour-context`.

This skeleton is intended to be edited.

Replace the placeholder paths, add your own skills, and commit the result as your own private context repo.

It is intentionally unopinionated. Keep what fits your workflow and change what does not.

## Getting started

- Create a new `harbour-context` directory from this repo

```sh
git clone --depth 1 git@github.com:agent-harbour/harbour-context-skeleton.git harbour-context
rm -rf harbour-context/.git
```

- Configure `runtime.env`

`WORKSPACE_ROOT` is the workspace path on the host. The same path is mounted
inside the VM.

```sh
WORKSPACE_ROOT=/Users/your-user/git
```

- Update `repos.yaml` with the repos you want mounted
- Remove `skills/example-skill/`
- Add your own skills under `skills/`
- Commit it as your own repo if you want to keep your context in Git
