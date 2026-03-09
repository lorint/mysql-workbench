# AGENTS.md

## Goal
Create and maintain GitHub Actions workflows for this repository.

## Build target
- Platform: x64
- OS: Windows
- CI system: GitHub Actions
- Primary deliverable: .github/workflows/build_assets.yml

## Requirements
- Inspect the repository before writing YAML.
- Detect the real solution and project names instead of assuming paths.
- Prefer official Visual Studio / MSBuild setup on GitHub-hosted Windows runners.
- Use PowerShell for Windows-specific steps.
- Preserve existing configuration names if they already exist in the solution.
- If dependencies are missing on GitHub runners, add explicit setup steps.
- Explain all assumptions in comments or in the task summary.
- Do not invent paths, filenames, or configuration names without checking the repo.
- Surface blockers instead of inventing success.

## Validation
- Verify the solution path exists.
- Verify the selected configuration/platform pair exists.
- Verify any referenced tools or SDKs are installed in CI, or add steps to install them.
- Keep the workflow minimal but runnable.
