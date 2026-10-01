# Relative Valuation Screener: Semiconductors

A Python screen that ranks major semiconductor companies by a peer-relative composite valuation score, used to build an investment thesis on Micron Technology (MU).

📄 **[Read the full investment thesis (PDF)](Micron_Technology__MU__Investment_Thesis.pdf)**

## Overview

The screen covers ten major semiconductor companies: AMD, NVDA, INTC, QCOM, AVGO, TXN, MU, ON, MRVL and ADI.

Each stock is scored on three valuation multiples, which are standardised into z-scores relative to the peer group and combined into a single composite score. A negative composite means the stock is cheaper than its peers on average.

## Methodology

- **Multiples used:** trailing P/E, EV/EBITDA, Price/Book
- **Standardisation:** each multiple converted to a z-score against the peer set
- **Composite score:** z-scores combined into one peer-relative valuation score
- **Fundamentals check:** revenue growth and profit margin compared alongside valuation to spot mismatches between price and quality

## Key Finding: Micron

| Metric | Micron | Context |
|---|---|---|
| Revenue growth (YoY) | 345.7% | Highest in peer set by a wide margin |
| Profit margin | 55.9% | Second highest in peer set |
| Composite valuation z-score | −0.48 | Among the cheapest in the peer set |

The anomaly: the company with the best growth and near-best profitability in the sector screens below the peer-average valuation.

The [full thesis](Micron_Technology__MU__Investment_Thesis.pdf) explains why the gap exists (high-bandwidth memory demand from AI data centres, sold-out fixed-price contracts), and weighs the bull case against the bear case of a classic memory-cycle peak. **Recommendation: BUY**, framed as a bet on how long the AI memory supply-demand imbalance lasts.

<!-- Add a chart here if you have one, e.g.:
![Composite valuation z-scores by company](images/composite_scores.png)
-->

## Limitations

- Trailing multiples are a blunt tool for a company mid-inflection. Micron trades at roughly 44x trailing earnings but below 9x forward, so the screen's answer depends heavily on the earnings base used
- The screen is a single point-in-time snapshot
- A fuller analysis would add forward-looking multiples and scenario sensitivity

## How to Run

```bash
pip install pandas matplotlib yfinance
jupyter notebook RVSModel.ipynb
```

## Tech

Python · pandas · yfinance · matplotlib 
