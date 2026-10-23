# Legacy homelab: GitHub Actions paused

All three workflow files have a `.yml.disabled` suffix, so GitHub Actions no longer discovers them as workflows after this change reaches the default branch. Infrastructure deployment, linting, and runtime image builds are disabled, including manual dispatch.

The definitions are preserved for reference during the gradual rebuild. To restore a workflow, review its triggers, credentials, and target infrastructure before restoring its `.yml` extension.

This change does not cancel already queued/running jobs, remove stored artifacts or caches, or suspend Flux on existing clusters. Flux reconciliation must be paused separately before retiring or repurposing the old infrastructure.
