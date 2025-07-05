# 📦 Vinamilk ProBoost: FMCG Supply Chain Analytics Project (Simulation)

> 🇻🇳 **Dự án mô phỏng phân tích chuỗi cung ứng ngành sữa** – giả lập chiến dịch ra mắt sản phẩm mới **Vinamilk ProBoost** trong 6 tháng đầu tiên.  
> 🌐 End-to-end supply chain analytics simulation for a new dairy product launch by **Vinamilk**.

---

## 📑 Table of Contents

- [👤 Author](#-author)
- [🌟 Project Objective](#-project-objective)
- [📁 File Structure](#-file-structure)
- [📦 Star Schema Model](#-star-schema-model)
- [📊 Dashboards Overview (Power BI)](#-dashboards-overview-power-bi)
- [🧮 Core KPIs (DAX)](#-core-kpis-dax)
- [⚠️ Business Insights & Risks](#️-business-insights--risks)
- [🛠️ Tools Used](#-tools-used)
- [🎯 Strategic Recommendations](#-strategic-recommendations)
- [📬 Contact & License](#-contact--license)

---

## 👤 Author

**Phạm Minh Trung** – Intern Data Analyst  
📧 Email: [phamminhtrung1201@gmail.com](mailto:phamminhtrung1201@gmail.com)  
🔗 LinkedIn: [linkedin.com/in/pm-trung-data](https://www.linkedin.com/in/pm-trung-data/)

---

## 🌟 Project Objective

### 🔍 Why This Project?

Ra mắt sản phẩm mới trong ngành **FMCG** là một canh bạc: hàng tồn, thiếu hụt, phân phối không đều, và kênh bán không hiệu quả.  
Dự án này mô phỏng toàn bộ chuỗi phân tích dữ liệu – từ thu thập, xử lý, phân tích cho đến trình bày – để hỗ trợ **ra quyết định chính xác** cho sản phẩm **Vinamilk ProBoost**.

> A complete data analytics pipeline to support **data-driven strategy** in manufacturing, logistics, sales & marketing for the launch of **Vinamilk ProBoost**.

---

## 📁 File & Directory Overview

```bash
Vinamilk_ProBoost_SupplyChain/
├── data/
│   ├── vinamilk_proboost_6months_final.csv
│   ├── fact_sales_full.csv
│   ├── dim_customers.csv
│   ├── dim_provinces.csv
│   ├── dim_channels.csv
│   └── dim_skus.csv
│
├── analysis/
│   ├── data_cleaning_python.ipynb
│   ├── demand_forecast_model.ipynb
│   └── SQL_queries_analysis.sql
│
├── dashboards/
│   ├── vinamilk_powerbi_dashboard.pbix
│   ├── vinamilk_logo.png
│   └── screenshots/
│       ├── ![{07EEB116-582A-42EC-9F37-E7C9E474ED9C}](https://github.com/user-attachments/assets/5db45366-6162-4b38-96bf-911f61d9a2ec)
│       ├── ![{AC4B84CD-F4CC-4810-8A46-C01606A2287B}](https://github.com/user-attachments/assets/69c6a8fa-aadf-4b0c-b7af-26ee128e4bc4)
│       ├── ![{30FB325B-F01D-4145-A82D-88D1CC223D17}](https://github.com/user-attachments/assets/b0f87715-b318-4777-971b-fe0dc1e4e6a0)
│       ├── ![Uploading {3AC1BACA-7746-4AF3-BA90-D43A8FD9F1F8}.png…]()
│       ├── ![{534A4D1C-E887-4922-95DC-D802A05479B9}](https://github.com/user-attachments/assets/22955a74-c41c-40f2-9a86-9d2ced445d4d)
│       ├── ![{1C1668A9-0E47-4CF4-A525-ACD42585B484}](https://github.com/user-attachments/assets/1e7a9732-fc1b-49cc-b47a-c87e3580839a)
│       ├── ![{F31E5A22-6474-4F50-A521-CB7C94214187}](https://github.com/user-attachments/assets/4fee4dba-923a-40be-96b6-bf1e0df343a9)
│       └── ![{F0096A59-597C-4038-81B5-48E8B4721FAE}](https://github.com/user-attachments/assets/195b3bc2-6369-4f48-86cb-386d925d110f)

│
├── README.md
├── LICENSE
└── .gitignore
```

---

## 📦 Star Schema Model

```text
Fact Table:
- fact_sales_full

Dimension Tables:
- dim_customers
- dim_provinces
- dim_channels
- dim_skus
```

---

## 📊 Dashboards Overview (Power BI)

| # | Dashboard Title         | Key Insights & Visuals                                   |
|---|-------------------------|----------------------------------------------------------|
| 1 | Tổng Quan Doanh Thu     | KPIs, revenue trend, funnel chart                       |
| 2 | Hiệu Suất Theo Kênh     | GT/MT/Online comparison, Gauge chart, slicer            |
| 3 | Giao Hàng & Trả Hàng    | OTIF, Return funnel, tooltip by SKU                     |
| 4 | Tồn Kho & Turnover      | Inventory level, value, turnover ratio                  |
| 5 | Doanh Thu Theo Tỉnh     | Shape Map (64 provinces), Top 10 provinces              |
| 6 | SKU Bán Chạy            | Top SKUs, gross profit, AI visuals, funnel              |
| 7 | Phân Tích Trả Hàng      | Return rate, Key Influencers visual                     |
| 8 | Dự Báo Doanh Số         | Forecast next 3–6–12 months (Prophet/ARIMA)             |

---

## 🧮 Core KPIs (DAX)

```dax
Revenue = Quantity * Unit_Price
COGS = Quantity * Cost_Per_Unit
Gross Profit = Revenue - COGS
Return Rate = Returned Units / Quantity
OTIF = Orders Delivered On Time / Total Orders
Inventory Value = Stock_After * Cost_Per_Unit
Inventory Turnover = COGS / Average Inventory
```

---

## ⚠️ Business Insights & Risks

```markdown
🔁 Tỷ lệ trả hàng cao ở miền Bắc → logistics cần điều chỉnh  
📉 Kênh MT hoạt động dưới kỳ vọng  
🧊 Tồn kho lớn ở miền Trung → nguy cơ đóng băng vốn  
📦 3 SKU chiếm 60% doanh thu → rủi ro phụ thuộc  
🔮 Sai số dự báo nhu cầu → mất cân bằng sản xuất & phân phối
```

---

## 🛠️ Tools Used

```markdown
| Tool     | Purpose                           |
|----------|-----------------------------------|
| Python   | Data cleaning, EDA, forecasting   |
| SQL      | Aggregation, joins, data modeling |
| Excel    | Review, validation, cross-check   |
| Power BI | Visualization, KPI storytelling   |
```

---

## 🎯 Strategic Recommendations

```markdown
| Term        | Action                                             |
|-------------|----------------------------------------------------|
| Short-term  | Rebalance inventory in Central provinces           |
| Mid-term    | Boost Online channel (ads, promotion, UX)          |
| Long-term   | Expand SKU line based on forecast & sales trends   |
```

---

## 📬 Contact & License

```markdown
📧 Email: phamminhtrung1201@gmail.com  
🔗 LinkedIn: https://www.linkedin.com/in/pm-trung-data/  
📜 License: MIT
```

> 💬 “Let data guide your strategy – and storytelling amplify your insight.”  
> 💬 “Để dữ liệu dẫn đường – và Power BI kể chuyện.”
