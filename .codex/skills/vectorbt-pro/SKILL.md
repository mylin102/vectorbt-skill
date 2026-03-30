# vectorbt-pro

## Purpose
幫助使用者利用 vectorbt 進行高效的量化交易回測、數據分析與策略優化。提供從數據獲取、指標計算、信號產生到組合回測的完整引導。

## Trigger Phrases
- "backtest trading strategy"
- "vectorbt tutorial"
- "analyze financial data"
- "generate trading signals"
- "optimize portfolio"
- "策略回測"
- "vectorbt 使用教學"
- "量化交易分析"
- "產生交易信號"
- "投資組合優化"

## Instructions

### 核心原則
1. **向量化思維**：始終優先使用 vectorbt 的向量化操作，避免在大型數據集上使用 Python 迴圈。
2. **Numba 加速**：利用 vectorbt 底層的 Numba 加速功能處理複雜計算。
3. **廣播機制 (Broadcasting)**：利用 vectorbt 的自動廣播功能，同時測試多種參數或多個資產。
4. **互動式視覺化**：建議使用 Plotly 進行數據探索。

### 常用工作流

#### 1. 數據獲取與預處理
使用 `vbt.YFData.download` 或 `vbt.CCXTData.download` 獲取數據。
```python
import vectorbt as vbt
data = vbt.YFData.download("BTC-USD")
price = data.get("Close")
```

#### 2. 指標計算
使用內建指標或自定義指標工廠。
```python
fast_ma = vbt.MA.run(price, 10)
slow_ma = vbt.MA.run(price, 50)
```

#### 3. 信號產生
利用交叉函數產生進出場信號。
```python
entries = fast_ma.ma_crossed_above(slow_ma)
exits = fast_ma.ma_crossed_below(slow_ma)
```

#### 4. 組合回測
使用 `vbt.Portfolio.from_signals` 執行回測。
```python
pf = vbt.Portfolio.from_signals(price, entries, exits, init_cash=100)
print(pf.stats())
```

#### 5. 參數優化
利用 `run_combs` 測試參數組合。
```python
windows = np.arange(2, 101)
fast_ma, slow_ma = vbt.MA.run_combs(price, window=windows, r=2)
```

### 注意事項
- 確保安裝了必要的依賴：`pip install "vectorbt[full]"`。
- 大規模回測時注意內存使用。
- 始終檢查回測結果中的 `stats()` 以評估風險（如最大回撤、夏普比率）。

## References
- 官方文檔: https://vectorbt.dev/
- GitHub: https://github.com/polakowo/vectorbt
