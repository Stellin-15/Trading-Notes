# Phase 1 Notes — Core Strategy Archetypes & Technical Analysis

Reference sheet for Weeks 4-8. Goal: understand 4 strategy archetypes well enough to recognize them on a chart and state their entry/exit/stop rules from memory. These are suited to swing/position trading (holding days to weeks) — appropriate for a 5-10 hr/week side pursuit, not day trading.

For each strategy: **what it is → entry rules → exit/stop rules → when it works / when it fails.**

---

## 1. Trend-Following (Moving Average Crossover)

**Core idea**: identify an existing trend and ride it, rather than predicting reversals. "The trend is your friend."

**How it works**
- Use two moving averages: a fast one (e.g. 20-day SMA or 9-day EMA) and a slow one (e.g. 50-day SMA or 21-day EMA). Common pairs: 20/50, 50/200 ("golden cross" when fast crosses above slow on the 50/200 pair).
- **Bullish crossover** — fast MA crosses above slow MA → interpreted as upward momentum starting.
- **Bearish crossover** — fast MA crosses below slow MA → downward momentum.

**Entry rules**
- Go long when the fast MA crosses above the slow MA, or when price is above both MAs and pulls back to the fast MA then bounces.
- Filter: only take the signal if **ADX > 20-25** (confirms the market is actually trending, not choppy). Without this filter, raw crossovers tend to just break even — whipsaws in sideways markets chew up small gains. The filter isn't optional decoration; it's the actual edge.

**Exit / stop rules**
- Exit when the fast MA crosses back below the slow MA (momentum gone).
- Safety-net exit: if price closes below the slow MA, treat that as a sign medium-term support failed.
- Stop-loss: 2× ATR (Average True Range) below entry, trailed upward as the slow MA rises.

**Works well in**: strong, sustained directional markets (bull or bear runs).
**Fails in**: sideways/choppy/range-bound markets — you'll get repeatedly stopped out on false crossovers (whipsaws).

---

## 2. Mean-Reversion (RSI + Bollinger Bands)

**Core idea**: prices that move too far, too fast from their average tend to snap back toward it. You're betting on a bounce back to "normal," not a new trend.

**How it works**
- **Bollinger Bands**: a 20-day SMA (middle band) plus upper/lower bands set 2 standard deviations away. Bands widen when volatile, narrow when calm.
- **RSI (Relative Strength Index)**: 14-day momentum oscillator, 0-100. Above 70 = overbought, below 30 = oversold.

**Entry rules**
- **Long**: price closes at/through the lower Bollinger Band AND RSI is oversold (below 30) — ideally confirmed by a bullish candle closing back inside the band.
- **Short**: price closes at/through the upper Bollinger Band AND RSI is overbought (above 70), confirmed by a bearish candle.

**Exit / stop rules**
- Target: the middle band (20-day SMA) — that's the "mean" you're reverting to. Take profit there, don't get greedy for more.
- Stop-loss: 2× ATR(14) beyond your entry (below for longs, above for shorts).

**Works well in**: sideways, range-bound, choppy markets with no strong trend.
**Fails in**: strong trending markets — bands expand, price can "walk the band" (stay pinned to the upper/lower band for days), and buying "oversold" in a real downtrend just means catching a falling knife. Always check you're not fighting a trend from Strategy 1 above.

---

## 3. Breakout Trading

**Core idea**: when a stock has been coiled in a tight range (consolidation), the move that follows the range's end can be fast and sizable. You're trying to catch the start of that move, not the middle of it.

**How it works**
- **Consolidation patterns to watch for**: tight sideways ranges, triangles, flags, rectangles — price compresses, volume typically dries up while it does.
- A breakout is price closing decisively above resistance (or below support) that bounded the range.

**Entry rules**
- Wait for a strong close beyond the range boundary (resistance for longs, support for shorts) — not just an intraday poke through the line.
- **Volume confirmation is the key filter**: only trade the break if volume is meaningfully above the recent average (rule of thumb: at least 50-100%+ above the 20-day average volume). A breakout on low volume is a low-quality signal and prone to failing/reversing ("false breakout").

**Exit / stop rules**
- Stop-loss: just beyond the broken support/resistance level, or sized off ATR.
- Target: use a favorable risk/reward ratio, commonly aiming for at least 1:2 (risking 1R to make 2R+).
- Standard risk management applies regardless of strategy: 1-2% of account risked per trade.

