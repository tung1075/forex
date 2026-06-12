# Execution Engine Skill

Execute trading operations: open, modify, close trades and maintain broker synchronization.

## Purpose

Reliably and accurately execute trading instructions with broker sync and order tracking.

## Responsibilities

- **Open Order**: Place new entry orders
- **Modify Order**: Update existing order parameters (stop, target)
- **Close Order**: Close or partially close positions
- **Order Sync**: Maintain order state synchronization with broker
- **Error Handling**: Gracefully handle order rejection/cancellation

## Non-Responsibilities

- ❌ Market analysis or signal generation
- ❌ Position sizing or risk calculation
- ❌ Strategy decision making

## Inputs

```json
{
  "action": "open|modify|close",
  "symbol": "EURUSD",
  "side": "BUY|SELL",
  "volume": 0.05,
  "entry_price": 1.0850,
  "stop_loss": 1.0800,
  "take_profit": 1.0900,
  "order_id": "optional-for-modify-close",
  "magic_number": 29052026
}
```

## Outputs

```json
{
  "success": true,
  "order_id": "MT5-12345",
  "action_taken": "open",
  "symbol": "EURUSD",
  "volume": 0.05,
  "entry_price": 1.0851,
  "status": "filled",
  "error": null,
  "metadata": {
    "execution_timestamp": "2026-06-12T00:00:00Z",
    "execution_time_ms": 234
  }
}
```

## Examples

See `examples/` directory for order execution examples.
