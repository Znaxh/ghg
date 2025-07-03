# GHG Emissions Prediction App

A Streamlit web application for predicting Supply Chain Emission Factors with Margins based on various data quality metrics and environmental parameters.

## 🌍 Overview

This project provides a machine learning-powered tool to predict greenhouse gas (GHG) emissions in supply chains. The application uses a Linear Regression model trained on supply chain emission data to help organizations estimate their environmental impact.

## 🚀 Features

- **Interactive Web Interface**: Built with Streamlit for easy use
- **Multiple GHG Types**: Supports prediction for carbon dioxide, methane, nitrous oxide, and other GHGs
- **Data Quality Assessment**: Incorporates reliability, temporal, geographical, technological, and data collection quality scores
- **Real-time Predictions**: Instant emission factor predictions based on input parameters
- **Pre-trained Model**: Uses a trained Linear Regression model with data scaling

## 📁 Project Structure

```
ghg/
├── app.py                          # Main Streamlit application
├── GHG_Emissions_Prediction.ipynb  # Jupyter notebook for model development
├── SupplyChainEmissionFactorsforUSIndustriesCommodities.xlsx  # Dataset
├── models/
│   ├── LR_model.pkl                # Trained Linear Regression model
│   └── scaler.pkl                  # Data scaler for preprocessing
└── utils/
    ├── __init__.py
    └── preprocessor.py             # Data preprocessing utilities
```

## 🛠️ Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Znaxh/ghg.git
   cd ghg
   ```

2. **Install required dependencies**:
   ```bash
   pip install streamlit pandas numpy scikit-learn joblib
   ```

## 🏃‍♂️ Usage

1. **Run the Streamlit app**:
   ```bash
   streamlit run app.py
   ```

2. **Open your browser** and navigate to the provided local URL (typically `http://localhost:8501`)

3. **Input parameters**:
   - **Substance**: Select the type of GHG (carbon dioxide, methane, nitrous oxide, other GHGs)
   - **Unit**: Choose the measurement unit
   - **Source**: Select between Commodity or Industry
   - **Supply Chain Emission Factors without Margins**: Enter the base emission factor
   - **Margins of Supply Chain Emission Factors**: Enter the margin value
   - **Data Quality Scores**: Adjust sliders for various DQ metrics (0.0 to 1.0):
     - Reliability Score
     - Temporal Correlation
     - Geographical Correlation
     - Technological Correlation
     - Data Collection

4. **Get Predictions**: Click "Predict" to get the estimated Supply Chain Emission Factor with Margin

## 📊 Model Information

- **Algorithm**: Linear Regression
- **Features**: Substance type, unit, source, emission factors, margins, and 5 data quality metrics
- **Preprocessing**: Categorical encoding and feature scaling
- **Output**: Predicted Supply Chain Emission Factor with Margin

## 📈 Data Quality Metrics

The model incorporates five key data quality dimensions:

1. **Reliability Score**: Measures the reliability of the underlying data
2. **Temporal Correlation**: Assesses how well the data represents the time period of interest
3. **Geographical Correlation**: Evaluates geographical representativeness
4. **Technological Correlation**: Measures technological representativeness
5. **Data Collection**: Assesses the quality of data collection methods

## 🔧 Development

The project includes a Jupyter notebook (`GHG_Emissions_Prediction.ipynb`) for model development and experimentation. The trained model and scaler are saved as pickle files in the `models/` directory.

## 📝 Requirements

- Python 3.7+
- Streamlit
- Pandas
- NumPy
- Scikit-learn
- Joblib

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for any improvements or bug fixes.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**Note**: This application is designed for educational and research purposes. For production use, please ensure proper validation and testing of the model with your specific data.
