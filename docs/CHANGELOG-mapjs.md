# Mapjs Project Change Log

## mapjs 3.3.7

- `docs/CHANGELOG-mapjs.md`: Clean up history.

## mapjs 3.3.6

- Version 3.4.0 because latest mapjs tag is 3.3.6
- Add cumulative mapjs bugfixes:
- Fix add parent reason issue:
  - `test/start.js`: Errors sent to console.error, rather than alert which was incredibly annoying!
  - Fix toolbar buttons by restoring `src/browser/map-toolbar-widget` related code which was removed in commit 'initial jquery 3 migration' (`b2768ac`).
  - `src/core/content/content.js`: Fix reject call syntax which caused unrecognised function '_' error.
- `package.json`:
  - Add testcafe module for automated testing using chrome devtools recordings.
  - Add alias script keys to align with npm lifecycle as described in: <https://docs.npmjs.com/cli/v8/using-npm/scripts>
- Update .gitignore
- Add `package-lock.json` to repo.

## mapjs 3.3.5

- Fork of [mindmup/mapjs](https://github.com/mindmup/mapjs)

----------------

Uses [Semantic Versioning 2.0.0](https://semver.org/) and [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/).
