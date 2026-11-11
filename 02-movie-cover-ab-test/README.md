# Movie Cover A/B Testing Analysis

## Project Overview

Can changing a movie's cover image increase the number of users who start watching it?

This project explores A/B testing through a simulated experiment comparing two different movie cover designs: **Cover A** and **Cover B**.

Using Python, I simulate user behavior, calculate conversion rates, and estimate the uncertainty around the observed difference to evaluate whether one cover performs better than the other.

The goal is to practice statistical analysis and data-driven decision-making.

## Dataset

**Source:** Simulated data generated using NumPy.

The experiment includes **2,000 simulated users**, divided equally between two groups:

- **Group A:** 1,000 users shown Cover A.
- **Group B:** 1,000 users shown Cover B.

Each user has a binary outcome:

- `1` — The user started watching the movie.
- `0` — The user did not start watching the movie.

The simulation uses the following probabilities:

| Group | Simulated Start Probability |
|---|---:|
| Cover A | 8% |
| Cover B | 10% |

A fixed random seed (`42`) is used to make the simulation reproducible.

**Note:** This project uses synthetic data, not real user behavior or an actual production experiment.

## Tools & Technologies

- **Python** — Data analysis and statistical calculations
- **NumPy** — Random data generation and numerical calculations
- **Pandas** — Data manipulation and aggregation
- **Jupyter Notebook** — Interactive analysis and documentation

## Analysis Process

### 1. Data Simulation

Generated binary movie-start outcomes for both groups using NumPy's binomial distribution.

### 2. Conversion Rate Analysis

Calculated the number of users, movie starts, and movie-start rates for each group.

### 3. Performance Comparison

Measured the observed difference in movie-start rates between Cover A and Cover B.

### 4. Confidence Interval Calculation

Calculated an approximate **95% confidence interval** for the difference between two proportions using the normal approximation.

### 5. Decision Evaluation

Interpreted the observed improvement and its uncertainty to assess whether the experiment provides sufficient evidence for a potential design change.

## Results

The notebook reports the following results:

| Metric | Cover A | Cover B |
|---|---:|---:|
| Total Users | 1,000 | 1,000 |
| Movie Start Rate | 7.8% | 11.1% |

**Observed difference:** +3.3 percentage points

**95% Confidence Interval:** +0.74 to +5.86 percentage points

Cover B achieved a higher observed movie-start rate than Cover A.

The estimated confidence interval is entirely above zero, suggesting a positive difference under the statistical assumptions used.

However, the interval also indicates uncertainty about the true size of the improvement.

## Key Takeaways

- Cover B performed better than Cover A in the simulated experiment.
- The observed improvement was 3.3 percentage points.
- Confidence intervals provide more information than comparing conversion rates alone.
- Statistical evidence of a positive difference does not automatically establish that the improvement is large enough to justify a business decision.

For example, if adopting Cover B required an improvement of at least **2 percentage points**, the confidence interval's lower bound would not meet that threshold.

Therefore, the experiment would not provide sufficient evidence to confidently establish the required minimum improvement.

## Limitations

- The dataset is simulated and does not represent real users.
- The probabilities were predefined rather than estimated from actual behavior.
- The confidence interval uses a normal approximation, which has statistical assumptions.
- The analysis does not account for user demographics, device types, or other behavioral factors.
- No real-world deployment or business impact was measured.

## How to Run

1. Download or clone this repository.
2. Install the required libraries:

   ```bash
   pip install numpy pandas
   ```

3. Open `movie_cover_ab_test_en.ipynb` in Jupyter Notebook or another compatible environment.
4. Run all cells in order to reproduce the simulation and statistical calculations.

## AI-Assisted Development

This project was developed with assistance from OpenAI Codex as part of my hands-on learning in Python and data analysis.

It supports my exploration of experimental design, statistical reasoning, and data-driven decision-making.

---

*Part of my [Python Data Analysis](../) project collection.*
