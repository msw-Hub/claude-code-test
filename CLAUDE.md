# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

상세 규칙은 `.claude/rules/` 아래 주제별 파일로 나눠 두었다. 아래 임포트는 Claude Code가
자동으로 컨텍스트에 로드한다.

@.claude/rules/project-overview.md
@.claude/rules/code-style.md
@.claude/rules/git.md

## 요약 (빠른 참조)

- **빌드/테스트/린트 없음.** `index.html`을 브라우저로 직접 여는 게 실행의 전부다.
- **`tailwind.config.js`는 비어 있고 Tailwind는 미연결.** 스타일은 `index.html` 내 순수 CSS.
- **`index.html`은 루트 진입점으로 유지.** GitHub Pages가 루트에서 서빙한다.
- **단일 파일 + 외부 의존성 제로**가 설계 의도다. CDN·외부 이미지·외부 스크립트 금지.
- 커밋 메시지는 한국어 + Conventional Commits. 커밋/푸시는 요청 시에만.
