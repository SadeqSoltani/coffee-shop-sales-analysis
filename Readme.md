**Project Title: Coffee Shop Sales Analysis**

<img width="1400" height="600" alt="image" src="https://github.com/user-attachments/assets/c9dfa7e9-7456-46fa-9999-bd924a2af446" />


**Dataset Description:**
This dataset tracks consumer purchasing behavior across 45 coffee shops in 9 global cities over a full calendar year (January–December 2023), capturing how weather conditions, location-based pricing, and seasonal patterns influence daily sales. It is calibrated to real-world retail foot-traffic and point-of-sale (POS) benchmarks, incorporating city-level currency adjustments, transit hub pricing markups, and weather-driven demand shifts modeled with realistic autocorrelation patterns. To reflect the imperfections of real corporate data, approximately 5% of environmental records contain missing values and some demographic markers are obscured for non-loyalty customers both handled explicitly in the data cleaning phase of this project.


**Executive Summary:** This project analyzes coffee shop sales performance across multiple cities, product categories, customer demographics, weather conditions, and holiday periods using Power BI. The analysis identifies key revenue drivers, customer behavior patterns, and operational opportunities to support data-driven business decisions. Findings show that coffee products dominate overall sales, younger customers generate the highest revenue, older customers demonstrate stronger loyalty behavior, and weather and holidays significantly influence purchasing patterns across locations.


**Business Questions**
- Which product categories generate the highest revenue?
- How does customer behavior vary across age groups?
- Do discounts improve basket size or reduce profitability?
- How do weather conditions influence customer demand?
- Which holidays generate stronger customer spending?
- Which cities and store types perform best?


**Business Value:**
- optimize staffing during peak demand periods
- improve product promotion strategies
- increase average order value
- identify high-value customer segments
- improve seasonal and weather-based planning
- support location-specific operational decisions

**Dashboard Preview Section:**

KPI Summary: Across all time periods, the business generated $129.54K in total revenue from 19K transactions, with an average order value of $6.85.

**Section 1. Time-Driven Revenue Optimization:**

<img width="1426" height="797" alt="image" src="https://github.com/user-attachments/assets/a884acc3-ef42-48dc-9399-a9ef2eae1413" />


**1.1 Hour-Based Performance:**
Revenue follows a sharp morning concentration, climbing steeply from hour 5 onward and peaking at hour 9 with $17.2K , consistent with commuter-driven demand during the morning rush. After a sharp midday dip to $7.6K at hour 11, revenue partially recovers to a secondary peak of $8.3K at hour 15, suggesting a distinct afternoon demand window, likely driven by post-lunch and work-break visits. From hour 16 onward, revenue declines steadily, reaching its lowest levels after hour 20 ($1.0K). This two-peak daily pattern a dominant morning spike and a smaller afternoon recovery, indicates that the business has two meaningful demand windows rather than one. Operationally, staffing and inventory should be concentrated in the 7–10 AM window, while the 14–16 PM window presents an underutilized opportunity for targeted afternoon promotions such as discounted beverages or snack bundles to deepen that secondary peak.

**1.2 Day-Level Performance:**
Weekly revenue shows a relatively flat pattern from Monday ($13.7K) through Wednesday ($15.0K), then accelerates sharply from Thursday ($15.9K) through Saturday ($25.4K), the highest-revenue day of the week. Sunday maintains strong performance at $22.4K, making the full weekend (Saturday + Sunday: $47.8K combined) responsible for approximately 37% of weekly revenue.
This weekend concentration reflects leisure-driven purchasing behavior with higher dwell time and transaction values. Staffing, inventory, and promotional activity should be significantly scaled up across the full weekend, not just Saturday. For the flat Mon–Wed window, targeted weekday loyalty incentives or lunchtime promotions could help shift the revenue distribution toward a more balanced weekly profile.

**1.3 Month-Level Performance:**
Monthly revenue shows a volatile, oscillating pattern rather than a smooth seasonal curve, ranging from a low of $10.18K in March to a high of $11.71K in January. Two distinct peaks are visible: a winter peak in January ($11.71K) and December ($11.61K), likely driven by holiday season traffic and increased hot beverage consumption, and a summer peak in July and August (both ~$11.23K) suggesting a second demand cycle driven by leisure activity and iced beverage demand. These two peaks are separated by notable troughs in March ($10.18K), June ($10.38K), and September ($10.42K), transitional months where demand weakens as seasonal patterns shift.
This pattern highlights the need for a bi-seasonal planning approach rather than a single winter-focused strategy. Peak periods in January, July–August, and December warrant increased inventory, staffing, and seasonal product launches. Transitional months particularly March, June, and September should be targeted with limited-time offers and marketing campaigns to prevent avoidable revenue dips.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Section 2. Location & Market Performance**

