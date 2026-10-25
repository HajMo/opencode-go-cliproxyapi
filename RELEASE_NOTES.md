## What's Changed

### Bug Fixes

- Default `base-url` is now `https://opencode.ai/inference/go/v1`, the endpoint used by the current OpenCode Go docs. The legacy `https://opencode.ai/zen/go/v1` still works and can be set explicitly.
- Upstream requests (completions, messages, responses and catalog refresh) now send `User-Agent: opencode-go-cliproxyapi/<version>` instead of the host's generic `Go-http-client/1.1`, as OpenCode Go asks clients to identify themselves.

### Build

- Release builds use the latest patched Go 1.27 toolchain (fixes GO-2026-6613 in `net/http` present in Go 1.27.0).
- GitHub Actions are pinned to commit SHAs, and workflow permissions are read-only except for the release job.
- Dropped the windows/arm64 and freebsd/amd64 builds, which depended on a third-party cross-compilation action.

## Upgrade Notes

- Replace the old plugin binary with the new release binary.
- Restart CLIProxyAPI after replacing the plugin.
- Ensure `plugins.configs.opencode-go-cliproxyapi.enabled: true` is set; CLIProxyAPI leaves plugins disabled by default.

**Full Changelog**: https://github.com/HajMo/opencode-go-cliproxyapi/compare/v0.2.2...v0.2.3
