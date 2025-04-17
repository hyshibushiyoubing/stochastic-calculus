# 📘 QF620 Final Project – Stochastic Modelling in Finance

This repository contains my final project submission for **QF620: Stochastic Modelling in Finance**, covering four major components involving option pricing, model calibration, static replication, and dynamic hedging.

---

## 🧩 Project Structure

### Part I – Analytical Option Pricing
Implemented and derived pricing formulas for:
- Vanilla European options
- Digital cash-or-nothing options
- Digital asset-or-nothing options  
Under the following models:
- Black-Scholes  
- Bachelier  
- Black  
- Displaced-Diffusion

---

### Part II – Model Calibration
Used market data (SPX and SPY options on 1-Dec-2020) and calibrated:
- **Displaced-Diffusion model**
- **SABR model** (β fixed at 0.7)

Outputs:
- Fitted implied volatility smiles
- Estimated parameters (σ, β, α, ρ, ν)
- Sensitivity analysis on β, ρ, and ν

---

### Part III – Static Replication of Exotic Payoffs
Valued an exotic option with payoff:
$$ S_T^(1/3) + 1.5 × log(S_T) + 10 $$


Methods used:
- Black-Scholes (σ selection discussed)
- Bachelier model  
- Static replication using SABR-implied volatilities

---

### Part IV – Dynamic Delta Hedging
Simulated delta-hedged portfolios under Black-Scholes with:
- 21 and 84 hedge intervals (N)
- 50,000 simulation paths
- Histogram analysis of hedging error

Assumptions:
- S₀ = $100, σ = 20%, r = 5%, T = 1/12 (1 month), K = $100

---

## 🙋 Contribution

I was responsible for **Part III – Static Replication of Exotic Payoffs**.
---

