# Hotel-Management

This project is all about understanding hotel prices and discounts.  
I explored how different hotels change their prices, how much discount they give,  
and how these discounts affect booking behavior.

I used Python to clean the data, create useful features, visualize patterns, and group hotels into clusters based on their pricing strategy.

---

## Project Structure 
---

## 1. Data Cleaning (What I fixed)

- Removed duplicate rows  
- Converted dates into proper format  
- Removed wrong values (like -1 rooms)  
- Checked that no important columns had missing values  
- Converted price columns into numeric form  

This step helps in making the dataset clean and ready for analysis.

---

## 2. Feature Engineering (New useful columns)

I created new features to understand hotel behavior better:

- **discount_pct** → how much discount is given  
- **price_per_night** → actual cost per night after discount  
- **days_to_checkin** → time gap between today and check-in  
- **checkin_month**  
- **checkin_weekday**

These features helped in EDA, clustering, and optional ML.

---

## 3. Exploratory Data Analysis (Understanding the data)

I visualized the data using plots such as:

- Price distribution  
- Discount distribution  
- Price vs discount  
- Hotel star rating count  
- Correlation heatmap  

These charts helped me understand how hotels behave with pricing and discounts.

---

## 4. Clustering (KMeans)

I grouped hotels into 3 clusters based on their  
**price_per_night** and **discount_pct**.

### 🔹 Cluster meanings:
1. **Budget Hotels** → Low price & high discount  
2. **Mid-range Hotels** → Medium price & moderate discount  
3. **Premium Hotels** → High price & low discount  

This helped me understand which hotels are discount-heavy and which ones depend more on brand value.

---

## 5. ML Model (Just for checking)

I used **RandomForestRegressor** to see if my features can predict bookings/room availability.

- Model performance: **R² ≈ 0.94**

This step confirm that the feature engineering was correct.

---

## 6. Key Insights 

- Budget hotels use discounts more aggressively  
- Premium hotels don’t need big discounts  
- Discount alone doesn’t guarantee bookings  
- Combination of price + discount + timing matters  
- Clustering gives a clear picture of hotel behavior  

----------------------------------------------------------------------
