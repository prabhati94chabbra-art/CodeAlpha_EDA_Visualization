# Black Friday EDA — Key Findings

## Dataset profile
- 550,068 transaction rows and 12 columns.
- 5,891 unique customers and 3,631 unique products.
- 0 exact duplicate rows.
- `Product_Category_2`: 173,638 missing values (31.57%).
- `Product_Category_3`: 383,247 missing values (69.67%).

## Purchase distribution
- Mean purchase: 9,263.97.
- Median purchase: 8,047.
- Minimum: 12; maximum: 23,961.
- Skewness: approximately 0.600 (positive/right skew).
- IQR screening flags 2,677 upper outliers (0.49%); no lower outliers. These values are retained pending business validation.

## Customer and segment patterns
- Gender transaction mix: M 414,259 (75.31%); F 135,809 (24.69%).
- Age 26–35 is the largest segment by transaction volume: 219,587 transactions (39.92%).
- City category B has the most transactions: 231,173 (42.03%) and the highest total recorded purchase amount: 2,115,533,605.
- City category C has the highest average purchase per transaction: 9,719.92.
- Male transactions have a higher transaction-weighted mean purchase than female transactions (9,437.53 vs 8,734.57). This is a descriptive, transaction-level comparison.
- For the formal Welch t-test, the unit is one row per customer: mean customer-level average transaction is 9,806.87 for male customers and 8,965.20 for female customers; the difference is statistically significant (t = 16.486, p < 0.001). This does not establish causality.

## Product category patterns
- Product Category 1 code 5 has the highest transaction count: 150,933.
- Product Category 1 code 1 has the highest total recorded purchase: 1,910,013,754.
- Product IDs are identifiers, not product descriptions; category codes are not labelled in the supplied CSV.

## Interpretation and limitations
- There is no date/time field, so daily/monthly/seasonal trends cannot be measured.
- There is no quantity, unit-price, cost, or profit field, so units sold, pricing, margin, and profit cannot be calculated.
- Purchase currency is not specified in the CSV.
- Occupation and product/category fields are codes; no codebook was supplied.
- Missing category values are not imputed because their business meaning is unknown.
- Statistical significance does not imply causation. Customer-level hypothesis testing is used to avoid treating repeated transactions from the same person as independent observations.
