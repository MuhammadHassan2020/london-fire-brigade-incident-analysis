
# 🔥 Predicting and Analyzing Fire Incidents – London Fire Brigade (Bexley)

## 📌 Project Overview  
This project focuses on **analyzing and predicting emergency incidents** reported by the **London Fire Brigade (LFB)** in the **Borough of Bexley (2019–2022)**. Using advanced **data mining, clustering, and machine learning** techniques, the project aims to uncover trends and improve emergency resource planning through predictive modeling.  

Three key business problems were addressed:  
1. Where and when fire incidents are most likely to occur.  
2. Which fire station is most likely to respond to a new incident.  
3. Can incident types (Fire, False Alarm, Special Service) be predicted from early data?

## 🧠 Business Problem  

- **Business Problem 1 – Descriptive:**  
  Identify **hotspot wards and peak time ranges** to optimize emergency response readiness and resource planning.

- **Business Problem 2 – Predictive:**  
  Predict **which fire station ground** will respond to a new incident based on time, location, and other incident features.

- **Business Problem 3 – Predictive + Descriptive:**  
  Predict the **type of incident** and analyze the **factors contributing to fire, false alarms, and special services** for improved categorization and decision-making.

## 💥 Business Impact  
- 🚒 Supports **faster and smarter emergency response** by forecasting station dispatch responsibilities.  
- 🕔 Allows **optimized deployment** during peak hours (e.g., 5–9 PM).  
- 📊 Enables **data-driven public safety campaigns** and ward-level emergency planning.  
- 💡 Helps reduce false alarms and improve equipment/resource utilization through intelligent prediction.  


## ✅ Solution  
The project used a full data mining pipeline:

- **Descriptive Modeling**  
  - Clustering (K-Means) with PCA for trend discovery  
  - Spatial and temporal hotspot analysis

- **Predictive Modeling**  
  - Classifiers: **Random Forest**, **XGBoost**, **Logistic Regression**  
  - Balanced training using **SMOTE**  
  - Hyperparameter tuning with **GridSearchCV**  
  - Evaluation using **Stratified K-Fold CV**, accuracy, and confusion matrices

**Top Results:**
- Incident Type Prediction (Random Forest): **96.3% accuracy**  
- Fire Station Prediction (RF/XGBoost): **100% balanced accuracy**


## 🧰 Tools & Technologies Used  
- **Languages**: Python  
- **Libraries**: pandas, scikit-learn, seaborn, matplotlib, XGBoost  
- **Techniques**: K-Means, PCA, SMOTE, Random Forest, GridSearchCV  
- **Platform**: Jupyter Notebook  
- **Dataset**: London Fire Brigade (2019–2022), Bexley Borough incidents  


## 📊 Dataset Information  
- Source: **London Fire Brigade (LFB)**  
- Scope: **9,000+ records** from Bexley  
- Features:  
  - Temporal: `DateOfCall`, `HourOfCall`  
  - Spatial: `WardName`, `Latitude`, `Longitude`  
  - Operational: `PumpCount`, `PumpHours`, `Notional Cost`  
  - Labels: `IncidentGroup`, `IncidentStationGround`
## Link of the Dataset
https://drive.google.com/file/d/1c7ombS0zbwJSKBm3sVD8Jwi834xoYb__/view?usp=sharing

## 🔍 Key Analysis Steps  
✔ Metadata alignment and data type fixing  
✔ Missing value handling (geo-coordinates, times)  
✔ Outlier treatment (IQR capping)  
✔ Class imbalance correction (SMOTE)  
✔ Label encoding and standard scaling  
✔ Feature selection using PCA loadings  
✔ Descriptive clustering (K=3 and K=6)  
✔ Predictive modeling with cross-validation  

## 📈 Results Summary  
- 🔥 Fire incidents peak between **5 PM–9 PM** in Thamesmead East, Slade Green, Belvedere  
- 🧠 PCA revealed `PumpCount` and `Notional Cost` as key features  
- 🚓 Predictive modeling accurately classifies **incident types** and **station response zones**  
- 🗺️ K-Means clusters revealed **high-resource incident groups**

## 🔍 Why This Project?  
I undertook this project to apply **end-to-end data science methodologies** in a **real-world public safety domain**, combining **descriptive analytics** with **predictive power**. The challenge of optimizing emergency services with data is not only technically demanding but also socially impactful.

## 🚀 Future Work  
- 📌 Integrate real-time streaming data for live predictions  
- 🧠 Add NLP analysis from incident reports  
- 📡 Deploy models into an operational **dashboard for LFB**  
- 🌍 Expand project to other boroughs beyond Bexley  
- 📊 Use GIS for visualizing and tracking response coverage


## 📂 Repository Usage  
To run or explore this project:

```bash
git clone https://github.com/your-username/fire-incident-analysis.git
