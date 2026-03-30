# vectorbt-pro Gemini CLI Skill

這是一個專為 **Gemini CLI (Claude Code / Codex)** 設計的 AI 技能倉庫。
它將 `vectorbt` 的量化交易專業知識封裝成 AI 指令，讓您能透過自然語言進行高效的策略回測與分析。

## 如何安裝此技能？

請確保您已安裝 Gemini CLI，然後執行以下指令：

```bash
# 建立目錄
mkdir -p ~/.claude/skills

# 下載並連結技能 (請將路徑替換為您本地克隆此倉庫的位置)
ln -sf $(pwd)/.claude/skills/vectorbt-pro ~/.claude/skills/vectorbt-pro
```

## 觸發詞 (Trigger Phrases)
- "幫我用 vectorbt 回測策略"
- "如何使用 vectorbt 獲取數據？"
- "vectorbt tutorial"
- "backtest trading strategy"

---
本倉庫基於 [vectorbt](https://github.com/polakowo/vectorbt) 核心功能構建。
