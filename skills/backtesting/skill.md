# Backtesting Skill

Run historical backtests to identify strategy weaknesses, drawdown risks, and optimal regimes.

## Purpose

Validate strategy robustness through historical analysis before live trading.

## Philosophy

Backtesting goal is NOT to prove strategy is correct.

Goal is to find:

```
Weaknesses
    ↓
Drawdown Risk
    ↓
Failing Regimes
    ↓
Failure Conditions
```

## Responsibilities

- **Run Backtest**: Execute strategy on historical data
- **Calculate Metrics**: Compute win rate, profit factor, max drawdown
- **Generate Equity Curve**: Track account equity over time
- **Identify Weak Regimes**: Find market conditions where strategy underperforms
- **Report Drawdowns**: Highlight periods of account deterioration

## Non-Responsibilities

- ❌ Send orders to broker
- ❌ Make live trading decisions
- ❌ Execute trades

## Inputs

```json
{
  "strategy": "strategy_object",
  "symbol": "EURUSD",
  "start_date": "2025-01-01",
  "end_date": "2025-12-31",
  "initial_balance": 10000,
  "lot_size": 0.01,
  "spread_points": 1.5,
  "slippage_points": 0.5
}
```

## Outputs

```json
{
  "success": true,
  "summary": {
    "total_trades": 234,
    "winning_trades": 145,
    "losing_trades": 89,
    "win_rate": 0.62,
    "profit_factor": 2.34,
    "max_drawdown_pct": 18.5,
    "max_drawdown_amount": 1850,
    "final_balance": 12340,
    "total_return_pct": 23.4
  },
  "equity_curve": [...],
  "weak_periods": [...],
  "metadata": {
    "backtest_duration_seconds": 3.4
  }
}
```

## Examples

See `examples/` directory for backtesting examples.
