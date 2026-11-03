# Decisions

See [[architecture]]. Reasons come from the README.

- **Report modest numbers honestly.** The goal is the process, not a high score: the first "78% accuracy" model was no better than always answering the largest bucket.
- **Predict only from launch-day information.** Features that exist only after release were dropped even though they raised the score.
- **Drop zero-owner entries** (unreleased or delisted artifacts) and merge the five smallest buckets (as few as 4 games each) into nine classes.
- **Train `release_year` both ways:** it ranked 2nd by permutation importance but added only +0.003 macro F1 and encodes a maturity bias.
- **Show both models in the dashboard,** not just the better one.
- **Commit the processed parquet and the model, not the raw CSV,** so the dashboard runs without a 927 MB download.
