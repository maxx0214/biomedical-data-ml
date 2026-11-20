# Biomedical Data Machine Learning

Sangmyung University(BioHealth) — Biomedical Data Machine Learning Lab coursework (생체데이터기계학습실습).

## Projects

| Project | Description |
| --- | --- |
| [Mushroom classification](mushroom-classification/) | Classifies edible vs. poisonous mushrooms from 22 categorical features using SVM, decision trees, and a neural network. |
| [Chest X-ray pneumonia classification](chest-xray-pneumonia/) | Compares plain and residual CNNs with and without data augmentation; evaluates on the official held-out test set and visualizes predictions with Grad-CAM. |

## Setup

Clone this repository:

```bash
git clone https://github.com/maxx0214/biomedical-data-ml.git
cd biomedical-data-ml
```

Create a virtual environment (Python 3.12 for mushroom classification; Python 3.11 for chest X-ray classification).

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS/Linux, use `source .venv/bin/activate`.

### Mushroom classification

```bash
cd mushroom-classification
python -m pip install -r requirements.txt
python -m jupyter lab mushroom_classification.ipynb
```

Place `mushrooms.csv` alongside the notebook, select the environment's Python kernel, and run every cell in order.

### Chest X-ray pneumonia classification

```bash
cd chest-xray-pneumonia
python -m pip install -r requirements.txt
python -m jupyter lab chest_xray_pneumonia.ipynb
```

Download [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) separately. Place the extracted `chest_xray/` folder or `chest-xray-pneumonia.zip` alongside the notebook, or configure `LOCAL_DATA` / `XRAY_DATA` to point to the dataset. Then run the cells in order. CUDA is used automatically if available. A compatible PyTorch build is needed for GPU training.

The notebook writes evaluation artifacts to `xray_results/` by default.

### Install all dependencies (optional)

```bash
python -m pip install -r requirements.txt
```

Datasets, generated artifacts, local environments, and notebook execution outputs are intentionally excluded from version control. The original notebook source cells are retained.

**Educational use only:** these models are not intended for mushroom consumption decisions or medical diagnosis.
