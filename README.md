# Morning Routine Dataset Analysis

##  Dataset Description

This dataset contains personal morning routine records including sleep, meditation, exercise, breakfast, journaling, and productivity. The main goal of this project is to **analyze patterns, correlations, and perform basic feature engineering** for potential predictive modeling.

**Columns:**

| Column | Description |
|--------|-------------|
| Date | When the routine was recorded |
| Wake-up Time | Time you wake up |
| Sleep Duration (hrs) | Hours of sleep |
| Meditation (mins) | Minutes meditated |
| Exercise (mins) | Minutes exercised |
| Breakfast Type | Type of breakfast (Protein-rich, Carb-rich, Heavy, Light, Skipped) |
| Journaling (Y/N) | Whether journaling was done |
| Work Start Time | Time when work starts |
| Productivity Score (1-10) | Self-reported productivity |
| Mood | Mood label (Sad, Neutral, Happy) |
| Notes | Free text notes |


## Libraries and Tools Used

- **Python 3.x**
- **Pandas** → Data manipulation and analysis  
- **NumPy** → Numerical operations  
- **Matplotlib** → Basic plotting and visualization  
- **Seaborn** → Advanced visualization and correlation analysis  


## Exploratory Data Analysis (EDA)

1. **Sleep Duration Analysis**  
   - Checked unique values to determine if sleep hours are discrete or continuous.  
   - Categorized sleep into:  
     - **Under Sleep:** 5–6 hours  
     - **Normal Sleep:** 6–8.5 hours  
     - **Over Sleep:** 8.5–9 hours  
   - Created histograms to visualize the distribution of sleep categories.

2. **Correlation Analysis**  
   - Calculated correlation between:  
     - Sleep Duration and Meditation → nearly 0 (no correlation)  
     - Sleep Duration and Productivity → measured correlation to analyze effect of sleep on productivity  
     - Mood (encoded numerically) and Productivity  

3. **Meditation + Exercise Analysis**  
   - Compared days with more vs less total minutes of meditation and exercise using bar charts.

4. **Categorical Visualizations**  
   - **Breakfast Type:** Pie chart to show proportion of breakfast types.  
   - **Journaling:** Bar chart to visualize journaling frequency.

5. **Productivity and Mood**  
   - Scatter plot of Productivity vs Sleep Duration colored by Mood to identify patterns.


## 🛠 Feature Engineering Performed

1. **Datetime Conversion**  
   - Converted `Date` to `datetime64` type for easier time-based analysis.  
   - Converted `Wake-up Time` and `Work Start Time` into numeric features (hour, minutes) for modeling.

2. **Encoding Categorical Variables**  
   - `Journaling (Y/N)` → mapped `Yes/No` to `1/0`  
   - `Breakfast Type` → one-hot encoding with `pd.get_dummies`

3. **Boolean Conversion**  
   - Any boolean columns resulting from one-hot encoding converted to integer (`1/0`) for modeling.


## Visualizations Generated

- Histograms for **sleep duration categories**  
- Bar charts for **journaling frequency**  
- Pie chart for **breakfast type distribution**  
- Scatter plots for **sleep vs productivity** colored by mood  
- Bar chart comparing **days with more vs less total meditation + exercise minutes**

