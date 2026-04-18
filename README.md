# Ark Indicator - Smart Money Concepts Toolkit

## Overview
Advanced TradingView Pine Script v6 indicator implementing institutional Smart Money Concepts (SMC):

**Core Features:**
- Killzones (Sydney/Asia/London/NY AM/PM)
- Order Blocks & Breaker Blocks
- Fair Value Gaps (FVG)
- Market Structure Shifts (MSS/CHoCH)
- Equal Highs/Lows (EQH/EQL)
- Market Open Gaps (MOG/GAP)
- Liquidity Timing Lines
- Moving Averages (21EMA/50SMA/200SMA)
- Real-time Dashboard (RSI + Session + Liq)

## Quick Start
1. Copy Ark_Indicator_copy.pine
2. Pine Editor → Paste → Save → Add to Chart
3. Settings → Configure sessions/colors
4. Test on 1H/15M XAUUSD chart

## Key Settings
```
Sessions: UTC-4 (NY Time)
FVG Filter: 0.5 ATR (adjust for volatility)
OB Length: 5 bars swing detection
MSS Length: 7 bars pivot detection
Liq Labels: Toggle for timing lines
```

## Trading Sessions (EST)
```
Pre-Asian: 6PM-8PM
Asian Open: 8PM-9:30PM
Pre-London: 1AM-3AM
London Open: 3AM-4:30AM
Pre-NY: 6:30AM-8AM
NY Open: 8AM
NYSE: 9:30AM
London Close: 10AM-11AM
```

## Status: Production Ready
```
✅ MSS Perfect
✅ EQ Perfect  
✅ MOG Perfect
✅ OB Perfect
✅ MA Perfect
✅ FVG: Fixed (threshold 0.3)
✅ Liq Labels: Vertical text, no top/bottom extend, no bubble, fixed height
📝 Supporting files updated below
```

**Copy Ark_Indicator_copy.pine to main script when ready.**

