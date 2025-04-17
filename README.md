# 🛍️ Customer Segmentation using K-Means Clustering

This project applies **K-Means Clustering** on customer transaction data to segment users into actionable groups using **RFM analysis** (Recency, Frequency, Monetary). The primary goal is to understand and optimize marketing strategies for each customer group based on purchasing behavior.

---

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository – Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Size**: 525,461 rows × 8 columns  
- **Duration**: 01-Dec-2009 to 09-Dec-2011
- **Country**: Primarily United Kingdom with some international data.

### 📊 Dataset Info

```plaintext
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 525461 entries, 0 to 525460
Data columns (total 8 columns):
 #   Column       Non-Null Count   Dtype         
---  ------       --------------   -----         
 0   Invoice      525461 non-null  object        
 1   StockCode    525461 non-null  object        
 2   Description  522533 non-null  object        
 3   Quantity     525461 non-null  int64         
 4   InvoiceDate  525461 non-null  datetime64[ns]
 5   Price        525461 non-null  float64       
 6   Customer ID  417534 non-null  float64       
 7   Country      525461 non-null  object        
## 📊 Customer Segments
---
The following customer segments were identified using K-Means clustering based on RFM features:

| Cluster | Segment Name | Description |
|---------|--------------|-------------|
| 0       | **RETAIN**   | Customers who purchase regularly but spend a moderate amount. They're important to retain with consistent service. |
| 1       | **REWARD**   | Loyal, high-frequency and high-spending customers. They are the most valuable and should be rewarded with loyalty perks. |
| 2       | **RE-ENGAGE**| Previously active customers who haven't purchased in a while. Marketing campaigns should aim to re-engage them. |
| 3       | **NURTURE**  | New or low-frequency buyers. Potential to grow into loyal customers through nurturing and onboarding. |
| -1      | **PAMPER**   | Low-frequency customers who make high-value purchases. They respond well to personalized, high-touch offers. |
| -2      | **UPSELL**   | Customers who purchase frequently but spend less. Potential to introduce them to premium offerings. |
| -3      | **DELIGHT**  | Ideal customers with recent, frequent, and high-value purchases. Top tier – delight them to ensure long-term loyalty. |

---

## 🛠️ Tech Stack

- Python
- Pandas
- Scikit-learn
- Seaborn
- Matplotlib
- Jupyter Notebook

---

## 📦 Requirements

Install the required libraries using:

```bash
pip install -r requirements.txt
