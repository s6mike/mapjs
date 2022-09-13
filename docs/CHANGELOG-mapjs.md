# Mapjs Project Change Log

## mapjs 3.3.16

- Move environment variables from `scripts/mapjs.env` to external file to simplify git bisect process.

## mapjs 3.3.15

- Enable cut/copy/paste:
  - Undo changes made in commit 'remove internal clipboard, to be replaced with browser clipboard actions' (925dc863d260f2d02c65f490617ebd328be8553).
  - [README.md](README.md): Add keyboard shortcuts for cut/copy/paste.

## mapjs 3.3.14

- `src/browser/dom-map-widget.js`:
  - Add missing keyboard shortcuts (hotkeyEventHandlers) for zoom in/out/reset, from commit 'connector removed, node removed' (75d00a37c585a0c564ff30b493078db80bc6b40e).
    - Add comment for copy/cut/paste, since functions have since been removed from codebase.
    - [README.md](README.md): Add keyboard shortcuts for zoom.

## mapjs 3.3.13

- [README.md](README.md):
  - Add table listing keyboard shortcuts.
  - Fix lint issues (from [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)).

## mapjs 3.3.12

- `src/browser/dom-map-widget.js`:
  - Fix undo/redo keyboard shortcuts, removed in commit 'move undo/redo hotkeys to menus' (9fe20371f6f64051f043f546269227103935abed).

## mapjs 3.3.11

- `scripts/mapjs.env`:
  - Add `PATH_REPLAY_SCRIPT_BUTTON_UNDO_REDO` and `PATH_REPLAY_SCRIPT_KEYS_UNDO_REDO` for new devtools recording.
  - Update diff file name in variable.
  - Update destination folder for expect path variable.

## mapjs 3.3.10

- Align with argmap changes.

## mapjs 3.3.9

- `src/core/map-model.js`: Fix left click on node to select (introduced in commit 'moved addLinkMode out of mapModel' 354071624edb6c257441fcdfcb3f11ab92ad395e).
  - Relevant function `clickNode` triggered by `mouseup`: `button` value wasn't used, so test `which` value instead.

## mapjs 3.3.8

- Merge fixes from stash 'All mapjs fixes up to toolbar': just a settings.json with bash terminal init file.
- Add 'scripts/mapsjs.env' to hold new environment variables: PATH_LOG_FILE_EXPECT, PATH_REPLAY_SCRIPT, PATH_REPLAY_SCRIPT_ADD_IDEA, PATH_BISECT_PATCH_FILE

## mapjs 3.3.7

- `docs/CHANGELOG-mapjs.md`: Clean up history.

## mapjs 3.3.6

- Version 3.4.0 because latest mapjs tag is 3.3.6
- Add this Change Log file.
- Add cumulative mapjs bugfixes:
  - Fix add parent reason issue.
  - `test/start.js`: Errors sent to console.error, rather than alert which was incredibly annoying!
  - Fix toolbar buttons by restoring `src/browser/map-toolbar-widget` related code which was removed in commit 'initial jquery 3 migration' (`b2768ac`).
  - `src/core/content/content.js`: Fix reject call syntax which caused unrecognised function '_' error.
- `package.json`:
  - Add TestCafe module for automated testing using chrome devtools recordings.
  - Add alias script keys to align with npm lifecycle as described in: <https://docs.npmjs.com/cli/v8/using-npm/scripts>
- Update .gitignore
- Add `package-lock.json` to repo.

## mapjs 3.3.5

- Fork of [mindmup/mapjs](https://github.com/mindmup/mapjs)

----------------

Uses [Semantic Versioning 2.0.0](https://semver.org/) and [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)
