# Changelog

All notable changes to the CCPL VS Code extension are documented here. The
format follows Keep a Changelog, and versions follow Semantic Versioning.

## [0.4.0] on November 24, 2026

### Added

* Highlighting for `extern`, `from`, and `as`.
* Highlighting for `pyexec`, `pyeval`, and the `cstr` type.
* Decimal string escapes in the string pattern.

### Changed

* Version aligned with the compiler release.
* Release workflow publishes only on version tags.

## [0.3.0] on September 21, 2026

### Added

* GitHub Actions build workflow that packages the extension and publishes a
  release on every build.
* New extension icon.

## [0.2.0] on September 21, 2026

### Added

* Repository metadata, MIT license, icon, and gallery banner.
* Highlighting for native parameter and return type annotations.

### Changed

* Grammar synced with the compiler keyword and builtin set.

## [0.1.0] on September 1, 2026

### Added

* Initial release: syntax highlighting, bracket matching, and comment support
  for `.ccpl` files.
