# Extra Notes — Deeper Risk & Money Management

Expands the risk sections spread across [Phase 1](phase1-strategies.md), [Phase 2](phase2-backtesting.md), and [Phase 3](phase3-paper-trading.md). The 1-2%-per-trade rule you already know is the beginner-safe default. This is what's underneath it, and how professionals think about sizing when they go beyond a flat percentage.

---

## 1. The Kelly Criterion — the math behind "optimal" position sizing

The **Kelly Criterion** is a formula that calculates the theoretically optimal fraction of your capital to risk per trade, to maximize long-term account growth given your strategy's actual win rate and reward-to-risk ratio.

Simplified formula: `Kelly % = W − [(1 − W) / R]`
- `W` = your win rate (from your journal — see Phase 2/3)
- `R` = your average win ÷ average loss (reward-to-risk ratio)

**The catch**: full Kelly is mathematically optimal but practically brutal — it often recommends position sizes so large that the short-term volatility and drawdowns are unbearable, even though the *long-run* growth rate is maximized. Almost no professional trader uses full Kelly.

**What's actually used**: **fractional Kelly** — taking some fraction (commonly a quarter to a half) of what the formula recommends, trading off some theoretical growth for a much smoother, survivable equity curve. This is the practical middle ground between "flat 1-2% forever" and "mathematically optimal but terrifying."

**Why this matters even if you never calculate it precisely**: it explains *why* the 1-2% rule exists — it's a conservative, simplified stand-in for a fractional-Kelly-style approach, calibrated for someone who doesn't have (yet) the trade sample size to trust a precise win-rate/reward-ratio input.

---

## 2. Portfolio Heat — thinking beyond one trade at a time

**Portfolio heat** = the total risk currently "live" across all your open positions at once, not just the risk of any single trade.

- If you risk 2% per trade and have 5 positions open simultaneously, your total portfolio heat is up to 10% of your account — meaning a bad day where several trades hit their stops at once could genuinely hurt.
- **Practical rule**: cap total portfolio heat (e.g., never more than 6-8% at risk across all open positions combined), not just per-trade risk. This is why Phase 1/3 capped you at 3-5 open positions — it's an implicit heat limit.

---

## 3. Correlation Risk — why "diversified" positions aren't always diversified

- If you apply your position-sizing rule independently to multiple trades that are actually **correlated** (e.g., 3 different tech stocks, or a stock and an ETF that both track the same index), you're not really spreading risk — you're stacking the same bet three times without realizing it.
- Treating correlated positions as independent for sizing purposes systematically over-bets your real, combined exposure — if a macro event hits that shared factor (a sector sell-off, a rate hike), all positions move together and your actual risk was much higher than the sum of the individual 1-2% allocations suggested.
- **Practical rule** (extending the sector-diversification point from Phase 1): when sizing multiple positions, ask whether they'd likely move together in a shock. If yes, treat them as one combined position for risk purposes, not several independent ones.

---

## 4. Hedging — reducing risk without closing a position

- **Hedging** = taking an offsetting position to reduce risk on an existing one, rather than exiting it outright.
- Simple beginner-relevant example: buying a **put option** ([see options basics](extra2-options-basics.md)) on a stock you own, as insurance against a sharp drop, without having to sell the stock itself.
- Not necessary at the beginner stage — flagged here as a concept that exists once you're managing more capital or a more complex portfolio; the stop-loss you're already using is a simpler, sufficient form of downside protection for now.

---

## 5. Bringing It Together — a practical sizing hierarchy for where you are

1. **Beginner (Phases 0-3, current)**: flat 1-2% risk per trade, hard cap of 3-5 open positions, treat correlated positions as combined exposure.
2. **Once you have 100+ live trades and trust your win-rate/reward-ratio numbers**: consider calculating your fractional Kelly percentage as a sanity check against your flat rule — if Kelly suggests less than 1-2%, that's a signal your edge may be weaker than assumed and you should size down, not up.
3. **Always**: portfolio heat and correlation checks apply regardless of which sizing method you use — they're a ceiling on top of, not a replacement for, per-trade risk rules.

---

## Quick Self-Check
1. Why do professional traders almost never use "full Kelly" position sizing despite it being mathematically optimal?
2. If you risk 2% per trade and have 5 open positions, what's your maximum portfolio heat, and why does that number matter beyond any single trade's risk?
3. Give an example of two positions that look diversified on the surface but are actually correlated — why does that matter for sizing?
4. What's a simple beginner-relevant example of hedging, and how is it different from just setting a stop-loss?

---

## Sources
- [Kelly Criterion Trading: How to Size Positions with Confidence — Above The Green Line](https://abovethegreenline.com/kelly-criterion-trading/)
- [The Kelly Criterion in Financial Markets — Atlas Peak Research](https://www.atlaspeakresearch.com/report/07bf72)
- [Kelly Criterion for Position Sizing Explained — JournalPlus](https://journalplus.co/learn/guides/kelly-criterion-guide/)
- [Kelly Criterion: Optimal Position Sizing for Traders — Ryan O'Connell, CFA](https://ryanoconnellfinance.com/kelly-criterion/)
