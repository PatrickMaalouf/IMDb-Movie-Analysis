# Exploratory Data Analysis of IMDb Movie Data

## 🎯 Project Objective
The goal of this project is to act as a data analyst for a film studio by analyzing the IMDb movie dataset. The analysis aims to uncover trends and insights within the film industry by answering key questions about movie profitability, genre popularity, runtime distributions, and the correlation between budget and revenue.

---

## 📊 Dataset
This analysis uses the **"IMDb movies extensive dataset"** sourced from Kaggle. The dataset contains information on over 85,000 movies, including details on genre, runtime, budget, worldwide gross income, user ratings, and directors.

---

## 🧹 Data Cleaning and Preparation
Before analysis, the raw data required several cleaning and preparation steps:
* **Handling Missing Values**: Rows with missing `budget` or `worlwide_gross_income` data were removed to ensure the accuracy of financial calculations.
* **Correcting Data Types**: The `budget` and `worlwide_gross_income` columns, which were originally formatted as strings with various currency symbols (e.g., `$`, `NOK`), were cleaned using regular expressions to strip all non-numeric characters. They were then converted to a numeric data type.
* **Feature Engineering**: A `profit_usd` column was created by subtracting the cleaned budget from the cleaned worldwide gross income to facilitate profitability analysis.

---

## 📈 Analysis & Key Findings

The analysis was guided by several key questions, with the following findings:

#### 1. What are the top 10 most profitable movies?
The analysis identified the most profitable films, which are typically large-scale, global blockbusters.

![Bar chart of the top 10 most profitable movies](charts/profit_barchart.png)

#### 2. Is there a correlation between a movie's budget and its income?
A clear **positive correlation** exists between a movie's budget and its worldwide gross income. After filtering out extreme data outliers, the trend shows that movies with higher budgets generally achieve higher gross incomes.

![Scatter plot showing budget vs. income](charts/budget_vs_income_scatter.png)

#### 3. How has the popularity of different genres changed over the decades?
The popularity of major genres has shifted significantly over time. The line chart below illustrates a notable rise in the production of **Action**, **Adventure**, and **Sci-Fi** films in recent decades.

![Line chart showing genre trends over decades](charts/genre_trends_linechart.png)

#### 4. Who are the top directors by average movie rating?
To ensure a fair comparison, the analysis filtered for directors with a significant body of work (10+ films). The top directors by average user rating are established figures known for critically acclaimed work. For example, the analysis identified figures like **Frank Darabont** and **Christopher Nolan** among the top-rated directors.

#### 5. What is the distribution of movie runtimes?
The distribution of movie runtimes is concentrated around the **95-120 minute mark**, which represents the most common length for a feature film. The histogram shows a right skew, indicating that very long movies are less common.

![Histogram of movie runtime distribution](charts/runtime_histogram.png)

---

## 🛠️ Tools Used
* **Programming Language**: Python
* **Libraries**:
    * **Pandas**: For data manipulation, cleaning, and analysis.
    * **Matplotlib & Seaborn**: For data visualization and creating charts.
    * **Re**: For cleaning text data using regular expressions.
* **Environment**: Jupyter Notebook (via Google Colab).
