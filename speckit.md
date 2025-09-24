# Spec Kit 실용 가이드

## 1. Spec Kit이란?
Spec Kit은 GitHub에서 제공하는 오픈소스 도구로,  
AI와 함께 프로젝트를 설계하고 개발 과정을 단계별로 진행할 수 있도록 도와준다.  

CLI(Command Line Interface)와 슬래시 명령어(Slash Commands)를 사용하여  
**명세 → 계획 → 작업 분해 → 구현** 과정을 체계적으로 관리할 수 있다.

---

## 2. 설치 방법

### uv 설치
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### PATH 설정 (WSL)
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Spec Kit 설치
```bash
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```

### 설치 확인
```bash
specify --help
```

---

## 3. 주요 명령어 (CLI)

| 명령어 | 설명 |
|--------|------|
| `specify init <project>` | 새 프로젝트 초기화 |
| `specify check` | 환경과 필요한 도구 점검 |
| `specify --help` | 도움말 출력 |

### `specify init` 자주 쓰는 옵션
- `--ai <agent>` : AI 선택 (예: copilot, claude 등)  
- `--here` : 현재 디렉토리에 프로젝트 생성  
- `--no-git` : Git 초기화 생략  
- `--force` : 강제로 초기화 진행  

---

## 4. 슬래시 명령어 (AI 협업)

Spec Kit은 AI와 협업할 때 **슬래시 명령어**를 제공한다.  
이 명령들은 프로젝트의 규칙을 정의하고, 개발 과정을 정리하는 데 쓰인다.

| 명령어 | 기능 |
|--------|------|
| `/constitution` | 프로젝트 원칙 정의 (코드 품질, 테스트 기준, UX, 성능 등) |
| `/specify` | 프로젝트 요구사항 명세 작성 |
| `/clarify` | 모호한 명세를 구체화 |
| `/plan` | 기술 스택, 아키텍처 등 구체적 계획 |
| `/tasks` | 작업을 작은 단위로 분해 |
| `/analyze` | 명세와 계획의 일관성 점검 |
| `/implement` | 실제 코드 작성 및 실행 |

---

## 5. 사용 예시

### 프로젝트 초기화
```bash
specify init my-project --ai copilot
cd my-project
```

### AI와 협업 (채팅 환경에서 입력)
```text
/constitution Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

```text
/specify Build a habit-tracking web app with user profiles, daily logs, reminders, and analytics dashboard
```

```text
/plan Use React + Node.js + SQLite; Tailwind for frontend; REST API; deploy to Vercel
```

```text
/tasks
/analyze
/implement
```

---

## 6. 정리
- **Spec Kit**은 AI와 협업하는 개발 도구다.  
- CLI 명령어로 프로젝트를 초기화하고,  
- 슬래시 명령어로 **명세 → 계획 → 구현**을 단계별로 진행한다.  
- 이를 통해 학생이나 개발자가 더 쉽게 프로젝트를 구조화할 수 있다.
