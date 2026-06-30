# stock-hiclaw skill

`stock-hiclaw skill` is the public strategy brief for the Stock Hiclaw box-breakout research system.

`stock-hiclaw skill` 是 Stock Hiclaw 股票箱体突破研究系统的公开策略说明版本。

This public repository is designed for product explanation, strategy communication, and research-oriented discussion. It does not publish private customer data, payment data, backend permissions, or a complete trading execution model.

本仓库用于产品说明、策略沟通和研究复盘，不公开客户数据、支付数据、后台权限规则，也不公开完整交易执行模型。

## Strategy Overview / 策略总览

Stock Hiclaw currently includes four strategy modules:

Stock Hiclaw 目前包含 4 个策略模块：

| Strategy | 中文名称 | Public Scope / 公开范围 |
| --- | --- | --- |
| Today Breakout | 今日突破 | High-level introduction only / 仅做概览说明 |
| Super Potential | 超级潜力 | High-level introduction only / 仅做概览说明 |
| Strict Super Potential | 严选超级潜力股 | Documented in this public version / 本公开版重点说明 |
| Swing Selected | 波段严选 | Documented in this public version / 本公开版重点说明 |

This repository publicly explains **Strict Super Potential / 严选超级潜力股** and **Swing Selected / 波段严选**.

本仓库公开展示其中两个策略的核心说明：**严选超级潜力股** 和 **波段严选**。

## Strict Super Potential / 严选超级潜力股

Strict Super Potential is a higher-threshold observation list built on top of the Super Potential strategy. It aims to reduce noisy candidates and keep two types of samples:

严选超级潜力股是在“超级潜力”基础上继续过滤出来的更高门槛样本。它主要关注两类股票：

- **Strong confirmation / 强势确认型**: price is close to, or has just moved above, the box-top area, but the breakout is not excessively stretched.
- **Calm setup / 温和蓄势型**: short-term heat is lower, volume starts to activate, and MACD momentum improves.

Public explanation:

公开口径可以理解为：

- close to the box-top area, or only slightly above it;
- volume starts to expand;
- MACD trend improves;
- box structure should not be too wide or too narrow;
- reduce mid-move and unstable chase samples.

- 接近箱体上轨或刚突破不远；
- 量能开始放大；
- MACD 趋势向上；
- 箱体结构不能过宽或过窄；
- 主动减少中途追高和胜率不稳定的样本。

## Swing Selected / 波段严选

Swing Selected is a swing-oriented observation strategy. It does not only look at the current day's percentage gain; it focuses more on whether momentum, volume, and box position remain balanced.

波段严选更偏向“主线确认后的波段观察”，不会只看当天涨幅。它更重视：

- whether the price is close to the box-top area;
- whether the current gain is still within a controlled range;
- whether volume expands moderately instead of extremely;
- whether MACD confirms the trend;
- whether longer-window rise and amplitude still leave room;
- whether the sample avoids overheated chase risk.

- 是否靠近箱体上轨；
- 涨幅是否处在相对可控区间；
- 量能是否温和放大，而不是极端放量；
- MACD 是否具备趋势确认；
- 长周期涨幅和振幅是否仍有空间；
- 是否避免已经过热的追高样本。

Public explanation:

公开口径可以理解为：

- **Pullback watch / 回踩低吸型**: the stock has not broken above the box top yet, but is already near the key area.
- **Breakout confirmation / 突破确认型**: the stock has moved above the box top, but the breakout distance is still controlled.

## Author / 作者介绍

The author maintains the Stock Hiclaw research system and focuses on A-share box-breakout screening, daily review, strategy visualization, and research workflow optimization.

作者是 Stock Hiclaw 研究系统维护者，长期关注 A 股箱体突破筛选、每日复盘、策略可视化和研究流程优化。

The public version is written as a research and product brief. It should not be read as a personal investment advisory service, a guaranteed win-rate promise, or a buy/sell instruction.

本公开版定位为研究说明和产品说明，不应被理解为个人投资顾问服务、收益承诺、胜率承诺或具体买卖指令。

## Contact / 联系方式

For strategy discussion or collaboration, contact the author through the author's publicly shared WeChat channel.

想沟通更多策略细节或合作方式，可以通过作者对外公开的微信渠道联系作者。

For privacy and public-repository safety, this repository intentionally does **not** publish:

出于隐私和 public 仓库安全考虑，本仓库不公开：

- personal phone numbers;
- SMS verification codes;
- customer phone numbers;
- customer order or commission data;
- unconfirmed private WeChat IDs.

- 个人手机号；
- 手机验证码；
- 客户手机号；
- 客户订单或佣金数据；
- 未确认可公开的私人微信号。

If a fixed public WeChat ID should be shown later, provide the exact public ID and replace this section with that approved wording.

如后续需要展示固定微信号，请先确认这是可公开发布的微信 ID，再替换为明确联系方式。

## Risk Disclaimer / 风险说明

This content is for quantitative strategy research, historical review, and product explanation only. It is not investment advice and does not promise returns or accuracy.

本仓库内容仅用于量化策略研究、交易复盘和产品说明，不构成投资建议，也不承诺任何收益或胜率。

The stock market involves risk. Strategy signals may fail. Any buy, sell, holding, or position-sizing decision should be made independently by the user according to their own risk tolerance.

股票市场有风险，策略信号可能失效。任何买入、卖出、持仓和仓位决策，都应由使用者根据自身风险承受能力独立判断。
