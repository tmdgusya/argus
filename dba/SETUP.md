# DBA Profile 설정

## 1. 프로파일 생성

```bash
hermes profile create dba --clone
```

## 2. SOUL.md 교체

```bash
cp ~/projects/argus/dba/SOUL.md ~/.hermes/profiles/dba/SOUL.md
```

## 3. Discord Bot Token 설정

```bash
echo 'DISCORD_BOT_TOKEN=<your-bot-token>' >> ~/.hermes/profiles/dba/.env
```

> 기존 DISCORD_BOT_TOKEN은 반드시 새 토큰으로 교체하세요.

## 4. Discord 채널 설정

```bash
hermes -p dba config edit
```

config.yaml에 추가:
```yaml
discord:
  require_mention: false
  allowed_channels: "<#argus-dba-channel-id>"
  auto_thread: true
  reactions: true
```

## 5. 스킬 설치

```bash
hermes -p dba skills install codex
hermes -p dba skills install github-pr-workflow
hermes -p dba skills install linear
```

## 6. 확인

```bash
hermes profile show dba
hermes -p dba skills list
dba chat
```

## 7. Gateway 실행

```bash
dba gateway run
```
