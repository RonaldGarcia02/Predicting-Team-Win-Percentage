# ⚾ Predicting MLB Team Win Percentage

This project builds a machine learning model to **predict the win percentage (W-L record)** of MLB teams based on financial and performance-related statistics such as payroll, attendance, and offensive metrics.

The notebook includes full data cleaning, preprocessing, and training of a Random Forest regression model.

---

## 📊 Dataset Overview

The dataset includes team-level statistics from MLB seasons (2015–2024), featuring:

- **Financials**: Approximate Payroll  
- **Fan Engagement**: Total & Average Attendance  
- **Performance Stats**: Run Differential, Hits, Walks, Stolen Bases, Strikeouts, Batting Average, On-Base %, Slugging %  
- **Outcome**: Win Percentage (`W-L Record`)  

---

## 🧹 Data Cleaning Highlights

- Merged duplicate team names (e.g. `"KAS Royals"` → `"KC Royals"`)
- Removed null rows (e.g. incomplete entries like 2024 Oakland Athletics)
- Converted dollar-formatted payroll values to `float`
- Renamed and normalized column names to snake_case
- Created numeric `team_code` values using categorical encoding

---

## 🤖 Model: Random Forest Regressor

The target variable is the team's **win percentage**.

### 🔧 Features Used

['approx_payroll', 'total_attendance', 'avg_attendance', 'run_difference',
'runs/games', 'hits', 'stolen_bases', 'walks', 'strike_outs',
'batting_average', 'on_base_%', 'slugging_%']

### 📈 Results

- **R² Score**: `0.648`  
- **RMSE**: `0.0031`

---

## 📋 Output Sample

| Actual Win % | Predicted Win % |
|--------------|------------------|
| 0.5124       | 0.5057           |
| 0.5432       | 0.5009           |
| 0.5617       | 0.5912           |
| 0.5247       | 0.5086           |

---

## 📁 Files
- `stats.csv` - Original dataset containing all original data 
- `Predicting_Team_Win_Percentage.ipynb` — Main notebook (data cleaning, modeling, evaluation)  
- `win_predictions.csv` — Table of actual vs. predicted win percentages  

---

## 📌 Future Improvements

- Add pitching stats (ERA, WHIP) for deeper predictive power  
- Tune model with cross-validation and `GridSearchCV`  
- Test with other regressors (e.g. XGBoost, Linear Regression baseline)  

---

## 🧠 Author

**Ronald Garcia**  
Built in Google Colab | May 2025  
[GitHub Profile](https://github.com/RonaldGarcia02)
