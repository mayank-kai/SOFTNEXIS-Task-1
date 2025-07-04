# SOFTNEXIS-Task-1
Data Cleaning & and Preprocessing

# 🧼 1000 Supermarket Sales — Data Cleaning & Preprocessing

This project involves cleaning and preprocessing the `1000-Supermarket-Sales.csv` dataset to prepare it for downstream analysis or machine learning tasks. The dataset contains transaction-level sales data from a fictional supermarket chain.

---
![Image](https://github.com/user-attachments/assets/bdb8cb16-49c5-4b49-b6ba-4945fe466a35)
## 📁 Dataset Overview

**Filename**: `1000-Supermarket-Sales.csv`

**Columns** may include (based on version):

- `Invoice ID`
- `Branch`
- `City`
- `Customer type`
- `Gender`
- `Product line`
- `Unit price`
- `Quantity`
- `Tax 5%`
- `Total`
- `Date`
- `Time`
- `Payment`
- `COGS`
- `Gross margin percentage`
- `Gross income`
- `Rating`

---

## 🛠️ Tasks Performed

### ✔️ Step-by-Step Data Cleaning

1. **Load the data** using `pandas`
2. **Standardize column names**
3. **Convert columns** to appropriate data types:
   - `Date` → `datetime`
   - `Time` → `datetime.time` + extracted `hour`
   - Numeric fields → converted using `pd.to_numeric`
4. **Handle missing values**
   - Checked for `NaN` entries
   - Applied conditional filling (if required)
5. **Standardize categorical text**
   - Stripped and title-cased values in `Gender`, `City`, `Product Line`
6. **Feature Engineering**
   - Extracted `Month`, `Day of Week`, `Hour`
   - Created `Is_Weekend` flag
   - Calculated `Gross Margin` (`Gross Income / Total`)
7. **Remove duplicate entries**
8. **Export the cleaned dataset** as `cleaned_1000_supermarket_sales.csv`

---

## 📊  Visualization

```python
# Total sales by city
df.groupby('city')['total'].sum().plot(kind='bar', title='Total Sales by City')


💾 Output
The final cleaned dataset is saved as:
cleaned_1000_supermarket_sales.csv

🧰 Requirements
Make sure you have the following Python libraries installed:
pip install pandas matplotlib

📌 How to Run
Clone this repo or download the script.

Place 1000-Supermarket-Sales.csv in the same directory.

Run the Python script:
python clean_supermarket_sales.py




