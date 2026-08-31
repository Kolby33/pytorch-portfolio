# Data

Small CSVs used by the notebooks are committed here:

| File | Used by | Source |
|------|---------|--------|
| `iris.csv` | `ann/iris-classification-ann.ipynb` | Classic Iris dataset |
| `NYCTaxiFares.csv` | `ann/taxi-fare-regression-ann.ipynb` | Sample of NYC taxi trips |
| `d_output.csv` | `ann/anaemia-prediction.ipynb` | Anaemia image-derived RGB / blood features |

Larger datasets are **not** committed (see `.gitignore`) and are pulled on first run:

- **MNIST**, **CIFAR-10** — downloaded automatically by `torchvision.datasets` into this folder.
- **Dogs vs. Cats** — download from
  [Kaggle: Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data) and extract to
  `Data/CATS_DOGS/CATS_DOGS/{train,test}/{CAT,DOG}/`.
