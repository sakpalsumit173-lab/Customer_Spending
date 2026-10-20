# ShopSmart 🛒
### Customer Spending Prediction

ShopSmart is a machine learning web application that predicts how much a customer is likely to spend based on their demographic information, income, shopping activity, membership type, and shopping preferences.

The application is built with **Python, Pandas, Scikit-learn, and Streamlit** and provides an interactive interface for entering customer details and viewing predicted spending in Indian rupees (₹).

## ✨ Features

- **Customer input:** Enter age, annual income, website visits, and previous purchases.
- **Membership selection:** Select the customer's membership type.
- **Shopping preferences:** Choose a preferred product category.
- **Location information:** Select the customer's city tier.
- **Discount information:** Specify whether the customer used a discount.
- **Spending prediction:** Generate a predicted spending amount using a trained machine learning pipeline.
- **Interactive interface:** Use the Streamlit web application to obtain predictions without manually running model inference code.

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Streamlit
- Pickle for loading the saved model pipeline

## 📁 Project Structure

```text
ShopSmart/
├── app(1).py
├── best_model_pipeline.pkl
├── cleaned_data.csv
├── ShopSmart_data.csv
├── EDA.ipynb
├── logo.png
├── requirements(1).txt
└── README.md
```

| File | Description |
|---|---|
| `app(1).py` | Streamlit application for customer spending prediction |
| `best_model_pipeline.pkl` | Serialized, trained machine learning pipeline |
| `cleaned_data.csv` | Cleaned dataset used to populate the application's selection options |
| `ShopSmart_data.csv` | Dataset containing customer attributes and spending amounts |
| `EDA.ipynb` | Notebook for exploratory data analysis and machine learning preparation |
| `logo.png` | Application logo |
| `requirements(1).txt` | Python package dependencies |
| `README.md` | Project documentation |

## 📊 Dataset

The provided datasets contain 2,000 customer records. The customer attributes and prediction target are:

| Column | Description |
|---|---|
| `Age` | Customer's age |
| `Annual_Income` | Customer's annual income |
| `Website_Visits` | Number of website visits |
| `Previous_Purchases` | Number of previous purchases |
| `Membership_Type` | Customer membership category |
| `Preferred_Category` | Preferred shopping category |
| `City_Tier` | Customer's city tier |
| `Discount_Used` | Indicates whether a discount was used |
| `Amount_Spent` | Customer spending amount and prediction target |

The prediction interface uses the first eight attributes to estimate `Amount_Spent`.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd ShopSmart
```

Replace `<your-repository-url>` with your GitHub repository URL.

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it using the command for your operating system.

**Windows:**

```bash
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r "requirements(1).txt"
```

### 4. Run the application

```bash
streamlit run "app(1).py"
```

Streamlit will display a local URL in the terminal. Open that URL in your browser to use the application.

**Important:** Keep `best_model_pipeline.pkl`, `cleaned_data.csv`, and `logo.png` in the expected locations relative to the application script. The current code loads these files using relative paths.

## 🚀 How to Use

1. Start the Streamlit application.
2. Enter the customer's age.
3. Enter their annual income.
4. Specify the number of website visits.
5. Enter the number of previous purchases.
6. Select membership type, preferred category, and city tier.
7. Indicate whether the customer used a discount.
8. Click **Predict Spend**.
9. View the predicted spending amount displayed in rupees.

## 🧠 Machine Learning Workflow

The project includes exploratory data analysis and a saved machine learning pipeline.

The application follows this prediction workflow:

1. Collect customer information through the Streamlit interface.
2. Organize the inputs into a Pandas DataFrame.
3. Pass the input data to the saved machine learning pipeline.
4. Generate a spending prediction.
5. Round the prediction to two decimal places.
6. Display the result in Indian rupees.

The saved pipeline is loaded from `best_model_pipeline.pkl`. The application's prediction code calls the pipeline's `predict()` method, so any preprocessing required by the trained pipeline is applied as part of inference.

## 📦 Dependencies

The provided requirements file includes:

```text
pandas
numpy
matplotlib
scikit-learn
seaborn
streamlit
```

## 🔮 Future Improvements

- Add model evaluation metrics such as MAE, RMSE, and R².
- Display prediction explanations and key contributing features.
- Add visualizations to help users understand customer spending patterns.
- Improve input validation and error handling.
- Deploy the application online so it can be accessed by other users.
- Add automated tests for prediction and data preprocessing.

## 🎯 Project Objective

The objective of ShopSmart is to demonstrate how machine learning can be integrated into an interactive web application to estimate customer spending from customer and shopping-related attributes.

## 📄 License

A license has not yet been specified. Add a license file if you intend to distribute or reuse the project publicly.

---

**ShopSmart — Turning customer data into spending predictions.**
