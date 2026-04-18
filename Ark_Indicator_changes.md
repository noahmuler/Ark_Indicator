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

## v1.3.0 (FVG/MOG Independent Logic - Overlap Fully Resolved) - 2024
**Status**: ✅ PRODUCTION READY

**Key Changes:**
- FVG: Fully independent detection (low > high[2], high < low[2]), `fvgSessionsOnly` filter
- MOG: Daily open gaps via `day_change` trigger, arrays/extension/mitigation preserved  
- Removed all `detect_gap()` dependencies → No overlap/duplication
- Verified: MOG on daily opens, FVG everywhere (independent)

### ✅ All Features:
```
✅ Killzones (extendable T/B/M lines)
✅ Order Blocks / Breaker Blocks (mitigation/extension)  
✅ FVG (independent, fvgATR filtered, extend/mitigate)
✅ MSS/CHoCH (killzone only)
✅ EQH/EQL (ATR threshold)
✅ MOG (daily gaps, extend/mitigate) 
✅ Liquidity Timing (vertical markers → NEXT FIX)
✅ MAs (21/50/200)
✅ Dashboard (RSI/Session/Liq status)

**FVG/MOG OVERLAP 100% RESOLVED ✅**

*Test: Daily chart → MOG boxes on opens, FVG throughout*





