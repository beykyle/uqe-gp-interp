# gp_interp

Gaussian process interpolation notebook (`gp_E_interp.ipynb`), built on NumPy, SciPy,
scikit-learn and Matplotlib.

Requires Python 3.10 or newer (tested with 3.13). Pick one of the setups below, then
open `gp_E_interp.ipynb` in Jupyter and run all cells. A full run takes under a minute.

## uv (recommended)

[uv](https://docs.astral.sh/uv/) installs the exact versions pinned in `uv.lock`:

```sh
uv sync
uv run jupyter lab gp_E_interp.ipynb
```

## pip

```sh
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install .
jupyter lab gp_E_interp.ipynb
```

## conda

```sh
conda create -n gp_interp python=3.13 pip
conda activate gp_interp
pip install .
jupyter lab gp_E_interp.ipynb
```

## Using VS Code or an existing Jupyter install

Select the environment's interpreter (for example `.venv/bin/python`) as the notebook
kernel. To make the environment show up in another Jupyter install, register it as a
kernel from inside the activated environment:

```sh
python -m ipykernel install --user --name gp_interp --display-name "Python (gp_interp)"
```

With uv, run `uv run python -m ipykernel install ...` instead.

## Dependencies

All dependencies are declared in `pyproject.toml`; `pip install .` and `uv sync` both read
from it (the project isn't a real package, `pip install .` just installs the dependencies).
After adding or changing a dependency, run `uv lock` to update `uv.lock`.