<img width="1428" height="797" alt="image" src="https://github.com/user-attachments/assets/bda1962b-ce1c-46a9-9a12-2d7a845cc4d9" />


**2.1 City-Level Performance:**
Revenue across the nine cities reveals a clear two-tier market structure. The top tier — Melbourne ($15.84K, 12.23%), New York ($15.75K, 12.16%), and Sydney ($15.74K, 12.15%) — are tightly clustered and together account for approximately 36.5% of total revenue. A middle tier of four cities: Los Angeles ($14.79K), Chicago ($14.39K), Toronto ($14.32K), and Vancouver ($14.27K)  contributes consistently in the $14.2K–$14.8K range. London ($12.84K, 9.91%) and Manchester ($11.62K, 8.97%) form a clear lagging tier, generating meaningfully less revenue than every other market.
This tiered structure is more informative than the surface-level observation that revenue is "evenly distributed. While no single city dominates, the bottom two markets London and Manchester are underperforming relative to their geographic peers by approximately 15–25%. Understanding whether this gap is driven by store count, format mix, pricing, or local demand patterns is a key operational question for leadership.

**2.2 Store-Type Performance:**
Store format performance varies significantly across cities and does not follow a uniform pattern. Standalone stores are the dominant format in Vancouver, London, Manchester, and Toronto, where they generate the majority of location revenue with limited contribution from other formats. However, in Sydney, the airport store is the highest-performing format a notable exception that likely reflects the high-traffic nature of Sydney's transit hub and the premium pricing that airport locations command. In Melbourne and New York, all three formats contribute more evenly, suggesting a balanced multi-format strategy is viable in mature, high-revenue markets. Mall kiosks show the most inconsistent performance across cities strong in some markets (Melbourne, New York) and minimal in others (Vancouver, London) indicating that kiosk viability is highly dependent on local foot traffic and placement quality rather than being a reliably scalable format.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Section 3. Product & Menu Performance**

<img width="1424" height="800" alt="image" src="https://github.com/user-attachments/assets/d4e96659-3a0d-4474-8bc8-467c73f96d53" />



**3.1 Category-Level Revenue & Transaction Performance:**
Coffee is the dominant product category by a significant margin, generating $55K in revenue across approximately 9K transactions representing roughly 42% of total revenue and 47% of all transactions. Tea is the clear second contributor at $28K and 5K transactions. Beyond these two beverage leaders, the remaining categories are considerably smaller: Sandwich ($17K, 2K transactions), Merchandise ($11K, 1K transactions), Pastry ($10K, 2K transactions), and Smoothie ($9K, 1K transactions).
A notable pattern emerges when comparing revenue to transaction volume: Merchandise generates $11K from only 1K transactions, implying a high revenue-per-transaction rate consistent with its status as the highest average order value category in the portfolio. This makes merchandise a strategically important category despite its lower transaction volume, as each sale contributes disproportionately to revenue. The heavy concentration of demand in coffee and tea (70% of total revenue combined) underscores the need to protect quality and availability in these categories while developing strategies to grow the contribution of higher-margin items like merchandise.

**3.2 Discount Impact on Purchase Quantity:**
Discounts produce minimal and inconsistent effects on purchase quantity across categories. The largest lift occurs in Merchandise, where average quantity increases from 1.70 to 1.92 with a discount applied — a 13% increase and the strongest discount response of any category. Coffee (+4%), Smoothie (+4%), and Tea (+3%) show small but positive responses. Pastry shows no change at all (1.71 in both conditions).
The most analytically interesting finding is Sandwich, where discounts are associated with a slight decrease in average quantity purchased (1.73 to 1.67). This counter-intuitive result may suggest that sandwich buyers are not price-sensitive in their quantity decisions, or that discounting attracts a different customer profile with lower purchase intent. Overall, the data indicates that broad discounting is an ineffective lever for driving volume across most categories — with merchandise being the notable exception where discount-driven quantity uplift may justify the margin trade-off.

