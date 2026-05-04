# JsonPlaceholder-JMeter-Test
# JMeter 性能測試專案 - JSONPlaceholder API

一個使用 Apache JMeter 完成的 REST API 性能測試專案。

##  專案說明
- **測試目標**：模擬真實使用者行為，對公開 API 進行壓力測試與功能驗證
- **測試類型**：API 性能測試 + 功能驗證
- **工具**：Apache JMeter 5.6.3

##  測試場景
- 取得文章列表 (GET /posts)
- 查看單筆文章 (GET /posts/{id})
- 新增文章 (POST /posts)
- 修改文章 (PUT /posts/{id})
- 刪除文章 (DELETE /posts/{id})
- 使用 JSON Extractor 做資料關聯
- 加入 JSON Assertion 驗證回應

## 測試結果重點
- 支援 10 / 50 / 100 併發用戶測試
- 平均響應時間、90分位、錯誤率等指標
- 已產生完整 HTML Dashboard 報告

##  檔案說明
- `JsonPlaceholder_Test.jmx` → 主測試腳本
- `Report/` → HTML 性能測試報告
- `screenshots/` → 測試截圖

##  報告截圖

<img width="1884" height="918" alt="image" src="https://github.com/user-attachments/assets/7e0e1194-b708-48a9-835d-67a9261ee4d5" />
<img width="1556" height="466" alt="image" src="https://github.com/user-attachments/assets/64e18a22-88fe-4b17-bebf-be97b61304d7" />


## 🚀 如何執行
```bash
jmeter -n -t JsonPlaceholder_Test.jmx -l results.jtl -e -o Report
```

包含技術

Thread Group 與併發控制
HTTP Request + Header Manager
JSON Extractor 資料提取
JSON Assertion 結果驗證
非 GUI 模式執行與報告生成
參數化與關聯技術
