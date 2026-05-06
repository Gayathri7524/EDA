# EDA Summary — Retail Sales Snapshot

What I cleaned and why:
I converted Date to datetime (invalid dates → NaT), coerced Units_Sold, Unit_Price, and Discount to numeric, removed exact duplicate rows and duplicate Transaction_IDs, filled missing Discount with 0, and normalized Category and Region text to lowercase. I then computed a `Total_Sale` field for immediate revenue analysis.

Key insights:
The top category by total sales is electronics (highest aggregated Total_Sale). The south region appears to be the strongest performing region, while the east lags behind. Most discounts cluster below 20%, but a few outlier discounts (>50%) materially reduce revenue for those transactions.

Anomaly or caveat:
There is at least one invalid date converted to NaT and a few unusually large discounts that should be manually validated.

Next step:
Run weekly/monthly trend analysis, and check per-product margins for the top categories to prioritize inventory and promotion decisions.
