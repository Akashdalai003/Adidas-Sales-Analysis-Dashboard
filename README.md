# Adidas-Sales-Analysis-Dashboard


ADIDAS US SALES ANALYTICS
Interactive Power BI Dashboard | Project Documentation
Fiscal Period: January 2020 – December 2021  |  Dataset: 9,648 Transactions  |  Coverage: 50 States


1. Executive Summary
This Power BI project delivers a comprehensive, end-to-end sales intelligence dashboard for Adidas US operations spanning two full fiscal years (2020–2021). Drawing from a structured transactional dataset of 9,648 records across 50 states and 52 cities, the dashboard transforms raw sales data into actionable business intelligence. It provides leadership and commercial teams with a single-pane view of revenue performance, product mix, retailer contribution, regional dynamics, and sales channel efficiency.
The analysis covers all six major Adidas product lines, six national retail partners, three sales channels, and five geographic regions—enabling multi-dimensional performance benchmarking and strategic decision-support.

2. Key Performance Indicators (KPIs)
The dashboard surfaces the following headline KPIs as prominent card visuals at the top of each report page, enabling instant performance assessment at a glance:

$899.9M
Total Revenue	$332.1M
Operating Profit	2.48M
Units Sold	42.3%
Avg. Operating Margin

Beyond the headline figures, the dashboard tracks the following granular KPI dimensions:

Revenue by Retailer	West Gear ($243M) leads, followed by Foot Locker ($220M), Sports Direct ($182M), Kohl’s ($102M), Amazon ($78M), Walmart ($75M)
Revenue by Product	Men’s Street Footwear tops at $209M; Women’s Apparel second at $179M; Men’s Athletic Footwear third at $154M
Revenue by Region	West region leads at $270M, followed by Northeast ($186M), Southeast ($163M), South ($145M), Midwest ($136M)
Revenue by Channel	In-store: $357M (39.7%) | Outlet: $296M (32.9%) | Online: $248M (27.6%)
Operating Margin Range	25% (Women’s Apparel) to 50% (Men’s Street Footwear / Women’s Apparel via Outlet)
Price per Unit Range	$25 (entry-level Sports Direct) to $70+ (premium Walmart apparel lines)

3. Dataset Architecture & Preparation
The underlying dataset, “Adidas Sales Database,” is structured as a single flat table (Sheet: Data Sales Adidas) containing 9,648 transaction-level records with 13 dimensions. The following data preparation and modelling work was completed prior to visualization:

3.1 Source Columns
Retailer	6 retail partners: Foot Locker, Walmart, Sports Direct, West Gear, Kohl’s, Amazon
Retailer ID	Unique numeric identifier per retailer entity
Invoice Date	Daily granularity from 01-Jan-2020 to 31-Dec-2021; parsed to enable time intelligence
Region	Five US regions: West, Northeast, Southeast, South, Midwest
State	All 50 US states covered for geographic drill-down
City	52 distinct cities enabling city-level filtering
Product	6 lines: Men’s Street Footwear, Men’s Athletic Footwear, Women’s Street Footwear, Women’s Athletic Footwear, Men’s Apparel, Women’s Apparel
Price per Unit	Numeric field used for average selling price analysis and margin benchmarking
Units Sold	Volume metric used in trend and contribution analyses
Total Sales	Primary revenue measure; product of price × units; used in all revenue visuals
Operating Profit	Absolute profitability measure for margin analysis
Operating Margin	Percentage measure; used in profitability heatmaps and comparison charts
Sales Method	Three channels: In-store, Outlet, Online

3.2 Data Preparation Steps
•	Validated and cleaned date fields (Invoice Date) to enable Power BI time intelligence functions (YTD, MoM, QoQ)
•	Structured Operating Margin as a decimal field formatted as percentage for accurate DAX measure computation
•	Applied consistent data types across all columns to ensure filter and slicer compatibility
•	Confirmed referential integrity across Retailer, Region, Product, and Sales Method dimensions
•	Loaded data into Power BI Desktop and verified row count (9,648 records) against source file

4. Dashboard Visuals & Design
The dashboard is organized across multiple report pages with a consistent branded layout. Each visual was selected to optimally communicate the underlying data pattern, with interactivity enabled through cross-filtering, slicers, and drill-through capabilities.

4.1 KPI Cards
KPI CARDS	KPI Card Tiles — Total Revenue, Operating Profit, Units Sold, Operating Margin
Prominent summary cards positioned at the top of each page. Display total values with conditional formatting indicators (color-coded thresholds) to signal performance against targets. Provides instant executive-level context before any detailed exploration.

4.2 Time-Series Analysis
LINE CHART	Monthly Revenue & Profit Trend — Line / Area Chart
Plots Total Sales and Operating Profit across 24 months (Jan 2020–Dec 2021). Enables identification of seasonal peaks, growth trajectories, and year-over-year performance comparison. Configured with a date hierarchy allowing drill-down from Year → Quarter → Month.

