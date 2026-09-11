# Movie Industry Exploratory Data Analysis (EDA)

## 📌 Overview
An exploratory data analysis of the **TMDB 5000 Movies Dataset** to understand what drives movie success—comparing **financial success (revenue)** against **critical/audience success (rating)**.

The analysis investigates whether high-rated movies also generate high revenue, and identifies the factors most strongly associated with box office performance.

---

## 🎯 Objectives
- Determine whether **high ratings** correlate with **high revenue**
- Identify the strongest predictors of financial success
- Analyze how **genre**, **budget**, **runtime**, and **release year** influence outcomes
- Visualize relationships using scatter plots, heatmaps, and time-series charts
- Summarize actionable insights from the data

---

## 📂 Dataset
**TMDB 5000 Movies Dataset** (Kaggle)
- `movies.csv` — movie metadata (budget, revenue, genres, ratings, etc.)
- `credits.csv` — cast and crew information

> Download both files and place them in the project root directory before running the notebook.

---

## 🛠️ Tech Stack & Skills
| Category | Tools / Skills |
|----------|----------------|
| Language | Python 3.x |
| Libraries | Pandas, NumPy, Matplotlib, Seaborn |
| Techniques | Data cleaning, JSON parsing, missing value handling, correlation analysis |
| Deliverable | Jupyter Notebook with visualizations + written findings |

---

## 📁 Project Structure
movie-industry-eda/
│
├── data/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── movie_eda.ipynb          # Main analysis notebook
├── README.md                # Project documentation
└── requirements.txt         # Dependencies

---

## 🔧 Setup & Installation
1. Clone The Repo
```bash
git clone https://github.com/your-username/movie-industry-eda.git
cd movie-industry-eda
```

2. Create a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook
```bash
jupyter notebook EDA.ipynb
```

---

## 🧹 Data Cleaning Steps

<ul>
<li>Merged movies and credits datasets on title</li>
<liParsed JSON columns: genres, keywords, production_companies, production_countries, spoken_languages, cast, crew</li>
<li>Extracted director name from crew JSON</li>
<li>Replaced 0 values in budget and revenue with NaN (indicates missing data)</li>
<li>Dropped rows missing critical fields (budget, revenue, vote_average)</li>
<li>Derived new features: profit, profit_margin, release_year</li>
</ul>

---

## 📊 Visualizations Included

<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>Visualization</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Scatter plot: Revenue vs. Rating</td>
      <td>Test correlation between acclaim and earnings</td>
    </tr>
    <tr>
      <td>Scatter plot: Budget vs. Revenue</td>
      <td>Assess budget as a revenue predictor</td>
    </tr>
    <tr>
      <td>Correlation Heatmap</td>
      <td>Compare all numeric features at once</td>
    </tr>
    <tr>
      <td>Bar chart: Median Revenue by Genre</td>
      <td>Identify high-earning genres</td>
    </tr>
    <tr>
      <td>Line chart: Average Rating Over Time</td>
      <td>Track rating trends across decades</td>
    </tr>
  </tbody>
</table>

---

## 🔍 Key Findings

<ul>
<li>Revenue ≠ Rating — Weak correlation (~0.03) between vote_average and revenue. Highly rated films are not necessarily profitable.</li>
<li>Budget is the strongest predictor of revenue, showing a strong positive correlation.</li>
<li>Genre influences revenue — Adventure, Action, and Animation genres yield the highest median revenues.</li>
<li>Ratings have declined over time — A steady downward trend since the mid-20th century, likely due to changing audience behavior rather than film quality.</li>
<li>Data limitations — Zero values in budget/revenue were treated as missing; ratings are subjective and influenced by community dynamics.</li>
</ul>

---

## 🚀 Future Work
<ul>
<li>Build a regression model to predict revenue using budget, runtime, popularity, and vote average</li>
<li>Perform sentiment analysis on movie overviews or reviews</li>
<li>Include cast popularity and director track record as features</li>
<li>Extend to time-series forecasting of box office trends</li>
</ul>

---
## 🙏 Acknowledgments
Dataset: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata