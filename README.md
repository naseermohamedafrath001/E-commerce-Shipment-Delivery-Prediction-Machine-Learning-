# Orderrr: E-commerce Shipment Delivery Prediction

Predicting shipment delivery delays is a critical challenge in e-commerce logistics. This project utilizes machine learning to classify whether a shipment will reach its destination on time based on various logistical and customer tracking parameters.

## 🚀 Project Overview
The "Orderrr" system leverages historical tracking data to provide actionable insights for logistics management. By predicting potential delays, businesses can proactively manage customer expectations and optimize their supply chain operations.

## 👥 Contributors
- **Anshath Ahamed**
- **Mohamed Naseer Mohamed Afrtath**

## 📊 Dataset Analysis
The dataset contains over 11,000 shipment records with features including:
- **Warehouse Block:** Location of storage.
- **Mode of Shipment:** Flight, Ship, or Road.
- **Customer Care Calls:** Number of inquiries made by the customer.
- **Customer Rating:** Feedback from the customer.
- **Cost of the Product:** Value of the shipment.
- **Prior Purchases:** Customer loyalty metrics.
- **Product Importance:** Low, medium, or high priority.
- **Discount Offered:** Promotional intensity.
- **Weight in Gms:** Physical weight of the product.
- **Target Variable:** `Reached.on.Time_Y.N` (1 = Late, 0 = On Time).

## 🛠️ Technical Workflow
1. **Data Preprocessing:**
   - Handled non-standard missing values.
   - Standardized numerical features using `StandardScaler`.
   - Performed **One-Hot Encoding** on categorical features (Warehouse, Shipment Mode, Gender, Importance).
2. **Feature Engineering:**
   - Engineered a custom `High_Discount` feature to capture the correlation between high promotional offers and logistics bottlenecks.
3. **Machine Learning Models:**
   - Evaluated multiple classification algorithms:
     - **Logistic Regression**
     - **Decision Tree Classifier**
     - **Random Forest Classifier**
     - **Support Vector Machine (SVM)**
4. **Model Performance:**
   - Used an 80/20 hold-out split for training and validation.
   - Evaluated models using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

## 🏆 Key Results
| Model | Accuracy | Precision | ROC-AUC |
| :--- | :--- | :--- | :--- |
| **Random Forest** | **67.1%** | 77.7% | **0.738** |
| **SVM** | 66.6% | **85.6%** | 0.737 |
| **Logistic Regression** | 64.6% | 71.9% | 0.723 |
| **Decision Tree** | 63.8% | 69.4% | 0.622 |

- **Top Performer:** The **Random Forest** model provided the most reliable overall predictions with the highest accuracy and area under the curve.
- **Business Insight:** The **SVM** model achieved high **Precision (85.6%)**, making it a powerful tool for minimizing false delivery promises.

## 📂 Project Structure
- `Supervised.ipynb`: Main Jupyter Notebook containing data analysis, visualization, and model training.
- `Train.csv`: Original dataset.
- `Preprocessed_Delivery.csv`: Cleaned and standardized dataset ready for production.

---
*Created for the purpose of demonstrating advanced data science and machine learning capabilities in logistics.*
