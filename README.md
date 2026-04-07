# Beyond Black–Scholes: Local and Stochastic Volatility Modeling for Exotic Option Pricing

A quantitative finance project that goes beyond the constant-volatility Black–Scholes framework by implementing and comparing **Local Volatility (Dupire)** and **Stochastic Volatility (Heston)** models for option pricing.

The project studies the implied volatility smile/skew observed in real markets and shows how advanced volatility models improve pricing consistency for both **vanilla** and **exotic** options such as **barrier options**. It also includes numerical pricing using **Monte Carlo simulation** and **Carr–Madan FFT** methods.

## Overview

The Black–Scholes model assumes constant volatility, which is often insufficient to capture market-implied volatility surfaces. This project explores:

- **Local Volatility modeling** using the Dupire framework
- **Stochastic Volatility modeling** using the Heston model
- **Calibration** to market prices / implied volatility surfaces
- **Exotic option pricing** including barrier and vanilla options
- **FFT-based pricing** using the Carr–Madan approach
- **Monte Carlo simulation** for path-dependent derivatives

## Key Features

- Black–Scholes baseline for comparison
- Dupire local volatility surface construction
- Heston stochastic volatility dynamics
- Calibration framework for market-fit parameters
- Monte Carlo pricing for path-dependent options
- Carr–Madan FFT pricing for efficient European option valuation
- Comparison of model prices against simulated / market-style prices

## Models Covered

### 1. Black–Scholes
A constant-volatility benchmark model used as the starting point for comparison.

### 2. Local Volatility Model
Uses a volatility function that depends on both time and underlying asset price:

\[
dS_t = (r - q)S_t\,dt + \sigma_{loc}(t, S_t)S_t\,dW_t
\]

### 3. Heston Stochastic Volatility Model
Models variance as its own stochastic process:

\[
dS_t = (r - q)S_t\,dt + \sqrt{v_t}S_t\,dW_t^{(S)}
\]

\[
dv_t = \kappa(\theta - v_t)dt + \xi\sqrt{v_t}\,dW_t^{(v)}
\]

with correlation between the two Brownian motions.

## Exotic Options Priced

- Barrier options
- Vanilla call options
- Other path-dependent structures discussed in the report

## Numerical Methods

- **Monte Carlo Simulation** for path-based pricing
- **PDE methods** for model-based valuation
- **Fast Fourier Transform (FFT)** for efficient option pricing
- **Carr–Madan formula** for Fourier-based call pricing under Heston

## Results / Highlights

- Black–Scholes produces a flat implied volatility surface
- Local volatility introduces strike and maturity dependence
- Heston captures skew/smile behavior more realistically
- FFT prices closely match Monte Carlo prices for vanilla options

## Getting Started
### Requirements
- Python 3.10+
- NumPy
- Pandas
- Matplotlib
- SciPy
- Jupyter Notebook
- Installation
- pip install numpy pandas matplotlib scipy jupyter
- Run the Notebook
- jupyter notebook

### Open the notebook and run the cells step by step to reproduce the simulations, calibration, and pricing results.

### Usage
- Load or define market parameters
- Generate the implied volatility surface
- Calibrate the chosen model
- Price vanilla or exotic options
- Compare model outputs with Monte Carlo / FFT results

### Future Improvements
- More robust market calibration
- Arbitrage-free surface interpolation
- Better variance reduction for Monte Carlo
- Support for additional exotic structures
- Visualization dashboard for volatility surfaces and pricing output

##Author
- Dev Patel
