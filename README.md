# infineon-financial-performance-2021-2025
## Project Background

Infineon Technologies AG is a semiconductor company, focused on power systems and IoT. Infineon was established as an independent company in 1999. Semiconductors are essential components in cars, industrial equipment, energy infrastructure, data centers and consumer electronics. Demand is growing, driven by electric vehicles, renewable energy and artificial intelligence. For this analysis, I focus on the 2021-2025 period. Infineon manufactures semiconductor components and system solutions. At the end of 2025, Infineon generated €14.66bn in revenue, a 10.5% EBIT margin and €1.02bn net income. I focused on 4 categories to understand the company’s performance.

Insights and recommendations are provided on the following key areas:

- **Category 1:** Overall Financial Performance
- **Category 2:** Segment & Geographic Performance
- **Category 3:** Profitability & Cost Structure
- **Category 4:** Cash Flow & Financial Position

The data came from Infineon Financial Data 2021-2025 which can be found here `2025-infineon-financial-data-2021-2025-v01-00-en.pdf`

An interactive Power BI dashboard used to report and explore the financial performance of the company can be found here [Download the Power BI file (.pbix)](Infineon_dashboard.pbix).

## Tools

- **Excel:** transcription of the financial data from Infineon’s report
- **Power Query:** data cleaning and transformation (unpivoting, renaming, data types)
- **Power BI Desktop:** data model (star schema) and interactive dashboard
- **DAX:** measures, ratios and dynamic formatting
- **Claude (AI assistant), via Microsoft’s Power BI Modeling MCP:** help with refining DAX measures and formatting

## Data Structure & Initial Checks

The figures were transcribed from the PDF into an Excel workbook and then transformed in Power Query: the year columns were unpivoted, "–" values replaced by 0, and footnote markers removed from labels (e.g. `Automotive1` → `Automotive`).

The resulting Power BI model follows a star schema of 11 tables.

### Key DAX logic

- About 25 measures (Revenue, EBIT, Free Cash Flow…) display amounts in € billions.
- **Ratios are recalculated, never summed.** When several years are selected, the EBIT margin is computed as total EBIT / total revenue instead of the sum of annual margins (which wrongly gave 83%). RoCE uses a simple average because capital employed is not included in the Financial Data 2021–2025 dataset used for the dashboard.

## Executive Summary

- **Profit fell much faster than revenue.** Revenue grew 47% between 2021 and 2023, then fell only 10% by 2025. Over the same two years, EBIT fell 62% (from €4.02bn to €1.54bn) and the EBIT margin went from 24.6% to 10.5%.
- **Infineon depends more and more on Automotive and China.** Automotive now generates half of group revenue (50.5% in 2025, vs 43.8% in 2021) and stays the most profitable segment. Greater China accounts for 38% of revenue and was the only region to grow in 2025 (+8.8%). Industrial (Green Industrial Power) and Connected Secure Systems saw their margins collapse.
- **2025 was an investment year financed by debt.** Free cash flow turned negative (−€1.05bn). Financial debt rose 42% to €6.83bn and RoCE fell to 4.9%. The balance sheet remains solid, with a 56% equity ratio.

## Insights Deep Dive

### Category 1: Overall Financial Performance

- **Revenue peaked in 2023 before declining.** Revenue increased from €11.06bn in 2021 to €16.31bn in 2023 (+47%), the highest point of the period. It then declined to €14.96bn in 2024 and €14.66bn in 2025 (−10% from the peak). The 2025 decline (−2%) was much smaller than in 2024 (−8%), which suggests the downturn was flattening.
- **Net income dropped by two-thirds.** Profit for the period fell from €3.14bn in 2023 to €1.02bn in 2025 (−68%).
- **Automotive is the largest segment every year**, and its share of group revenue grew from 44% in 2021 to 50% in 2025.
- **Free cash flow became negative in 2025** (−€1.05bn) for the first time in the period, after €1.57bn in 2021 and a barely positive €23m in 2024 (see Category 4).

### Category 2: Segment & Geographic Performance

- **Segment ranking:** Automotive is number one every year, followed by Power & Sensor Systems. Green Industrial Power ranks third in every year except 2022, when Connected Secure Systems briefly overtook it (€1.82bn vs €1.79bn).
- **Segment profitability diverges sharply.** Between 2023 and 2025:
  - Automotive's segment result margin fell from 28.9% to 20.7%, but it remains the most profitable segment. In 2025, its Segment Result fell 24% (from €2.02bn to €1.53bn), mainly because of higher underutilization costs and price adjustments.
  - Green Industrial Power fell from 30.0% to 12.3%, with revenue down 16% in 2025.
  - Connected Secure Systems fell from 23.9% to 10.9%.
