# Architecture

See [[features-built]] and [[gotchas]].

Data science portfolio project: can a Steam game's audience (owners bucket) be predicted before launch?

- `notebook/steam_analysis.ipynb`: the whole analysis, cleaning through modelling. Needs the raw `steam_games.csv` (927 MB, not committed) in the repo root; source is the Kaggle "Steam Games Dataset (daily updates)" by Hubert Sidorowicz.
- `data/processed/games.parquet` (~32 MB): the notebook's cleaned output, committed so the dashboard runs without the raw file. List columns survive in parquet.
- `models/owners_classifier.joblib`: both trained models, vocabularies and test metrics.
- `app/streamlit_app.py` and `app/theme.py`, `.streamlit/config.toml`: the Streamlit dashboard. `.claude/launch.json` starts it on port 8501.
- `requirements.txt`: pinned versions; `scikit-learn==1.9.0` must match the pickled model.
