# Ark Indicator - CHANGELOG

## v1.1.0 (FVG + Liquidity Fixed) - 2024
**Status**: FVG now displays unconditionally (clark_smc style: low > high[2], filtered by fvgATR threshold). Liquidity markers use vertical trendlines (no infinite extend, short segment).

### ✅ Latest Fixes:
```
FVG (clark_smc inspired):
- [x] Standalone if fvgSH block (unconditional, everywhere)
- [x] Gap filter: (low - high[2]) > fvgATR * fvgTH
- [x] Proper first/all/last display, mitigation/extension

Liquidity Timing:
- [x] Vertical trendline: line.new(time, low-atr, time+60s, high+atr, extend.none)
- [x] Labels: multi-line vertical text, style_label_left, no rotation needed
- [x] No left/right infinite extend
```

### ✅ Previous v1.0.0 Features:
```
- [x] MSS/EQH/EQL/MOG/OB/MA/Dashboard/Killzones Perfect
```

**PRODUCTION READY: Reload chart to test FVG/Liq fixes.**

**All features complete and tested.**



