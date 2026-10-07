# 🎬 Netflix Case Study: Exploratory Data Analysis

An exploratory data analysis (EDA) of Netflix's catalogue of Movies and TV Shows. The goal is to find patterns in the content library and turn them into business insights: **what type of content to produce and how Netflix can grow in different countries.**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📌 Problem Statement

Netflix is one of the world's leading streaming platforms with thousands of Movies and TV Shows. Using the catalogue data, this case study answers questions such as:

- What is the split between Movies and TV Shows?
- Which countries produce the most content?
- Which genres are the most popular?
- Which directors and actors appear most often?
- How has content production changed over the years?
- When is the best time to launch new content?
- What kind of content should Netflix focus on in each market?

---

## 🗂️ Dataset

The data is in `netflix_titles.csv`.

| Column | Description |
|---|---|
| `show_id` | Unique ID of each title |
| `type` | Movie or TV Show |
| `title` | Title of the content |
| `director` | Director(s) of the content |
| `cast` | Actors involved |
| `country` | Country or countries where it was produced |
| `date_added` | Date it was added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating (TV-MA, PG-13, etc.) |
| `duration` | Duration in minutes (Movies) or number of seasons (TV Shows) |
| `listed_in` | Genre(s) / category |
| `description` | Short summary of the content |

---

## 🔬 Analysis Workflow

1. **Data exploration**: shape, data types and basic statistics
2. **Data cleaning**
   - Missing value detection and treatment
   - Converting `date_added` to datetime
   - Un-nesting columns with multiple values (director, cast, country, genre)
   - Removing duplicates
3. **Univariate analysis**: Movies vs TV Shows, ratings, genres, countries
4. **Bivariate analysis**: content type vs country, genre vs year, release trends
5. **Insights and recommendations**: what to produce, where, and when

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data handling | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

---

## 📁 Project Structure

```
Netflix-Case-Study/
├── netflixCaseStudy.ipynb          # Main case study analysis
├── NetflixIntroduction (1).ipynb   # Introductory notebook
├── netflix_titles.csv              # Dataset
└── README.md
```

---

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/muzzammil03/Netflix-Case-Study.git
cd Netflix-Case-Study
```

**2. Install dependencies**

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

**3. Launch the notebook**

```bash
jupyter notebook netflixCaseStudy.ipynb
```

Run the cells from top to bottom. Make sure `netflix_titles.csv` is in the same folder as the notebook.

---

## 💡 Key Insights

> Add your own findings here after checking the notebook. Examples:

- Movies vs TV Shows: which type dominates the catalogue
- Top countries and genres by number of titles
- Year-wise growth in content added
- Best months or periods to release new content
- Recommendations for different markets

---

## 🔭 Future Improvements

- Add an interactive dashboard (Streamlit or Power BI)
- Build a content-based recommendation system using `description` and `listed_in`
- Apply NLP on descriptions for topic analysis

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 👤 Author

**Muzzammil**
GitHub: [@muzzammil03](https://github.com/muzzammil03)

---

⭐ If you found this project useful, please give it a star!
