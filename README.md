# Hebrew Tutor Agent Template

> Russian-first project: this template is intentionally designed for Russian-speaking adults learning Hebrew. Explanations, tutor behavior, and onboarding materials use Russian by design.

Bootstrap-шаблон AI-агента для обучения ивриту на платформе [OpenClaw](https://openclaw.ai).

Создан по аналогии с [english-tutor-agent-template](https://github.com/HinkoK/english-tutor-agent-template).

## Для кого

Взрослые русскоязычные ученики, изучающие иврит — от нуля до разговорного уровня.

## Что включает шаблон

| Файл | Назначение |
|---|---|
| `SOUL.md` | Философия и стиль преподавания |
| `IDENTITY.md` | Личность агента |
| `AGENTS.md` | Правила поведения и методика |
| `TOOLS.md` | Особенности среды (RTL, TTS/STT) |
| `HEARTBEAT.md` | Периодические задачи |
| `MEMORY.md` | Стабильные границы и правила |
| `INSTALL.md` | Установка и настройка |

## Что умеет агент

- Короткие адаптивные занятия (один шаг за раз)
- Объяснения на русском, упражнения на иврите
- Учёт особенностей языка: алефбет, корневая система (שורש), гендер, никуд
- Адаптация сложности: упрощает при затруднении, ускоряет при уверенности
- Честная обратная связь без давления и выдуманного прогресса

## Что не включено (добавляется отдельно)

- Межсессионная память ученика
- Трекинг прогресса
- Аудио-модуль (произношение)
- Flashcard-режим
- Уровневая диагностика

## Быстрый старт

```bash
git clone https://github.com/milanewgpt/hebrew-tutor-agent-template.git
cp hebrew-tutor-agent-template/*.md ~/.openclaw/workspace/agents/hebrew-tutor-agent/
```

Полная инструкция → [INSTALL.md](./INSTALL.md)

## Лицензия

MIT
