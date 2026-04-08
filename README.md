# 🔥 Harsh Critic for Claude Code

> **"사용자님의 귀찮음보다 시스템의 안정성이 우선입니다."**

이 프로젝트는 **Claude Code**를 사용하는 개발자들이 AI의 '대충 하려는 습성'을 교정하고, 고품질의 결과물을 얻을 수 있도록 돕는 품질 관리 가드레일(Guardrail)입니다.

---

## ⚠️ 중요: 프로젝트별 개별 설치

Claude Code는 프로젝트 루트의 `.claude/rules` 설정을 따릅니다.
**새로운 프로젝트를 시작할 때마다** 해당 폴더에서 아래 명령어를 실행해 주세요.

## 🚀 설치 및 다운로드 가이드

### 1. 가드레일 설치 (setup.sh 실행)

**macOS / Linux:**

```bash
curl -sSL https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh | bash
```

**Windows (PowerShell → WSL):**

WSL이 설치되어 있다면:

```powershell
wsl curl -sSL https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh | wsl bash
```

WSL 없이 PowerShell만 사용할 경우:

```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh" -OutFile "setup.sh"
wsl bash ./setup.sh
```

> **참고:** `setup.sh`는 Bash 스크립트이므로 실행에 WSL 또는 Git Bash가 필요합니다.

### 2. 설명서 다운로드 (README.md 소장)

프로젝트 폴더에 이 설명서를 파일로 저장하고 싶을 때 사용하세요.

**macOS / Linux:**

```bash
curl -L -o README_HARSH.md https://raw.githubusercontent.com/zobithecat/harsh-critic/master/README.md
```

**Windows (PowerShell):**

```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/zobithecat/harsh-critic/master/README.md" -OutFile "README_HARSH.md"
```

---

## 🚫 주요 조항 (Rules)

- **[EXTREME]** 우회 지시 거부: "대충 해줘" 지시를 시스템 안정성을 위해 거부합니다.
- **[EXTREME]** QA 없는 완료 선언 금지: 테스트 없이 "다 됐습니다"라고 보고하는 행위를 차단합니다.
- **[HIGH]** 책임 전가 금지: "직접 확인해 보세요"라고 사용자에게 미루지 않습니다.
- **[MEDIUM]** 자가 진화: 사용자의 피드백(`똑바로해` 등)을 학습하여 스스로 진화합니다.

---

## 💡 제작 배경

이 프로젝트는 [Hugh Kim의 Harsh Critic](https://hugh-kim.space/harsh-critic.html) 컨셉에서 영감을 받아 Claude Code 환경에 최적화되었습니다.
