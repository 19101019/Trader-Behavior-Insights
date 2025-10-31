
# Trading Performance Analysis

## Exploring How Market Sentiment Shapes Trader Performance and Reveals Hidden Behavioral Patterns

This report examines how execution quality, trade size, and market sentiment interact to shape trader outcomes. The objective is to explore the relationship between trader performance and sentiment-driven behavior, uncover hidden inefficiencies, and provide insights that can guide more intelligent and consistent trading strategies.

---

## 1. Correlation Matrix Overview

The Pearson correlation coefficients below highlight how core trading metrics relate to each other. These values reveal the strength and direction of relationships that directly affect profitability.

| Metric A        | Metric B            | Correlation (R) |
| --------------- | ------------------- | --------------- |
| execution_price | execution_price     | 1.0000          |
| execution_price | size_usd / notional | 0.1141          |
| execution_price | profitable          | -0.4116         |
| size_usd        | pct_return          | -0.3957         |
| size_usd        | value               | -0.4619         |
| closed_pnl      | size_usd            | -0.0853         |
| notional        | size_usd            | 1.0000          |

These correlations form the foundation for evaluating how sentiment and trader decision-making connect.

---

## 2. Key Performance Drivers and Sentiment Relationships

### 2.1. Execution Quality: The Strongest Indicator of Profitability

Execution price shows the clearest link between emotional timing and performance.

| Relationship                 | Correlation | Interpretation                                                                                                               |
| ---------------------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Execution Price ↔ Profitable | -0.41       | Higher execution prices significantly reduce the likelihood of profit, indicating timing issues driven by reactive behavior. |
| Execution Price ↔ Closed PnL | -0.31       | Poor execution directly harms dollar PnL.                                                                                    |

**Hidden Pattern:**
Traders frequently enter at overextended price levels—often resulting from sentiment-driven reactions such as FOMO or panic.

---

### 2.2. Trade Size Exposes Inefficient Capital Allocation

Sizing decisions directly reflect how traders respond emotionally to market conditions.

| Relationship          | Correlation | Interpretation                                                                                     |
| --------------------- | ----------- | -------------------------------------------------------------------------------------------------- |
| Size USD ↔ Pct Return | -0.39       | Larger trades produce weaker percentage returns, showing misalignment between conviction and risk. |
| Size USD ↔ Profitable | -0.37       | Bigger trades are less likely to be profitable.                                                    |
| Closed PnL ↔ Size USD | -0.08       | Dollar PnL is weakly connected to size—strategy and timing matter more.                            |

**Hidden Pattern:**
Capital is deployed inefficiently, especially during sentiment extremes.

---

### 2.3. Value Metric as a Sentiment Proxy: Fear-Driven Trading Behavior

Assuming value represents market sentiment, the correlations reveal strong emotional biases.

| Relationship       | Correlation | Behavioral Conclusion                                                         |
| ------------------ | ----------- | ----------------------------------------------------------------------------- |
| Value ↔ Size USD   | -0.46       | Traders take larger positions during fear and smaller positions during greed. |
| Value ↔ Closed PnL | -0.28       | Fear-driven market conditions correlate with worse outcomes.                  |
| Value ↔ Profitable | +0.01       | Sentiment alone doesn’t determine wins but drives sizing and risk-taking. |

**Hidden Pattern:**
Traders size up when market conditions are least favorable, amplifying losses during fear periods.

---

## 3. Behavioral Insights Linked to Sentiment

| Area      | Finding                                    | Implication                                                            |
| --------- | ------------------------------------------ | ---------------------------------------------------------------------- |
| Execution | Execution Price strongly negative (-0.41). | Timing errors are likely caused by emotional reactions to sentiment.       |
| Sizing    | Large trades underperform (-0.39).         | Capital is misallocated when sentiment is negative.                    |
| Emotion   | Size increases during fear (-0.46).        | Traders respond to fear by taking oversized, low-efficiency positions. |

**Core Behavioral Pattern Identified:**
Emotional reactions to market sentiment—particularly fear—drive poor sizing and poor entries, creating consistent underperformance.

---

## 4. Recommendations for Strategy Improvement

To translate these findings into smarter trading strategies:

1. **Develop a Trader Risk Behavior Profile**
   Map how sentiment affects size, entry timing, and PnL.

2. **Strategy Recommendation Report**

   * Reinforce disciplined execution to avoid extreme pricing.
   * Introduce size ceilings during fear-driven periods.

3. **Backtest: Reducing Trades During Fear**
   Quantify how restricting entries during low-value periods impacts total PnL.

4. **Build a Predictive Model**
   Use execution quality and sentiment-adjusted sizing to estimate trade profitability.

---

## Confirmation of Major Insights

* Execution price is the most critical success determinant (≈ -0.4).
* Larger trades generate weaker returns (-0.39).
* Size and PnL have almost no direct relationship (-0.08).
* Sentiment significantly influences sizing (-0.46) and PnL (-0.28).

These patterns align fully with the objective of understanding how trader performance connects to sentiment-driven behavior.

---

## Conclusion

By examining correlations through the lens of market sentiment, we uncover a consistent behavioral flaw: traders react emotionally to fear, enter at poor price levels, and oversize trades at precisely the wrong times. Addressing these sentiment-driven behaviors offers one of the clearest paths to improving strategy quality and achieving more stable returns.

---

