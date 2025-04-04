 Real-Time Option Greeks Calculator using KiteConnect

This project calculates real-time option Greeks — Delta, Theta, Gamma, Vega, Vomma, and Implied Volatility (IV) — for NIFTY options using the Black-Scholes Model.

⚙️ Key Features
Fetches live market data from Zerodha's Kite API.
Supports both CE and PE options across a range of strikes around ATM.

Calculates:
Delta – Price sensitivity
Theta – Time decay
Gamma – Rate of change of delta
Vega – Sensitivity to volatility
Vomma – Sensitivity of vega to volatility
Implied Volatility (IV) using Brent's method

Logs Greeks values every minute during market hours.
Plug-and-play architecture for expiries, risk-free rates, dividend yield, etc.

* Requirements
  
kiteconnect
pandas, numpy
scipy, math
datetime, logging

* Logic Overview
  
Retrieves NIFTY index spot price.
Iterates over multiple strikes for both Call and Put options.
Pulls option premium using historical_data.
Applies Black-Scholes Model to:
Calculate Greeks
Derive IV using Brent’s root-finding algorithm

* Output Example
  
Each log entry (updated every minute during market hours):

2025-01-31 09:45:00 - Strike 22500 CE: Delta=0.6123, Theta=-6.1423, Vega=12.4321, Gamma=0.0021, Vomma=1.4323

* Where to Use
  
Greeks-based option strategies (e.g., Delta-neutral, Vega-neutral)
Real-time risk management
Volatility modeling

*Note* 

Designed for live market conditions.
Requires active KiteConnect session and access to instruments list.
Modify Expiry, Rosk free rate, Dividend yield as per requirement.
