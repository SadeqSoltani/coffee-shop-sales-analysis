
# Coffee Shop Sales Analysis

> A business intelligence project analyzing 19,000+ transactions across 9 global cities to uncover revenue drivers, validate behavioral hypotheses, and deliver actionable strategies for operations, pricing, product, and customer retention.
---

## Table of Contents

- [Project Overview](#project-overview)
- [Key Metrics](#key-metrics)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Statistical Validation](#statistical-validation)
- [Key Findings](#key-findings)
- [Power BI Dashboard](#power-bi-dashboard)
- [Strategic Recommendations](#strategic-recommendations)
- [Getting Started](#getting-started)
- [Author](#author)

---

## Project Overview

This project performs a full business intelligence analysis of a multi-city coffee shop chain operating across 9 cities in Australia, the UK, Canada, and the United States. The analysis covers 19,000+ transactions spanning a full calendar year, examining how time, location, product category, customer demographics, weather conditions, and holiday events interact to drive revenue.

The project moves through four analytical layers:

- **Data Cleaning and Engineering** : timestamp parsing, feature extraction, and quality validation
- **Exploratory Data Analysis** : correlation mapping, distribution profiling, and outlier detection
- **Statistical Validation** : hypothesis testing using ANOVA and t-tests to confirm which patterns are statistically significant versus visually coincidental
- **Business Intelligence** : six themed deep-dive analyses translated into a 6-page interactive Power BI dashboard

Every finding in this project is backed by statistical evidence before being elevated to a business recommendation.

---

## Key Metrics

| Metric | Value |
|--------|-------|
| Total Transactions | 19,000+ |
| Total Revenue | $129,541 |
| Average Order Value | $6.85 |
| Cities Analyzed | 9 |
| Product Categories | 6 |
| Store Formats | 3 (Airport, Mall Kiosk, Standalone) |
| Countries | 4 (AUS, UK, CAN, USA) |
| Holidays Analyzed | 7 |
| Weather Conditions | 4 (Rainy, Sunny, Cloudy, Snowy) |

---

## Project Structure

```
coffee-shop-sales-analysis/
│
├── screenshots/
│   ├── 01_time_revenue.png
│   ├── 02_location_market.png
│   ├── 03_product_menu.png
│   ├── 04_customer_demographics.png
│   ├── 05_weather_impact.png
│   └── 06_holiday_events.png
│
├── data/
│   └── coffee_shop_sales.csv
│
├── notebooks/
│   └── coffee_shop_analysis.ipynb
│
├── dashboard/
│   └── coffee_shop_dashboard.pbix
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.9+ |
| Data Processing | Pandas, NumPy |
| Statistical Testing | SciPy |
| Visualization | Matplotlib, Seaborn |
| Business Intelligence | Power BI Desktop |
| Development | Jupyter Notebook, VS Code |

---

## Dataset

The dataset contains 19,000+ coffee shop transactions with 20 columns covering every dimension of the business:

| Column | Description |
|--------|-------------|
| transaction_id | Unique transaction identifier |
| timestamp | Full datetime of transaction |
| store_id | Store identifier |
| city | City of the store |
| country | Country of the store |
| store_type | Airport, Mall Kiosk, or Standalone |
| product_category | Coffee, Tea, Sandwich, Merchandise, Pastry, Smoothie |
| product_name | Specific product name |
| unit_price | Price per unit |
| quantity | Number of items purchased |
| discount_applied | Whether a discount was applied |
| payment_method | Credit Card, Debit Card, Mobile Wallet |
| customer_id | Customer identifier |
| customer_age_group | Age bracket of customer |
| customer_gender | Gender of customer |
| loyalty_member | Whether customer is a loyalty member |
| weather_condition | Weather at time of transaction |
| temperature_c | Temperature in Celsius |
| holiday_name | Name of holiday if applicable |
| total_amount | Transaction revenue |

**Engineered features:** hour, day of week, month, date, is_weekend

---

## Statistical Validation

All major business findings were tested for statistical significance before being included in recommendations. Visual patterns that look meaningful in charts are not always real. The tests below confirm which ones are.

| Hypothesis | Test | Statistic | p-value | Result |
|-----------|------|-----------|---------|--------|
| Weather affects revenue | One-way ANOVA | F = 4.07 | 0.0067 | Confirmed significant |
| Holidays increase order value | Independent t-test | t = 2.58 | 0.0099 | Confirmed significant |
| Discounts reduce order value | Independent t-test | t = -3.39 | 0.0007 | Confirmed significant |
| Store type affects revenue | One-way ANOVA | F = 69.29 | 0.0000 | Strongly confirmed |
| City location affects revenue | One-way ANOVA | F = 24.81 | 0.0000 | Strongly confirmed |
| Weekend revenue exceeds weekday | Independent t-test | t = 1.10 | 0.2732 | Not significant |

The weekend result is the most important finding from statistical testing. Despite the dashboard showing Saturday ($25.4K) and Sunday ($22.4K) as the highest-revenue days visually, the statistical test confirms that weekend revenue per transaction is not significantly different from weekday revenue. The visual gap is driven by higher transaction volume on weekends, not higher spending per visit. This means weekend strategies should focus on throughput and capacity rather than order value incentives.

---

## Key Findings

Findings are organized by analytical theme and combine dashboard observations with statistical validation results.

---

### Time-Driven Revenue Patterns

**Hour-level:** Revenue follows a sharp morning concentration, climbing steeply from hour 5 onward and peaking at hour 9 with $17.2K, consistent with commuter-driven demand during the morning rush. After a sharp midday dip to $7.6K at hour 11, revenue partially recovers to a secondary peak of $8.3K at hour 15, suggesting a distinct afternoon demand window driven by post-lunch and work-break visits. From hour 16 onward, revenue declines steadily, reaching its lowest levels after hour 20 ($1.0K). This two-peak daily pattern indicates the business has two meaningful demand windows rather than one, and the 14-16 PM window represents an underutilized opportunity for targeted afternoon promotions.

**Day-level:** Weekly revenue shows a relatively flat pattern from Monday ($13.7K) through Wednesday ($15.0K), then accelerates sharply from Thursday ($15.9K) through Saturday ($25.4K). The full weekend (Saturday + Sunday: $47.8K combined) is responsible for approximately 37% of weekly revenue. Importantly, the statistical t-test (p = 0.2732) confirms this is a volume effect rather than a per-transaction spending effect. Weekend customers visit more frequently but do not spend more per order.

**Month-level:** Monthly revenue oscillates between $10.18K (March) and $11.71K (January), revealing two distinct seasonal peaks: a winter peak in January ($11.71K) and December ($11.61K) driven by holiday traffic and hot beverage demand, and a summer peak in July and August (both approximately $11.23K) driven by leisure activity and iced beverage demand. Three transitional troughs appear in March ($10.18K), June ($10.38K), and September ($10.42K), where demand weakens as seasonal patterns shift.

---

### Location and Market Performance

**City performance:** Revenue across the nine cities reveals a clear three-tier market structure. The top tier consists of Melbourne ($15.84K, 12.23%), New York ($15.75K, 12.16%), and Sydney ($15.74K, 12.15%), which together account for approximately 36.5% of total revenue. A middle tier of four cities (Los Angeles, Chicago, Toronto, Vancouver) contributes consistently in the $14.2K-$14.8K range. London ($12.84K, 9.91%) and Manchester ($11.62K, 8.97%) form a clear lagging tier, underperforming their geographic peers by approximately 15-25%. The city ANOVA (F = 24.81, p = 0.0000) confirms these differences are statistically significant and not sampling noise.

**Store format:** Standalone stores are the dominant format in Vancouver, London, Manchester, and Toronto, generating the majority of location revenue with limited contribution from other formats. In Sydney, the airport store is the highest-performing format, reflecting the high-traffic nature of a transit hub and the premium pricing airport locations command. In Melbourne and New York, all three formats contribute more evenly, suggesting a balanced multi-format strategy is viable in mature, high-revenue markets. Mall kiosks show the most inconsistent performance across cities, performing strongly in some markets and minimally in others.

---

### Product and Menu Performance

**Category revenue:** Coffee dominates by a significant margin, generating $55K across approximately 9K transactions, representing 42% of total revenue and 47% of all transactions. Tea is the clear second contributor at $28K and 5K transactions. Together these two beverage categories account for 70% of total revenue. The remaining categories contribute substantially less: Sandwich ($17K, 2K transactions), Merchandise ($11K, 1K transactions), Pastry ($10K, 2K transactions), and Smoothie ($9K, 1K transactions).

A strategically important pattern emerges in merchandise: it generates $11K from only 1K transactions, the highest revenue-per-transaction ratio in the portfolio at approximately $22.45 average order value. This makes merchandise a high-value category despite low volume, and each sale contributes disproportionately to total revenue.

**Discount impact on quantity:** Discounts produce minimal and inconsistent effects on purchase quantity across categories. The largest lift occurs in Merchandise, where average quantity increases from 1.70 to 1.92 with a discount applied (13% increase). Coffee (+4%), Smoothie (+4%), and Tea (+3%) show small but positive responses. The most analytically interesting result is Sandwich, where discounts are actually associated with a slight decrease in average quantity purchased (1.73 to 1.67), suggesting sandwich buyers are not price-sensitive in their quantity decisions. The independent t-test (t = -3.39, p = 0.0007) confirms that discounts significantly reduce order value without reliably increasing quantities purchased, making broad discounting a value-destructive strategy across most categories.

**Discount impact on order value:** Discounts consistently reduce average order value across all six categories. Pastry shows the steepest percentage decline, from $4.04 to $3.61 (-11%). Tea drops from $6.04 to $5.51 (-9%), and Coffee from $6.36 to $5.94 (-7%). Sandwich falls from $10.07 to $8.68 (-14% in absolute terms), the largest absolute dollar drop among mid-tier categories. Merchandise is the most discount-resilient category: despite having the highest average order value at $22.61, discounting reduces it only to $21.61, a 4% drop that is proportionally the smallest of any category.

---

### Customer Demographics and Loyalty

**Revenue by age group:** The 25-34 segment leads with $31.65K, followed by 35-44 at $25.41K. Together these two groups account for approximately 44% of total revenue. A notable tie exists between 55-64 and 18-24, both contributing exactly $20.03K, suggesting comparable spending power despite being at opposite ends of the working-age spectrum. The 45-54 segment ($19.31K) underperforms both its adjacent age brackets, making it the second-lowest contributor ahead of only the 65+ group ($13.11K). This underperformance from a typically peak-earning demographic suggests a product, marketing, or experience misalignment worth investigating.

**Loyalty behavior by age group:** The loyalty data reveals a sharp structural divide between customers aged 35 and above versus those under 35. The four older age groups cluster tightly between 36.83% (55-64) and 38.07% (65+), a range of just 1.24 percentage points, indicating consistently high and stable loyalty participation. In sharp contrast, younger groups fall significantly below this band: 18-24 at 22.71% and 25-34 at 20.75%. The central tension is that the 25-34 group generates the most revenue of any segment but carries the lowest loyalty rate in the entire portfolio, meaning the highest-spending customers are also the least retained. The 18-24 group, despite contributing the same revenue as 55-64, shows a loyalty rate nearly 15 percentage points lower, representing a significant untapped retention opportunity.

---

### Weather Impact Analysis

The one-way ANOVA (F = 4.07, p = 0.0067) confirms that weather conditions have a statistically significant effect on revenue. This is not a visual illusion.

**Revenue by weather condition:** Rainy conditions generate the highest total revenue at $50,730.98 (approximately 39% of total), followed by Sunny at $48,022.76 (approximately 37%), Cloudy at $22,468.81 (approximately 17%), and Snowy at $1,736.36 (approximately 1%). Together, rainy and sunny conditions account for 76% of total revenue.

**City-level weather patterns:** London generates its highest revenue under rainy conditions ($6,536.03), by far its strongest weather state, while its snowy revenue ($24.60) is essentially zero, suggesting heavy weather reduces London foot traffic to near-zero. Los Angeles ($8,382.35) and New York ($7,244.22) are the clear leaders under sunny conditions. Vancouver and Manchester generate their highest revenue in rainy conditions, consistent with their climates and the association between wet weather and hot beverage consumption. Chicago shows a notable reversal, performing stronger in sunny ($5,601.70) than rainy ($4,894.88) conditions, indicating Chicago customers are more deterred by rain than their counterparts in other markets.

**Product and weather interaction:** Coffee dominates across all weather conditions ($21,523.72 in rainy, $20,439.55 in sunny). Tea shows strong rainy-weather performance ($11,204.22), reinforcing the hot beverage demand pattern. A counter-intuitive finding appears in Smoothies, which generate slightly more revenue in rainy conditions ($3,647.98) than sunny ($3,303.55), suggesting smoothie purchases are driven more by impulse than weather preference. Merchandise shows near-identical performance across rainy ($4,100.69) and sunny ($4,177.67) conditions, confirming it is weather-neutral and should be promoted consistently regardless of forecast.

---

### Holiday and Event Impact Analysis

The independent t-test (t = 2.58, p = 0.0099) confirms that holiday periods generate significantly higher average order values than non-holiday periods.

**Overall holiday effect:** Average order value rises to $7.30 during holidays compared to $6.84 on non-holiday days, a 6.7% premium. Applied across 19K total transactions, properly activating holiday periods represents a meaningful revenue opportunity.

**Product performance across holidays:** Merchandise is the highest AOV category across most holidays, peaking on Boxing Day ($25.92), Christmas Day ($23.52), and New Year's Day ($21.75), all significantly above the merchandise baseline of $22.45. This confirms that gift-related and seasonal purchasing is concentrated in the December-January holiday cluster.

The most striking product-holiday combination is Independence Day, where Tea AOV reaches $13.24 (more than double its overall average of $5.97) and Sandwich AOV hits $15.11, well above its $9.89 baseline. This suggests Independence Day drives a fundamentally different consumption pattern linked to social gatherings and celebratory meals.

**The Boxing Day paradox:** Despite Merchandise hitting its highest AOV of the year on Boxing Day ($25.92), the overall Boxing Day AOV ($6.15) falls below the non-holiday baseline ($6.84). This indicates the day is dominated by high-volume low-value transactions, likely reflecting post-holiday discount shopping behavior, while a smaller subset of customers makes high-value merchandise purchases. A minimum spend threshold or bundle mechanic could correct this imbalance.

**City-level holiday variation:** New York, Melbourne, and Los Angeles demonstrate strong average order values during specific holidays, while London and Manchester show more moderate customer spending behavior during holiday periods, consistent with their overall underperformance in the market tier analysis.

---

## Power BI Dashboard

The Power BI dashboard translates all Python analysis findings into an interactive 6-page visual story for business stakeholders. 

**Page 1: Time-Driven Revenue Optimization**

Hour-level, day-level, and month-level revenue trend lines revealing the dual morning-afternoon demand structure, weekend volume concentration, and the bi-seasonal January-August peak pattern.

<img width="1426" height="797" alt="01_time_revenue" src="https://github.com/user-attachments/assets/9ea0222e-fd24-40b3-8b84-d712707430e8" />


---

**Page 2: Location and Market Performance**

City revenue distribution and store type performance by market. Reveals the three-tier city structure and the format-specific performance patterns that vary significantly by geography.

<img width="1428" height="797" alt="02_location_market" src="https://github.com/user-attachments/assets/24022d10-edc0-4ff4-8a2e-90f60c081ce9" />


---

**Page 3: Product and Menu Performance**

Category revenue and transaction volume comparison, discount impact on quantity purchased, and discount impact on average order value across all six categories.

<img width="1424" height="800" alt="03_product_menu" src="https://github.com/user-attachments/assets/3be1e35e-fc24-4529-827d-43df5e75e9f8" />


---

**Page 4: Customer Demographics and Loyalty**

Revenue contribution by age group paired with loyalty rate by age group, revealing the central tension between the 25-34 segment's high revenue and low retention.

<img width="1415" height="788" alt="04_customer_demographics" src="https://github.com/user-attachments/assets/dc8f525b-d5ff-42e1-808a-a2de95fb7b12" />


---

**Page 5: Weather Impact Analysis**

Revenue heatmap by weather condition and city, and revenue breakdown by weather condition and product category, validated by one-way ANOVA (p = 0.0067).

<img width="1420" height="798" alt="05_weather_impact" src="https://github.com/user-attachments/assets/e50facbe-4e25-41a2-816e-c530fde20764" />


---

**Page 6: Holiday and Event Impact Analysis**

Average order value during holidays versus non-holidays, product AOV by holiday name, and city-level holiday performance matrix, validated by independent t-test (p = 0.0099).

<img width="1414" height="792" alt="06_holiday_events" src="https://github.com/user-attachments/assets/b238dcf2-71a1-4e07-8b80-653dbd683e2e" />


---

## Strategic Recommendations

Recommendations are ordered by operational domain and derived directly from statistical analysis and business intelligence findings.

---

**Operations and Staffing**

Concentrate staffing and inventory around the two proven demand windows: the morning peak (7-10 AM) and the secondary afternoon window (2-4 PM). Scale up fully for the complete weekend (Saturday + Sunday), which drives approximately 37% of weekly revenue through volume rather than higher per-transaction spending.

Build a bi-seasonal operational calendar with distinct inventory, staffing, and promotional plans for the winter peak (December-January) and summer peak (July-August), with targeted stabilization campaigns during the transitional dips in March, June, and September.

Develop city-specific weather response plans. London and Vancouver require rainy-day operational readiness. Los Angeles and Chicago need sunny-period capacity planning. Rainy and sunny conditions together account for 76% of total revenue.

---

**Pricing and Discounting**

Discontinue broad discounting programs across most categories. Statistical testing confirms that discounts reduce average order value (t = -3.39, p = 0.0007) without meaningfully increasing purchase quantity, making them value-destructive at scale.

Replace discounting with beverage-plus-food bundle offers (for example, coffee + pastry) as a higher-ROI alternative that grows basket size without eroding per-unit revenue.

Reposition merchandise as a premium, full-price category. Buyer behavior shows it is price-insensitive and holds AOV well even without promotional support. The only category where discounting shows meaningful quantity uplift is merchandise (13% increase), so targeted merchandise promotions may be justified where inventory clearance is a priority.

---

**Product and Menu Strategy**

Protect coffee and tea as the revenue engine. Together they represent 70% of total revenue, and any degradation in quality, availability, or service in these two categories has an outsized business impact.

Promote hot beverages aggressively during rainy and cloudy conditions, where demand data confirms a clear uplift. Extend smoothie promotion beyond sunny periods, as the data shows smoothies sell slightly more in rainy conditions than expected.

Maintain consistent merchandise visibility year-round since it is weather-neutral, while concentrating merchandise campaign investment in the Boxing Day-Christmas-New Year's window, where AOV peaks at $21-$26.

---

**Market and Location Strategy**

Address the London and Manchester performance gap as a priority. Both cities consistently underperform across revenue, holiday AOV, and weather conditions. Investigate whether the gap is driven by store format mix, pricing, local demand, or marketing investment before committing to expansion in either market.

Use Sydney's airport store as an internal benchmark for transit hub operations and evaluate whether airport formats in other cities are being fully optimized for premium pricing and throughput.

Reassess mall kiosk viability on a city-by-city basis. The format performs well in some markets and poorly in others and should not be treated as a uniform expansion vehicle.

---

**Customer Retention and Loyalty**

Make the 25-34 segment the primary retention investment target. This group generates the most revenue of any age bracket but has the lowest loyalty rate (20.75%). Even modest retention improvement here would yield significant revenue gains.

Design digital-first loyalty mechanics (app-based rewards, gamification, personalized offers) specifically for under-35 customers, who are unlikely to respond to traditional loyalty programs at the same rate as older cohorts.

Investigate the 45-54 revenue underperformance. This segment should theoretically be a strong contributor given peak earning years, and its relative weakness suggests a product, marketing, or experience misalignment worth diagnosing.

---

**Holiday and Event Activation**

Localize all holiday campaigns by market. Australia Day applies to Melbourne and Sydney only. Canada Day applies to Toronto and Vancouver only. Independence Day and Veterans Day apply to US cities only. Generic global holiday campaigns dilute impact and waste spend.

Build Independence Day into the US promotional calendar as a high-priority food and beverage event. Tea and sandwich AOV spike dramatically on this day, indicating strong social gathering-driven demand.

Investigate the Boxing Day AOV paradox. Merchandise AOV peaks at $25.92 but overall day AOV falls below the non-holiday baseline, suggesting high-volume low-value transactions are dragging the average down. A minimum spend threshold or bundle mechanic could correct this.

---

## Getting Started

### Prerequisites

- Python 3.9 or higher
- Power BI Desktop (free download from Microsoft) for the .pbix dashboard file

### Installation

```bash
# Clone the repository
git clone https://github.com/SadeqSoltani/coffee-shop-sales-analysis.git
cd coffee-shop-sales-analysis

# Install dependencies
pip install -r requirements.txt
```

### Run the Notebook

Open `notebooks/coffee_shop_analysis.ipynb` in Jupyter Notebook or VS Code and run all cells in order. The notebook is self-contained and requires only the CSV file in the `data/` folder.

### Open the Power BI Dashboard

Open `dashboard/coffee_shop_dashboard.pbix` in Power BI Desktop. All data is embedded and no additional configuration is required.

### Dependencies

```
pandas
matplotlib
seaborn
numpy
scipy
```

---

## Author

**Sadeq Soltani**
