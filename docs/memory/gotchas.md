# Gotchas

See [[architecture]].

- **Results describe one snapshot** (31 August 2026). A fresh Kaggle download will not reproduce the figures exactly, and the catalog only grows.
- **Pin scikit-learn to 1.9.0** (the model was pickled with it); other versions may warn or fail to unpickle.
- **The raw `steam_games.csv` is git-ignored** and must be downloaded and placed in the repo root to rerun the notebook.
- **Adding boolean columns in pandas does not give a count:** summing three boolean platform columns returns a boolean (and `NaN` forced `object` dtype), with no error.
- **`price_status = "unavailable"` means neither "no price" nor "delisted";** both were tested and ruled out.
- **Branch is `master`,** not `main`.
- **`graphify.exe` is blocked on this machine;** use `python -m graphify update .`.
