# Video Game Market Analysis & Sales Drivers (Project 1)

[Notebook project](./c9422a73-b3ae-49fc-a64f-3d6d61cab188.ipynb)

**TL;DR:** EDA on `games.csv` to find what drives sales by **platform, genre, and region**. Built `total_sales`, ran simple statistical tests, and summarized business takeaways to inform 2017 planning.

## Dataset
`games.csv` with: `name`, `platform`, `genre`, `year_of_release`, `na_sales`, `eu_sales`, `jp_sales`, `other_sales`, `critic_score`, `user_score`, `rating`.

## Method
- Clean & prep: normalize columns/types; convert `TBD→NaN`; median/mode imputations; create **`total_sales = na + eu + jp + other`**.
- Trend analysis by year, platform, genre, and regions (NA/EU/JP).
- Statistical checks on PS4 (critic/user vs. sales) and **hypothesis testing** (Levene + two-sample t-tests).

## Key Findings
- **Critic score ↗ sales on PS4 (r≈0.41)**; **user score** shows ~no signal (≈−0.03).
- **2010–2016** is the most useful window to infer **2017** trends.
- Boxplots: higher medians/variance on **X360/PS4/PS3**; **PSP/PSV** lower.
- Regions: **NA/EU** favor **Action/Shooter/Sports**; **JP** leans **RPG/handheld**.
- Hypotheses: **XOne vs PC** user scores → no difference; **Action vs Sports** → different means (α=0.05).

## How to Run
```bash
python -V   # 3.9+
pip install -r requirements.txt
jupyter lab  # open notebooks/01_eda_video_games.ipynb






