# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.6] - 2026-07-21

### Changed

- Update popup release notes link now opens the CHANGELOG instead of the release page (which shows installation instructions)

## [1.0.5] - 2026-07-20

### Fixed

- Google Drive folder thumbnails no longer flash and then get stuck on a loading spinner while cloud files are being materialized
- Grid thumbnails now refresh automatically when a Google Drive file is modified remotely (content signature added to the thumbnail cache key)
- Thumbnail requests cancelled by folder reloads are now retried instead of leaving a permanent spinner

## [1.0.4] - 2026-07-19

### Added

- Japanese display language

## [1.0.3] - 2026-07-19

### Added

- 8 new display languages: Simplified Chinese, Traditional Chinese, Spanish, French,
  German, Russian, Portuguese, and Italian
- Localized display names for macOS system root folders (Users, Applications, Library, System)
  in all supported languages

### Changed

- OS language detection now prefers the longest matching locale prefix,
  so Traditional Chinese locales (zh-TW, zh-Hant, zh-HK) resolve correctly

## [1.0.2] - 2026-07-18

### Added

- Installation & Activation Guide (PDF) for customers, delivered with every purchase

### Changed

- The update dialog now shows a "View release notes" link instead of embedding release-note text,
  so the dialog stays fully localized regardless of the release language
- README and CHANGELOG are now maintained in English

### Fixed

- "Buy a license" now opens the actual checkout page
- License activation now verifies that the key belongs to the official QuickFinder store and product

## [1.0.1] - 2026-07-18

### Added

- Video editor: aspect-ratio-preserving downscale option (Original/75%/50%/25%) — applies to both segment export and GIF export
- Video editor: playback-speed export option (x1.2/x1.5/x2.0/x3.0) — keeps audio pitch via atempo, caps output at 30fps to reduce file size
- GIF preview: toggle button to show an outline around the image bounds

### Fixed

- Default names for new folders/documents were always created in Korean regardless of the language setting (English: New Folder / New Document)
- GIF→MP4 conversion, segment export/delete, and video merge failed with the bundled FFmpeg (LGPL build, no libx264)
  — switched to an encoder fallback chain: OS encoders first (macOS VideoToolbox / Windows Media Foundation), then libx264, then mpeg4

## [1.0.0] - 2026-07-17

### Added

- First release of QuickFinder
- Category-based folder shortcuts and a built-in file explorer (grid/list/column/detail views)
- Image · PSD · video thumbnails, native OS drag & drop, undo (Ctrl+Z)
- Media tools: image/video/PDF compression, GIF conversion, font merging, and more
- Auto-update via GitHub Releases

### Changed

- Strengthened license compliance: removed FFmpeg (GPL) and Ghostscript (AGPL) from the bundle;
  now ships a self-built LGPL FFmpeg binary, and PDF compression is implemented natively in Rust
- Bundled third-party open-source notices (THIRD-PARTY-NOTICES.md)
