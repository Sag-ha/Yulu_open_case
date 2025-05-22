# Yulu_open_case

**Project Overview**

This project involves an extensive exploratory data analysis (EDA) and statistical investigation of Yulu bike-sharing usage patterns. The dataset was sourced from an online CSV file and explores user behavior based on weather, holidays, weekdays, and seasonal patterns.

**Dataset Description**

Source: yulu.csv (downloaded from this public link)
Rows: 10,886
Columns: 12 primary + 2 derived (Date, Time)
Key Columns
datetime: Timestamp of the record
season: Categorical (1: Spring, 2: Summer, 3: Fall, 4: Winter)
holiday: Binary (1: Holiday, 0: Not a holiday)
workingday: Binary (1: Working day, 0: Weekend/holiday)
weather: Categorical (1 to 4 indicating weather conditions)
temp: Actual temperature
atemp: "Feels-like" temperature
humidity: Humidity level
windspeed: Wind speed
casual, registered, count: Usage metrics

**📊 Analysis Summary**

1. Data Cleaning
No missing or duplicate records.
Derived Date and Time from the datetime column.
Outliers in windspeed were clipped using the 5th and 95th percentiles.
2. Univariate Analysis
Distribution plots for temperature, humidity, and windspeed.
Categorical plots for season and weather.
Boxplots to identify outliers in continuous variables.
3. Correlation Analysis
Heatmap used to explore Pearson correlation among variables.
Strong correlations observed between temperature (temp, atemp) and ride counts.
4. Statistical Tests
5. 
**Weekdays vs Weekends**

Significant difference for casual and registered rides.
No significant difference in total count.
Holidays vs Non-Holidays

Significant difference for both casual and registered rides.
No significant difference in total count.
Weather Conditions

Kruskal-Wallis test showed significant differences in ride demand across weather types.
Seasonal Impact

Significant statistical differences across seasons for all ride types.
T-tests confirmed differences in specific seasonal pairs.
Weather vs Season Dependency

Chi-squared test showed a significant association between season and weather.
**📌 Recommendations**

Offer Discounts on Weekdays for registered users to balance weekday usage.
Premium Pricing on Weekends & Holidays for casual riders.
Adjust Pricing by Season: Higher prices in summer and fall when casual rides peak.
Marketing Campaigns during favorable weather seasons to boost ride volume.
🛠️ Technologies Used

Python
Pandas, NumPy
Matplotlib, Seaborn
SciPy (for hypothesis testing)

**How to Run**
# Install dependencies
pip install pandas numpy seaborn matplotlib scipy

# Load dataset
df = pd.read_csv("yulu.csv")

