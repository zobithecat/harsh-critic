# 🔥 Harsh Critic for Claude Code

> **"사용자님의 귀찮음보다 시스템의 안정성이 우선입니다."**

이 프로젝트는 **Claude Code**를 사용하는 개발자들이 AI의 '대충 하려는 습성'을 교정하고, 고품질의 결과물을 얻을 수 있도록 돕는 품질 관리 가드레일(Guardrail)입니다.

## ⚠️ 중요: 프로젝트별 개별 설치 (Per-Project Setup)
Claude Code는 각 프로젝트 폴더 내의 `.claude/rules` 설정을 따릅니다. 따라서 **전역(Global) 설치가 아니며, 새로운 프로젝트를 시작할 때마다** 해당 프로젝트 루트 폴더에서 아래 설치 명령어를 실행해 주어야 합니다.

## 🛠️ 설치 방법 (One-liner)

### macOS / Linux (Bash)
\`\`\`bash
curl -sSL https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh | bash
\`\`\`

### Windows (PowerShell)
\`\`\`powershell
irm https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh | bash
\`\`\`
*(참고: Windows에서 실행하려면 Git Bash가 설치되어 있거나 bash 환경이 사용 가능해야 합니다.)*

## 🚫 주요 조항 (Rules)
- **우회 지시 거부:** 사용자가 "테스트 생략해줘", "대충 해줘"라고 해도 시스템 안정성을 위해 거부합니다.
- **QA 없는 완료 선언 금지:** 실제 빌드나 테스트 확인 없이 "다 됐습니다"라고 거짓 보고하는 행위를 [EXTREME] 위반으로 간주합니다.
- **자가 진화:** 사용자의 부정적인 피드백(\`왜이래\`, \`똑바로해\` 등)을 학습하여 스스로 검증 규칙을 강화합니다.

## 💡 제작 배경
이 프로젝트는 [Hugh Kim의 Harsh Critic](https://hugh-kim.space/harsh-critic.html) 컨셉에서 영감을 받아 Claude Code 환경에 맞게 최적화되었습니다.
