# batch_defect_data_converter_v1

批次將多份 Excel 檔案轉換為 PostgreSQL 可匯入的三張資料表格式：

- `wafer_inspections.csv`: 主表，每筆檢驗的基本資訊
- `defect_breakdown.csv`: 各類 defect 類別統計
- `defect_code_logs.csv`: 各 defect code 數量紀錄

## 📁 使用前準備
1. 將所有 Excel 檔案放進指定資料夾，例如：
   ```
   C:\Users\irene\OneDrive\桌面\AVI defect code data\Defect code data
   ```

2. 確保每份 Excel 格式一致，第一列為標題，第二列開始為資料。

## ▶ 使用方式（在 Jupyter Notebook 中）
執行整段程式即可完成：
- 自動處理所有 Excel
- 自動跳過不合格式的檔案
- 匯出三個 CSV 至 `output/` 子資料夾

## ⚠ 注意事項
- 若有 Excel 缺少必要欄位，程式會略過並列出檔名。
- 欄位名稱區分大小寫，會自動標準化。
