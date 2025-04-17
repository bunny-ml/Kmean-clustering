# 🛍️ Customer Segmentation using K-Means Clustering

This project applies **K-Means Clustering** on customer transaction data to segment users into actionable groups using **RFM analysis** (Recency, Frequency, Monetary). The primary goal is to understand and optimize marketing strategies for each customer group based on purchasing behavior.

## 📁 Dataset

* **Source**: [UCI Machine Learning Repository – Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
* **Size**: 525,461 rows × 8 columns
* **Duration**: 01-Dec-2009 to 09-Dec-2011
* **Country**: Primarily United Kingdom with some international data.

## 📊 Dataset Information

The dataset contains the following columns:

|   | **Column Name** | **Description** | **Data Type** |
| :-- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------ |
|   | Invoice           | Invoice number. Nominal, a 6-digit integral number uniquely assigning each transaction. If this code starts with letter 'c', it indicates a cancellation.                       | Object            |
|   | StockCode         | Product (item) code. Nominal, a 5-digit integral number uniquely assigning each distinct product.                                                                             | Object            |
|   | Description       | Product (item) name. Nominal.                                                                                                                                               | Object            |
|   | Quantity          | The quantities of each product (item) per transaction. Numeric.                                                                                                               | Int64             |
|   | InvoiceDate       | Invoice Date and time. Numeric, the day and time when each transaction was generated.                                                                                         | Datetime64\[ns\]    |
|   | Price             | Unit price. Numeric, Product price per unit in sterling.                                                                                                                      | Float64           |
|   | Customer ID       | Customer number. Nominal, a 5-digit integral number uniquely assigning each customer.                                                                                         | Float64           |
|   | Country           | Country name. Nominal, the country where each customer resides.                                                                                                               | Object            |

## 📊 Customer Segments

The following customer segments were identified using K-Means clustering based on RFM features:

| **Cluster** | **Segment Name** | **Description** |
| :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------- |
| 0           | **RETAIN** | Customers who purchase regularly but spend a moderate amount. They're important to retain with consistent service. |
| 1           | **REWARD** | Loyal, high-frequency, and high-spending customers. They are the most valuable and should be rewarded with loyalty perks. |
| 2           | **RE-ENGAGE** | Previously active customers who haven't purchased in a while. Marketing campaigns should aim to re-engage them.     |
| 3           | **NURTURE** | New or low-frequency buyers. Potential to grow into loyal customers through nurturing and onboarding.           |
| -1          | **PAMPER** | Low-frequency customers who make high-value purchases. They respond well to personalized, high-touch offers.         |
| -2          | **UPSELL** | Customers who purchase frequently but spend less. Potential to introduce them to premium offerings.               |
| -3          | **DELIGHT** | Ideal customers with recent, frequent, and high-value purchases. Top tier – delight them to ensure long-term loyalty.         |

## 🛠️ Tech Stack

* Python
* Pandas
* Scikit-learn
* Seaborn
* Matplotlib
* Jupyter Notebook

## 📦 Requirements

Install the required libraries using:

pip
