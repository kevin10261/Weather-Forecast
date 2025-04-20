# Weather Forecast Model

## Overview
This Jupyter Notebook implements a complete workflow for forecasting daily temperatures in Edmonton using historical weather data and machine learning techniques. It covers data cleaning, preprocessing, feature engineering, modeling with multiple algorithms, and evaluation through visualization and cross-validation.

## Repository Structure
```
├── Weather_Forecast_Model.ipynb  # Main notebook
└── data/
    └── city_temperature.csv       # Raw dataset file (place here)
```

## Getting Started
### Prerequisites
- Python 3.8 or higher
- Virtual environment tool (optional but recommended)

### Installation
1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd <repo-directory>
   ```
2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate    # Windows
   ```
3. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Data Preparation
1. **Download the dataset**: Go to the Kaggle page at https://www.kaggle.com/datasets/sudalairajkumar/daily-temperature-of-major-cities, sign in, accept the terms, and download the CSV file.
   - Rename the downloaded file (e.g. `daily_temperature.csv`) to **`city_temperature.csv`**.
2. **Organize data directory**:
   ```bash
   mkdir -p data
   mv path/to/city_temperature.csv data/
   ```
3. **Load data in notebook**:
   The notebook reads the file with:
   ```python
   pd.read_csv('data/city_temperature.csv')
   ```

## Notebook Outline
The notebook is organized into the following sections:

1. **Introduction**
   - Overview of the forecasting problem and dataset description.

2. **Missing Value Imputation**
   - Strategies to identify and fill missing temperature entries.

3. **Outlier Detection and Treatment**
   - Methods to detect anomalous temperature readings and handle them.

4. **Resampling to Different Time Frequencies**
   - Aggregating daily data into weekly/monthly averages.

5. **Feature Engineering**
   - Creation of temporal features such as day of year, rolling statistics, etc.
   - **Temporal Features** subtitled section.

6. **Modeling Framework**
   - **Data Split**: Train/test split respecting time ordering.
   - **Linear Regression Model**
   - **Random Forest Model**
   - **XGBoost Model**
   - **Cross Validation for Time Series Forecasting**

7. **Analysis and Visualization**
   - **Historical Data and Predictions**: Plots for each model (Linear Regression, Random Forest, XGBoost, Time Series CV).
   - **Feature Importance**: Visualization of top predictors.
   - **Error Metrics Over Time**: Tracking model performance across the test period.

## Usage
1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook Weather_Forecast_Model.ipynb
   ```
2. Run all cells sequentially to reproduce data processing, model training, and results.
3. Inspect plots and performance metrics generated in the **Analysis and Visualization** section.

## Results
- Model performance metrics (MAE, RMSE) and visual comparisons are displayed inline.
- Feature importance charts highlight the most predictive variables for temperature forecasting.

## Contributing
Contributions and improvements are welcome:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`
3. Commit your changes and push: `git push origin feature/YourFeature`
4. Open a Pull Request.

## License
This project is released under the MIT License. See [LICENSE](LICENSE) for details.

## Contact
For questions or feedback, please reach out to:
- **Seongeun Yu**
- Email: kyyse1026@gmail.com
- GitHub: https://github.com/kevin10261

