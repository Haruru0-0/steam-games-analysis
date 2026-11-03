# Features built

Structure: [[architecture]].

- **Analysis of 139,580 games** (one snapshot, 31 August 2026) from raw CSV to a leak-free model, with a written account of the dataset's problems.
- **Seven data problems documented and fixed**, for example `tags` stored as a dict for about 23,500 rows, `estimated_owners` in two formats that split 14 categories into 26, and `tags_count` capped at 20 for 24% of rows.
- **Model results** (nine owners buckets): unweighted baseline 0.783 accuracy but macro F1 0.140 (no better than a constant that always answers the largest bucket); class-weighted 0.193; with genres, tags and categories 0.248; clean, leak-free 53-feature model 0.565 accuracy, 0.193 macro F1, 79.6% within one bucket.
- **Leakage found and removed:** `tags_count` (player-applied tags accumulate after launch), `dlc_count` and localisation counts; about 22% of the best model's macro F1 came from launch-unavailable information.
- **Other findings:** indie is 66.5% of the catalog; prices cluster at charm points; higher-priced games reach more owners; free-to-play dominates the very top buckets.
- **Streamlit dashboard:** an Explore tab (genre, price, release year filters; the whole catalog as one proportional strip) and a Predict tab that runs both models side by side. Not deployed yet.
- GitHub Actions mirrors the repo to GitLab on every push.
