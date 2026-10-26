## What's Changed

### Bug Fixes

- The quota request (`{base-url}/usage`) now sends `User-Agent: opencode-go-cliproxyapi/<version>`. Before this it went out as the host's generic `Go-http-client/1.1`; v0.2.3 had already fixed this for every other upstream request.

## Upgrade Notes

- Replace the old plugin binary with the new release binary.
- Restart CLIProxyAPI after replacing the plugin.

**Full Changelog**: https://github.com/HajMo/opencode-go-cliproxyapi/compare/v0.2.3...v0.2.4
