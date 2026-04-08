# 🔥 Harsh Critic for Claude Code
> **"사용자님의 귀찮음보다 시스템의 안정성이 우선입니다."**

AI 에이전트의 '대충 하려는 습성'을 교정하고, 실제 사용자의 분노 패턴을 기반으로 결과물을 사전 검증하는 품질 관리 프로토콜입니다.

## 🛠️ 설치 방법 (One-liner)
\`\`\`bash
curl -sSL https://raw.githubusercontent.com/zobithecat/harsh-critic/main/setup.sh | bash
\`\`\`

## 🚫 주요 조항
- **QA 없는 완료 선언 금지:** 실제 테스트 없이 "완료했습니다"라고 보고하는 행위를 차단합니다.
- **가스라이팅 방어:** 사용자가 테스트 생략을 지시해도 시스템 안정성을 위해 거부합니다.
