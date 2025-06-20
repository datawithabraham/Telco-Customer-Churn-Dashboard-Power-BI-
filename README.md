# Telco-Customer-Churn-Dashboard-Power-BI-
This project simulates churn analysis for a fictional telecom company called Vertex Mobile using Power BI.



## Problem Statement

This project aimed to discover the rate at which customers of a Telcom company (Vertex Mobile) 
were switching to other networks and offers, and or abandoning the use of the Telcom services 
completely.
Since it is difficult and expensive to acquire a new customer, especially in the Telecommunications 
space, it is necessary to dive deep into available data and observe patterns of customer exits. 
This can help in several ways to help the company develop and implement strategies capable of 
maintaining existing customers.The dashboard answers questions such as:

- Which customer segments are churning the most?
- How does churn vary by contract type, payment method, or age group?
- What patterns exist across customer tenure or account length?

---

## 🛠️ Tools Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Simulated telecom dataset (CSV)**
- GitHub for project version control and sharing

---
## Data Preparation
The dataset was acquired from Only Quality Data for educational purposes only.
The data contains 30 columns and 1687 rows.
Reliability checks were made to ensure if dataset available can be able to answer the business question.
The data was cleaned in Power Bi to standardize the data and also eliminate duplicates. 
The 'Keep duplicates' function was used on the primary key; the custumer_Id column to determine if there were any duplicates. There were no duplicates found.
Duplicates were found in the phone_number column. Since a customer is supposed to acquire a single phone number, the duplicates were removed in order not to skew the distribution. 
The 'keep rows' > 'keep duplicates' function was used to filter duplicated phone numbers after which 
'remove rows' > 'remove duplicates' function was used to clear the duplicated phone numbers
The cleaned dataset was renamed **Vertex_Cleaned** 

### Snapshot of Table
![Image](https://github.com/user-attachments/assets/0ea27658-3ffd-4773-af13-23086fc3a4f3)

## Analytics
Measures were created in Power Bi to calculate sums and averages
           
           Total no of Customers = Total Customers = CALCULATE(COUNTROWS(Vertex_Cleaned))

![Image](https://github.com/user-attachments/assets/f8fa1b43-501c-469e-a4c4-6797d7cfcc09)

           Churned_Customers = CALCULATE(COUNTROWS(Vertex_Cleaned),
           FILTER(Vertex_Cleaned, Vertex_Cleaned[churn_label] = "yes"))

![Image](https://github.com/user-attachments/assets/f8fa1b43-501c-469e-a4c4-6797d7cfcc09)

Further measures were created to arrive at visualizations that answer the business question.

## Snapshot of Dashboard

![Image](https://github.com/user-attachments/assets/6d302eda-1e3d-4489-abd3-be1a6cca513e)

## Key Dashboard Features

- **KPI Card**: Displays total number of customers (6.68K)
- **KPI Card**: Displays the total number of churned customers
- **Churn Analysis by**:
  - Contract type (Month-to-Month, One Year, Two Year)
  - Age group, Gender, and Unlimited Plan
  - Account length in months
  - Payment method (Paper Check, Direct Debit, Credit Card)
- **Group vs Non-Group Customers** churn comparison
- **Intl Plan vs Churn** breakdown table
- **Dynamic Slicers**:
  - Gender, Age Group, and U.S. State

---

## 📁 Repository Contents

| File / Folder | Description |
|---------------|-------------|
| `Vertex_Churn_Analysis.pbix` | Main Power BI dashboard file |
| `churn_data.csv` | Simulated and anonymized dataset |
| `screenshots/` | Contains dashboard preview images |
| `README.md` | Documentation for the project |
| `insights.md` | Summary of findings and actionable recommendations (optional) |


---

## Insights
- Our analysis reveals that month- month contract holders represents the most significant churn 
risk. This asserts that new customers are more susceptible to leaving within initial months of sign 
up on the company. This is a critical churn accelerator in the analysis.
           
           Month-to-month contract holders churned at 46.7%, One Year at 11.31%, and Two Year contract holders at 2.97%.
  
- The second highest risk of churn lies within the 65 – 85 age range. This age group churned the most but the highest number of churned customers lie between the 30 - 44 age range. This insight could possibly be the death of such customers due to their age. This represents a variable that may not be able to 
be controlled for.
           
           Age range 65-85 churned the most at 38.1% but age range 30 - 44
          has the highest number of customer churns 1762 customers churning in that range.
  
- It also appears that customers who are active internationally churn more. Especially those who are signed on in international offer but are not active internationally (71%) followed by customers who are not on international plan and are internationally active (40%). This is a rather puzzling metric.

           
            ![image](https://github.com/user-attachments/assets/81b8e5dc-3394-4fe0-935a-e323bd48ce4c)


- **Month-to-Month contracts** show the highest churn rate (~40%)
- Customers with **Unlimited Plan = No** churn significantly more (66.54%)
- **Senior citizens (65+)** churn at higher rates than younger groups
- Customers using **Paper Check** are more likely to churn compared to those using Direct Debit or Credit Card
- Customers **with international plans** also exhibit higher churn

---


## 👤 About the Author

**Abraham Tetteh**  
Data Analyst | Power BI Developer | Background in Psychology & Information Studies  
📍 Ghana  
📧 [tettehabraham590@gmail.com]  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/abraham-tetteh-b03057350/)

---

> 🚨 *Disclaimer: This project is for educational purposes only. The dataset used is fictional or anonymized and does not represent real customer information.*


