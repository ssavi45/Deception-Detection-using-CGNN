# Deception-Detection-using-CGNN

Causal Graph Neural Network (C-GNN-D) style notebook for deception detection.

## Dataset layout
The notebook expects this folder structure:

```
DOLOS_Train/
	truth/
		*.mp4
	lie/
		*.mp4

RLT_Test/
	truth/
		*.mp4
	lie/
		*.mp4
```

Large datasets are intentionally ignored by git via `.gitignore`.

## Setup (Windows)
1) Create + activate a virtual environment.

2) Install dependencies:
- `pip install -r requirements.txt`

Notes:
- MediaPipe is sensitive to Python version support. For full FaceMesh landmarks, prefer Python 3.10–3.12.
- `torch-geometric` sometimes requires matching wheels for your installed `torch`. If `pip install torch-geometric` fails, install PyG following the official instructions for your Torch/CUDA version.
- Audio MFCC extraction from `.mp4` may require FFmpeg on your system, depending on how `librosa`/`soundfile` is built.

## Run
Open and run the notebook:
- `Causal_GNN_Experiment.ipynb`

By default it trains on `DOLOS_Train/` and evaluates on `RLT_Test/`.
