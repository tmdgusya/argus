# Frontend Profile 설정

## 1. Telegram 봇 생성

1. Telegram에서 @BotFather 검색 후 대화 시작
2. `/newbot` 전송
3. 표시 이름 입력: `Argus Frontend`
4. 사용자 이름 입력: `argus_frontend_bot` (고유해야 함, `bot`으로 끝나야 함)
5. BotFather가 준 **API 토큰** 복사

## 2. 그룹 채팅 설정

1. Telegram에서 새 그룹 생성 (예: `Argus Frontend`)
2. 생성한 봇을 그룹에 초대
3. 아래 둘 중 하나를 반드시 적용
   - 방법 A: 봇을 그룹 **관리자**로 승격
   - 방법 B: BotFather에서 privacy mode 비활성화 (`/setprivacy` → 봇 선택 → `Disable`)

> Telegram 봇은 기본적으로 privacy mode가 켜져 있어 `/` 명령 중심으로만 수신됩니다.
> 그룹 일반 메시지를 읽게 하려면 관리자 승격 또는 `setprivacy Disable` 중 하나가 필요합니다.

### 2-1. BotFather `/setprivacy` 절차 (선택)

1. Telegram에서 `@BotFather` 대화창 열기
2. `/setprivacy` 입력
3. 대상 봇 선택 (`@argus_frontend_bot`)
4. `Disable` 선택
5. 완료 후 그룹에서 `@argus_frontend_bot 안녕하세요` 테스트

> 주의:
> - 여러 봇을 같은 그룹에서 동시에 운영하면 `setprivacy Disable`일 때 봇 응답이 섞일 수 있습니다.
> - 멀티봇 운영은 `setprivacy Enable` + 대상 봇 멘션 방식이 더 안정적입니다.

## 3. 프로파일 생성

```bash
hermes profile create frontend --clone
```

## 4. SOUL.md 교체

```bash
cp ~/projects/argus/frontend/SOUL.md ~/.hermes/profiles/frontend/SOUL.md
```

## 5. Telegram 토큰 설정

```bash
sed -i '/^TELEGRAM_BOT_TOKEN=/d' ~/.hermes/profiles/frontend/.env
echo 'TELEGRAM_BOT_TOKEN=<your-telegram-bot-token>' >> ~/.hermes/profiles/frontend/.env
```

## 6. 허용 사용자 설정

```bash
sed -i '/^TELEGRAM_ALLOWED_USERS=/d' ~/.hermes/profiles/frontend/.env
echo 'TELEGRAM_ALLOWED_USERS=<your-telegram-user-id>' >> ~/.hermes/profiles/frontend/.env
```

> `TELEGRAM_ALLOWED_USERS`는 `@username`이 아니라 숫자 user ID를 사용하세요.

## 7. 홈 채널 설정 (선택)

```bash
sed -i '/^TELEGRAM_HOME_CHANNEL=/d' ~/.hermes/profiles/frontend/.env
echo 'TELEGRAM_HOME_CHANNEL=<your-group-chat-id>' >> ~/.hermes/profiles/frontend/.env
```

## 8. 그룹 멘션 강제 설정 (권장)

여러 봇(`backend/frontend/dba`)을 같은 그룹에서 운영할 때는 반드시 켜세요.
이 설정이 없으면 `setprivacy Disable` 상태에서 모든 봇이 같은 메시지에 답할 수 있습니다.

```bash
sed -i '/^TELEGRAM_REQUIRE_MENTION=/d' ~/.hermes/profiles/frontend/.env
echo 'TELEGRAM_REQUIRE_MENTION=true' >> ~/.hermes/profiles/frontend/.env
frontend gateway restart
```

동작:
- 그룹에서 `@argus_frontend_bot ...` 멘션이 있을 때만 응답
- 멘션 없는 일반 메시지는 무시

## 9. (선택) 워크플로우 스킬 확인

```bash
hermes -p frontend skills list | grep -E 'github-pr-workflow|linear'
```

> 참고: 이 단계는 setup 필수가 아닙니다.
> Codex는 `codex` CLI 스킬이 아니라 Hermes에 연동하는 provider/모델 의미입니다.

## 10. 확인

```bash
hermes profile show frontend
hermes -p frontend skills list
frontend chat
```

## 11. Gateway 실행

```bash
frontend gateway run
```
