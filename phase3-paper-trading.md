# Phase 3 Notes — Paper Trading

Reference sheet for Weeks 15-22. Goal: trade your [Phase 1](phase1-strategies.md) strategies live, in real time, with fake money — the step between "this looked good in a backtest" and "this is my actual behavior under real market conditions." Backtesting proves a strategy *could* work on the past; paper trading proves *you* can execute it in the present.

---

## 1. Setting Up a Paper Trading Account

You have several free options — pick one and stick with it rather than platform-hopping:

- **TradingView** — built-in paper trading account with $100,000 virtual cash, works directly on the charts you're already using for backtesting. Easiest option if you're already living in TradingView from Phase 2.
- **thinkorswim (Charles Schwab) — paperMoney** — sign up for a free Guest Pass, get a simulator account with $100,000 in virtual buying power, toggle "paperMoney" mode (interface turns orange) to trade against live market data.
- **Webull** — gives $1,000,000 virtual cash, one-tap toggle between paper and live trading in the mobile app — fastest to get going from a phone.

**Important setup step**: change the paper account's starting balance to match the amount you actually plan to trade with live (e.g. if you're planning to start with $2,000-$5,000 real money, set the paper account to that, not the default $100k-$1M). Trading a $100k paper account teaches you nothing about position sizing at your real, smaller account size — the psychology and math are completely different.

---

## 2. How Long / How Many Trades

Don't rush this phase — it exists to protect your real capital later.

- **Minimum**: 30-50 trades with consistent rule-following before even considering real money.
- **Better target**: 50-100+ trades, ideally across at least 2-3 months, so you experience different market conditions (not just one lucky trending month).
- Sample size matters here for the same reason it mattered in backtesting (see [Phase 2](phase2-backtesting.md)) — a handful of paper trades tells you almost nothing; it takes volume to see if your edge and your discipline are both real.

**Readiness checklist before going live** — you should be able to say yes to all of these:
- I can stick to my entry/exit/stop rules consistently (not just when it's easy).
- My max drawdown in paper trading stayed within a range I could stomach with real money.
- I can explain, in plain language, *why* I took every trade — no "gut feeling" entries.
- I've been through both a losing streak and a winning streak without changing my rules mid-stream.

---

## 3. Keep the Same Journal — Track Two Things Separately

Reuse the exact journal template from Phase 2 (Date, Ticker, Strategy, Direction, Entry, Stop, Target, Exit, R-Multiple, Win/Loss, Notes) — consistency between backtesting and paper trading lets you compare the two directly.

Add one more thing that backtesting can't capture: **did you actually follow your own rules?**

- **Rule adherence** — track this separately from P&L. A losing trade where you followed every rule perfectly is a *good* trade in the sense that matters (process). A winning trade where you broke your stop-loss rule and got lucky is a *bad* trade — it will bite you eventually if repeated.
- Tag each trade: did you enter on your actual signal, or did you chase? Did you honor your stop, or move it? Did you take profit at your target, or get greedy/fearful and exit early/late?

---

## 4. The Discipline Problems That Show Up Here (Not in Backtesting)

Backtesting has no emotions. Paper trading — even with fake money — starts revealing the behavioral patterns that will threaten your real account later. Watch for:

- **Revenge trading** — breaking your entry rules to chase a trade and "win back" a previous loss. This is one of the most account-destroying patterns there is, and it starts as a discipline problem, not a strategy problem.
- **Overtrading** — exceeding your own daily/weekly trade limits because you're bored, chasing action, or anxious to "make something happen."
- **FOMO entries** — jumping into a trade that doesn't actually meet your setup criteria because the price is moving without you.
- **Moving your stop** — the single most common rule violation; it turns a defined, small loss into an undefined, growing one.

**The key structural fix**: discipline that depends on willpower alone will fail eventually. Replace willpower with systems:
- A short pre-trade checklist (does this setup actually meet my Phase 1 rules? yes/no, no exceptions).
- Grade your setups (A/B/C) and only take A/B trades.
- A **reset rule**: the trade right after a rule violation or a loss is the highest-risk moment for compounding the mistake into a spiral. Build in a mandatory pause (or end the session) after any rule violation, rather than trying to immediately "fix it" with another trade.

---

## 5. Risk Management for This Stage

- **1-2% risk per trade** — same rule as backtesting, but now apply it with real position-sizing math against your paper account's (realistic) balance.
- Set a **daily loss limit** and a **weekly loss limit** (e.g., stop trading for the day/week if you hit -3% to -5%). This exists specifically to prevent the revenge-trading spiral above.
- Cap concurrent open positions (3-5, per Phase 1) so you can actually track and manage each one properly.

---

## 6. Weekly Review Ritual

Every week, sit down with your journal and ask:
1. What worked? Which setups produced the best R-multiples?
2. What didn't? Any recurring losing pattern?
3. Rule violations — how many, and what triggered them (boredom, fear, a specific market condition)?
4. Pick **one** specific process change to make next week based on the most common trigger — don't try to fix everything at once.

---

## Quick Self-Check (test yourself end of Phase 3)
1. Why should your paper account balance match your planned real account balance, not the platform's $100k default?
2. What's the difference between judging a trade by its P&L versus judging it by rule adherence — and why does the second one matter more at this stage?
3. What is revenge trading, and what's the single structural rule that prevents its spiral?
4. Roughly how many paper trades, and over what timeframe, should you complete before considering real money?
5. Name three of the four readiness criteria before going live.

If you can answer all five — and your journal shows real rule adherence over 50-100+ trades — you're ready for Phase 4 (real money).

---

## Sources
- [thinkorswim® paperMoney®: Stock Trading Simulator — Charles Schwab](https://www.schwab.com/learn/story/thinkorswim-papermoney-stock-trading-simulator)
- [How to Set Up a Paper Trading Account (Step-by-Step) — DayTradingToolkit](https://daytradingtoolkit.com/beginners-guide/how-to-use-paper-trading-account)
- [Paper Trading: The Complete Guide to Risk-Free Practice — ChartMini](https://chartmini.com/blog/paper-trading-guide)
- [Paper Trading vs. Live Trading: A Data-Backed Guide — Alpaca](https://alpaca.markets/learn/paper-trading-vs-live-trading-a-data-backed-guide-on-when-to-start-trading-real-money)
- [Paper Trading Practice: How to Build Trading Skill Before Going Live — WeMasterTrader](https://wemastertrade.com/paper-trading-practice-how-to-build-trading-skill-before-going-live/)
- [Trading Discipline: Follow Your Rules Every Session — Traders Second Brain](https://traderssecondbrain.com/guides/trading-discipline)
- [Trading Discipline: The Rule Adherence Score — TradeZella](https://www.tradezella.com/blog/trading-discipline)
- [Trading Journal Emotional Discipline Checklist — WealthBee](https://wealthbee.io/learn/trading-journal-emotional-discipline-checklist/)
