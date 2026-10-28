# 🎬 Netflix Movie Data Analysis
### Exploratory Data Analysis with Python

A data-driven exploration of movie genres, vote-average categories, popularity scores, and release-year trends.

**Python · Pandas · NumPy · Matplotlib · Seaborn**

</div>

---

## 📌 Project Overview

This project applies **Exploratory Data Analysis (EDA)** to a movie dataset to uncover patterns in genre distribution, audience vote averages, movie popularity, and release years. The workflow includes inspecting and preparing the data, transforming selected columns, analyzing key questions, and presenting observations through visualizations.

> **Dataset note:** The notebook describes the source as Netflix movie data. This project analyzes the supplied dataset; it does not independently verify that every listed title was available on Netflix.

## 🎯 Problem Statement

The goal is to explore the dataset and answer five analytical questions:

1. **Genre distribution:** Which genre appears most frequently in the dataset?
2. **Vote-average category:** Which vote-average category has the highest number of records?
3. **Highest popularity:** Which movie has the highest popularity score, and what genre or genres does it belong to?
4. **Lowest popularity:** Which movie has the lowest popularity score, and what genre or genres does it belong to?
5. **Release-year trend:** Which year has the highest number of movie releases in the dataset?

## 🧰 Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Core analysis |
| Pandas | Data inspection, cleaning, and transformation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical and categorical charts |
| Jupyter Notebook / Google Colab | Analysis environment |

## 🗂️ Dataset Preview

The original dataset contains **9,827 rows and 9 columns**. The notebook selects relevant fields for analysis and converts the release date to a year. It also expands comma-separated genres into individual rows for genre-level analysis.

### Sample records

| Release Year | Movie Title | Popularity | Vote Count | Vote Average | Genres |
|---:|---|---:|---:|---:|---|
| 2021 | Spider-Man: No Way Home | 5083.954 | 8940 | 8.3 | Action, Adventure, Science Fiction |
| 2022 | The Batman | 3827.658 | 1151 | 8.1 | Crime, Mystery, Thriller |
| 2022 | No Exit | 2618.087 | 122 | 6.3 | Thriller |
| 2021 | Encanto | 2402.201 | 5076 | 7.7 | Animation, Comedy, Family, Fantasy |
| 2021 | The King's Man | 1895.511 | 1793 | 7.0 | Action, Adventure, Thriller, War |

**Dataset preview image:** Add a screenshot of `df.head()` or the prepared dataset here.

![Dataset Preview](images/06_dataset_preview.jpeg)

## 🔎 Analysis & Visual Results

The notebook investigates the five questions below. Add the corresponding notebook output screenshots or exported plots to the `images/` folder using the filenames shown.

### 1. Most Frequent Genre

Identify the genre that occurs most often after splitting and counting individual genre values.

![Most Frequent Genre](images/01_most_frequent_genre.png)

**Notebook observation:** Drama is the most frequent genre in the dataset's genre-level analysis.

### 2. Vote-Average Category

Compare the number of records in each vote-average category created during preprocessing.

![Vote Average Categories](images/02_vote_average_categories.png)

**Notebook observation:** The notebook groups vote averages into `not_popular`, `below_avg`, `average`, and `popular`. The displayed counts depend on whether records are counted before or after genres are expanded.

### 3. Movie with the Highest Popularity

Find the maximum value in the `Popularity` column and inspect the corresponding title and genre rows.

![Highest Popularity Movie](images/03_highest_popularity.png)

**Notebook observation:** *Spider-Man: No Way Home* has the highest popularity score in the notebook output, with the genres Action, Adventure, and Science Fiction.

### 4. Movie(s) with the Lowest Popularity

Find the minimum value in the `Popularity` column and inspect all matching records.

![Lowest Popularity Movie](images/04_lowest_popularity.png)

**Notebook observation:** The minimum popularity score is **13.354**. The notebook output shows tied records for *The United States vs. Billie Holiday* and *Threads*, with genre rows associated with each title.

### 5. Year with the Most Movie Releases

Explore the distribution of movie release years using a histogram.

![Movie Releases by Year](images/05_releases_by_year.png)

**Notebook observation:** The notebook's conclusion identifies **2020** as the year with the highest number of movie releases.

## ⚙️ Workflow

1. Load the CSV file into a Pandas DataFrame.
2. Inspect the dataset structure, data types, descriptive statistics, and duplicate records.
3. Convert `Release_Date` to datetime and extract the release year.
4. Remove columns not required for the analysis.
5. Categorize `Vote_Average` into four groups.
6. Split comma-separated genre values and expand them into separate rows.
7. Check and handle missing values.
8. Answer the analytical questions using summaries and visualizations.

## ▶️ How to Run

1. Clone or download this repository.
2. Place `mymoviedb.csv` in the location used by the notebook, or update the CSV path.
3. Open `NETFLIX_DATA_ANALYSIS.ipynb` in Jupyter Notebook or Google Colab.
4. Install the dependencies if needed:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

5. Run the notebook cells in order.

## 📁 Suggested Repository Structure

```text
Netflix-Movie-Data-Analysis/
├── NETFLIX_DATA_ANALYSIS.ipynb
├── mymoviedb.csv
├── README.md
└── images/
    ├── 01_most_frequent_genre.png
    ├── 02_vote_average_categories.png
    ├── 03_highest_popularity.png
    ├── 04_lowest_popularity.png
    ├── 05_releases_by_year.png
    └── 06_dataset_preview.png
```

**Image tip:** Save or capture the relevant chart/table outputs from the notebook with these filenames. GitHub will display the images automatically when the paths match. If you do not have an image ready, remove that image line until you add it.

## 💡 Key Takeaways

- Genre-level analysis identifies **Drama** as the most frequent genre.
- Vote averages can be compared by grouping the numeric values into descriptive categories.
- The highest popularity score in the notebook belongs to *Spider-Man: No Way Home*.
- The minimum popularity value is shared by multiple title records in the notebook output.
- The notebook's conclusion identifies **2020** as the year with the most movie releases.

## 👤 Author

**Yash Pawar** · Aspiring Data Analyst

- [GitHub](https://github.com/Yashpawar2804)
- [LinkedIn](www.linkedin.com/in/yashpawar2804)

---

*This project was created for learning and portfolio purposes to practice data cleaning, exploratory analysis, and visualization with Python.*
