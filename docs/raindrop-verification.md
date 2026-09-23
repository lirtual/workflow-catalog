# Raindrop business verification

The independent catalog stages the Raindrop YAML and business-specific
verification scripts from the exact reviewed Engine baseline. The tests run
offline without credentials, deployment or trusted publisher permissions.

Optional `npm run raindrop:discover` and `npm run raindrop:manual` invoke
real MCP services only when an operator supplies the required access token;
catalog CI and the trusted Engine publisher never execute these commands.

Legacy Engine files are preserved until publisher activation, nonterminal Run
continuity and rollback are verified. The scheduled verifier still depends on
the Engine's generic scheduling helper and has not been migrated. This
source-only Draft PR does not establish T11 completion or production release.
