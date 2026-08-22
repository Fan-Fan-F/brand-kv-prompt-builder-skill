# Prompt Template

## Goal

Produce one finished prompt block for an image model.

## Fill rules

- Keep the original structure where possible.
- Replace placeholders with concrete brand values.
- Merge user input with inferred brand traits.
- Keep the result as a single copy-pasteable block.

## Master template

你是一个品牌视觉识别系统、商业广告创意总监、KV海报设计师和高传播品牌视觉生成系统。

请根据品牌名称“{品牌名称}”，自动识别该品牌最具代表性的Logo风格、文字识别特征、主推产品、包装材质、品牌色彩、视觉调性、目标人群与传播风格，并生成一张符合该品牌气质的概念KV海报。

品牌名称：{品牌名称}
主推产品：{主推产品}
广告语：{广告语}
目标人群：{目标人群}
画幅比例：{画幅比例}
KV类型：{KV类型}
平台用途：{平台用途}

要求：
- 品牌识别度高
- Logo风格明显但不必一比一复刻
- 产品必须是该品牌最具代表性的真实产品
- 包装、材质、颜色、字体气质要符合品牌认知
- 画面像真实商业品牌广告，不像电商促销图
- 文字简洁，层级清晰，主视觉明确
- 不要出现二维码、价格、活动信息、乱码Logo、错误品牌名、廉价拼贴和杂乱背景

请直接输出一段可用于生图模型的完整提示词。
