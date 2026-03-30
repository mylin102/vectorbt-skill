# vectorbt-pro Skill

## 簡介
`vectorbt-pro` 是一個為量化交易開發者設計的 Gemini CLI 技能。它提供了使用 `vectorbt` 庫進行高效策略開發、回測和分析的專家級建議。

`vectorbt` 以其極快的向量化運算能力著稱，特別適合處理大型數據集和大規模參數優化。

## 主要功能
- **引導式策略開發**：從零開始構建交易策略。
- **高性能回測**：利用 Numba 加速的底層引擎進行快速回測。
- **多資產/多參數分析**：利用廣播機制同時測試數千種組合。
- **詳盡的性能指標**：自動生成包含 Sharpe Ratio、Max Drawdown 等在內的統計報告。
- **數據視覺化**：整合 Plotly 提供互動式圖表。

## 如何觸發
你可以使用以下指令（或類似語句）來啟動此技能：
- "幫我用 vectorbt 回測一個 SMA 交叉策略"
- "如何使用 vectorbt 獲取加密貨幣數據？"
- "vectorbt 的 portfolio 統計數據包含哪些指標？"
- "backtest a simple moving average crossover with vectorbt"

## 安裝
此技能已集成在 vectorbt 倉庫中。你可以通過以下方式全局安裝：
```bash
# 在 vectorbt 倉庫根目錄執行
ln -sf $(pwd)/.claude/skills/vectorbt-pro ~/.claude/skills/vectorbt-pro
```

## 依賴
使用此技能建議安裝 vectorbt 的完整版本：
```bash
pip install "vectorbt[full]"
```
