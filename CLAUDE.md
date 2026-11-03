# Steam games analysis

Analysis of 139,580 Steam games ending in a model that predicts owners before launch, plus a Streamlit dashboard. See `README.md`.

## Commands
- `py -m venv .venv`, then `pip install -r requirements.txt` (scikit-learn is pinned to 1.9.0 to match the saved model).
- `streamlit run app/streamlit_app.py`: the dashboard (port 8501 in `.claude/launch.json`).
- Rerun the notebook `notebook/steam_analysis.ipynb` only with the raw `steam_games.csv` in the repo root.

## Conventions
- Default branch is `master`. Commit messages are plain, with no `Co-Authored-By` trailer.
- Report model results honestly; do not use features unavailable before launch.

## Memory and code map
- At session start read `docs/memory/index.md`. Save durable decisions there as Markdown.
- `graphify-out/GRAPH_REPORT.md` summarizes code structure; refresh with `python -m graphify update .` (the `.exe` is blocked on this machine).
