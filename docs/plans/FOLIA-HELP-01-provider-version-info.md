# FOLIA-HELP-01 plan

1. Inspect installed CLI, actual feature branch and normalized provider metadata. Read repository README/testing rules.
2. Add behavior regressions for early missing-provider failure, help and no inferred recording classifications; observe RED.
3. Share the narrow usage preflight between CLI entry and command resolver. Update search table and renderer response with honest unknown metadata; align protocol/README examples.
4. Run the existing offline CLI suite, focused renderer behavior test and syntax checks. Preserve installed Folia and playback. Record that original/cover distinctions require verified upstream metadata.

Validation (2026-10-25): three new CLI cases were observed RED before implementation, then all 33 offline Node CLI tests passed. The focused renderer response test passed with the available Vitest 3.2.7 runner and a minimal external config; this is not a full run of the repository's Vitest 4 dependency environment. Node syntax checks and git diff whitespace checks passed. No full frontend typecheck/build/package run, live music search, playback or installed-app change was performed.
