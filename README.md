# 📘 QF620 Final Project – Stochastic Modelling in Finance

This repository contains my final project submission for **QF620: Stochastic Modelling in Finance**, covering four major components involving option pricing, model calibration, static replication, and dynamic hedging.

---

## 🧩 Project Structure

### Part I – Analytical Option Pricing
Consider the following European options:
- Vanilla European options
- Digital cash-or-nothing options
- Digital asset-or-nothing options
  
Derive and implement the following models to value these options in Python:
- Black-Scholes model
- Bachelier model
- Black model
- Displaced-Diffusion model

---

### Part II – Model Calibration
On 1-Dec-2020, the S&P500 (SPX) index value was 3662.45, while the SPDR
S&P500 Exchange Traded Fund (SPY) stock price was 366.02. The call and
put option prices (bid & offer) over 3 maturities are provided in the
spreadsheet:
- [SPX options.csv](./SPX%20options.csv)  
- [SPY options.csv](./SPY%20options.csv) 
  
The discount rate on this day is in the file: [zero_rates_20201201.csv](./zero_rates_20201201.csv).

Calibrate the following models to match the option prices:
- **Displaced-Diffusion model**
- **SABR model** (β fixed at 0.7)
Plot the fitted implied volatility smile against the market data.

Outputs:
- Fitted implied volatility smiles
- Estimated parameters (σ, β, α, ρ, ν)
- Sensitivity analysis on β, ρ, and ν

---

### Part III – Static Replication of Exotic Payoffs
On 1-Dec-2020, we evaluate an exotic European derivative expiring on 15-Jan-2021 with the following payoff:

1. Payoff function:  
> S<sub>T</sub><sup>1/3</sup> + 1.5 × log(S<sub>T</sub>) + 10.0

2. Model-Free Integrated Variance:

We use the expected integrated variance over the contract's life:

> **σ²<sub>MF</sub> T = E [ ∫₀ᵀ σ<sub>t</sub>² dt ]**

We determine the price of the exotic payoff using:
1. **Black-Scholes model** – Choose an appropriate constant volatility σ  
2. **Bachelier model** – Choose a suitable volatility input  
3. **Static Replication** – Use vanilla European options (via SABR-implied volatilities)

---

## Part IV - Dynamic Hedging

We simulate delta-hedging under Black-Scholes assumptions:

- S₀ = $100  
- σ = 20%  
- r = 5%  
- T = 1/12 year  
- K = $100  
- 21 trading days per month  
- Hedge N times per month

> **Hedged portfolio formula:**  
> C<sub>t</sub> = ϕ<sub>t</sub> S<sub>t</sub> – ψ<sub>t</sub> B<sub>t</sub>

Delta (ϕ<sub>t</sub>) and bond position (ψ<sub>t</sub>) are computed using Black-Scholes greeks and risk-neutral pricing assumptions.



---

## 🙋 Contribution

I was responsible for **Part III – Static Replication of Exotic Payoffs**([`project_part3.ipynb`](./project_part3.ipynb)).

