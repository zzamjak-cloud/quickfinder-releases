# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.1] - 2026-07-18

### Added

- 동영상 편집: 비율 유지 크기 축소 옵션 (원본/75%/50%/25%) — 구간 내보내기·GIF 내보내기에 적용
- 동영상 편집: 배속 내보내기 옵션 (x1.2/x1.5/x2.0/x3.0) — 오디오 음정 유지(atempo), 30fps 제한으로 용량 절감
- GIF 미리보기: 이미지 경계 아웃라인 표시 토글 버튼

### Fixed

- 새 폴더·새 문서 생성 시 기본 이름이 언어 설정과 무관하게 한국어로 고정되던 문제 (영어: New Folder / New Document)
- GIF→MP4 변환, 구간 내보내기/삭제, 이어붙이기가 번들 FFmpeg(LGPL, libx264 미포함)에서 실패하던 문제
  — OS 인코더(macOS VideoToolbox / Windows Media Foundation) 우선 + libx264·mpeg4 폴백 체인으로 전환

## [1.0.0] - 2026-07-17

### Added

- QuickFinder 첫 릴리스
- 카테고리별 폴더 바로가기, 통합 파일 탐색기 (그리드/리스트/컬럼/상세 뷰)
- 이미지·PSD·동영상 썸네일, OS 드래그&드롭, 실행취소(Ctrl+Z)
- 이미지/동영상/PDF 압축, GIF 변환, 폰트 병합 등 미디어 도구
- GitHub Releases 기반 자동 업데이트

### Changed

- 라이선스 준수 강화: FFmpeg(GPL)·Ghostscript(AGPL)를 번들에서 제거하고,
  최초 사용 시 공식 배포 채널에서 사용자 기기로 직접 설치하는 방식으로 전환
- 서드파티 오픈소스 고지 문서(THIRD-PARTY-NOTICES.md) 동봉
