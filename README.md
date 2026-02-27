# 香港 10 分鐘風向與風速

這是一個簡易的靜態網站，會從香港天文台的開放資料 API 抓取 **10 分鐘平均風向、平均風速以及最高陣風風速**（GeoJSON），並以表格與折線圖顯示。

## 功能
- 自動取得最新的風向/風速資料（CSV 形式的 GeoJSON）
- 下拉選單可依 **區域**（全部、港島、九龍、新界）篩選
- 顯示 **資料更新時間**
- 表格顯示 *區域、時間、平均風向、平均風速、最高陣風*
- 使用 Chart.js 以折線圖呈現 **平均風速走勢**

## 使用方式
1. 開啟網站後會自動向以下 API 發送 GET 請求：
   ```
   https://portal.csdi.gov.hk/geoportal/api/records/1.0/search?
   datasetId=hko_rcd_1634953844424_88011&lang=zh-hk&format=geojson&limit=500
   ```
2. 取得的 GeoJSON 會被解析成 JavaScript 陣列，然後根據使用者在下拉式選單的選擇過濾。
3. 表格與圖表會即時更新。

## 部署
- **GitHub**：<https://github.com/iampeterstark/weather-wind-10min>
- **Netlify**：<https://weather-wind-10min-5f4c9e8c1e6c9c0001c1f4b5.netlify.app/>

## 授權
本專案採用 **MIT License**，可自由修改與再發佈。

---
*資料來源：香港天文台 (10 分鐘風速) - https://data.weather.gov.hk/weatherAPI/hko_data/regional-weather/*
