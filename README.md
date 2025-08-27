# ARC Test Repository

This repository is used to test the GitHub Actions Runner Controller (ARC) self-hosted runners.

## Purpose
- Validate that ARC runners can be triggered from any repository in the panoai organization
- Test runner scaling from 0 to handle workflows
- Verify self-hosted runner labels work correctly

## Test Workflow
The `hello-world-arc.yml` workflow tests:
- Runner startup and basic functionality
- Runner environment information
- Scaling behavior (min: 0, max: 5)

## Runner Configuration
- **Labels**: `self-hosted`, `terraform`, `gke-cicd`
- **Node pool**: cicd-nodes (GKE)
- **Scaling**: 0-5 runners based on demand
- **Namespace**: arc-runners

## Usage
Trigger the workflow by:
1. Pushing to main branch
2. Manual trigger via GitHub Actions UI
3. Using GitHub CLI: `gh workflow run "Hello World ARC Test"`
