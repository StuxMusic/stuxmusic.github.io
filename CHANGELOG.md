# Changelog

All notable changes to stuxmusic.github.io are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-1

### Added

- A `test` branch: work happens there (or on a branch off it), and changes reach `main` only through a pull request from `test`, reviewed and merged by Leo. CONTRIBUTING has a new Branches section, and the README's Versioning section says so
- A CI workflow (`.github/workflows/ci.yml`) running `tests/version.sh` on pushes to `main` and `test` and on pull requests, so a pull request into `main` has a check to pass

### Changed

- `commit.sh` and `commit.bat` say to push `test` with its tags and open a pull request into `main`, instead of pushing `main`

## v26.11.06

### Changed

- The README describes this repo as what it is, Stux.Music's own GitHub Pages redirect to github.com/StuxMusic, instead
  of a generic "redirect your username.github.io" template with `example.com` setup steps
- The README and CONTRIBUTING logos follow GitHub's light or dark theme (`<picture>` with the brand's `logo-light`/`logo-dark` files)
- The README's footer uses the current Stux.Music footer, and its License section is now a Copyright section naming Stux.Group

### Removed

- The README's claim that the redirect preserves URL paths: the meta refresh always goes to github.com/StuxMusic

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.2
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v1.0.2

### Added
- `.gitignore` for OS/editor cruft, local `.env` overrides, and `node_modules/`

## v1.0.1

### Fixed
- GitHub Pages was using the legacy branch-deploy build system, which can silently stop auto-deploying with no error recorded anywhere (discovered on SeasonalOverlaysLibrary — its live site served stale content for over an hour with no visible failure). Switched to GitHub Actions-based Pages deployment (`.github/workflows/pages.yml`), making every deploy an ordinary, observable CI run instead.

## v1.0.0

### Added
- Initial GitHub Pages redirect repo for Stux.Music, redirecting `stuxmusic.github.io` to `github.com/StuxMusic` — `VERSION.md`/`CHANGELOG.md`/`CONTRIBUTING.md`/`commit.sh`+`commit.bat` added, following the standard release-flow convention used across other Stux.Group family repos.
