# 1인 기업 창작자를 위한 세컨 브레인 — deeper OS

디퍼 언브랜딩 살롱의 사유 자산화 시스템을 클로드 코드 플러그인으로 묶은 저장소입니다.
멤버는 명령 세 줄로 스킬·서브에이전트 템플릿·세팅 커맨드를 설치합니다.

## 설치 (멤버용)

클로드 코드에서 **한 줄씩** 차례로 입력합니다.

```
/plugin marketplace add https://github.com/clbookslower/deeper-os.git
/plugin install deeper-os@deeper-os
/reload-plugins
```

> 설치가 목록에 안 보이면 `/plugin` 메뉴 → `Marketplaces` → `deeper-os` → `Install for you (user scope)` 로 설치하세요.

## 세팅 전에 — 기존 노트는 안전합니다

다음 단계인 `/deeper-os:setup`은 **기존 노트·폴더를 절대 수정하거나 지우지 않습니다.** 없는 폴더·파일만 새로 추가하고, 매 단계마다 확인을 받습니다.

그래도 한 달 넘게 쌓아온 볼트라면, 마음 편히 시작하시도록 **세팅 전에 볼트 폴더를 통째로 한 번 복사해 백업**해 두시길 권합니다. (옵시디언 볼트는 그냥 폴더라서, 복사 한 번이면 완전한 백업이 됩니다.)

이미 자기만의 폴더 구조로 정리해 두셨다면, 세팅 중 폴더 생성을 건너뛰어도 됩니다.

## 초기 세팅

준비되면 실행합니다. CLAUDE.md·폴더 구조·의미의 축을 대화로 만들어 줍니다.

```
/deeper-os:setup
```

## 구성

```
deeper-os/
├── .claude-plugin/
│   ├── marketplace.json     마켓플레이스 정의 (name: deeper-os)
│   └── plugin.json          플러그인 정의 (name: deeper-os)
├── skills/                  공통 방법론 — 필요할 때 자동 로드
│   ├── meaning/             의미   · 로고테라피 의미 발굴
│   ├── voice/               목소리 · 언어 지문 5층위 분석
│   ├── topography/          지형도 · 지식 지형도 + 콘텐츠 추천
│   └── branding/            브랜딩 · 이상적 독자·IP 확장·오퍼 (논리)
├── agents/
│   └── writing.md            서브에이전트 예시 — 각자 매체로 복제
├── commands/
│   └── setup.md             /deeper-os:setup — 초기 세팅
└── README.md
```

## 사용

- **먼저 `meaning`으로 '의미의 축'을 만든 뒤**, voice·topography·branding 순으로 쓰면 가장 매끄럽습니다.
- 스킬은 대화 맥락에 맞게 자동으로 불려 옵니다. (예: "내 목소리 분석해 줘")
- 서브에이전트는 자기 매체대로 이름 붙여 만듭니다. (예: 글쓰기·유튜브·뉴스레터)
- 서브에이전트는 스킬을 활용합니다. (예: 글쓰기 → voice·branding)
- 모든 분석과 추천은 `01-Grammar/Insights/_의미의축.md` 를 기준점으로 삼습니다.

## 갱신

저장소를 수정해 푸시하면, 멤버는 클로드 코드에서 마켓플레이스를 새로고침하여 최신 버전을 받습니다.

---

© 2026 deeper unbranding salon. All Rights Reserved.
