# Git 컨벤션

## 원격 / 브랜치

- 원격: `https://github.com/msw-Hub/claude-code-test.git`
- 기본 브랜치: `main`. 현재는 `main`에 직접 커밋·푸시하는 흐름으로 운영 중이다
  (실험용 저장소라 브랜치 전략을 두지 않았다).

## 커밋 메시지

- **한국어**로 작성한다.
- Conventional Commits 접두사를 붙인다: `feat:`, `fix:`, `chore:`, `docs:` 등.
- 제목은 "무엇을 왜" 한 줄로. 본문이 필요하면 한 줄 비우고 배경·이유를 적는다.
- 예: `fix: test.html을 index.html로 변경해 Pages 루트 진입점 제공`

## 커밋 / 푸시 시점

- 커밋과 푸시는 사용자가 명시적으로 요청할 때만 한다. 요청 없이 선제적으로 커밋하지 않는다.

## Claude 설정 파일 추적 정책

- `.claude/settings.json` — **공유 설정.** 커밋한다. 권한 허용/거부 목록, 출력 스타일 등
  팀·프로젝트 공통 설정이 들어간다.
- `.claude/settings.local.json` — **개인 로컬 설정.** `.gitignore`(28번째 줄)로 제외된다.
  개인 환경에서만 필요한 오버라이드는 여기에 둔다. 이 파일을 추적 대상으로 만들지 말 것.
- 로컬 설정 중 팀이 공유해야 할 항목이 생기면 `settings.json`으로 옮긴다.

## .gitignore가 이미 커버하는 것

`node_modules/`, `dist/`, `build/`, `*.min.css`, `.env*`, 로그, OS 파일(`.DS_Store`, `Thumbs.db`),
에디터 설정(`.vscode/`, `.idea/`). 이 범주의 파일을 강제로 커밋하지 않는다.