**3.3 Discount Impact on Average Order Value:**
Discounts consistently reduce average order value across all six categories, but the magnitude varies meaningfully. Pastry shows the steepest percentage decline — from $4.04 to $3.61 (−11%) — making it the category where discounting is most costly relative to its already-low base price. Tea drops from $6.04 to $5.51 (−9%), and Coffee from $6.36 to $5.94 (−7%). Sandwich falls from $10.07 to $8.68 (−14% in absolute terms), the largest absolute dollar drop among mid-tier categories. Merchandise is the most discount-resilient category: despite having the highest average order value at $22.61, discounting reduces it only to $21.61  a 4% drop that is proportionally the smallest of any category. This suggests that merchandise buyers are relatively price-insensitive and are purchasing based on product appeal rather than price incentive, making it a strong candidate for premium positioning rather than promotional discounting.
The combined picture across 3.2 and 3.3 is clear: discounts reduce revenue per transaction without reliably increasing quantity purchased, making broad discounting a value-destructive strategy for most categories. Targeted, category-specific promotions — particularly bundle offers pairing coffee or tea with pastries — are likely to be more effective than blanket discounting.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Section 4. Customer Demographics & Loyalty Analysis**

<img width="1415" height="788" alt="image" src="https://github.com/user-attachments/assets/b9dfa921-ff2e-4817-8249-fb2a69df31c0" />


**4.1 Revenue Contribution by Age Group**
Revenue distribution across age groups reveals a clear spending hierarchy with two notable anomalies. The 25–34 segment leads with $31.65K, followed by 35–44 at $25.41K  together these two groups account for approximately 44% of total revenue. The middle of the distribution contains a notable tie: both 55–64 and 18–24 contribute exactly $20.03K, suggesting comparable spending power despite being at opposite ends of the working-age spectrum. The 45–54 segment ($19.31K) underperforms both its adjacent age brackets, making it the second-lowest contributor ahead of only the 65+ group ($13.11K).
The 45–54 anomaly is worth investigating: this age group typically represents peak earning years and should theoretically show stronger spending. Its relative underperformance may reflect lower visit frequency, different product preferences, or lower engagement with the brand's current marketing and product mix. The tie between 55–64 and 18–24 similarly suggests that age alone is not a reliable predictor of spending visit frequency, loyalty status, and product category preferences are likely more meaningful drivers of revenue contribution.

**4.2 Loyalty Behavior by Age Group**
The loyalty data reveals a striking structural divide between customers aged 35 and above versus those under 35. The four older age groups cluster tightly between 36.83% (55–64) and 38.07% (65+) a range of just 1.24 percentage points indicating consistently high and stable loyalty participation regardless of age within this cohort. In sharp contrast, both younger groups fall sharply below this band: 18–24 at 22.71% and 25–34 at 20.75%.
The inverse relationship between revenue contribution and loyalty rate is the central tension of this section. The 25–34 group generates the most revenue of any segment but has the lowest loyalty rate in the entire portfolio meaning the business's highest-spending customers are also its least retained. Conversely, the 65+ group is the most loyal segment but the lowest revenue contributor, likely reflecting lower visit frequency or lower average spend per transaction. The 18–24 group, despite contributing the same revenue as 55–64, shows a loyalty rate nearly 15 percentage points lower — suggesting a significant untapped retention opportunity among younger customers who are already transacting at a meaningful level.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Section 5. Weather Impact Analysis**

<img width="1420" height="798" alt="image" src="https://github.com/user-attachments/assets/1eb5f462-84b2-41a6-b192-f15b53601217" />


**5.1 Weather Impact Across Cities:**
Revenue breaks down across four weather conditions as follows: Rainy ($50,730.98, ~39% of total), Sunny ($48,022.76, ~37%), Cloudy ($22,468.81, ~17%), and Snowy ($1,736.36, ~1%). Together, rainy and sunny conditions account for approximately 76% of total revenue, while cloudy conditions contribute a meaningful additional 17% that is often overlooked in high-level weather analysis.
City-level patterns reveal important geographic differentiation. Vancouver ($7,593.05) and Manchester ($7,437.61) generate their highest revenue under rainy conditions consistent with their climates and the strong association between wet weather and hot beverage consumption. Melbourne ($7,249.77) also peaks in rainy conditions and is the overall top-revenue city. London shows the most weather-dependent revenue pattern of any city: its rainy revenue ($6,536.03) is by far its strongest condition, while its snowy revenue ($24.60) is essentially zero the lowest city-weather data point in the entire dataset suggesting that heavy weather reduces London foot traffic to near-zero. Los Angeles ($8,382.35) and New York ($7,244.22) are the clear leaders under sunny conditions, reflecting stronger baseline demand in warmer, sunnier climates. Chicago shows notable weather sensitivity, performing stronger in sunny ($5,601.70) than rainy ($4,894.88) conditions the reverse of most other cities indicating that Chicago customers are more deterred by rain than their counterparts in other markets.