**Works well in**: stocks coming out of genuine accumulation/distribution with real volume behind the move (often around catalysts — earnings, news).
**Fails in**: low-volume breakouts, or breakouts in choppy markets that just fake out both directions ("bull trap" / "bear trap").

---

## 4. Fundamentals Overlay (Lightweight — not deep value investing)

**Core idea**: technical setups work better when the underlying stock has a tailwind behind it — a catalyst, strong earnings, or a strong sector. This isn't about deep-dive valuation modeling; it's a filter layered on top of Strategies 1-3.

**Components**
- **Earnings / catalysts**: watch earnings dates. A stock that gaps up on earnings with strong volume often keeps drifting in that direction for days as more buyers pile in — the "gap and go" pattern. The disciplined entry is on the first pullback after the gap, not chasing the initial spike.
- **Sector strength**: compare a stock's sector performance against the broader market (S&P 500). Trading breakouts/trends in outperforming sectors improves odds versus fighting a weak sector.
- **Correlation risk**: if you hold multiple positions in the same sector and a macro event hits that sector, all your positions drop together. Spread swing trades across 2-3 different sectors rather than stacking all of them in one.

**How to use this layer**: before taking a technical signal from Strategies 1-3, ask — is this stock in a strong sector, and is there a recent catalyst (earnings beat, news) supporting the move? If yes, the technical signal has more behind it. If the stock is fighting its sector with no catalyst, treat the signal with more skepticism.

---

## Universal Risk Rules (apply to all 4 strategies)

- Risk only **1-2% of account capital per trade** — this is the single biggest lever for surviving a string of losses.
- Always define your stop-loss *before* entering, not after.
- As a beginner, cap yourself at **3-5 open positions** at once so you can actually manage them.
- Every strategy above has a regime it fails in — knowing *when not to use it* matters as much as the entry rules.

---

## Quick Self-Check (test yourself end of Phase 1)
1. Why does a moving-average crossover strategy need an ADX filter to actually work?
2. In a mean-reversion setup, what's the difference between "oversold" in a sideways market vs. "oversold" in a strong downtrend?
3. Why is volume the deciding factor between a real breakout and a false one?
4. If you own 5 stocks all in the same sector, what risk are you exposed to that diversification across sectors would reduce?
5. Which of the 4 strategies would you avoid using in a strongly trending market, and why?

If you can answer all five in your own words, you're ready for Phase 2 (backtesting these strategies to see if they'd actually have worked historically).

---

## Sources
- [Moving Average Crossovers for Entry and Exit — LuxAlgo](https://www.luxalgo.com/blog/moving-average-crossovers-for-entry-and-exit/)
- [Moving Average Crossover Strategies: A Complete Guide — TrendSpider](https://trendspider.com/learning-center/moving-average-crossover-strategies/)
- [Trend Following Strategy: Trading Strategies and Systems — QuantifiedStrategies.com](https://www.quantifiedstrategies.com/trend-following-trading-strategy/)
- [Enhanced Mean Reversion Strategy with Bollinger Bands and RSI Integration — Medium](https://medium.com/@redsword_23261/enhanced-mean-reversion-strategy-with-bollinger-bands-and-rsi-integration-87ec8ca1059f)
- [Mean Reversion Trading: Fading Extremes with Precision — LuxAlgo](https://www.luxalgo.com/blog/mean-reversion-trading-fading-extremes-with-precision/)
- [Mean Reversion Strategies: Introduction, Building Blocks — QuantInsti](https://blog.quantinsti.com/mean-reversion-strategies-introduction-building-blocks/)
- [Breakout Trading: Definition, Strategies, Pros & Cons — Forextester](https://forextester.com/blog/breakout-trading-strategy/)
- [Volume Breakout Strategy — Pro Trader Dashboard](https://protraderdashboard.com/blog/volume-breakout-strategy/)
- [How Volume Confirms Breakouts in Trading — LuxAlgo](https://www.luxalgo.com/blog/how-volume-confirms-breakouts-in-trading/)
- [Swing Trading Guide 2026 — MNCL Group](https://www.mnclgroup.com/swing-trading-complete-guide-for-beginners-to-pro-swing-trading-guide)
- [7 Swing Trading Strategies That Actually Work — TradingSim](https://www.tradingsim.com/blog/swing-trading-strategies)
