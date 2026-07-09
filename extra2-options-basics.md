# Extra Notes — Options Trading Basics

A new topic beyond stocks/equities. Options are more complex and riskier to misuse than plain stock trading — treat this as background knowledge for later, not something to trade before you're solid on Phases 0-4. Flagged in [Phase 0](phase0-foundations.md) as "advanced — not touching this until stocks are solid," this is that deeper look, for whenever you're ready.

---

## 1. What an Option Actually Is

An **option** is a derivative — a contract whose value is derived from an underlying asset (usually a stock). It gives the buyer the **right, but not the obligation**, to buy or sell that stock at a specific price by a specific date. You're buying a choice, not a commitment.

Two types:
- **Call option** — the right to **buy** the stock at a set price. Buyers want the stock to go UP.
- **Put option** — the right to **sell** the stock at a set price. Buyers want the stock to go DOWN.

## 2. The Core Vocabulary

- **Strike Price** — the fixed price at which you can buy (call) or sell (put) the stock, regardless of where the stock is actually trading.
- **Expiration Date** — the date the contract expires. After this, the option is worthless if not exercised.
- **Premium** — the price you pay to buy the option contract (paid upfront, non-refundable). Quoted per-share, but each contract covers 100 shares — so a premium quoted at $3.50 actually costs $350 for one contract ($3.50 × 100).
- **In the Money (ITM) / Out of the Money (OTM)**:
  - A call is ITM when the stock price is *above* the strike (it'd be profitable to exercise).
  - A put is ITM when the stock price is *below* the strike.
  - OTM is the opposite in each case — the option currently has no "exercise value," only time value.

## 3. Buying a Call (the simplest bullish options play)

- You pay a premium for the right to buy the stock at the strike price.
- **Max loss**: capped at the premium you paid — you simply let the option expire worthless if the stock doesn't cooperate. This is a key structural advantage over plain stock ownership: your downside is fixed and known upfront.
- **Max gain**: theoretically unlimited as the stock price rises above the strike.
- **Break-even**: strike price + premium paid.

## 4. Buying a Put (the simplest bearish/hedging play)

- You pay a premium for the right to sell the stock at the strike price.
- **Max loss**: capped at the premium paid.
- **Max gain**: large (though capped, since a stock can only fall to $0) as the stock price falls below the strike.
- Often used as **insurance/hedging** — e.g., an investor holding a stock can buy puts to protect against a big drop, similar in spirit to the stop-loss concept from Phase 0, but bought as insurance rather than a hard exit order.

## 5. Why Options Are Riskier to Misuse Than They Look

- **Time decay (theta)** — an option loses value simply as time passes, even if the stock doesn't move, because there's less time left for the bet to pay off. This means you can be "right" about direction and still lose money if it takes too long.
- **Selling options (as opposed to buying them)** carries fundamentally different, often much larger risk — e.g., selling a "naked" call has theoretically unlimited loss potential. This is an entirely different risk profile than buying calls/puts and is not something to approach without a solid grasp of the buyer's side first.
- **Leverage cuts both ways** — options let you control 100 shares' worth of exposure for a fraction of the stock's price, which magnifies both gains and losses relative to your capital, similar in spirit to the margin/leverage warning in Phase 0 — but faster and with an expiration clock attached.

## 6. Where This Fits Your Roadmap

Do not treat options as a shortcut past Phases 1-4. The suggested order:
1. Get solid at spot/stock trading first — strategy discipline, backtesting, paper trading, and psychology all transfer directly.
2. If you explore options later, start with simply **buying calls/puts** (defined, capped risk) before ever considering selling/writing options (undefined or large risk).
3. Paper trade options specifically before using real money on them — the mechanics (strike selection, expiration timing, premium pricing) are different enough from stock trading that your stock-trading paper trading reps don't automatically transfer.

---

## Quick Self-Check
1. What's the maximum you can lose buying a single call option, and why is that a structural advantage over owning the stock outright?
2. Why can you be right about a stock's direction and still lose money on an option you bought?
3. What's the difference in risk between *buying* a put and *selling* (writing) a call?
4. Why shouldn't you skip straight to options before being solid on the stock-trading roadmap (Phases 0-4)?

---

## Sources
- [Basic Call and Put Options Strategies — Charles Schwab](https://www.schwab.com/learn/story/basic-call-and-put-options-strategies)
- [What are call and put options? — Vanguard](https://investor.vanguard.com/investor-resources-education/understanding-investment-types/what-are-call-put-options)
- [What Is Options Trading? Understanding Calls, Puts and the Basics — Chase](https://www.chase.com/personal/investments/learning-and-insights/article/options-trading-calls-puts-basics)
- [Options: Calls and Puts - Overview, Examples, Trading Long & Short — Corporate Finance Institute](https://corporatefinanceinstitute.com/resources/derivatives/options-calls-and-puts/)
