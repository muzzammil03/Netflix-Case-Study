# Netflix Content Analysis (Case Study)

Exploratory data analysis of the Netflix titles dataset to understand what kind of content Netflix hosts, where it comes from, and when it is added to the platform.

## Objective

Answer practical business questions about Netflix's catalog:

- Which countries produce the most Movies and TV Shows?
- Which month / week is the best time to release a Movie or TV Show?
- Which genres are produced the most?
- Which directors appear most often?
- How long after release does a movie get added to Netflix?

## Dataset

- File: `netflix_titles.csv`
- Size: 8,807 titles, 12 columns
- Columns: `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## Data Preparation

- Dropped rows with a missing title and reset the index.
- Wrote a helper (`splitNested`) to split comma-separated columns (`director`, `country`, `listed_in`) into one value per row using `str.split`, `pd.melt`, and merged them back on `title`.
- Converted `date_added` to datetime and engineered `year_added`, `month_added`, and `week_added`.
- Used `nunique` on titles when counting, so titles with multiple countries/genres are not double counted.

## Analysis and Key Findings

| Question | Result |
| --- | --- |
| Top Movie-producing countries | United States (2058), India (893), United Kingdom (206), Canada (122), Spain (97) |
| Top TV Show-producing countries | United States (760), United Kingdom (213), Japan (169), South Korea (158), India (79) |
| Best month for Movies | July (565), April (550), December (547) |
| Best month for TV Shows | July (254), December (250), September (246) |
| Best weeks for TV Shows | Week 27 (85), Week 31 (79), Week 24 (75) |
| Most produced genres | International Movies (2752), Dramas (2427), Comedies (1674) |
| Most frequent director | Rajiv Chilaka (19 titles), followed by Raul Campos & Jan Suter (18) and Marcus Raboy / Suhas Kadav (16) |
| Release to Netflix delay (movies, last 5 years of additions) | Median about 949 days (about 2.6 years) |

Charts included: bar charts for countries and months, a bar chart of weekly additions, a pie chart of top genres, and a boxplot of days-to-Netflix.

## Repository Structure

```
Netflix-Case-Study/
├── netflixCaseStudy.ipynb       # Main analysis notebook
├── NetflixIntroduction (1).ipynb
├── netflix_titles.csv           # Dataset
└── README.md
```

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/muzzammil03/Netflix-Case-Study.git
   cd Netflix-Case-Study
   ```
2. Install dependencies
   ```bash
   pip install numpy pandas matplotlib seaborn jupyter
   ```
3. Open the notebook
   ```bash
   jupyter notebook netflixCaseStudy.ipynb
   ```

## Notes and Limitations

- The dataset only has `release_year`, not the exact release date, so the release-to-Netflix delay is approximated using January 1 of the release year. Treat it as a rough estimate.
- "Best month/week to release" is based on when titles were added to Netflix, not on viewership or ratings.

## Future Work

- Build a content-based recommendation system using TF-IDF on `description`/`listed_in` and cosine similarity.
- Add rating and duration analysis.
- Build an interactive dashboard.

## Author

Muzzammil
[GitHub](https://github.com/muzzammil03)
