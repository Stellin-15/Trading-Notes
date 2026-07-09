# Phase 2 Notes — Backtesting Your Strategies

Reference sheet for Weeks 9-14. Goal: take the strategies from [Phase 1](phase1-strategies.md) and test whether they would actually have made money historically, before risking a single dollar (even paper dollars) on them.

---

## 1. What Backtesting Actually Is

**Backtesting** = running a strategy's rules against historical price data to see how it would have performed, before trading it live. It's how you find out if a strategy has a real edge or if it just "sounds good."

It will NOT tell you a strategy will definitely work in the future — markets change. But it will tell you whether a strategy has *any* historical basis at all, and roughly what its risk/reward profile looks like (how big are the losing streaks, how often does it win, etc.).

---

## 2. The Three Biases That Silently Wreck Backtests

These are the traps that make a backtest look great on paper and then fail in real trading. Know them before you start — you will be tempted to fall into all three.

- **Curve-fitting (a.k.a. overfitting / data-snooping bias)** — tweaking your strategy's parameters over and over until the backtest numbers look amazing. The problem: you've fit the rules to *that specific slice of history*, not to any real, repeatable market behavior. It'll fall apart on new data. **Guard against it**: keep rules simple, test on more than one time period/stock, and be suspicious of any strategy you had to "tune" heavily to make profitable.
- **Look-ahead bias** — accidentally using information in your test that wouldn't have been available at that moment in real time. Classic example: using a day's *closing* price to decide you'd have entered a trade "that day" — in reality you'd only see the close after the market shut, so you could only act the next morning. **Guard against it**: always ask "could I have actually known this at the time?"
- **Survivorship bias** — testing only on stocks that are still around today (and doing well), silently excluding companies that got delisted, went bankrupt, or were acquired during your test window. This can inflate your apparent returns by several percent a year, compounding into a very misleading picture. **Guard against it**: be skeptical of backtests run only on today's "winners" list (e.g. current S&P 500 members) applied to past years — that index didn't have the same members back then.

---

## 3. Two Ways to Backtest (No-Code Path)

### A) Manual Backtesting — TradingView Bar Replay
No coding required. This is your starting point.
- In TradingView, click the **Replay** button (play-button-with-a-clock icon) on a chart.
- This rewinds the chart to a past date and lets you step forward candle-by-candle, exactly as if you were trading it live — you can't see what happens next, which keeps you honest about look-ahead bias.
- At each candle, apply your strategy's rules (from Phase 1) and decide: would I enter here? Where's my stop? Where's my target?
- Log every decision in a spreadsheet (template below) as you go.
- Do this for **20-30 historical setups minimum** to get a first read on a strategy.