**5.2 Weather Impact Across Product Categories:**
Coffee dominates revenue across all weather conditions: $21,523.72 in rainy, $20,439.55 in sunny, $9,682.32 in cloudy, and $654.47 in snowy conditions. Tea is a consistent second contributor, with particularly strong rainy-weather performance ($11,204.22 vs $10,237.63 in sunny) reinforcing the hot beverage demand pattern during adverse weather. Sandwich is the third-largest category overall ($16,650.04), with broadly similar performance across rainy ($6,381.46) and sunny ($6,496.81) conditions, suggesting food demand is less weather-sensitive than beverage demand.
Two category-level anomalies are worth highlighting. First, Smoothie generates slightly more revenue in rainy conditions ($3,647.98) than in sunny ($3,303.55) counter to expectations, as smoothies are typically associated with warm weather purchases. This may reflect impulse purchasing behavior rather than weather-driven preference. Second, Merchandise shows near-identical performance in rainy ($4,100.69) and sunny ($4,177.67) conditions confirming that merchandise demand is essentially weather-neutral and should be promoted consistently year-round regardless of seasonal weather planning.
The sharp revenue collapse under snowy conditions ($1,736.36 total) confirms that snow significantly reduces store traffic across all cities and categories, making snow event preparedness a relevant operational consideration for affected markets.

------------------------------------------------------
**Section 6. Holiday & Event Impact Analysis**

<img width="1414" height="792" alt="image" src="https://github.com/user-attachments/assets/b26e2149-b424-42d2-969b-0aa4ab146e90" />


**6.1 Holiday Impact on Average Order Value:**

Holidays drive a measurable uplift in spending behaviour: average order value rises to $7.30 during holidays compared to $6.84 on non-holiday days a 6.7% premium that, applied across 19K total transactions, represents a meaningful revenue opportunity when holiday periods are properly activated. The dataset covers seven named holidays across the nine cities, each with different geographic reach and product mix implications.

**6.2 Product Performance Across Holidays:**
Product performance during holidays reveals sharp, event-specific demand patterns that go well beyond general seasonal trends.
Merchandise is the highest AOV category across most holidays, peaking on Boxing Day ($25.92), Christmas Day ($23.52), and New Year's Day ($21.75) all significantly above the merchandise baseline of $22.45. This confirms that gift-related and seasonal merchandise purchasing is concentrated in the December–January holiday cluster, making this a critical inventory and visibility window for the category.
The most striking product-holiday combination in the entire dataset is Independence Day, where Tea AOV reaches $13.24 — more than double its overall average of $5.97 and Sandwich AOV hits $15.11, well above its $9.89 baseline. This suggests that Independence Day drives a fundamentally different consumption pattern, likely linked to social gatherings and celebratory meals, creating a distinct demand profile from other holidays.
Veterans Day also stands out for Sandwich performance ($12.35 AOV), reinforcing that food categories experience their strongest holiday uplift during US patriotic events rather than winter holidays. Tea peaks on Australia Day ($8.56) in Australia-specific markets, reflecting regional celebration patterns.
Boxing Day presents an analytical contradiction: despite merchandise hitting its highest AOV of the year ($25.92), the overall Boxing Day AOV ($6.15) falls below the non-holiday baseline ($6.84). This indicates that while a subset of customers make high-value merchandise purchases, the day is dominated by high-volume, low-value transactions — possibly reflecting post-holiday discount shopping behaviour. Pastry hits its lowest AOV of any holiday on Boxing Day at $2.40, the lowest single category-holiday value in the dataset.

**6.3 City-Level Holiday Performance:**
City-level analysis reveals that holiday impact is heavily shaped by geographic relevance holidays only drive uplift in the markets where they are culturally observed.
The single highest city-holiday AOV in the dataset is New York on Independence Day at $12.46 nearly double the city's overall average of $7.30 confirming that locally resonant holidays create disproportionate spending spikes in their home markets. Veterans Day is similarly US-specific, appearing only for Chicago ($7.02) and New York ($8.19). Australia Day data appears only in Melbourne ($7.56) and Sydney ($6.08), while Canada Day is observed only in Toronto ($8.40) and Vancouver ($4.65) with Toronto significantly outperforming Vancouver on this holiday.
At the city total level, Chicago leads with the highest overall AOV across all holidays at $6.90, followed by Melbourne ($7.63 second highest) and Los Angeles ($7.11). Manchester ($5.87) and London ($6.01) post the two lowest city-level holiday AOVs, falling below the non-holiday baseline consistent with their broader underperformance identified in Section 2, and suggesting that holiday activations in these two markets are currently failing to generate the spending uplift seen elsewhere.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Overall Strategic Recommendations**

