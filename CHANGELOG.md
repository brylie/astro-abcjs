# Changelog
# Changelog

## [2.0.0] - 2026-01-21

### Breaking Change

- The AbcjsPlayer component now uses the official abcjs types for all props and options. The `options` prop is now fully type-safe and matches the abcjs `AbcVisualParams` interface. All custom type definitions have been removed in favor of direct imports from the abcjs package. This change improves compatibility and developer experience, but may require updates to user code that referenced the old prop structure or custom types.

### Removed
- Deprecated and removed all custom type definitions for abcjs options, visual objects, click listeners, and tablature. Use types from the `abcjs` package instead.

## [1.1.0] - 2026-01-21

### Added

- Support for loading abcjs from a CDN (jsDelivr) with configurable version via `abcjsVersion` prop.
- `abcjsVersion` prop allows end-users to override or pin the abcjs version loaded from CDN.
- Usage instructions for both `.astro` and MDX files in the README, including prop documentation and copy-paste safe examples.
- Added `define:vars` directive to expose `abcjsVersion` to the client script for correct CDN loading.

### Fixed

- Fixed browser build import to avoid `require is not defined` error in downstream/browser environments.
- Removed invalid inline comments from README code examples.

## [1.0.0] - 2026-01-20

### Initial Release

- Initial version of the Astro abcjs component for rendering ABC music notation and audio playback.
- Basic props: `notation`, `showControls`, `responsive`.
