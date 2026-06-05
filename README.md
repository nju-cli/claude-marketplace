# NJU CLI Claude Cowork Marketplace

This repository is the Claude Cowork plugin for `nju-cli`.

## Structure

- `.claude-plugin/plugin.json`: Plugin metadata.
- `skills/nju-cli`: Cowork skills for NJU services.
- `bin/`: Packaged `nju-cli` release binaries (populated by CI).
- `scripts/`: Cross-platform wrappers for invoking the packaged binary.

## CLI Releases

The `nju-cli` binary is built and released from <https://github.com/nju-cli/nju-cli>.

After a tagged release, `sync-cli-binaries.yml` downloads the release artifacts, unpacks them into `bin/`, and commits the result.

To trigger that sync automatically from `nju-cli/nju-cli`, set a `MARKETPLACE_SYNC_TOKEN` secret in the source repository with permission to run workflows and push contents in `nju-cli/claude-marketplace`.
