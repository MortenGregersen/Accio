# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- None.
### Changed
- None.
### Deprecated
- None.
### Removed
- None.
### Fixed
- None.
### Security
- None.

## [0.6.1] - 2019-04-26
### Added
- Adds several popular GitHub projects for official integration support testing to the Demo project.  
  PR: [#10](https://github.com/JamitLabs/Accio/pull/10) | Author: [Cihat Gündüz](https://github.com/Dschee)
### Changed
- None.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixes an issue where two or more targets for the same platform would cause project linking issues.  
  Issue: [#29](https://github.com/JamitLabs/Accio/issues/29) | PR: [#34](https://github.com/JamitLabs/Accio/pull/34) | Author: [Murat Yilmaz](https://github.com/mrylmz)
- Fixes an issue where temporary changes to SwiftPM-only frameworks would be reset before building.  
  Issue: [#35](https://github.com/JamitLabs/Accio/issues/35) | PR: [#36](https://github.com/JamitLabs/Accio/pull/36) | Author: [Cihat Gündüz](https://github.com/Dschee)
### Security
- None.

## [0.6.0] - 2019-04-19
### Added
- Correctly recognizes App Extensions and doesn't add build phases for them. Fixes [#25](https://github.com/JamitLabs/Accio/issues/25).
- Points to detailed information about conflicting name issues with SwiftPM. Fixes [#26](https://github.com/JamitLabs/Accio/issues/26).
- The `init` command now properly detects test targets and lists them as such in the created manifest file. Fixes [#23](https://github.com/JamitLabs/Accio/issues/23).
### Changed
- Improves reading of supported deployment targets.
- Improves init command by treating empty manifest files like non-existing ones. Fixes [#24](https://github.com/JamitLabs/Accio/issues/24).
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixes an issue where Accio commands where failing when Git resets failed.
- Fixes an issue where Accio didn't reset changed files untracked by Git.
### Security
- None.

## [0.5.6] - 2019-04-09
### Added
- Adds support for automatically finding schemes named like 'MBProgressHUD Framework tvOS'.
### Changed
- Some improvements that make the output information on the console more precise.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixes the broken cleanup command of temporary frameworks after completing install.
- Fixes an issue with multiple targets linking a single framework with schemes named after their platforms.
- Fixes an issue with different platform specifiers used in scheme names.
### Security
- None.

## [0.5.5] - 2019-04-05
### Added
- None.
### Changed
- The framework copy build phase now optimizes "dirty" build timing by specifying the output files. [#13](https://github.com/JamitLabs/Accio/issues/13)
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixes an issue where broken previous install attempt leftovers cause errors on subsequent installs. [#12](https://github.com/JamitLabs/Accio/issues/12)
### Security
- None.

## [0.5.4] - 2019-04-03
### Added
- None.
### Changed
- None.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fix symbolic linking of .framework and .dSYM files.
### Security
- None.

## [0.5.3] - 2019-04-01
### Added
- None.
### Changed
- None.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixes an issue where recursive copies of non symbolic links could cause build errors.
### Security
- None.

## [0.5.2] - 2019-04-01
### Added
- None.
### Changed
- None.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Keep symlinks in cached ZIP files for macOS support.
### Security
- None.

## [0.5.1] - 2019-03-31
### Added
- None.
### Changed
- Check if shared cache path is available, else add new build products to local cache.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fixed an issue with copying unzipped cache build products back to project.
### Security
- None.


## [0.5.0] - 2019-03-30
### Added
- Demo project for integration testing with popular Swift frameworks.
### Changed
- Compress cached build products in a .zip file. Old style cached build products can be deleted.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Multiple issues with paths, names, symbolic links & more.
### Security
- None.

## [0.4.0] - 2019-03-29
### Added
- Add support for test targets.
- Sort `Dependencies` group alphabetically.
### Changed
- Change structure of `Dependencies` folder.
- Delete unneeded groups & references from `Dependencies` group.
- Delete unneeded files & folders from `Dependencies` folder.
- Only link frameworks when not already linked.
- Unlink frameworks that are no longer included.
- Don't save build products to local cache if shared cache is available.
- Cleanup Accio run script phase when target gets removed.
### Deprecated
- None.
### Removed
- None.
### Fixed
- Fix typo in local cache logging.
- Fix missing use of `Constants.xcodeDependenciesGroup` & `Constants.dependenciesPath`.
### Security
- None.

## [0.3.0] - 2019-03-26
### Added
- None.
### Changed
- Add support for Swift 5 and Xcode 10.2.
- Separate cached frameworks by Swift tools version.
### Deprecated
- None.
### Removed
- Drop support for Swift 4.2 and Xcode <=10.1.
### Fixed
- None.
### Security
- None.

## [0.2.2]
### Fixed
- Fixed an issue with some frameworks sym-linking to themselves.

## [0.2.1]
### Added
- Support for setting a default `shared-cache-path` via configuration.
- New sub command `set-shared-cache` for setting the shared cache path.
### Fixed
- Also correctly recognize scheme names like "SwiftyBeaver (iOS)".

## [0.2.0]
### Added
- Initial working release with `init`, `install`, `update`, `clean` and `clear-cache` sub commands
