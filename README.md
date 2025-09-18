# Machine Learning and Deep Learning — Coursework and Final Exam

This repository contains three assignments and the final exam materials for the Machine Learning and Deep Learning course. The final project is a comparative study of brain-tumor MRI classification, focusing on careful preprocessing, balanced evaluation, and pragmatic model selection.

## Repository structure

| Path | Type | Description |
| --- | --- | --- |
| `assignment_1.ipynb` | Jupyter Notebook | Introductory models and preprocessing. |
| `assignment_2.ipynb` | Jupyter Notebook | Model comparison and evaluation routines. |
| `assignment_3.ipynb` | Jupyter Notebook | Extended experiments and diagnostics. |
| `final_project/ML&DL_final_exam.ipynb` | Jupyter Notebook | End-to-end pipeline used for the exam project. |
| `final_project/ML&DL_exam_Written_Product.pdf` | PDF | Exam write-up covering data, pipeline, metrics, and limitations. |
| `README.md` | Markdown | This file. |

## Final project overview

Goal: Classify MRI scans into four classes (glioma, meningioma, pituitary and no tumor) and compare methods under consistent preprocessing and validation.

Data: A unified dataset is built from four public sources (PMRAM, Brain Tumor Data, China_Dataset, AD_VS_CN). Exact duplicates are removed with SHA-1 and perceptual hashing. All images are resized to 256×256 and converted to grayscale where needed. A 70/15/15 train–test–validation split is used after merging. Augmentation is applied at training time with small rotations, zoom, light Gaussian blur, and brightness shifts.

Models: Four approaches are implemented: a baseline MLP, two CNNs of increasing depth with batch-norm and dropout, and an SVM pipeline using HOG features, standardization, PCA, and Bayesian hyper-parameter optimization.
