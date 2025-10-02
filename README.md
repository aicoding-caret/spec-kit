<div align="center">
    <a href="./README.en.md">English</a>
</div>

<div align="center">
    <img src="./media/logo_small.webp"/>
    <h1>🌱 Spec Kit</h1>
    <h3><em>더 빠르게, 더 높은 품질의 소프트웨어를 만드세요.</em></h3>
</div>

<p align="center">
    <strong>Spec-Driven Development(명세 기반 개발)를 통해 조직이 차별성 없는 코드 작성 대신 제품 시나리오에 집중할 수 있도록 돕는 프로젝트입니다.</strong>
</p>

[![Release](https://github.com/github/spec-kit/actions/workflows/release.yml/badge.svg)](https://github.com/github/spec-kit/actions/workflows/release.yml)

---

## 목차

- [🤔 Spec-Driven Development란?](#-spec-driven-development란)
- [⚡ 시작하기](#-시작하기)
- [📽️ 비디오 개요](#️-비디오-개요)
- [🤖 지원되는 AI 에이전트](#-지원되는-ai-에이전트)
- [🔧 Specify CLI 레퍼런스](#-specify-cli-레퍼런스)
- [📚 핵심 철학](#-핵심-철학)
- [🌟 개발 단계](#-개발-단계)
- [🎯 실험적 목표](#-실험적-목표)
- [🔧 사전 요구사항](#-사전-요구사항)
- [📖 더 알아보기](#-더-알아보기)
- [📋 상세 과정](#-상세-과정)
- [🔍 문제 해결](#-문제-해결)
- [👥 관리자](#-관리자)
- [💬 지원](#-지원)
- [🙏 감사 인사](#-감사-인사)
- [📄 라이선스](#-라이선스)

## 🤔 Spec-Driven Development란?

Spec-Driven Development는 전통적인 소프트웨어 개발의 **패러다임을 전환**합니다. 수십 년간 코드가 왕이었습니다 — 명세서는 코딩이라는 "진짜 작업"이 시작되면 버려지는 비계에 불과했습니다. Spec-Driven Development는 이를 바꿉니다: **명세서가 실행 가능**해지며, 단지 구현을 안내하는 것을 넘어 직접 작동하는 구현을 생성합니다.

## ⚡ 시작하기

### 1. Specify 설치

선호하는 설치 방법을 선택하세요:

#### 옵션 1: 영구 설치 (권장)

한 번 설치하고 어디서든 사용하세요:

```bash
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```

그 후 도구를 직접 사용하세요:

```bash
specify init <프로젝트명>
specify check
```

#### 옵션 2: 일회성 사용

설치 없이 직접 실행하세요:

```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <프로젝트명>
```

**영구 설치의 이점:**

- 도구가 설치되어 PATH에서 항상 사용 가능
- 셸 별칭을 만들 필요 없음
- `uv tool list`, `uv tool upgrade`, `uv tool uninstall`로 더 나은 도구 관리
- 더 깔끔한 셸 설정

### 2. 프로젝트 원칙 수립

**`/constitution`** 명령어를 사용하여 프로젝트의 지배 원칙과 개발 가이드라인을 만들어 모든 후속 개발을 안내하세요.

```bash
/constitution 코드 품질, 테스트 표준, 사용자 경험 일관성, 성능 요구사항에 초점을 맞춘 원칙을 만듭니다
```

### 3. 명세서 작성

**`/specify`** 명령어를 사용하여 만들고 싶은 것을 설명하세요. 기술 스택이 아닌 **무엇을** 그리고 **왜**에 집중하세요.

```bash
/specify 사진을 별도의 사진 앨범으로 정리하는 데 도움이 되는 애플리케이션을 만듭니다. 앨범은 날짜별로 그룹화되며 메인 페이지에서 드래그 앤 드롭으로 재구성할 수 있습니다. 앨범은 다른 앨범에 중첩되지 않습니다. 각 앨범 내에서 사진은 타일과 같은 인터페이스로 미리 볼 수 있습니다.
```

### 4. 기술 구현 계획 수립

**`/plan`** 명령어를 사용하여 기술 스택과 아키텍처 선택을 제공하세요.

```bash
/plan 이 애플리케이션은 최소한의 라이브러리와 함께 Vite를 사용합니다. 가능한 한 바닐라 HTML, CSS, JavaScript를 사용합니다. 이미지는 어디에도 업로드되지 않으며 메타데이터는 로컬 SQLite 데이터베이스에 저장됩니다.
```

### 5. 작업 분할

**`/tasks`**를 사용하여 구현 계획에서 실행 가능한 작업 목록을 만드세요.

```bash
/tasks
```

### 6. 구현 실행

**`/implement`**를 사용하여 모든 작업을 실행하고 계획에 따라 기능을 구축하세요.

```bash
/implement
```

자세한 단계별 지침은 [종합 가이드](./spec-driven.md)를 참조하세요.

## 📽️ 비디오 개요

Spec Kit의 실제 작동 모습을 보고 싶으신가요? [비디오 개요](https://www.youtube.com/watch?v=a9eR1xsfvHg&pp=0gcJCckJAYcqIYzv)를 시청하세요!

[![Spec Kit video header](/media/spec-kit-video-header.jpg)](https://www.youtube.com/watch?v=a9eR1xsfvHg&pp=0gcJCckJAYcqIYzv)

## 🤖 지원되는 AI 에이전트

| 에이전트                                                  | 지원 | 참고                                                              |
|-----------------------------------------------------------|------|-------------------------------------------------------------------|
| [Caret/Cline (호환)](https://github.com/aicoding-caret/spec-kit) | ✅   | `.caretrules`, `.clinerules`, 및 커스텀 브랜드 규칙을 지원합니다. |
| [Claude Code](https://www.anthropic.com/claude-code)      | ✅   |                                                                   |
| [GitHub Copilot](https://code.visualstudio.com/)          | ✅   |                                                                   |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | ✅   |                                                                   |
| [Cursor](https://cursor.sh/)                              | ✅   |                                                                   |
| [Qwen Code](https://github.com/QwenLM/qwen-code)          | ✅   |                                                                   |
| [opencode](https://opencode.ai/)                          | ✅   |                                                                   |
| [Windsurf](https://windsurf.com/)                         | ✅   |                                                                   |
| [Kilo Code](https://github.com/Kilo-Org/kilocode)         | ✅   |                                                                   |
| [Auggie CLI](https://docs.augmentcode.com/cli/overview)   | ✅   |                                                                   |
| [Roo Code](https://roocode.com/)                          | ✅   |                                                                   |
| [Codex CLI](https://github.com/openai/codex)              | ⚠️   | Codex는 슬래시 명령어에 대한 사용자 정의 인수를 [지원하지 않습니다](https://github.com/openai/codex/issues/2890). |

## 🔧 Specify CLI 레퍼런스

`specify` 명령어는 다음 옵션을 지원합니다:

### 명령어

| 명령어 | 설명                                                                                             |
|--------|--------------------------------------------------------------------------------------------------|
| `init` | 최신 템플릿으로 새 Specify 프로젝트를 초기화합니다                                               |
| `check`| 설치된 도구(`git`, `claude`, `gemini`, `code`/`code-insiders`, `cursor-agent`, `windsurf`, `qwen`, `opencode`, `codex`)를 확인합니다 |

### `specify init` 인자 및 옵션

| 인자/옵션              | 타입 | 설명                                                                                                                            |
|------------------------|------|---------------------------------------------------------------------------------------------------------------------------------|
| `<project-name>`       | 인자 | 새 프로젝트 디렉토리의 이름 ( `--here` 사용 시 선택 사항, 또는 현재 디렉토리는 `.` 사용)                                        |
| `--ai`                 | 옵션 | 사용할 AI 어시스턴트: `cline`, `claude`, `gemini`, `copilot`, `cursor`, `qwen`, `opencode`, `codex`, `windsurf`, `kilocode`, `auggie`, 또는 `roo` |
| `--script`             | 옵션 | 사용할 스크립트 변형: `sh` (bash/zsh) 또는 `ps` (PowerShell)                                                                    |
| `--ignore-agent-tools` | 플래그 | Claude Code와 같은 AI 에이전트 도구 확인을 건너뜁니다                                                                           |
| `--no-git`             | 플래그 | git 저장소 초기화를 건너뜁니다                                                                                                  |
| `--here`               | 플래그 | 새 디렉토리를 만드는 대신 현재 디렉토리에 프로젝트를 초기화합니다                                                               |
| `--force`              | 플래그 | 현재 디렉토리에 초기화할 때 병합/덮어쓰기를 강제합니다 (확인 건너뛰기)                                                          |
| `--skip-tls`           | 플래그 | SSL/TLS 확인을 건너뜁니다 (권장하지 않음)                                                                                       |
| `--debug`              | 플래그 | 문제 해결을 위한 상세 디버그 출력을 활성화합니다                                                                                |
| `--github-token`       | 옵션 | API 요청에 사용할 GitHub 토큰 (또는 GH_TOKEN/GITHUB_TOKEN 환경 변수 설정)                                                        |

### 예시

```bash
# 기본 프로젝트 초기화
specify init my-project

# 특정 AI 어시스턴트로 초기화
specify init my-project --ai claude

# Caret/Cline 호환 템플릿으로 초기화
specify init my-project --ai cline
# .clinerules, .caretrules, 또는 커스텀 브랜드 중 하나를 선택하라는 메시지가 표시됩니다.

# Cursor 지원으로 초기화
specify init my-project --ai cursor

# Windsurf 지원으로 초기화
specify init my-project --ai windsurf

# PowerShell 스크립트로 초기화 (Windows/크로스 플랫폼)
specify init my-project --ai copilot --script ps

# 현재 디렉토리에 초기화
specify init . --ai copilot
# 또는 --here 플래그 사용
specify init --here --ai copilot

# (비어 있지 않은) 현재 디렉토리에 확인 없이 강제 병합
specify init . --force --ai copilot
# 또는
specify init --here --force --ai copilot

# git 초기화 건너뛰기
specify init my-project --ai gemini --no-git

# 문제 해결을 위한 디버그 출력 활성화
specify init my-project --ai claude --debug

# API 요청에 GitHub 토큰 사용 (기업 환경에 유용)
specify init my-project --ai claude --github-token ghp_your_token_here

# 시스템 요구사항 확인
specify check
```

### 사용 가능한 슬래시 명령어

`specify init` 실행 후, AI 코딩 에이전트는 구조화된 개발을 위해 다음 슬래시 명령어에 액세스할 수 있습니다:

| 명령어          | 설명                                                                 |
|-----------------|----------------------------------------------------------------------|
| `/constitution` | 프로젝트 지배 원칙 및 개발 가이드라인을 생성 또는 업데이트합니다     |
| `/specify`      | 만들고 싶은 것을 정의합니다 (요구사항 및 사용자 스토리)              |
| `/clarify`      | 불분명한 영역을 명확히 합니다 (명시적으로 건너뛰지 않는 한 `/plan` 전에 실행해야 함; 이전 `/quizme`) |
| `/plan`         | 선택한 기술 스택으로 기술 구현 계획을 수립합니다                     |
| `/tasks`        | 구현을 위한 실행 가능한 작업 목록을 생성합니다                       |
| `/analyze`      | 아티팩트 간 일관성 및 커버리지 분석 ( /tasks 후, /implement 전 실행) |
| `/implement`    | 계획에 따라 기능을 구축하기 위해 모든 작업을 실행합니다              |

### 환경 변수

| 변수              | 설명                                                                                                                                                                                          |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `SPECIFY_FEATURE` | 비-Git 저장소의 기능 감지를 재정의합니다. Git 브랜치를 사용하지 않을 때 특정 기능에서 작업하려면 기능 디렉토리 이름(예: `001-photo-albums`)으로 설정하세요.<br/>**`/plan` 또는 후속 명령어를 사용하기 전에 작업 중인 에이전트의 컨텍스트에서 설정해야 합니다.** |

## 📚 핵심 철학

Spec-Driven Development는 다음을 강조하는 구조화된 프로세스입니다:

- **의도 기반 개발**: 명세서가 "_어떻게_"보다 "_무엇을_" 먼저 정의합니다
- **풍부한 명세서 작성**: 가드레일과 조직 원칙을 사용합니다
- **다단계 개선**: 프롬프트에서 한 번에 코드를 생성하는 대신 여러 단계를 거쳐 개선합니다
- **고급 AI 모델 능력에 대한 높은 의존도**: 명세서 해석을 위해 고급 AI 모델을 적극 활용합니다

## 🌟 개발 단계

| 단계                               | 초점                   | 주요 활동                                                                                             |
|------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------|
| **0-to-1 개발** ("Greenfield")     | 처음부터 생성          | <ul><li>고수준 요구사항으로 시작</li><li>명세서 생성</li><li>구현 단계 계획</li><li>프로덕션 준비 애플리케이션 구축</li></ul> |
| **창의적 탐색**                    | 병렬 구현              | <ul><li>다양한 솔루션 탐색</li><li>여러 기술 스택 및 아키텍처 지원</li><li>UX 패턴 실험</li></ul>         |
| **반복적 개선** ("Brownfield")     | Brownfield 현대화      | <ul><li>기능을 반복적으로 추가</li><li>레거시 시스템 현대화</li><li>프로세스 조정</li></ul>             |

## 🎯 실험적 목표

우리의 연구 및 실험은 다음에 중점을 둡니다:

### 기술 독립성

- 다양한 기술 스택을 사용하여 애플리케이션 생성
- Spec-Driven Development가 특정 기술, 프로그래밍 언어 또는 프레임워크에 얽매이지 않는 프로세스라는 가설 검증

### 기업 제약 조건

- 미션 크리티컬 애플리케이션 개발 시연
- 조직적 제약(클라우드 제공업체, 기술 스택, 엔지니어링 관행) 통합
- 기업 디자인 시스템 및 규정 준수 요구사항 지원

### 사용자 중심 개발

- 다양한 사용자 집단 및 선호도에 맞는 애플리케이션 구축
- 다양한 개발 접근 방식(바이브 코딩에서 AI 네이티브 개발까지) 지원

### 창의적 및 반복적 프로세스

- 병렬 구현 탐색 개념 검증
- 강력한 반복적 기능 개발 워크플로우 제공
- 업그레이드 및 현대화 작업을 처리하도록 프로세스 확장

## 🔧 사전 요구사항

- **Linux/macOS** (또는 Windows의 WSL2)
- AI 코딩 에이전트: [Claude Code](https://www.anthropic.com/claude-code), [GitHub Copilot](https://code.visualstudio.com/), [Gemini CLI](https://github.com/google-gemini/gemini-cli), [Cursor](https://cursor.sh/), [Qwen CLI](https://github.com/QwenLM/qwen-code), [opencode](https://opencode.ai/), [Codex CLI](https://github.com/openai/codex), 또는 [Windsurf](https://windsurf.com/)
- 패키지 관리를 위한 [uv](https://docs.astral.sh/uv/)
- [Python 3.11+](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads)

에이전트와 문제가 발생하면 통합을 개선할 수 있도록 이슈를 열어주세요.

## 📖 더 알아보기

- **[완전한 Spec-Driven Development 방법론](./spec-driven.md)** - 전체 프로세스에 대한 심층 분석
- **[상세 워크스루](#-상세-과정)** - 단계별 구현 가이드

---

## 📋 상세 과정

<details>
<summary>자세한 단계별 워크스루를 보려면 클릭하세요</summary>

Specify CLI를 사용하여 프로젝트를 부트스트랩할 수 있으며, 이는 환경에 필요한 아티팩트를 가져옵니다. 실행:

```bash
specify init <project_name>
```

또는 현재 디렉토리에서 초기화:

```bash
specify init .
# 또는 --here 플래그 사용
specify init --here
# 디렉토리에 이미 파일이 있을 때 확인 건너뛰기
specify init . --force
# 또는
specify init --here --force
```

![터미널에서 새 프로젝트를 부트스트래핑하는 Specify CLI](./media/specify_cli.gif)

사용 중인 AI 에이전트를 선택하라는 메시지가 표시됩니다. 터미널에서 직접 지정할 수도 있습니다:

```bash
specify init <project_name> --ai claude
specify init <project_name> --ai gemini
specify init <project_name> --ai copilot
specify init <project_name> --ai cursor
specify init <project_name> --ai qwen
specify init <project_name> --ai opencode
specify init <project_name> --ai codex
specify init <project_name> --ai windsurf
# 또는 현재 디렉토리에서:
specify init . --ai claude
specify init . --ai codex
# 또는 --here 플래그 사용
specify init --here --ai claude
specify init --here --ai codex
# 비어 있지 않은 현재 디렉토리에 강제 병합
specify init . --force --ai claude
# 또는
specify init --here --force --ai claude
```

CLI는 Claude Code, Gemini CLI, Cursor CLI, Qwen CLI, opencode 또는 Codex CLI가 설치되어 있는지 확인합니다. 설치되어 있지 않거나 올바른 도구를 확인하지 않고 템플릿을 받으려면 명령어에 `--ignore-agent-tools`를 사용하세요:

```bash
specify init <project_name> --ai claude --ignore-agent-tools
```

### **1단계:** 프로젝트 원칙 수립

프로젝트 폴더로 이동하여 AI 에이전트를 실행하세요. 이 예에서는 `claude`를 사용합니다.

![Claude Code 환경 부트스트래핑](./media/bootstrap-claude-code.gif)

`/constitution`, `/specify`, `/plan`, `/tasks`, `/implement` 명령어가 사용 가능하면 올바르게 설정된 것입니다.

첫 번째 단계는 `/constitution` 명령어를 사용하여 프로젝트의 지배 원칙을 수립하는 것입니다. 이는 모든 후속 개발 단계에서 일관된 의사 결정을 보장하는 데 도움이 됩니다:

```text
/constitution 코드 품질, 테스트 표준, 사용자 경험 일관성, 성능 요구사항에 초점을 맞춘 원칙을 만듭니다. 이러한 원칙이 기술적 결정과 구현 선택을 어떻게 안내해야 하는지에 대한 거버넌스를 포함하세요.
```

이 단계는 `.specify/memory/constitution.md` 파일을 생성하거나 업데이트하며, AI 에이전트가 명세, 계획, 구현 단계에서 참조할 프로젝트의 기본 가이드라인을 담습니다.

### **2단계:** 프로젝트 명세서 작성

프로젝트 원칙이 수립되었으므로 이제 기능 명세서를 작성할 수 있습니다. `/specify` 명령어를 사용한 다음 개발하려는 프로젝트의 구체적인 요구사항을 제공하세요.

>[!IMPORTANT]
>_무엇을_ 만들려고 하는지와 _왜_에 대해 가능한 한 명시적으로 작성하세요. **이 시점에서는 기술 스택에 집중하지 마세요**.

예시 프롬프트:

```text
팀 생산성 플랫폼인 Taskify를 개발합니다. 사용자는 프로젝트를 만들고, 팀원을 추가하고,
작업을 할당하고, 칸반 스타일의 보드 간에 작업을 이동하고 댓글을 달 수 있어야 합니다. 이 기능의 초기 단계에서는,
"Create Taskify"라고 부르겠습니다. 여러 사용자가 있지만 사용자는 미리 정의될 것입니다.
제품 관리자 한 명과 엔지니어 네 명, 두 가지 다른 카테고리에 다섯 명의 사용자를 원합니다. 세 가지
다른 샘플 프로젝트를 만듭시다. 각 작업의 상태에 대해 "To Do", "In Progress", "In Review", "Done"과 같은 표준 칸반 열을
갖도록 합시다. 이 애플리케이션에는 로그인이 없을 것입니다. 이것은 우리의 기본 기능이 설정되었는지 확인하기 위한
첫 번째 테스트일 뿐입니다. 작업 카드의 UI에서 각 작업에 대해
칸반 작업 보드의 다른 열 간에 작업의 현재 상태를 변경할 수 있어야 합니다.
특정 카드에 대해 무제한으로 댓글을 남길 수 있어야 합니다. 해당 작업
카드에서 유효한 사용자 중 한 명을 할당할 수 있어야 합니다. Taskify를 처음 시작하면
선택할 수 있는 다섯 명의 사용자 목록이 표시됩니다. 비밀번호는 필요하지 않습니다. 사용자를 클릭하면
프로젝트 목록을 표시하는 기본 보기로 이동합니다. 프로젝트를 클릭하면 해당 프로젝트의 칸반 보드가 열립니다.
열이 표시됩니다. 카드를 다른 열 간에 드래그 앤 드롭할 수 있습니다.
현재 로그인한 사용자에게 할당된 모든 카드는 다른 모든 카드와 다른 색상으로 표시되어
자신의 카드를 빠르게 볼 수 있습니다. 자신이 만든 댓글은 편집할 수 있지만 다른 사람이 만든 댓글은 편집할 수 없습니다.
자신이 만든 댓글은 삭제할 수 있지만 다른 사람이 만든 댓글은 삭제할 수 없습니다.
```

이 프롬프트가 입력되면 Claude Code가 계획 및 명세 초안 작성 프로세스를 시작하는 것을 볼 수 있습니다. Claude Code는 또한 저장소를 설정하기 위해 내장된 스크립트 중 일부를 트리거합니다.

이 단계가 완료되면 새 브랜치(예: `001-create-taskify`)가 생성되고 `specs/001-create-taskify` 디렉토리에 새 명세서가 생성되어야 합니다.

생성된 명세서에는 템플릿에 정의된 대로 사용자 스토리 및 기능 요구사항 집합이 포함되어야 합니다.

이 단계에서 프로젝트 폴더 내용은 다음과 같아야 합니다:

```text
└── .specify
    ├── memory
    │	 └── constitution.md
    ├── scripts
    │	 ├── check-prerequisites.sh
    │	 ├── common.sh
    │	 ├── create-new-feature.sh
    │	 ├── setup-plan.sh
    │	 └── update-claude-md.sh
    ├── specs
    │	 └── 001-create-taskify
    │	     └── spec.md
    └── templates
        ├── plan-template.md
        ├── spec-template.md
        └── tasks-template.md
```

### **3단계:** 기능 명세서 명확화 (계획 전 필수)

기본 명세서가 생성되었으므로 첫 번째 시도에서 제대로 포착되지 않은 요구사항을 명확히 할 수 있습니다.

다운스트림에서의 재작업을 줄이기 위해 기술 계획을 수립하기 **전에** 구조화된 명확화 워크플로우를 실행해야 합니다.

권장 순서:
1. `/clarify` (구조화됨) 사용 – 답변을 Clarifications 섹션에 기록하는 순차적, 커버리지 기반 질문.
2. 여전히 모호한 부분이 있다면 선택적으로 자유 형식의 개선을 진행합니다.

의도적으로 명확화를 건너뛰고 싶다면(예: 스파이크 또는 탐색적 프로토타입), 에이전트가 누락된 명확화로 인해 막히지 않도록 명시적으로 언급하세요.

예시 자유 형식 개선 프롬프트 (`/clarify` 이후 필요한 경우):

```text
생성하는 각 샘플 프로젝트 또는 프로젝트에 대해 5개에서 15개 사이의 가변적인 수의 작업이
각각 다른 완료 상태로 무작위로 배포되어야 합니다. 각 완료 단계에 최소한 하나의 작업이 있는지 확인하세요.
```

또한 Claude Code에게 **검토 및 수락 체크리스트**를 검증하도록 요청하여, 기능 명세가 기준을 충족하는 항목을 체크하고 그렇지 않은 항목은 체크하지 않은 상태로 두도록 할 수 있습니다. 다음 프롬프트를 사용할 수 있습니다:

```text
검토 및 수락 체크리스트를 읽고, 기능 명세가 기준을 충족하면 체크리스트의 각 항목을 체크하세요. 그렇지 않으면 비워두세요.
```

Claude Code와의 상호 작용을 명세서에 대해 명확히 하고 질문할 기회로 사용하는 것이 중요합니다 - **첫 번째 시도를 최종본으로 취급하지 마세요**.

### **4단계:** 계획 생성

이제 기술 스택 및 기타 기술 요구사항에 대해 구체적으로 설명할 수 있습니다. 프로젝트 템플릿에 내장된 `/plan` 명령어를 다음과 같은 프롬프트와 함께 사용할 수 있습니다:

```text
.NET Aspire를 사용하여 Postgres를 데이터베이스로 생성할 것입니다. 프론트엔드는
드래그 앤 드롭 작업 보드, 실시간 업데이트가 포함된 Blazor 서버를 사용해야 합니다. 프로젝트 API,
작업 API, 알림 API가 포함된 REST API가 생성되어야 합니다.
```

이 단계의 출력에는 여러 구현 세부 정보 문서가 포함되며, 디렉토리 트리는 다음과 같을 것입니다:

```text
.
├── CLAUDE.md
├── memory
│	 └── constitution.md
├── scripts
│	 ├── check-prerequisites.sh
│	 ├── common.sh
│	 ├── create-new-feature.sh
│	 ├── setup-plan.sh
│	 └── update-claude-md.sh
├── specs
│	 └── 001-create-taskify
│	     ├── contracts
│	     │	 ├── api-spec.json
│	     │	 └── signalr-spec.md
│	     ├── data-model.md
│	     ├── plan.md
│	     ├── quickstart.md
│	     ├── research.md
│	     └── spec.md
└── templates
    ├── CLAUDE-template.md
    ├── plan-template.md
    ├── spec-template.md
    └── tasks-template.md
```

`research.md` 문서를 확인하여 지침에 따라 올바른 기술 스택이 사용되었는지 확인하세요. 구성 요소가 눈에 띄면 Claude Code에 개선을 요청하거나, 사용하려는 플랫폼/프레임워크의 로컬 설치 버전을 확인하도록 할 수도 있습니다(예: .NET).

또한, 선택한 기술 스택이 빠르게 변화하는 경우(.NET Aspire, JS 프레임워크 등) Claude Code에 세부 정보를 조사하도록 요청할 수 있습니다. 다음과 같은 프롬프트를 사용하세요:

```text
구현 계획과 구현 세부 정보를 검토하여 .NET Aspire가 빠르게 변화하는 라이브러리이므로
추가 연구가 필요한 영역을 찾아주세요. 추가 연구가 필요하다고 식별한 영역에 대해
이 Taskify 애플리케이션에서 사용할 특정 버전에 대한 추가 세부 정보로 연구 문서를 업데이트하고
웹의 연구를 사용하여 세부 정보를 명확히 하기 위한 병렬 연구 작업을 생성하세요.
```

이 과정에서 Claude Code가 잘못된 것을 연구하느라 막히는 것을 발견할 수 있습니다 - 다음과 같은 프롬프트로 올바른 방향으로 유도할 수 있습니다:

```text
이것을 일련의 단계로 나누어야 할 것 같습니다. 먼저, 구현 중에
확실하지 않거나 추가 연구가 필요한 작업 목록을 식별하세요.
해당 작업 목록을 작성하세요. 그런 다음 각 작업에 대해
별도의 연구 작업을 시작하여 순 결과가
모든 특정 작업을 병렬로 연구하는 것이 되도록 하세요. 당신이 하고 있는 것을 보니
일반적으로 .NET Aspire를 연구하는 것 같았는데, 이 경우에는 별 도움이 되지 않을 것 같습니다.
그것은 너무 목표가 없는 연구입니다. 연구는 특정 목표 질문을 해결하는 데 도움이 되어야 합니다.
```

>[!NOTE]
>Claude Code는 지나치게 열성적이어서 요청하지 않은 구성 요소를 추가할 수 있습니다. 그 근거와 변경 출처를 명확히 하도록 요청하세요.

### **5단계:** Claude Code가 계획을 검증하도록 하기

계획이 수립되면 Claude Code가 누락된 부분이 없는지 확인하도록 해야 합니다. 다음과 같은 프롬프트를 사용할 수 있습니다:

```text
이제 구현 계획과 구현 세부 정보 파일을 감사하도록 하세요.
이것을 읽고 명백하게 해야 할 작업 순서가 있는지 여부를 판단하는 데 중점을 두세요.
여기에 충분한 정보가 있는지 모르겠습니다. 예를 들어,
핵심 구현을 볼 때, 핵심 구현이나 개선의 각 단계를 진행하면서
정보를 찾을 수 있는 구현 세부 정보의 적절한 위치를 참조하는 것이 유용할 것입니다.
```

이는 구현 계획을 개선하고 Claude Code가 계획 주기에서 놓친 잠재적인 사각지대를 피하는 데 도움이 됩니다. 초기 개선 패스가 완료되면 구현에 들어가기 전에 Claude Code에 체크리스트를 다시 한 번 검토하도록 요청하세요.

또한 [GitHub CLI](https://docs.github.com/en/github-cli/github-cli)가 설치되어 있다면 Claude Code에 현재 브랜치에서 `main`으로 상세한 설명과 함께 풀 리퀘스트를 생성하도록 요청하여 노력이 제대로 추적되도록 할 수 있습니다.

>[!NOTE]
>에이전트가 구현하기 전에 Claude Code에 세부 정보를 교차 확인하여 과도하게 설계된 부분이 있는지 확인하는 것도 가치가 있습니다(기억하세요 - 지나치게 열성적일 수 있습니다). 과도하게 설계된 구성 요소나 결정이 있는 경우 Claude Code에 해결하도록 요청할 수 있습니다. Claude Code가 계획을 수립할 때 기본이 되는 [constitution](base/memory/constitution.md)을 준수하도록 하세요.

### 6단계: 구현

준비가 되면 `/implement` 명령어를 사용하여 구현 계획을 실행하세요:

```text
/implement
```

`/implement` 명령어는 다음을 수행합니다:
- 모든 전제 조건(constitution, spec, plan, tasks)이 갖추어졌는지 확인합니다
- `tasks.md`에서 작업 분석을 파싱합니다
- 종속성 및 병렬 실행 마커를 존중하여 올바른 순서로 작업을 실행합니다
- 작업 계획에 정의된 TDD 접근 방식을 따릅니다
- 진행 상황 업데이트를 제공하고 오류를 처리합니다

>[!IMPORTANT]
>AI 에이전트는 로컬 CLI 명령어(`dotnet`, `npm` 등)를 실행합니다 - 컴퓨터에 필요한 도구가 설치되어 있는지 확인하세요.

구현이 완료되면 애플리케이션을 테스트하고 CLI 로그에 표시되지 않을 수 있는 런타임 오류(예: 브라우저 콘솔 오류)를 해결하세요. 이러한 오류를 복사하여 AI 에이전트에 붙여넣어 해결할 수 있습니다.

</details>

---

## 🔍 문제 해결

### Linux의 Git Credential Manager

Linux에서 Git 인증에 문제가 있는 경우 Git Credential Manager를 설치할 수 있습니다:

```bash
#!/usr/bin/env bash
set -e
echo "Git Credential Manager v2.6.1 다운로드 중..."
wget https://github.com/git-ecosystem/git-credential-manager/releases/download/v2.6.1/gcm-linux_amd64.2.6.1.deb
echo "Git Credential Manager 설치 중..."
sudo dpkg -i gcm-linux_amd64.2.6.1.deb
echo "Git이 GCM을 사용하도록 설정 중..."
git config --global credential.helper manager
echo "정리 중..."
rm gcm-linux_amd64.2.6.1.deb
```

## 👥 관리자

- Den Delimarsky ([@localden](https://github.com/localden))
- John Lam ([@jflam](https://github.com/jflam))

## 💬 지원

지원이 필요하면 [GitHub 이슈](https://github.com/github/spec-kit/issues/new)를 열어주세요. 버그 보고, 기능 요청, Spec-Driven Development 사용에 대한 질문을 환영합니다.

## 🙏 감사 인사

이 프로젝트는 [John Lam](https://github.com/jflam)의 작업과 연구에 크게 영향을 받았으며 이를 기반으로 합니다.

## 📄 라이선스

이 프로젝트는 MIT 오픈 소스 라이선스 조건에 따라 라이선스가 부여됩니다. 전체 조건은 [LICENSE](./LICENSE) 파일을 참조하세요.
