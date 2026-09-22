# Workflow Catalog

Independent, Git-owned workflow definitions for [lirtual/mcp-workers](https://github.com/lirtual/mcp-workers), governed by the v0.2 approved specification (PR #148) and T09/T11 acceptance (Issues #157 and #159).

## Boundary

- `workflows/*.yaml` holds declarative workflow definitions. Business-specific test fixtures may live in separate non-executable directories.
- The trusted publisher **runs from the engine repository**, checks this repository's numeric GitHub ID and an exact reviewed commit SHA, and validates a canonical digest and approved policy before any stage/activation.
- Catalog contents never receive engine admin authority, runtime credentials, GitHub Actions publisher permissions, or arbitrary code-execution rights.
- Do not add credentials, tokens, personal data, private endpoint values, runnable publisher scripts or privileged workflows.
- A catalog YAML change does not itself deploy an engine, activate a definition or authorize a new production Run.

## Operational status

This repository's initial setup is not evidence that GitHub branch protection, owner approval, source-digest equivalence, isolated testing or real platform publication has passed. The existing Cloudflare Worker may be used as a **live test target by explicit owner permission**, subject to a recorded backup, safe policy checks and separately authorized production release. No production Cron change or upstream write is approved by repository creation.

See the engine [T09 issue](https://github.com/lirtual/mcp-workers/issues/157) and its trusted publisher runbook for the exact publication sequence.
