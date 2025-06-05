# Market Basket Analysis with PySpark

This project applies Association Rule Mining using PySpark's FPGrowth algorithm to uncover purchasing patterns from a dataset of 75,000 bakery transactions. The goal is to identify frequent itemsets and strong product associations that can inform marketing strategies, product bundling, and inventory management in retail settings.

## Project Objectives

- Analyze co-purchase behavior in transactional data
- Identify high-frequency itemsets and strong association rules
- Visualize purchasing trends and actionable relationships
- Recommend potential business strategies based on discovered rules

## Technologies Used

- PySpark (DataFrames, MLlib FPGrowth)
- pandas, matplotlib
- Jupyter Notebook
- Big data handling and EDA

## Key Steps

1. **Data Preprocessing**
   - Loaded and cleaned two datasets: transactional logs and product metadata
   - Joined transaction and goods data to generate item descriptions (e.g., “Green Tea Cookie”)

2. **Exploratory Data Analysis**
   - Counted item frequency and top co-occurring pairs
   - Visualized top 10 items and item pairs using bar charts

3. **Frequent Pattern Mining**
   - Applied PySpark’s `FPGrowth` to extract frequent itemsets and association rules
   - Explored support, confidence, and lift metrics for insights

4. **Advanced Use Case**
   - Grouped items by transaction and analyzed frequent flavor + product combinations
   - Plotted top frequent itemsets and lift vs. confidence of rules

## Results & Insights

- Common pairs like `["Coffee", "Eclair"]` and `["Green Tea", "Raspberry Lemonade"]` indicate cross-selling opportunities
- Rules with high confidence and lift (e.g., `[Green Tea] → [Raspberry Lemonade]`) suggest strong product relationships
- Recommendations:
  - Promote popular combos via discounts or bundles
  - Place associated products closer together in-store
  - Maintain inventory for high-frequency items and pairs

## How to Run

1. Open the notebook in Jupyter or your preferred environment with PySpark configured
2. Run each cell in order to process the data and generate insights
3. Modify `minSupport` or `minConfidence` in FPGrowth for different rule thresholds
