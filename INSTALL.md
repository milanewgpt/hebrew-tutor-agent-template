# INSTALL.md — Hebrew Tutor

This is a bootstrap template. It provides base agent files, not a complete application.

## What Gets Installed

Markdown files that define the personality, teaching method, boundaries, and logic of the Hebrew tutor agent.

## Installation

```bash
# 1. Clone the repository
git clone https://github.com/milanewgpt/hebrew-tutor-agent-template.git

# 2. Create the OpenClaw agent directory
mkdir -p ~/.openclaw/workspace/agents/hebrew-tutor-agent

# 3. Copy the files
cp hebrew-tutor-agent-template/*.md ~/.openclaw/workspace/agents/hebrew-tutor-agent/
```

## Register in OpenClaw

Add the agent to `~/.openclaw/openclaw.json`:

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

Or use the CLI:

```bash
openclaw agents add hebrew-tutor-agent
```

## Telegram Routing

If the agent runs through Telegram, configure routing and the bot token in `openclaw.json`:

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

## After Installation

1. Fill `TOOLS.md` for your environment: TTS/STT, RTL support, channel behavior.
2. Start the agent and run the first lesson. The agent should collect the learner profile itself.
3. Add product modules gradually: cross-session memory, progress tracking, and audio exercises.

## Future Extensions

- Cross-session learner memory.
- Progress tracking: completed topics and weak points.
- Pronunciation module using Hebrew-capable STT.
- Flashcard mode for vocabulary.
- Level separation: aleph-bet → basic → conversational → written Hebrew.
