# CoWoS 先進封裝 — 台灣供應鏈圖譜

台積電 Chip-on-Wafer-on-Substrate (CoWoS) 2.5D 先進封裝技術台灣供應鏈互動式網頁，涵蓋 39 家相關公司的財務數據與供應鏈分析。

**[→ 線上瀏覽](https://eli20261124.github.io/cowos-web/)**

## 功能

- 39 家公司按上游 / 中游 / 下游 / 相關四層供應鏈分類
- 各層依產業 (Sector) 再分組，每組 5–7 家
- 點擊公司卡片彈出詳細財務 Modal：
  - 公司概況（市值、企業價值、業務描述）
  - 年度財務（近3年 Revenue / 毛利率 / 淨利 / 現金流）
  - 季度財務（近4季）
  - 估值指標（P/E / Forward P/E / P/S / P/B / EV/EBITDA）

## 本地執行

```bash
# 重新產生 index.html（需在 My-TW-Coverage 目錄下）
python3 scripts/build_web_cowos.py

# 開啟預覽
open web/web.CoWos/index.html
```

## 目錄結構

```
web/
  web.CoWos/
    _template.html   # HTML 模板（含 {{PLACEHOLDERS}}）
    index.html       # 產生的靜態網頁（由 build script 產生）
```

## 致謝 / 資料來源

本專案的公司清單、供應鏈分類及財務數字，均來自以下開源研究專案：

**[My-TW-Coverage](https://github.com/Timeverse/My-TW-Coverage)** by [Timeverse](https://github.com/Timeverse)

> 涵蓋台灣上市公司的完整供應鏈研究資料庫，包含公司研究報告、財務數據、主題投資圖譜等。

## License

本網頁依原始資料來源的授權條款使用。