4.3 Retailer Performance
BAR CHART	Sales & Profit by Retailer — Clustered Bar Chart
Side-by-side bar comparison of Total Sales and Operating Profit for all six retail partners. Sorted descending by revenue to immediately surface top contributors. Reveals that West Gear and Foot Locker together account for over 51% of total revenue, highlighting key account dependency.

DONUT CHART	Retailer Revenue Share — Donut / Pie Chart
Proportional view of each retailer’s contribution to total revenue. Provides a quick structural view of the retail partner mix and enables management to assess portfolio concentration risk.

4.4 Product Analysis
COLUMN CHART	Revenue by Product Category — Stacked Bar / Column Chart
Compares revenue contribution across all six Adidas product lines. Men’s Street Footwear emerges as the highest-revenue category, while Women’s Apparel ranks second. Stacking by region or retailer is available via visual-level filters.

BAR CHART	Operating Margin by Product — Horizontal Bar Chart
Ranks product lines by profitability margin, highlighting the gap between high-margin footwear (up to 50%) and lower-margin apparel lines (25%). Actionable for pricing and portfolio strategy reviews.

4.5 Regional & Geographic Analysis
MAP VISUAL	Sales by US Region — Filled Map / Choropleth
A geographic map of the United States with state-level or region-level shading based on Total Sales magnitude. Allows immediate identification of high-performing geographies (West and Northeast) versus underperforming markets. Supports drill-through to state and city-level detail.

TREEMAP	Revenue by Region — Treemap / Stacked Column
Visualizes the proportional revenue contribution of each of the five US regions. The West region’s $270M output is prominently sized, while the Midwest ($136M) is identified as a growth opportunity area.

4.6 Sales Channel Decomposition
DONUT CHART	Revenue by Sales Method — Pie / Donut Chart
Breaks total revenue into three channel buckets: In-store (39.7%), Outlet (32.9%), and Online (27.6%). Reveals that physical retail still dominates but online channels are a material and growing contributor—relevant for channel investment strategy.

MATRIX	Channel vs. Profitability Matrix — Scatter / Matrix Visual
Cross-tabulates Sales Method against product or region to reveal channel-specific profitability patterns. Enables identification of which products or regions over-index on online vs. in-store, supporting targeted channel strategy.

4.7 Slicers & Interactivity
SLICER PANEL	Dynamic Slicers — Region, Retailer, Product, Sales Method, Date Range
A persistent slicer panel allows users to filter the entire report by any combination of Region, Retailer, Product Category, Sales Method, and Invoice Date range. All visuals cross-filter dynamically, enabling self-service exploration without requiring separate report views.

5. Key Analytical Insights Surfaced
The dashboard enables the following strategic insights to be derived directly from interactive exploration:

•	West Gear and Foot Locker collectively drive 51.4% of total US revenue, indicating high retailer concentration that warrants strategic account management attention.
•	Men’s Street Footwear delivers the highest absolute revenue ($208.8M) and the highest operating margin (50%), making it the most commercially valuable product category.
•	The West region outperforms all others at $269.9M — nearly double the output of the Midwest ($135.8M), pointing to geographic revenue imbalance.
•	Online sales ($247.7M) represent 27.6% of total revenue, confirming the growing significance of e-commerce and the need for digital channel investment.
•	Women’s Apparel carries the lowest operating margin (25%) despite being the second-largest revenue category, signalling a potential pricing or cost structure issue.
•	Outlet channel performance ($295.6M, 32.9% of total) indicates strong consumer demand for value-priced product, particularly relevant for clearance and stock rotation strategy.

6. Tools & Technologies Used

Data Source	Microsoft Excel (.xlsx) — Adidas US Sales Dataset, 9,648 rows, 13 columns
BI Platform	Microsoft Power BI Desktop (.pbix)
Data Modelling	Power Query (M Language) for data type enforcement, date parsing, and column validation
Measures & Calculations	DAX (Data Analysis Expressions) for KPI cards, YTD measures, operating margin computation, and dynamic titles
Visualisation Types	KPI Cards, Line/Area Charts, Clustered Bar Charts, Donut Charts, Treemaps, Filled Maps, Matrix, Slicers
Interactivity	Cross-filtering, drill-down hierarchies, slicer panels, bookmark navigation, and conditional formatting
Design Theme	Custom Adidas-aligned color palette (navy blue, black, white) with consistent typography and layout grid



This document provides a full account of the analytical scope, KPIs, visual design decisions, and data architecture underlying the Adidas US Sales Power BI Dashboard. The project demonstrates end-to-end business intelligence capability—from raw transactional data through to interactive, insight-ready reporting.

