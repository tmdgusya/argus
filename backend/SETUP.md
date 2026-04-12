# Backend Profile 설정

## 1. 프로파일 생성

```bash
hermes profile create backend --clone
```

`--clone`은 default 프로파일의 config.yaml, .env, SOUL.md를 복사합니다.

## 2. SOUL.md 교체

생성된 프로파일의 SOUL.md를 이 프로젝트의 것으로 교체:

```bash
cp ~/projects/argus/backend/SOUL.md ~/.hermes/profiles/backend/SOUL.md
```

## 3. Discord Bot Token 설정

```bash
echo 'DISCORD_BOT_TOKEN=<your-bot-token>' >> ~/.hermes/profiles/backend/.env
```

> 기존 DISCORD_BOT_TOKEN은 반드시 새 토큰으로 교체하세요.

## 4. Discord 채널 설정

```bash
hermes -p backend config edit
```

config.yaml에 추가:
```yaml
discord:
  require_mention: false
  allowed_channels: "<#argus-backend-channel-id>"
  auto_thread: true
  reactions: true
```

## 5. 스킬 설치

```bash
hermes -p backend skills install codex
hermes -p backend skills install github-pr-workflow
hermes -p backend skills install linear
hermes -p backend skills install e2e-testing-skill
```

## 6. 확인

```bash
hermes profile show backend
hermes -p backend skills list
backend chat
```

## 7. Gateway 실행

강의 실습에서는 별도 터미널에서 foreground로 실행:

```bash
backend gateway run
```

systemd 서비스로 백그라운드 실행 (선택):
```bash
backend gateway install
backend gateway start
backend gateway status
backend gateway logs
backend gateway stop
```
