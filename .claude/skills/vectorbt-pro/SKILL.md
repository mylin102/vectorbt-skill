---
name: vectorbt-pro
description: 專家級量化交易分析與策略回測工具，基於 vectorbt 庫。提供向量化運算與性能優化建議。
---

# vectorbt-pro

## Purpose
幫助使用者利用 vectorbt 進行高效的量化交易回測、數據分析與策略優化。提供從數據獲取、指標計算、信號產生到組合回測的完整引導。

## Trigger Phrases
- "backtest trading strategy"
- "vectorbt tutorial"
- "analyze financial data"
- "策略回測"
- "vectorbt 使用教學"

## Instructions
### 核心原則
1. **向量化思維**：始終優先使用 vectorbt 的向量化操作。
2. **Numba 加速**：利用底層 Numba 加速處理複雜計算。
3. **廣播機制**：利用自動廣播功能測試多種參數。

### 常用工作流
1. **數據獲取**：vbt.YFData.download
2. **指標計算**：vbt.MA.run
3. **組合回測**：vbt.Portfolio.from_signals

## References
- 官方文檔: https://vectorbt.dev/
