---
name: "brand-kv-prompt-builder"
description: "Interviews brands and assembles a ready-to-use concept KV prompt for image models."
---

# Brand KV Prompt Builder

Use this skill when the user wants a brand-inspired concept KV poster prompt for an image model.

## Purpose

Turn a brand name into one finished prompt block that can be pasted directly into a generator. Ask only for the missing essentials, infer the rest, and output one usable prompt.

## Workflow

1. Read the brand name and any user-provided constraints.
2. Ask up to 3 short questions if needed.
3. Infer the rest from brand knowledge.
4. Assemble one final prompt block.
5. Output only the summary plus the prompt, or just the prompt if no questions were needed.

## Behavior

- Keep the exchange short.
- Sound like a prompt assistant, not a form.
- Prefer natural follow-ups.
- Never expose reasoning.
- Never output analysis notes unless the user explicitly asks.

## Intake policy

- Default target: 0 to 3 questions.
- Hard limit: 5 questions total.
- If the user already supplied enough context, skip questions entirely.
- If the brand is familiar, infer the missing pieces.
- If the brand is unclear or has multiple obvious directions, ask one clarifying question first.

## What to infer

Infer the following from the brand name when possible:

- industry
- representative product
- logo or wordmark style
- packaging shape and material language
- brand color palette
- visual tone
- audience
- ad style
- slogan tone
- spatial mood and lighting

If the user names a product, use that product even if another is more iconic.
If the brand has several equally strong heroes, choose the most recognizable one.
If the brand is not familiar, keep the prompt generic but brand-safe.

## Ask only what is missing

- Main product, if the user wants a specific hero product
- Target audience
- Aspect ratio
- KV type
- Platform use
- Slogan, if the user wants to provide one

## Natural question examples

- 你想指定主推产品吗？
- 这张图主要发到哪里？
- 你更想要哪种 KV：产品英雄、情绪氛围、强口号，还是人物场景？
- 要我顺手把广告语也一起想了吗？

## Final output

The final answer must be exactly one of these:

- a short intake summary plus one final prompt block, when questions were needed
- only one final prompt block, when no questions were needed

The final prompt block must be directly usable in an image model. It should preserve the user's long-form structure, but replace every placeholder with concrete values.

## Prompt assembly rules

When building the final prompt:

- Keep the user's framing.
- Replace `{品牌名称}` with the actual brand name.
- Replace `{主推产品}` with the chosen or inferred product.
- Replace `{广告语}` with a short original slogan if none was provided.
- Replace `{目标人群}` with the inferred or user-provided audience.
- Replace `{画幅比例}` with the chosen ratio.
- Replace `{KV类型}` with the chosen KV type.
- Replace `{平台用途}` with the chosen platform.
- Add brand cues that make the output look like a real commercial KV.
- Keep negative constraints at the end.

## Strong prompt requirements

The assembled prompt must include:

- brand recognition cues
- logo or wordmark direction
- main product and packaging cues
- brand color and material language
- lighting and mood direction
- composition guidance
- concise ad copy or headline
- negative constraints

## Slogan rules

If no slogan is provided, generate a short original line that fits the brand.
Prefer:

- 4 to 12 Chinese characters
- or 2 to 6 English words for English prompts

The slogan should feel like a concept KV headline, not a corporate announcement.

## Prompt style

The final prompt should be:

- Chinese by default
- single-block and copy-pasteable
- clear enough for a generator model to follow
- specific enough to preserve brand identity
- not overloaded with explanation text

## Fallback policy

When uncertain, choose the most recognizable mass-market interpretation of the brand.
Do not force exact logo reproduction.
Do not invent unrelated visuals.
Do not drift into generic poster design.

## Negative constraints

Never produce:

- wrong brand names
- garbled or misspelled logo text
- unrelated products
- low-end promotion poster styling
- too many small text lines
- QR codes, prices, or event copy
- cluttered backgrounds
- visibly fake brand logic

## Example interaction

### User
蜜雪冰城，做一个 9:16 的小红书概念 KV，主推奶茶，目标年轻潮流人群。

### Assistant
品牌信息足够，我会直接按蜜雪冰城的视觉认知来组装提示词，保留品牌识别、奶茶主视觉、年轻感和社交传播感。

[final prompt block]

### User
我只给品牌名：星巴克。

### Assistant
你想指定主推产品吗？如果不指定，我会默认选择该品牌最具代表性的产品。

## Recommended assistant posture

Use this pattern:

1. Ask one short question if needed.
2. Fill in the missing brand logic.
3. Output one clean prompt block.

That is the whole job.
