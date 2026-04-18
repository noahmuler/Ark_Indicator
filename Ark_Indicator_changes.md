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

## v1.1.2 (FVG-MOG Overlap Fixed) - 2024
**New**: Added `fvgSkipMOG` toggle (default true). FVG detection now skips market open gaps (`day_change and not day_change[1]`) where MOG triggers, preventing overlap. FVG appears everywhere else.

### ✅ All Features:
```
✅ Killzones
✅ Order Blocks / Breaker Blocks  
✅ FVG (no MOG overlap, mitigation/extension ready)
✅ MSS/CHoCH
✅ EQH/EQL
✅ MOG (day_change gaps)
✅ Liquidity Timing
✅ MAs (21/50/200)
✅ Dashboard (RSI/Session/Liq)

**FULLY PRODUCTION READY ✅**

New input: fvgSkipMOG=true prevents FVG from duplicating MOG gaps.
Reload chart to test.**




