# OncoRiskAI — Breast Cancer Detection with Machine Learning

A collaborative academic project exploring benign/malignant breast-tumor classification, model comparison and a broader Streamlit demonstration interface.

**Original team repository:** [AhmedTrabelsy/OncoRiskAI](https://github.com/AhmedTrabelsy/OncoRiskAI).

This is the **Breast Cancer Detection — Machine Learning** group project listed in Ahmed Fekih's CV. It is distinct from the multimodal BCMID project.

## Breast cancer classification

The `CancerDetection/` directory contains the tabular experiments associated with the Wisconsin Diagnostic Breast Cancer dataset:

- Data preparation, exploratory analysis and feature standardization.
- Train/test splitting and comparison of classification algorithms.
- MLP, GRU-SVM, linear/softmax regression and SVM experiments.
- Accuracy, confusion-matrix and related classification evaluations.
- Additional model-comparison experiments in the evaluation notebook.

The project overview describes reproduction and extension of Abien Fred M. Agarap's paper, *On Breast Cancer Detection: An Application of Machine Learning Algorithms on the Wisconsin Diagnostic Dataset*. The included article is under `CancerDetection/article/`.

## Wider application

The root `app.py` contains a Streamlit interface with saved models, image-processing workflows and PDF-report generation. Other files cover cancer-type prediction, recommendations and breast/colon/skin image demonstrations. These experimental components are separate from the tabular WDBC benchmark.

## Repository guide

| Path | Purpose |
| --- | --- |
| `CancerDetection/PRETREATMENT.ipynb` | Data preparation |
| `CancerDetection/EVALUATION.ipynb` | Tabular model evaluation |
| `CancerDetection/datasets/data.csv` | Dataset used in the experiments |
| `CancerDetection/models/` | Saved classification models |
| `app.py` | Streamlit demonstration |
| `requirements.txt` | Pinned application dependencies |
| `rapport/ONCORISK_AI_REPORT.pdf` | Project report |
| `README.upstream.md` | Original team overview |

## Technologies

Python, TensorFlow/Keras, scikit-learn, Pandas, NumPy, Streamlit, Joblib, Pillow and ReportLab. The notebooks also import Matplotlib and Seaborn.

## Local setup

Use a Python version compatible with the pinned dependencies and create a virtual environment.

```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

For the tabular experiments, install Jupyter, Matplotlib and Seaborn, then open:

```bash
jupyter notebook CancerDetection/EVALUATION.ipynb
```

Review dataset paths before executing notebook cells: some paths may be specific to the original environment. Launch the Streamlit app from the repository root so that relative model paths resolve correctly. Saved model weights make the checkout relatively large.

## Evaluation and scope

Training, model loading and the application were not rerun during this documentation update. Existing results are available in the notebooks and report; no new accuracy or clinical-performance claim is made here. This is an educational and research project, not a clinically validated diagnostic service.

## Team attribution

Presented in Ahmed Fekih's portfolio as a **group project**. The original repository, Git authorship, report and previous README remain credited. This copy does not claim sole authorship or assign individual contributions that have not been documented.
