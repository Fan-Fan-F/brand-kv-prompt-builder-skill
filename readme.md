# Brand KV Prompt Builder Skill

Version 1.0.0. MIT-licensed OpenClaw/Codex Agent Skill for turning brand names into ready-to-use concept KV prompts for image models.

This repository packages the Agent-facing skill contract plus prompt template references. It does not generate images itself. It prepares a complete prompt block that can be pasted into a generator.

## Features

- Short brand intake with minimal questions.
- Brand-aware inference for product, audience, logo language, packaging, palette, mood, and ad style.
- Final output as one copy-pasteable prompt block.
- Chinese default output with clear placeholder substitution.
- Brand-safe fallback when the input is ambiguous.

## Import as an Agent Skill

Copy the `brand-kv-prompt-builder/` directory into the target Agent's skills directory. The Agent should load `brand-kv-prompt-builder/SKILL.md` when asked to turn a brand name into a brand-inspired KV prompt.

## Usage: natural language first

Examples:

- “把蜜雪冰城做成一张 9:16 的小红书概念 KV，主推奶茶，目标年轻潮流人群。”
- “我只给品牌名：星巴克，帮我补全信息并输出可直接喂给生图模型的 prompt。”
- “给我一个蜜雪冰城的产品英雄 KV，顺手生成广告语。”

The Agent should ask only for materially missing choices, infer the rest, and then output one final prompt block.

## Repository layout

- `brand-kv-prompt-builder/SKILL.md`: Agent-facing contract.
- `brand-kv-prompt-builder/references/prompt-template.md`: reusable master prompt template.
- `brand-kv-prompt-builder/references/intake-rules.md`: short question policy.
- `brand-kv-prompt-builder/references/output-format.md`: final response shape.

## License

MIT. See `license`.
