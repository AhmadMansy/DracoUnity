# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] -
### Added
- Performance improvements
  - Utilizes Advanced Mesh API
  - Two-step decoding allows to do more work of step two in threaded Jobs
- Burst
- Unit tests
### Changes
- API is now async/await based

## [1.4.0] - 2021-01-31
### Added
- Support for Apple Silicon on macOS
- Support for Universal Windows Platform (x86,x64,ARM and ARM64)
### Changed
- Re-built all libraries with updated environments (Xcode, Android NDK, Emscripten, etc.)
- WebAssembly lib is now built by draco CI as well
### Fixed
- macOS library is now excluded from other platform builds (thanks Cameron Newnham <cam@fologram.com>)

## [1.3.0] - 2020-09-17
### Added
- Support for bone weights and joints by providing attribute IDs. Needed for glTF skinning.

## [1.2.0] - 2020-02-24
### Changed
- Performance improvement: CreateMesh does not calculate missing normals or tangents anymore. Instead it provides its caller with all info necessary to decide for itself, if calculations are needed.

## [1.1.3] - 2020-02-22
### Added
- Support for Universal Windows Platform (not verified/tested myself)

## [1.1.2] - 2020-02-01
### Fixed
- Removed in-Editor error by adding missing Profiler.EndSample call

## [1.1.1] - 2019-11-22
### Fixed
- Calculate correct tangents if UVs are present (fixes normal mapping)

## [1.1.0] - 2019-11-21
### Changed
- Assume Draco mesh to be right-handed Y-up coordinates and convert the to Unity's left-handed Y-up by flipping the Z-axis.
- Unity 2018.2 backwards compatibility
### Fixed
- Reference assembly definition by name instead of GUID to avoid package import errors

## [1.0.1] - 2019-09-15
### Changed
- Updated Draco native library binaries
- iOS library is now ~15 MB instead of over 130 MB

## [1.0.0] - 2019-07-28
### Changed
- Recompiled dracodec_unity library with BUILD_FOR_GLTF flag set to true, which adds support for normal encoding and standard edge breaking.
- Opened up interface a bit, which enables custom mesh loading by users.

## [0.9.0] - 2019-07-11
- Initial release
