# Risk Engine Skill

Manage position sizing, stop loss, exposure, and daily risk budgeting for capital protection.

## Purpose

Ensure survival through rigorous capital management and risk control.

## Philosophy

```
Capital Protection
    ↓
Survival
    ↓
Profit
```

## Responsibilities

- **Position Sizing**: Calculate lot size based on risk/reward and equity
- **Stop Loss Placement**: Determine optimal stop loss levels
- **Exposure Control**: Limit total portfolio exposure
- **Daily Risk**: Track and enforce daily loss limits
- **Risk-Reward Ratio**: Validate reward exceeds risk threshold

## Non-Responsibilities

- ❌ Market analysis or trend detection
- ❌ Execution (order placement)
- ❌ Portfolio correlation analysis

## Inputs

```json
{
  "symbol": "EURUSD",
  "account_balance": 10000,
  "account_equity": 9800,
  "entry_price": 1.0850,
  "stop_price": 1.0800,
  "profit_target": 1.0900,
  "daily_loss_limit": 500,
  "daily_loss_to_date": 200,
  "max_daily_drawdown_pct": 5.0
}
```

## Outputs

```json
{
  "allowed": true,
  "position_size": 0.05,
  "unit": "lots",
  "risk_amount": 250,
  "reward_amount": 2500,
  "risk_reward_ratio": 1.0,
  "exposure_percent": 2.5,
  "message": "Position allowed within risk limits",
  "metadata": {
    "calculation_timestamp": "2026-06-12T00:00:00Z",
    "limiting_factor": "daily_loss"
  }
}
```

## Examples

See `examples/` directory for position sizing examples.
