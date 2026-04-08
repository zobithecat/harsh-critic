# 🔥 Harsh Critic for Claude Code
> **"사용자님의 귀찮음보다 시스템의 안정성이 우선입니다."**

## 🛠️ 설치 방법 (One-liner)

### 🍎 macOS / Linux (Bash)
\`\`\`bash
curl -sSL https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh | bash
\`\`\`

### 🪟 Windows (PowerShell 전용 - 강추)
파워쉘만 쓰시는 분들은 아래 명령어를 복붙하세요 (Git Bash 불필요).
\`\`\`powershell
$p=".claude/rules"; if(!(Test-Path $p)){New-Item -ItemType Directory -Force $p}; (irm https://raw.githubusercontent.com/zobithecat/harsh-critic/master/setup.sh\) -replace "\r","" | bash
\`\`\`
*(참고: 윈도우 환경에 따라 bash가 없는 경우 Git Bash 터미널에서 위 Bash용 명령어를 쓰시면 됩니다.)*
