# Raindrop business verification

The independent catalog stages the Raindrop YAML and business-specific
verification scripts from the exact reviewed Engine baseline. The tests run
offline without credentials, deployment or trusted publisher permissions.

Optional `npm run raindrop:discover` and `npm run raindrop:manual` invoke
real MCP services only when an operator supplies the required access token;
catalog CI and the trusted Engine publisher never execute these commands.

Legacy Engine files are preserved until publisher activation, nonterminal Run
continuity and rollback are verified. The scheduled verification wrapper and bounded 09:00/D1 verification helper
are also staged in this catalog. `npm run raindrop:scheduled` requires
operator-supplied Cloudflare/GitHub/MCP tokens and checks read-only evidence
against the existing deployment; it is **never run by catalog CI or the
trusted Engine publisher**. The engine retains the previous copies and static
registry until verified protected publication, old-Run continuity and rollback.

This source-only Draft PR does not establish T11 completion or production release.
