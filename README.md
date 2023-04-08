# Pairs Trader

This is a statistical arbitrage bot created to trade forex pairs through the MetaTrader 5 API. 

The program enumerates all forex pairs (excluding some problematic ones) and tests them all for cointegration first using the Johansen test and then an Augmented Dicky-Fuller, and finally tests them for Mean-Reversion using Hurst exponent. The pairs that pass all three tests are ran through a backtest with Vectorbt. The successful Forex pairs are ran in their own process.
