---
name: stock-hiclaw-skill
description: Multilingual public strategy brief for Stock Hiclaw A-share box-breakout research. Use when explaining the four-strategy framework, especially Strict Super Potential and Swing Selected logic, screening boundaries, author/contact copy, and compliant public risk wording.
---

# stock-hiclaw skill

## Purpose

Use this skill to explain the public Stock Hiclaw strategy framework in a compliant, research-oriented way.

Always frame the output as quantitative screening research, not investment advice. Do not promise returns, do not imply guaranteed accuracy, and do not tell users to buy or sell a specific stock.

## Language Rules

Use the language requested by the user:

- If the user writes in Chinese, answer in Chinese.
- If the user writes in English, answer in English.
- If the output is for a public README, landing page, repository, or international audience, provide Chinese and English side by side.
- Keep the original Chinese strategy names visible. On first mention, pair them with English labels:
  - 今日突破 / Today Breakout
  - 超级潜力 / Super Potential
  - 严选超级潜力股 / Strict Super Potential
  - 波段严选 / Swing Selected

Avoid machine-translation-heavy wording. Keep the English version concise, conservative, and research-oriented.

## Strategy Map

Stock Hiclaw has four strategy modules:

1. **今日突破**: stocks that already stand above the box-top area and satisfy current breakout conditions.
2. **超级潜力**: stocks close to the box top, or just slightly above it, intended for short-term observation.
3. **严选超级潜力股**: a stricter subset of Super Potential, using stronger confirmation or calmer setup filters.
4. **波段严选**: swing-oriented candidates that avoid overheated chase entries and favor controlled momentum near the box area.

This public skill documents **严选超级潜力股** and **波段严选** in detail. The other two strategies should be described only at a high level unless the user provides additional source rules.

## Data Assumptions

Use these field concepts when explaining the strategies:

- `price`: latest close or selected signal-day price.
- `boxUp`: upper edge of the box range.
- `distance = (boxUp - price) / boxUp * 100`: positive means still below box top; negative means already above it.
- `breakoutStretch = (price - boxUp) / boxUp * 100`: how far price has stretched beyond box top.
- `tChange`: signal-day percentage change.
- `v5`: current volume divided by 5-day average volume.
- `v20`: current volume divided by 20-day average volume.
- `boxRange`: box range width.
- `longChange`: longer-window price change.
- `longAmp`: longer-window amplitude.
- `macdReady`: MACD is above zero and DIF is greater than or equal to DEA.

## 严选超级潜力股

### Positioning

Describe it as a stricter observation list built on top of Super Potential. Its purpose is to reduce noisy candidates and focus on two profiles:

- **强势确认型**: strong but not excessively stretched confirmation near the box top.
- **温和蓄势型**: calmer setup with improving momentum and lower short-term heat.

### Base Super Potential Gate

A stock should first satisfy the Super Potential style gate:

- Close to the box-top area: `distance` between `-6%` and `3%`.
- Not too extended after breakout: `breakoutStretch <= 8%`.
- Longer-window rise not overheated: `longChange <= 60%`.
- Volume has started to activate: `v5 >= 1.35`.
- MACD trend is ready: `macdReady = true`.
- Box width is healthy: `20% <= boxRange <= 45%`.
- Avoid awkward mid-move samples: exclude `7% <= tChange < 9%`.

### Strict Branches

After passing the base gate, keep the stock only if it matches one of these branches:

**强势确认型**

- `9% <= tChange < 12%`
- `longChange <= 60%`
- `breakoutStretch <= 3%`

**温和蓄势型**

- `tChange < 6%`
- `v5 >= 1.35`
- `DIF - DEA >= 0.2`
- Market is not ChiNext / 创业板.

### Scoring Language

Explain the score as relative ranking inside the filtered pool. It is not a probability of profit.

Public wording:

- "更高门槛样本"
- "策略观察名单"
- "数量会更少"
- "来自历史复盘优化，但不代表未来收益承诺"

## 波段严选

### Positioning

Describe it as a swing-oriented observation strategy. It is designed to avoid overheated chase entries and prefer candidates near the box area with moderate momentum, acceptable volume, and room in the longer trend.

### Screening Gate

A candidate should satisfy:

- Timing near box area: `distance` between `-6%` and `3%`.
- Calm momentum: `1.5% <= tChange <= 9.8%`.
- Volume is active but not extreme: `1.2 <= v5 <= 4.5` and `v20 >= 1.1`.
- MACD trend is ready: `macdReady = true`.
- Box range is usable: `15% <= boxRange <= 50%`.
- Longer trend still has room: `longChange <= 70%` and `longAmp <= 130%`.

### Type Labels

Use these labels:

- If `distance > 0`: **回踩低吸型**.
- If `distance <= 0`: **突破确认型**.

### Scoring Language

Explain score as a ranking that rewards:

- closeness to the box top,
- moderate volume,
- MACD confirmation,
- momentum close to a balanced level around `5%`,
- acceptable box width,
- reasonable longer-window change.

Mention that candidates classified as "今日已突破" may receive a small boost, while "连续突破" can receive a small penalty to reduce chase risk.

Public wording:

- "偏向主线确认后的回踩低吸和突破不远样本"
- "避开过热追高"
- "防守位和卖出纪律仍需独立判断"

## Public Communication Rules

Use safe, compliant language:

- Say "筛选", "观察", "信号", "复盘", "研究辅助".
- In English, say "screening", "watchlist", "signal", "historical review", "research aid".
- Do not say "稳赚", "必涨", "荐股", "买入保证", "目标收益".
- In English, do not say "guaranteed return", "must rise", "stock tip", "buy guarantee", "target profit".
- Add a disclaimer when explaining any strategy:
  - "本内容仅用于量化策略研究和交易复盘，不构成投资建议。"
  - "股票市场有风险，策略信号可能失效。"
  - "This content is for quantitative strategy research and historical review only. It is not investment advice."
  - "The stock market involves risk, and strategy signals may fail."

## Author Copy

Use a restrained author introduction:

Chinese:

"作者是 Stock Hiclaw 研究系统维护者，长期关注 A 股箱体突破筛选、每日复盘、策略可视化和研究流程优化。本公开版定位为研究说明和产品说明，不构成个人投资顾问服务。"

English:

"The author maintains the Stock Hiclaw research system and focuses on A-share box-breakout screening, daily review, strategy visualization, and research workflow optimization. This public version is a research and product brief, not a personal investment advisory service."

Do not claim the author is a licensed investment advisor unless the user provides a verified license and asks to include it.

Do not describe historical strategy performance as guaranteed future accuracy.

## Contact Copy

When public-facing copy needs a contact line, use:

"Stock Hiclaw 目前包含今日突破、超级潜力、严选超级潜力股、波段严选四个策略。想沟通更多策略细节或合作方式，可以通过作者对外公开的微信渠道联系作者。"

For bilingual public copy, use:

"For strategy discussion or collaboration, contact the author through the author's publicly shared WeChat channel. 想沟通更多策略细节或合作方式，可以通过作者对外公开的微信渠道联系作者。"

For privacy and public-repository safety, do not publish:

- personal phone numbers,
- SMS verification codes,
- customer phone numbers,
- customer orders or commission data,
- unconfirmed private WeChat IDs.

Do not invent a WeChat ID. If the user provides a specific WeChat ID later, insert it exactly as provided.