**Operations & Staffing**
- Concentrate staffing and inventory around the two proven demand windows: the morning peak (7–10 AM) and the secondary afternoon window (2–4 PM), and scale up fully for the complete weekend (Saturday + Sunday), which drives approximately 37% of weekly revenue.
- Build a bi-seasonal operational calendar with distinct inventory, staffing, and promotional plans for the winter peak (December–January) and summer peak (July–August), with targeted stabilisation campaigns during the transitional dips in March, June, and September.
- Develop city-specific weather response plans — London and Vancouver require rainy-day operational readiness, while Los Angeles and Chicago need sunny-period capacity planning. Rainy and sunny conditions together account for 76% of total revenue.

**Pricing & Discounting**
- Discontinue broad discounting programs across most categories. The data consistently shows that discounts reduce average order value without meaningfully increasing purchase quantity — making them value-destructive at scale.
- Replace discounting with beverage-plus-food bundle offers (e.g., coffee + pastry) as a higher-ROI alternative that grows basket size without eroding per-unit revenue.
- Reposition merchandise as a premium, full-price category buyer behaviour shows it is price-insensitive and holds AOV well even without promotional support.

**Product & Menu Strategy**
- Protect coffee and tea as the revenue engine — together they represent 70% of total revenue, and any degradation in quality, availability, or service in these two categories has an outsized business impact.
 Promote hot beverages aggressively during rainy and cloudy conditions, where demand data confirms a clear uplift. Extend smoothie promotion beyond sunny periods, as the data shows smoothies sell slightly more in rainy conditions than expected.
- Maintain consistent merchandise visibility year-round it is weather-neutral while concentrating merchandise campaign investment in the Boxing Day–Christmas–New Year's window, where AOV peaks at $21–$26.

**Market & Location Strategy**
- Address the London and Manchester performance gap as a priority. Both cities consistently underperform across revenue, holiday AOV, and weather conditions. Investigate whether the gap is driven by store format mix, pricing, local demand, or marketing investment before committing to expansion in either market.
- Use Sydney's airport store as an internal benchmark for transit hub operations and evaluate whether airport formats in other cities are being fully optimised for premium pricing and throughput.
- Reassess mall kiosk viability on a city-by-city basis the format performs well in some markets and poorly in others, and should not be treated as a uniform expansion vehicle.

**Customer Retention & Loyalty**
- Make the 25–34 segment the primary retention investment target. This group generates the most revenue of any age bracket but has the lowest loyalty rate (20.75%) — even modest retention improvement here would yield significant revenue gains.
- Design digital-first loyalty mechanics (app-based rewards, gamification, personalised offers) specifically for under-35 customers, who are unlikely to respond to traditional loyalty programs at the same rate as older cohorts.
- Investigate the 45–54 revenue underperformance this segment should theoretically be a strong contributor given peak earning years, and its relative weakness suggests a product, marketing, or experience misalignment worth diagnosing.

**Holiday & Event Activation**
- Localise all holiday campaigns by market Australia Day for Melbourne and Sydney only, Canada Day for Toronto and Vancouver only, Independence Day and Veterans Day for US cities only. Generic global holiday campaigns dilute impact and waste spend.
- Build Independence Day into the US promotional calendar as a high-priority food and beverage event tea and sandwich AOV spike dramatically on this day, indicating strong social gathering-driven demand.
- Investigate the Boxing Day AOV paradox: merchandise AOV peaks at $25.92 but overall day AOV falls below the non-holiday baseline, suggesting high-volume low-value transactions are dragging the average down. A minimum spend threshold or bundle mechanic could correct this.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**How to Run:**

**Python Notebook:**

1. Clone the repo and navigate to the folder

```
git clone https://github.com/SadeqSoltani/coffee-shop-sales-analysis.git
cd coffee-shop-sales-analysis
```

2. Install required libraries

```
pip install pandas numpy matplotlib seaborn
```
3. Open and run coffee_analysis.ipynb in Jupyter or VS Code

**Power BI Dashboard:**

Open powerbi_dashboard.pbix in Power BI Desktop

If prompted, point the data source to coffee_shop_sales.csv in the same folder
