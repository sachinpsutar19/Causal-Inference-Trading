# Causal Inference Trading (Quantitative Risk Perspective)

## Objective
This project focuses on identifying *causal market risk drivers* rather than relying on simple correlations.
The objective is to estimate the *causal impact of volatility shocks on market returns* from a risk management perspective.

---

## Data
- Instrument: NIFTY 50 Index  
- Frequency: Daily  
- Period: 2018 – 2024  
- Prices adjusted using auto_adjust=True to ensure clean return calculation.

---

## Methodology
1. *Outcome Variable*
   - Daily log returns of the index.

2. *Treatment Variable*
   - Volatility shock defined as days where 20-day rolling volatility exceeds the 75th percentile.

3. *Confounder*
   - Lagged return to control for momentum and mean-reversion effects.

4. *Estimation*
   - Ordinary Least Squares (OLS) regression with controls.
   - Robustness check using continuous volatility instead of a binary shock.

5. *Validation*
   - Residual diagnostics to assess model assumptions.
   - Visualization of volatility regimes and shock thresholds.

---

## Key Findings
- Volatility shocks exhibit a *negative but statistically insignificant effect* on returns.
- The impact of volatility shocks is *unstable and regime-dependent*, varying across normal and crisis periods.
- Results highlight that volatility shocks increase uncertainty but do not guarantee directional return outcomes.

---

## Risk Interpretation
- Financial return series exhibit fat tails and regime shifts.
- Linear causal models capture average effects but underestimate tail risk.
- Volatility shocks should be used as *risk warning signals*, not predictive trading signals.
- The model complements traditional risk tools such as *VaR and stress testing*.

