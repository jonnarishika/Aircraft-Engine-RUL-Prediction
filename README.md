# Aircraft-Engine-RUL-Prediction
This project focuses on predicting the **Remaining Useful Life (RUL)** of aircraft engines using time-series sensor data. The goal is to anticipate how many operational cycles an engine has left before failure — a critical task in predictive maintenance.

>  Final Model Performance (Test Set):  
> - **RMSE:** [Your Final RMSE]  
> - **MAE:** [Your Final MAE]  
> - **R²:** [Your Final R²]

---

##  Dataset

The dataset comes from the **CMAPSS (Commercial Modular Aero-Propulsion System Simulation)** provided by NASA. Each engine’s life is recorded cycle-by-cycle, with sensor measurements and operational settings.

- `train_FD001.txt`: Full operational history until failure  
- `test_FD001.txt`: Partial history of test engines  
- `RUL_FD001.txt`: True RUL for test engines

---

##  Project Workflow

### 1. Data Loading and Preprocessing
- Renamed columns, handled missing values
- Removed redundant or constant columns

### 2. Feature Engineering
This was the game-changer.
- **Rolling statistics** (mean, std) to capture trends
- **Lag features** to provide context over time
- **Degradation indicators** based on cycle progression

> Feature engineering alone significantly improved model performance — even without hyperparameter tuning.

### 3. Exploratory Data Analysis
- Sensor behavior over cycles
- Correlation heatmaps
- RUL distributions

### 4. Model Building
Compared multiple regression models:
- Linear Regression
- Random Forest
- XGBoost
- LightGBM
- **CatBoost** (final choice)

### 5. Evaluation
Used:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

---

##  Hyperparameter Tuning

Due to runtime constraints, full hyperparameter tuning was **not performed**.  
However, the model already demonstrated strong performance with engineered features alone.

---

##  Key Learnings

- Feature engineering is crucial for time-series problems like RUL.
- Complex models like CatBoost benefit far more from clean, informative input than hyperparameter tweaks.
- Visualizing sensor trends can guide which features to engineer.

---

##  Tech Stack

- Python (Pandas, NumPy, Scikit-Learn)
- Visualization: Matplotlib, Seaborn
- Modeling: CatBoost, XGBoost, Random Forest
- Environment: Google Colab

---

##  Future Work

- Full hyperparameter optimization
- Use of deep learning models like LSTM/GRU
- Real-time dashboard for deployment (Streamlit or Flask)


##  Connect With Me

If you found this interesting or have suggestions, feel free to reach out!  => www.linkedin.com/in/rishikajonna