- **Geography:** Greater China is the largest region every year, with €5.58bn in 2025 (38% of revenue), €4.21bn of which comes from Mainland China and Hong Kong. Europe, Middle East and Africa is second with €3.49bn (24%), of which Germany is €1.44bn (10%). In 2025, Greater China was the only region to grow (+8.8%). EMEA (−10%), Japan (−13%) and the Americas (−8%) all declined.

### Category 3: Profitability & Cost Structure

- From 2021 to 2023, revenue rose 47% and operating profit rose 169% (from €1.47bn to €3.95bn). From 2023 to 2025, revenue fell 10% and operating profit fell 62% (to €1.52bn).
- The gross margin fell 6.3 points, from 45.5% in 2023 to 39.2% in 2025. The EBIT margin fell much more, by 14.1 points from 24.6% to 10.5%, because operating expenses kept rising while gross profit shrank. In 2025, operating expenses (R&D and SG&A) reached €3.81bn, slightly above 2024 (€3.72bn), and rose to 26.0% of revenue (vs 24.8%).
- R&D rose every year, from €1.45bn in 2021 to €2.23bn in 2025 (+54%), reaching 15.2% of revenue in 2025 (vs 12.2% in 2023). In 2025, gross R&D spending was almost stable (+1%, to €2.66bn), but Infineon received fewer public grants (€179m vs €215m, −17%), which explains about half of the €66m increase in reported R&D expenses. R&D headcount also grew 6% to 13,998 employees, partly because of the acquisition of Marvell’s Automotive Ethernet business. Investments include new manufacturing technologies, such as in-house 300-millimeter production of gallium nitride (GaN) semiconductors.
- SG&A remained stable at around €1.55–1.60bn per year since 2022 (10.8% of revenue in 2025). Other operating income and expense swung from a €119m gain in 2023 to a €429m charge in 2025.

### Category 4: Cash Flow & Financial Position

- Debt was high in 2021 (€6.59bn), was paid down to €4.73bn in 2023, and then rose to €6.83bn in 2025 (+42% vs 2024). The net cash position worsened from −€1.14bn in 2023 to −€4.73bn in 2025.
- **Free Cash Flow dropped because Investing outflows doubled.** Cash outflows from investing activities rose by €2.41bn to €4.57bn in 2025, mainly because of the €2.18bn purchase price paid for Marvell’s Automotive Ethernet business.
- **Large investment financed by debt.** 2025 is the only year with a positive financing cash flow (+€920m).
- RoCE peaked at 16.6% in 2023 and fell to 4.9% in 2025, the lowest of the period. In 2025, the return side fell (profit from continuing operations before interest down €688m, to €1.17bn), mainly because of sales price reductions and higher underutilization costs. At the same time, capital employed rose by €1.81bn to €23.60bn, mainly because of the Marvell acquisition. The equity ratio was highest in 2023–2024 (≈ 60%) and remains solid at 56.0% in 2025.

## Recommendations

Based on the insights and findings above, I would recommend the Finance & Strategy team to consider the following:

1. **Reduce concentration risk:** keep investing in Automotive, where electrification and driver assistance increase the semiconductor content per vehicle, while reducing dependence on Greater China (38% of revenue) by supporting growth in other regions.
2. **Measure the return on R&D:** monitor the revenue from new growth areas (AI data centers, silicon carbide and gallium nitride) to make sure R&D spending turns into future sales and profits.

## Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

- **Fiscal year vs. calendar year:** Infineon's fiscal year runs from October to September (e.g., FY2025 covers Oct 2024–Sep 2025), not the calendar year. All "Year" labels in this dashboard refer to Infineon's fiscal year rather than the calendar year.
- **Currency and display units:** all source figures are reported in € millions and displayed in € billions in this analysis. No currency conversion was applied.
- **Ratios over several years:** when no single year is selected, ratios are calculated as weighted ratios (e.g. total EBIT / total revenue), not as the sum of the annual percentages. RoCE is the simple average of the annual values, because capital employed is not included in the Financial Data 2021–2025 dataset used for the dashboard.
- **Corporate and Eliminations segment:** this line shows near-zero or negative values. It was kept in segment-level totals to match Infineon's official reporting, but excluded from any "top segment" ranking or share-of-revenue comparisons to avoid distorting the picture.

## Sources

- Infineon Technologies AG, *Financial Data 2021–2025*
- Infineon Technologies AG, *Annual Report 2025*

---

*Disclaimer: This is an independent portfolio project based on publicly available data. It is not affiliated with or endorsed by Infineon Technologies AG and does not constitute investment advice.*
