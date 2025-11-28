# Hotel-Management

Analyzed hotel pricing data to find which discounts increase bookings and built visualizations & clusters to optimize discount strategy.

## Project structure

Hotel-Management/
├─ data/
│ ├─ raw/ # original hotels_data.csv
│ └─ processed/ # (optional) processed CSVs
├─ notebooks/
│ └─ preprocess.ipynb # main analysis (EDA, FE, clustering)
├─ static/
│ └─ output.png # cluster plot (generated)
├─ app.py # small Flask app to generate and show the plot
├─ requirements.txt
└─ README.md


---

## 1. Data Cleaning  
- Removed duplicates  
- Converted date columns  
- Fixed datatypes  
- Removed invalid room entries  
- No missing values in dataset  

---

## 2. Feature Engineering  
Created useful features for analysis & modeling:

- `discount_pct` — percentage discount  
- `price_per_night` — actual nightly cost  
- `days_to_checkin` — time gap between snapshot & check-in  
- `checkin_month`  
- `checkin_weekday`

These features help understand pricing behavior and booking patterns.

---

## 3. Exploratory Data Analysis (EDA)  
Performed multiple visualizations:

- Price & Discount distributions  
- Scatter: Price vs Available Rooms  
- Hotel Star distribution  
- Correlation heatmap  
- Booking patterns over time  
- Feature relationships  

---

## 4. Clustering (KMeans)  
Hotels were segmented into **3 clusters** based on  
`price_per_night` & `discount_pct`.

**Clusters identified:**
1. **Budget Hotels** → Low price, High discount  
2. **Mid-range Hotels** → Medium price, Moderate discount  
3. **Premium Hotels** → High price, Low discount  

The final cluster scatter plot visually shows how hotels group based on pricing strategy.

---

## 5. (Optional) ML Model  
A baseline model was tested (RandomForest/XGBoost)  
for predicting room availability/bookings.  
Achieved strong performance with **R² ≈ 0.94**.

*This step is optional and not required to understand the clustering insights.*

---

## 6. Results & Insights  
- Lower-priced hotels use aggressive discount strategies.  
- Premium hotels rarely offer high discounts.  
- Discount percentage alone does not strongly correlate with bookings.  
- Price and discount combinations reveal natural clusters in hotel behavior.  

These insights can help hotels optimize pricing and discount patterns for better bookings.

---

## How to Run the Notebook

1. Install dependencies:
```bash
pip install -r requirements.txt
