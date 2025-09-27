# Repo B (ETLDeploy)

This repository receives JSON interface files from the ModelDeploy repository via GitHub Actions.

## Auto-synced Files

The following files are automatically synced from `ModelDeploy/output/interfaces/` to `app/mapping/`:

- MODELZ2_states.json
- MODELZ2_params.json
- MODELZ2_outputs.json
- MODELZ2_mapping.json
- MODELZ2_inputs.json

## Sync Process

1. When files are pushed to `ModelDeploy/output/interfaces/`
2. GitHub Actions workflow triggers automatically
3. Files are copied to this repository's `app/mapping/` folder
4. Changes are committed and pushed automatically

## Setup Requirements

The source repository (ModelDeploy) needs:
- A GitHub Personal Access Token with repo permissions
- Token stored as `REPO_ACCESS_TOKEN` secret
- Workflow configured to target this repository