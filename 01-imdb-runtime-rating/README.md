# IMDb Runtime & Rating Analysis
# IMDb Movie Runtime & Rating Analysis

## Project Overview

Do longer movies receive higher IMDb ratings?

This project explores the relationship between movie runtime and IMDb ratings, focusing on two popular genres: **Comedy** and **Drama**.

Using publicly available IMDb datasets, I analyze movie information, visualize rating distributions, and calculate correlations to investigate whether movie length is associated with audience ratings.

## Dataset

**Source:** [IMDb Non-Commercial Datasets](https://developer.imdb.com/non-commercial-datasets/)

The analysis uses two IMDb datasets:

- `title.basics.tsv.gz` — Movie titles, release years, runtimes, and genres.
- `title.ratings.tsv.gz` — Average IMDb ratings and number of votes.

### Data Filtering

To create a more focused dataset, I applied the following conditions:

- Only movies released between **2000 and 2025**
- Movies with a valid runtime greater than 0 minutes
- Movies with at least **1,000 IMDb votes**
- Comedy and Drama genres analyzed separately

Movies belonging to both genres may appear in both analyses.

## Tools & Technologies

- **Python** — Data processing and analysis
- **Pandas** — Data loading, filtering, merging, and correlation calculations
- **Matplotlib** — Data visualization
- **Jupyter Notebook** — Interactive analysis and documentation

## Analysis Process

### 1. Data Collection

Loaded IMDb's publicly available datasets directly from their official URLs.

The larger movie information dataset was processed in chunks to manage memory usage.

### 2. Data Cleaning & Filtering

Filtered movie records based on release year, runtime, and number of IMDb votes.

Merged movie information with rating data using the unique IMDb title identifier (`tconst`).

### 3. Exploratory Data Analysis

Created scatter plots to visualize the relationship between movie runtime and IMDb ratings.

Comedy and Drama movies were visualized separately to compare their distributions.

### 4. Correlation Analysis

Calculated **Spearman's rank correlation coefficient** to measure the strength and direction of the relationship between runtime and rating.

Spearman correlation measures how consistently two variables move together in terms of their rankings.

## Results

The notebook reports the following correlation values:

| Genre | Spearman Correlation |
|---|---:|
| Comedy | 0.28 |
| Drama | 0.30 |

Both genres show a **weak positive correlation** between movie runtime and IMDb ratings.

Drama movies have a slightly higher correlation than Comedy movies, although the difference is small.

## Key Takeaways

- Longer movies tend to have somewhat higher IMDb ratings within the analyzed dataset.
- The relationship is relatively weak in both genres.
- Movie runtime alone cannot reliably predict audience ratings.
- Correlation does not imply causation.

These findings describe associations within the selected IMDb records rather than demonstrating that increasing a movie's runtime would improve its rating.

## Limitations

- Only movies released between 2000 and 2025 were included.
- Movies with fewer than 1,000 IMDb votes were excluded.
- IMDb ratings reflect the users who submitted votes and may not represent all viewers.
- Other factors, such as genre, production quality, and audience preferences, were not controlled for.

## How to Run

1. Download or clone this repository.
2. Install the required Python libraries:

   ```bash
   pip install pandas matplotlib
   ```

3. Open `imdb_runtime_rating_analysis_en.ipynb` in Jupyter Notebook or another compatible environment.
4. Run the notebook cells in order.

An internet connection is required to download the IMDb datasets.

## AI-Assisted Development

This project was developed with assistance from OpenAI Codex as part of my hands-on learning in Python and data analysis.

The project supports my exploration of data processing, visualization, statistical methods, and analytical interpretation.

---
