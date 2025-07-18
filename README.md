# SPY-Heston-Monte-Carlo-stochastic-option-pricing-model


A Python-based Monte Carlo implementation of the **Heston Stochastic Volatility Model** for pricing SPY options and extracting an implied-volatility (IV) surface. Use it to identify mispriced contracts and build volatility-driven trading strategies.

---

## What It Does

* Simulates SPY call-option prices under a Heston stochastic-volatility process.
* Inverts those prices to Black-Scholes implied volatilities.
* Produces an IV surface across strikes and expiries.
* Prints a clean table with  
  – Strike  
  – Days to expiry  
  – Heston price  
  – Model IV (percent).

---

## What to use it for:

* Scan for mispriced volatility across strikes and maturities.  
* Compare model IVs to live or broker-quoted IVs.  
* Feed a delta-neutral or vol-arb trading engine.  
* Back-test IV-based strategies on a consistent, theoretically sound surface.

---

## Inputs

| Parameter | Description                               | Example |
|-----------|-------------------------------------------|---------|
| `S0`      | Current SPY price                         | `500.00` |
| `r`       | Annual risk-free rate                     | `0.01` |
| `v0`      | Initial variance (vol²)                   | `0.04` |
| `theta`   | Long-run variance                         | `0.04` |
| `kappa`   | Mean-reversion speed of variance          | `2.0` |
| `sigma`   | Volatility of volatility                  | `0.5` |
| `rho`     | Correlation between spot and variance     | `-0.7` |
| `expiries`| Option expiries (fraction of years)       | `[7/365, ...]` |
| `strikes` | Strike prices                             | `[470, 480, ...]` |

---

