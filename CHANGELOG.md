# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.0] - 2020-11-28

### Changed

- **BREAKING** List the full names of the GitHub repositories when using
  `--list` (thanks [@lfdebrux](https://github.com/lfdebrux) -
  [#8](https://github.com/erbridge/github-branch-renamer/pull/8))

## [0.2.4] - 2020-06-24

### Added

- Support dumping out a list of repositories that would be affected

## [0.2.3] - 2020-06-22

### Fixed

- Allow intentional pipefail when parsing query parameters (thanks
  [@lfdebrux](https://github.com/lfdebrux) -
  [#5](https://github.com/erbridge/github-branch-renamer/pull/5))

## [0.2.2] - 2020-06-22

### Fixed

- Fix binary flag options `--force` and `--dry-run`, again (thanks
  [@lfdebrux](https://github.com/lfdebrux) -
  [#6](https://github.com/erbridge/github-branch-renamer/pull/6))

## [0.2.1] - 2020-06-21

### Fixed

- Added `pipefail` option to catch errors in pipes (thanks
  [@rjw1](https://github.com/rjw1) -
  [#4](https://github.com/erbridge/github-branch-renamer/pull/4))

## [0.2.0] - 2020-06-15

### Added

- Support for running for GitHub teams only (thanks
  [@lfdebrux](https://github.com/lfdebrux) -
  [#3](https://github.com/erbridge/github-branch-renamer/pull/3))

### Fixed

- Fix binary flag options `--delete`, `--force`, and `--dry-run` (thanks
  [@lfdebrux](https://github.com/lfdebrux) -
  [#1](https://github.com/erbridge/github-branch-renamer/pull/1))

## [0.1.0] - 2020-06-14

Initial release.

[unreleased]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.3.0...HEAD
[0.3.0]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.2.4...v0.3.0
[0.2.4]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.2.3...v0.2.4
[0.2.3]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.2.2...v0.2.3
[0.2.2]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.2.1...v0.2.2
[0.2.1]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.2.0...v0.2.1
[0.2.0]:
  https://github.com/erbridge/github-branch-renamer/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/erbridge/github-branch-renamer/releases/tag/v0.1.0
