# AGENTS.md

## Cursor Cloud specific instructions

This repository contains a single Jupyter notebook (`neural_network_world_cup_tutorial.ipynb`) that teaches neural network fundamentals and builds a FIFA World Cup match outcome predictor using scikit-learn.

### Tech stack
- **Language:** Python 3.8+
- **Dependencies:** numpy, pandas, scikit-learn, matplotlib, seaborn, jupyter, ipykernel (see `requirements.txt`)
- **No backend services, databases, or Docker required**

### Running the notebook
- Install deps: `pip install -r requirements.txt`
- Launch: `python3 -m jupyter notebook --no-browser --ip=0.0.0.0 --port=8888 --NotebookApp.token="" --NotebookApp.password=""`
- Execute all cells headlessly: `python3 -m nbconvert --to notebook --execute --ExecutePreprocessor.timeout=300 neural_network_world_cup_tutorial.ipynb --output executed_output.ipynb`
- The `jupyter` CLI command may not be on `$PATH`; always invoke via `python3 -m jupyter` or `python3 -m nbconvert`.

### Gotchas
- matplotlib requires a non-interactive backend when running headlessly (the notebook already uses the default `Agg` backend in non-GUI environments).
- All cells must be run in order — later cells depend on variables/models defined in earlier cells.
- The notebook generates synthetic data (no external data download needed).

### Linting / Testing
- No dedicated lint or test configuration exists. To verify correctness, execute the notebook end-to-end with `nbconvert --execute` and check for a zero exit code.
