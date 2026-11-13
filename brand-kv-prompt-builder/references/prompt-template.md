# Prompt Template

## Goal

Produce one finished prompt block for an image model.

## Fill rules

- Keep the original structure where possible.
- Replace retained placeholders with concrete values from user input, verified references, or choices for this concept.
- Remove optional copy or logo lines when the user excludes them. Carry those exclusions into the image constraints.
- Use the specified hero product. Describe original packaging or identity as a design proposal when no existing reference is available.
- Keep the result as a single copy-pasteable block.

## Master template

为品牌“{品牌名称}”生成一张概念 KV 海报。以下品牌名称用于描述创作主体。画面中只呈现明确指定的文字和标识。

品牌名称：{品牌名称}
主推产品：{主推产品}
画面广告语（可选）：{广告语}
标识位置与样式（可选）：{标识方向}
目标人群：{目标人群}
画幅比例：{画幅比例}
KV类型：{KV类型}
平台用途：{平台用途}

要求：
- 以指定产品为主视觉，构图采用{构图}。
- 画面使用{配色}、{材质}与{光线}。按用户提供的产品和包装参考保留关键细节。
- 视觉层级清晰，背景简洁。允许出现文字时，仅使用给定文案。
- 负面约束：{用户明确排除的元素}。避免二维码、价格、活动信息、乱码、廉价拼贴和杂乱背景。
