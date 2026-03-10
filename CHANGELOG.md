# Changelog

All notable changes to the Tycana Claude plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-03-10

### Fixed
- `/tycana:morning` and `/tycana:review` now determine today's date and day of week from MCP response timestamps, preventing incorrect day references in briefings and reviews.
- `/tycana:upgrade` rewritten to work with Claude's plugin system (marketplace update + plugin update flow) instead of GitHub Releases.

## [1.0.0] - 2026-03-08

### Added
- Initial release.
- 5 commands: `/tycana:morning`, `/tycana:next`, `/tycana:review`, `/tycana:dump`, `/tycana:upgrade`.
- 2 background skills: `tycana-productivity` (smart capture, context-aware recommendations), `getting-started` (onboarding for new users).
- MCP server configuration for `https://app.tycana.com/mcp`.
