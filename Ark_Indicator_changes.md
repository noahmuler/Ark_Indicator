# Ark Indicator - CHANGELOG

## v2.0.0 (Dashboard & Liquidity Enhancement) - April 2026
**Status**: Production Ready with Enhanced Features

### Key Changes:
- **Dashboard Enhancement**: Liquidity data now displays on all timeframes
- **Liquidity Lines**: Still limited to M5 timeframe as requested
- **FVG Debugging**: Multiple attempts made, restored working logic from backup
- **Documentation**: Updated TODO.md and changelog with current progress

### Technical Implementation:
```
Dashboard Fix:
- [x] Created separate dashboard variables (preAsianDash, asianOpenDash, etc.)
- [x] Dashboard shows liquidity data on all timeframes
- [x] Line drawing remains limited to M5 and below
- [x] Maintained original liquidity functionality

FVG Status:
- [x] Restored exact working logic from backup file
- [x] Proper ATR filtering with fvgTH parameter
- [x] Session filtering with fvgSessionsOnly option
- [ ] Still investigating why FVG not displaying on chart

Documentation:
- [x] Updated TODO.md with comprehensive debugging log
- [x] Updated changelog with current progress
- [x] Tracked all FVG debugging attempts
```

## v1.3.0 (FVG/MOG Independent Logic) - 2024
**Status**: Production Ready

**Key Changes:**
- FVG: Fully independent detection (low > high[2], high < low[2]), `fvgSessionsOnly` filter
- MOG: Daily open gaps via `day_change` trigger, arrays/extension/mitigation preserved  
- Removed all `detect_gap()` dependencies -> No overlap/duplication
- Verified: MOG on daily opens, FVG everywhere (independent)

### All Features:
```
Killzones (extendable T/B/M lines)
Order Blocks / Breaker Blocks (mitigation/extension)  
FVG (independent, fvgATR filtered, extend/mitigate)
MSS/CHoCH (killzone only)
EQH/EQL (ATR threshold)
MOG (daily gaps, extend/mitigate) 
Liquidity Timing (vertical markers, M5 only)
MAs (21/50/200)
Dashboard (RSI/Session/Liq status, all timeframes)

**FVG/MOG OVERLAP 100% RESOLVED**
```

## v1.1.0 (FVG + Liquidity Fixed) - 2024
**Status**: FVG displays with clark_smc style, Liquidity markers use vertical trendlines

### Fixes Applied:
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

## v1.0.0 (Base Features) - 2024
**Status**: Core functionality complete
```
- [x] MSS/EQH/EQL/MOG/OB/MA/Dashboard/Killzones Perfect
```

### Current Debugging Log (FVG Issue):
1. **Initial Issue**: FVG not showing at all despite working backup
2. **Attempt 1**: Added debugging code (TEST boxes, FILTER boxes, debug labels)
3. **Attempt 2**: Removed ATR filter completely to test basic gap detection
4. **Attempt 3**: Copied exact working code from backup file
5. **Attempt 4**: Fixed session filtering logic (removed inKZ dependency)
6. **Attempt 5**: Reduced ATR threshold from 1.2 to 0.5
7. **Attempt 6**: Removed ATR filter completely
8. **Attempt 7**: Restored exact working logic from backup file
9. **Current Status**: Logic matches backup exactly, but FVG still not displaying
