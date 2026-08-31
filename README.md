# PyTorch Portfolio

A set of deep-learning projects I built with **PyTorch** while learning the framework —
feed-forward networks, CNNs, transfer learning, and end-to-end data prep / training / evaluation.
Every notebook is my own implementation (data loading, model definition, training loop,
metrics, and visualisations). Concepts were learned from a PyTorch course; the code here is
written from scratch, not copied from course solution files.

Each notebook is committed **with its outputs**, so it can be read on GitHub without running anything.

## Artificial Neural Networks — [`ann/`](ann/)

| Notebook | Problem | Approach | Result |
|----------|---------|----------|--------|
| [anaemia-prediction.ipynb](ann/anaemia-prediction.ipynb) | Predict anaemia from image-derived RGB / blood features | Feature engineering (pixel brightness) + fully-connected classifier | **98.6%** test accuracy (73/74) |
| [iris-classification-ann.ipynb](ann/iris-classification-ann.ipynb) | 3-class Iris species classification | 2-hidden-layer MLP, cross-entropy loss | Converges to near-perfect on held-out set |
| [taxi-fare-regression-ann.ipynb](ann/taxi-fare-regression-ann.ipynb) | Regress NYC taxi fare from trip data | Haversine-distance + datetime feature engineering, embeddings for categoricals, MLP regressor | Final training loss ≈ 3.7 |

## Convolutional Neural Networks — [`cnn/`](cnn/)

| Notebook | Problem | Approach | Result |
|----------|---------|----------|--------|
| [mnist-ann.ipynb](cnn/mnist-ann.ipynb) | MNIST digit classification, MLP baseline | Fully-connected network, confusion-matrix analysis | ~99% train / strong test accuracy |
| [mnist-cnn.ipynb](cnn/mnist-cnn.ipynb) | MNIST digit classification with convolutions | 2 conv layers + pooling + FC head | **98.7%** test accuracy |
| [cifar10-cnn.ipynb](cnn/cifar10-cnn.ipynb) | CIFAR-10 10-class image classification | Conv stack trained from scratch | **61.5%** test accuracy |
| [cats-vs-dogs-eda.ipynb](cnn/cats-vs-dogs-eda.ipynb) | Explore the Dogs vs. Cats image set | Image-size distribution analysis, corrupt-file handling, transform pipeline design | — |
| [cats-vs-dogs-cnn.ipynb](cnn/cats-vs-dogs-cnn.ipynb) | Binary cat/dog classification | Custom CNN (~79%), then **transfer learning** with a pretrained CNN | ~91% after one epoch of fine-tuning |

## Running the notebooks

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Datasets: small CSVs are in [`Data/`](Data/); MNIST and CIFAR-10 download automatically on
first run; Dogs vs. Cats must be fetched from Kaggle — see [`Data/README.md`](Data/README.md).
