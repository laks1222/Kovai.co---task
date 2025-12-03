# Data Analysis and Forecasting – KOVAI.CO

## Key Insights

### 1. Strong Seasonal Patterns Across All Major Routes
Ridership shows clear recurring yearly patterns across Local, Light Rail, Rapid, and School routes.
The School route displays the strongest seasonality, with sharp increases during school months and drops during vacations.

---

### 2. Structural Break Around Early 2020 (COVID-19 Impact)
A sudden and sharp decline appears across all services in early 2020, aligning with COVID-19 restrictions.
Histograms also show two distinct clusters:
- Normal ridership (pre- and post-COVID)
- Reduced ridership (2020–2021)

---

### 3. Rapid Route is the Dominant Service
The Rapid Route consistently shows:
- Highest passenger counts
- Large seasonal swings
- Strong sensitivity to external events
This makes it the most active and volatile route in the system.

---

### 4. Peak Service & Other Routes Are Low and Stable
These services remain nearly flat with minimal variation.
Their tight distributions indicate low but steady usage by a consistent passenger base.

---

### 5. Strong Recovery and Growth After 2022
Ridership steadily increases from mid-2022 onward.
By 2023–2024:
- Local and Rapid routes exceed pre-2020 levels
- Clear signs of recovery and renewed demand

---

## Monthly Average Passenger Journeys by Service
<img width="1256" height="546" alt="Screenshot 2025-12-03 113708" src="https://github.com/user-attachments/assets/3430b851-7241-4f43-9678-c8ad0f9c20e6" />

---

# Model Workflow

### 1. Data Loading & Cleaning
- Dataset is imported
- Missing values are handled
- Date column is parsed and set for time-series analysis

### 2. Data Pre-Processing
- Columns are renamed to Prophet format (ds, y)
- Data is sorted by date
- Optional transformations (log/normalization) are applied based on distribution

### 3. Train–Test Split
- Latest portion of data (last 7–14 days) is separated
- Used for evaluating the forecasting accuracy

### 4. Model Training (Prophet)
- Prophet model is initialized
- Seasonality and trend components are automatically learned
- Model is fit on historical data

### 5. Forecast Generation
- Future dataframe is created for the next 7 days
- Prophet generates predictions (yhat, yhat_lower, yhat_upper)

### 6. Model Evaluation
- Actual vs predicted values are compared
- Metrics like MAE and RMSE are calculated to measure the forecast error

### 7. Visualization & Interpretation
- Forecast plot
- Trend/seasonality components
- Actual vs predicted comparison plot
These help in interpreting the underlying patterns and forecast reliability.

---

## Forecasting for the Next 7 Days
<img width="804" height="262" alt="Screenshot 2025-12-03 121327" src="https://github.com/user-attachments/assets/d20349e9-d415-43ea-8c10-2d614a1478b1" />

---

## Thank You!
