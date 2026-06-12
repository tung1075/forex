# Journal Engine Skill

Record trade outcomes, evidence, and statistics for performance analysis and learning.

## Purpose

Create an auditable record of all trading activity for post-trade analysis and evolution learning.

## Philosophy

Journal is the datasource for Memory OS and Evolution Engine.

```
Trade Journal
    ↓
Evidence Storage
    ↓
Memory OS
    ↓
Evolution Learning
```

## Responsibilities

- **Save Trade Entry**: Record entry details including setup and evidence
- **Save Trade Exit**: Record exit with result and performance metrics
- **Trade Statistics**: Calculate win rate, profit factor, drawdown
- **Export Journal**: Generate reports for analysis
- **Evidence Linking**: Connect journal entries to market evidence

## Non-Responsibilities

- ❌ Execute trades
- ❌ Make trading decisions
- ❌ Analyze market conditions

## Inputs

```json
{
  "action": "entry|exit",
  "trade_id": "uuid",
  "symbol": "EURUSD",
  "side": "BUY|SELL",
  "entry_price": 1.0850,
  "exit_price": 1.0880,
  "volume": 0.05,
  "result": "win|loss|breakeven",
  "pnl": 150.00,
  "pnl_pct": 1.5,
  "evidence": {},
  "setup_type": "breakout|pullback|reversal"
}
```

## Outputs

```json
{
  "success": true,
  "journal_entry_id": "entry-uuid",
  "trade_id": "trade-uuid",
  "message": "Trade entry recorded",
  "statistics": {
    "total_trades": 45,
    "win_rate": 0.62,
    "profit_factor": 2.3,
    "max_drawdown_pct": 12.5
  },
  "metadata": {
    "recorded_timestamp": "2026-06-12T00:00:00Z"
  }
}
```

## Examples

See `examples/` directory for journal recording examples.