### B) Automated Backtesting — TradingView Strategy Tester
Requires a bit of Pine Script (TradingView's own scripting language — simpler than a general programming language, and there are free templates for the basic strategies in Phase 1, like MA crossovers).
- Once a strategy is coded, the Strategy Tester runs it across years of data in seconds and spits out a full report: Total Net Profit, Max Drawdown, % Profitable Trades, and more.
- Good for once you've validated a strategy manually and want to test it across a much larger sample (hundreds of trades, multiple tickers) faster.
- Not required to start — treat this as an upgrade once Bar Replay feels familiar.

**Optional future path**: once comfortable, some traders move to Python-based backtesting (pandas + libraries like `backtesting.py` or `vectorbt`) for more control. Flagged here as a later upgrade — not needed to get started.

---

## 4. Your Backtest Journal Template

Log every single test trade with these columns (spreadsheet — Google Sheets or Excel):

| Column | What to record |
|---|---|
| Date | The date of the historical setup |
| Ticker | The stock symbol |
| Strategy | Which Phase 1 strategy you're testing (trend/mean-reversion/breakout) |
| Direction | Long or short |
| Entry Price | Where you would have entered |
| Stop-Loss | Your predetermined stop, before the trade |
| Target | Your predetermined take-profit |
| Exit Price | Where the trade actually closed (stopped out, target hit, or rule-based exit) |
| R-Multiple | Result expressed as a multiple of your risk (see below) |
| Win/Loss | Outcome |
| Notes | Anything unusual — market condition, whether volume confirmed, etc. |

**R-Multiple**: if you risked $100 (entry to stop) and made $200, that's a **+2R** trade. If you lost your $100, that's **-1R**. Expressing every trade in R lets you compare strategies and position sizes on equal footing regardless of the dollar amounts involved.

---

## 5. The Metrics That Actually Matter

Once you've logged enough trades, calculate:

- **Win Rate** = (Winning Trades ÷ Total Trades) × 100. On its own this is misleading — a 90% win rate can still lose money if the rare losses are huge, and a 40% win rate can be very profitable if wins are big relative to losses. Never judge a strategy on win rate alone.
- **Average R** = the average R-multiple across all trades. This tells you, per trade, roughly how many multiples of your risk you're netting on average.
- **Expectancy** = the single most important number — it combines win rate and reward-to-risk into one figure that tells you whether the strategy makes money over time. Positive expectancy = you have a real edge. Formula: `(Win% × Avg Win) − (Loss% × Avg Loss)`, expressed in R.
- **Max Drawdown** = the largest peak-to-trough decline in your (paper) account equity during the test, as a percentage. This tells you how painful the worst stretch was — critical for knowing if you could psychologically and financially survive trading this strategy live.

**Sample size**: don't trust conclusions from a handful of trades. You need roughly **30-50 trades minimum** before win rate starts to stabilize, and closer to **100+** before expectancy and other statistics become meaningful. Early results are just noise — resist the urge to declare a strategy "good" or "bad" after 5-10 trades.

---

## Quick Self-Check (test yourself end of Phase 2)
1. Why can a backtest look great and still fail when traded live? Name the three biases.
2. What's the difference between using a day's closing price to *decide* to trade vs. to *enter* a trade — and why does that distinction matter?
3. Why is win rate alone a misleading measure of a strategy's quality?
4. What does a "+2R" trade mean in plain terms?
5. Roughly how many test trades do you need before you can trust your win-rate and expectancy numbers?

If you can answer all five, you're ready for Phase 3 (paper trading these strategies in real time, not just on historical data).

---

## Sources
- [Survivorship Bias In Trading (How To Avoid It) — QuantifiedStrategies.com](https://www.quantifiedstrategies.com/survivorship-bias-backtesting/)
- [Survivorship Bias in Backtesting Explained — LuxAlgo](https://www.luxalgo.com/blog/survivorship-bias-in-backtesting-explained/)
- [Successful Backtesting of Algorithmic Trading Strategies — QuantStart](https://www.quantstart.com/articles/Successful-Backtesting-of-Algorithmic-Trading-Strategies-Part-I/)
- [A Practical Guide To The Backtesting Mistakes That Kill Quant Strategies — HedgeFundAlpha](https://hedgefundalpha.com/education/backtesting-mistakes-kill-quant-strategies-guide/)
- [How to Backtest on TradingView: Bar Replay and Strategy Tester — Pineify](https://pineify.app/resources/blog/how-to-backtest-on-tradingview-comprehensive-2025-guide)
- [TradingView Backtesting 2026 — Strategy Tester & Bar Replay Guide — Quantum Algo](https://www.quantum-algo.com/blog/guides/tradingview-backtesting-complete-guide/)
- [The 5 KPIs That Matter Most in Backtesting a Strategy — FX Replay](https://fxreplay.com/learn/the-5-kpis-that-matter-most-in-backtesting-a-strategy)
- [Key Trading Metrics to Track in Your Journal — JournalPlus](https://journalplus.co/learn/guides/trading-journal-metrics-guide/)
- [Free Excel Trading Journal Template: Columns + Formulas — Traders Second Brain](https://traderssecondbrain.com/guides/excel-trading-journal-template)
