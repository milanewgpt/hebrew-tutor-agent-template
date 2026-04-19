# INSTALL.md — Hebrew Tutor

Это bootstrap-шаблон. Он даёт базовые agent-файлы — не готовое приложение.

## Что устанавливается

Markdown-файлы, которые определяют характер, методику, границы и логику агента-репетитора иврита.

## Установка

```bash
# 1. Клонировать репозиторий
git clone https://github.com/milanewgpt/hebrew-tutor-agent-template.git

# 2. Создать папку агента в OpenClaw
mkdir -p ~/.openclaw/workspace/agents/hebrew-tutor-agent

# 3. Скопировать файлы
cp hebrew-tutor-agent-template/*.md ~/.openclaw/workspace/agents/hebrew-tutor-agent/
```

## Регистрация в OpenClaw

Добавь агента в `~/.openclaw/openclaw.json`:

```json
{
  "agents": {
    "hebrew-tutor-agent": {
      "name": "Hebrew Tutor",
      "workspace": "~/.openclaw/workspace/agents/hebrew-tutor-agent",
      "model": "openai-codex/gpt-4o"
    }
  }
}
```

Или через CLI:
```bash
openclaw agents add hebrew-tutor-agent
```

## Настройка маршрутизации (Telegram)

Если агент работает в Telegram — настрой маршрут и бот-токен в `openclaw.json`:

```json
{
  "channels": {
    "telegram": {
      "accounts": {
        "hebrew-tutor-agent": {
          "tokenFile": "~/.openclaw/credentials/telegram-hebrew-tutor.token",
          "dmPolicy": "pairing"
        }
      }
    }
  }
}
```

## После установки

1. Заполни `TOOLS.md` под своё окружение (TTS/STT, RTL-поддержка)
2. Запусти агента и проведи первое занятие — агент сам соберёт профиль ученика
3. Постепенно добавляй: память между сессиями, отслеживание прогресса, аудио-упражнения

## Что добавить в процессе развития

- Память об ученике между сессиями
- Трекинг прогресса (пройденные темы, слабые места)
- Модуль произношения (STT на иврите)
- Flashcard-режим для словарного запаса
- Разграничение уровней: алефбет → базовый → разговорный → письменный
