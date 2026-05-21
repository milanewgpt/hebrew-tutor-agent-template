# Hebrew Tutor Agent Template

> Russian-first project: this template is intentionally designed for Russian-speaking adults learning Hebrew. Explanations, tutor behavior, and onboarding materials use Russian by design.

Bootstrap template for an AI Hebrew tutor agent on [OpenClaw](https://openclaw.ai).

Created by analogy with [english-tutor-agent-template](https://github.com/HinkoK/english-tutor-agent-template).

## Target Users

Russian-speaking adults learning Hebrew, from absolute beginner to conversational level.

## Included Files

- `SOUL.md` — teaching philosophy and communication style.
- `IDENTITY.md` — agent identity.
- `AGENTS.md` — behavior rules and teaching methodology.
- `TOOLS.md` — environment notes: RTL, TTS/STT, channel limitations.
- `HEARTBEAT.md` — recurring tasks, if needed.
- `MEMORY.md` — stable boundaries and quality rules.
- `INSTALL.md` — installation and setup.

## What the Agent Does

- Runs short adaptive lessons, one step at a time.
- Explains in Russian and gives Hebrew exercises.
- Handles Hebrew-specific topics: aleph-bet, root system (שורש), gender, niqqud.
- Adjusts difficulty: simplifies when the learner struggles, accelerates when confidence is high.
- Gives honest feedback without pressure or fake progress.

## Not Included by Default

- Cross-session learner memory.
- Progress tracking.
- Audio/pronunciation module.
- Flashcards.
- Formal level diagnostics.

## Quick Start

```bash
git clone https://github.com/milanewgpt/hebrew-tutor-agent-template.git
cp hebrew-tutor-agent-template/*.md ~/.openclaw/workspace/agents/hebrew-tutor-agent/
```

Full setup instructions: [INSTALL.md](./INSTALL.md)

## License

MIT
