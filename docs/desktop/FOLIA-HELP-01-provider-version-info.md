# FOLIA-HELP-01 — Online ID usage and honest recording versions

Base: existing `feat/control-mcp-cli` branch at 2fb91b6, not main. Source main has no control CLI; this patch depends on that feature branch.

- Online `play --id` requires explicit nonempty `--provider`; help shows both together. Missing provider is a usage error before token-file reads, discovery, transport or playback. Query play and `library play <local-id>` retain their existing routes.
- Search results show a VERSION column and each renderer search item includes `recordingVersion: 'unknown'`. The current normalized SongResult/UnifiedSong and provider metadata contracts carry no reliable original/cover assertion. Unknown is explicit; title, artist, aliases, album art and platform-specific unrelated flags do not establish originality.
- No original/cover classification is added without a verified provider field and end-to-end contract/tests. The unknown marker documents the present capability gap; it does not claim classification is now available.
- Raw JSON stays the server response; older servers lacking the new field still render unknown in the human table. No live provider searches, application restarts, playback changes or installed file edits are needed to validate this patch.

Acceptance: malformed ID play fails without touching an invalid token path or unreachable endpoint; valid provider ID and local library mappings remain correct; --help states the provider requirement; names containing Original/Cover stay unknown; full offline CLI suite passes.
