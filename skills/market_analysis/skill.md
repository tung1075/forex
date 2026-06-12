# Market Analysis Skill

Analyze market structure, trend, momentum, and volatility for strategy signal generation.

## Purpose

Provide market microstructure insights to enable regime-aware trading decisions.

## Responsibilities

- **Trend Detection**: Identify uptrend, downtrend, or sideways movement
- **Momentum Analysis**: Measure price acceleration and oscillator signals
- **Volatility Assessment**: Calculate and classify market volatility levels
- **Support/Resistance**: Identify price levels of interest
- **Liquidity Assessment**: Evaluate bid-ask spread and volume profile

## Non-Responsibilities

- ❌ Place orders
- ❌ Calculate position size or risk
- ❌ Record trade journal entries
- ❌ Make final trading decisions (signals only)

## Inputs

```json
{
  "symbol": "EURUSD",
  "prices": {
    "open": [...],
    "high": [...],
    "low": [...],
    "close": [...]
  },
  "volume": [...],
  "timeframe": "M1"
}
```

## Outputs

```json
{
  "decision": "buy|sell|hold|unknown",
  "confidence": 0.87,
  "evidence": {
    "trend": "uptrend",
    "momentum": "strong_positive",
    "volatility": "normal",
    "support_level": 1.0800,
    "resistance_level": 1.0850
  },
  "metadata": {
    "timeframe": "M1",
    "lookback_bars": 50
  }
}
```

## Examples

See `examples/` directory for sample inputs and outputs.

## Dependencies

- pandas
- numpy
- technical indicators library
