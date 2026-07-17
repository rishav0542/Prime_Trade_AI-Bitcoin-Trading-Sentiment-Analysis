# Primetrade.ai Data Science Intern Assignment – 1-Page Report
**Trader Performance vs BTC Market Sentiment (Fear/Greed) on Hyperliquid**

**Candidate:** Rishav | **Date:** July 2026

## Methodology (Part A)
- **Data**: Fear & Greed Index (daily) + Hyperliquid trades (~211k rows).
- **Key adaptation**: No leverage column → used **avg trade size (Size USD)** as risk/leverage proxy.
- Grouped trades by (date, Account) → daily metrics: `daily_pnl`, `win_rate`, `num_trades`, `avg_trade_size`, `long_proportion`.
- Merged with sentiment and filtered to Fear/Greed days.

## Part B – Key Findings
**Performance**  
Greed days show significantly higher avg daily PnL and win rate (p < 0.05).

**Behavior**  
Traders use larger size, trade more, and show stronger long bias on Greed days.

**Segments**  
- Size segments (Low/Med/High Size – leverage proxy)  
- Winner segments (Inconsistent/Average/Consistent Winners)  
High Size traders amplify outcomes; Consistent Winners perform well in both regimes.

**3+ Insights**  
1. Greed days drive better performance and more aggressive trading.  
2. Traders actively adapt behavior to sentiment.  
3. High-risk traders amplify sentiment effects (big opportunity + big risk).  
4. Consistent Winners have a resilient edge.

## Part C – Actionable Strategies
**Rule 1: Adaptive Position Sizing**  
- Fear days: Reduce size 30–50% (especially High Size traders).  
- Greed days: +15–25% size boost **only** for Consistent Winners.

**Rule 2: Selective Activity**  
- Increase frequency/size in Greed **only** for Consistent Winners.  
- In Fear: Defensive sizing for all; extra caution on High Size accounts.  
- Never boost Inconsistent traders.

These rules are evidence-based, segment-aware, and directly testable.

**Visuals & full code** available in repo. All statistical tests and charts included.
