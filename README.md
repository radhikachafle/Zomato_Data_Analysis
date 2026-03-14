# 🍽️ Zomato Data Analysis

Exploratory Data Analysis (EDA) of a Zomato restaurants dataset to uncover insights about dining trends, customer preferences, online ordering behavior, and restaurant ratings.

---

## 📋 Project Overview

This project analyzes a Zomato dataset of 148 restaurants using Python. It explores restaurant types, voting patterns, rating distributions, couple spending habits, and the impact of online ordering — all visualized through charts built with Matplotlib and Seaborn.

---

## 📁 Project Structure

```
Zomato-Data-Analysis/
│
├── Zomato_Data_Analysis.ipynb      # Main Jupyter Notebook with full analysis
├── Zomato_data_.csv                # Dataset used for analysis
├── requirements.txt                # Python dependencies
└── README.md                       # Project documentation
```

---

## 📊 Dataset

**File:** `Zomato_data_.csv`

The dataset contains information about 148 restaurants with the following columns:

| Column | Description |
|---|---|
| `name` | Name of the restaurant |
| `online_order` | Whether the restaurant accepts online orders (Yes/No) |
| `book_table` | Whether table booking is available (Yes/No) |
| `rate` | Customer rating (out of 5) |
| `votes` | Number of votes received |
| `approx_cost(for two people)` | Approximate dining cost for two people (₹) |
| `listed_in(type)` | Type/category of restaurant (Buffet, Cafes, Dining, Other) |

---

## 🔍 Analysis Performed

- **Data Loading & Preview** — Loading CSV and inspecting the dataset structure
- **Data Cleaning** — Converting the `rate` column from `"4.1/5"` string format to a numeric float using a custom function
- **Restaurant Type Distribution** — Count plot showing the spread across Buffet, Cafes, Dining, and Other
- **Votes by Restaurant Type** — Line plot of total votes grouped by restaurant category
- **Rating Distribution** — Histogram showing the frequency of ratings across all restaurants
- **Couple Spending Analysis** — Count plot of approximate cost for two people
- **Online vs Offline Order Ratings** — Box plot comparing ratings between online and offline ordering modes
- **Heatmap Analysis** — Pivot table heatmap of restaurant type vs online order availability

---

## 📈 Key Insights

- **Dining** is the most common restaurant category in the dataset.
- **Dining restaurants** received the maximum number of votes from customers.
- Most restaurants received ratings between **3.5 and 4.0**.
- The majority of couples prefer restaurants with an approximate cost of **₹300**.
- Restaurants accepting **online orders** received higher ratings compared to offline-only ones.
- The heatmap shows that **dining restaurants** predominantly serve offline customers (77 vs 33).

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical operations
- **Matplotlib** — Static visualizations
- **Seaborn** — Statistical data visualization
- **Jupyter Notebook** — Development environment

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Zomato-Data-Analysis.git
cd Zomato-Data-Analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch the notebook

```bash
jupyter notebook Zomato_Data_Analysis.ipynb
```

> **Note:** If running on Google Colab, upload `Zomato_data_.csv` to `/content/` and run all cells directly.

---

## ⚠️ Known Issue

The last cell uses `cmap="ReGnBu"` in the heatmap, which is not a valid Matplotlib colormap and will throw a `KeyError`. Fix it by replacing with a valid colormap:

```python
# Change this:
sns.heatmap(pivot_table, annot=True, cmap="ReGnBu", fmt='d')

# To this:
sns.heatmap(pivot_table, annot=True, cmap="YlGnBu", fmt='d')
```

---

## ☁️ Run on Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

Upload both `Zomato_Data_Analysis.ipynb` and `Zomato_data_.csv` to your Colab session and run all cells.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements, additional analyses, or bug fixes.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
