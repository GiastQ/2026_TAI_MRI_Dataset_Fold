# 2026 TAI MRI Dataset — Fold Partitions

This repository accompanies the following paper, currently **under review**:

> **A Hybrid AI-based System for Brain Tumor Segmentation and Explainable Classification from MRI Images**  
> Submitted to *IEEE Transactions on Artificial Intelligence (TAI)*  
> *(Full citation will be added upon publication)*

It provides the **data partitions** (train / validation / test splits) used in our experiments, so that other researchers can **exactly reproduce** our experimental setup using the same fold structure.

---

## Datasets

Two MRI brain tumor datasets are covered by this repository:

### 1. Figshare
Located under:
```
A_Datasets/A_Train_Yolo/A_figshare/A_fold_data/
```

### 2. BRISC2025
Located under:
```
A_Datasets/A_Train_Yolo/B_brisc2025/A_fold_data/
```

Each dataset is split into **5 rounds** (folds), each containing three subfolders:

```
round_X/
├── Train/
│   ├── images/
│   ├── labels/
│   └── masks/
├── Validation/
│   ├── images/
│   ├── labels/
│   └── masks/
└── Test/
    ├── images/
    ├── labels/
    └── masks/
```

---

## Purpose

This repository does **not** distribute any original dataset.  
It only provides the **file-level partition assignments** (i.e., which images belong to Train, Validation, or Test in each fold), so that anyone can reproduce the exact experimental setup described in our paper.

To use these partitions, download the original datasets from their official sources and reorganize the images according to the fold structure provided here.

---

## Disclaimer - BRISC2025 Filename Convention

> [!IMPORTANT]
> In the **BRISC2025** dataset partitions, you may notice that files with the prefix `brisc2025_test_XXXXX_...` appear inside **Train** folders (e.g., `round_1/Train/images/`).
>
> **This is NOT data leakage.**
>
> The filename prefix (`train` or `test`) reflects the **original split assignment** in the BRISC2025 dataset as distributed by its authors.  
> In our work, we took **all images from the full original dataset** (both the original `train` and `test` splits) and **re-partitioned them from scratch** into our own 5-fold cross-validation scheme.  
>
> Therefore, an image originally labelled `brisc2025_test_XXXXX` may legitimately appear in our training fold, and vice versa. The filename is merely an identifier inherited from the source dataset, it carries no semantic meaning about the split we used.

---

## Original Datasets

Please refer to the following publications to access and cite the original datasets:

**Figshare (Brain Tumor MRI Dataset)**
> Cheng, J., Huang, W., Cao, S., Yang, R., Yang, W., Yun, Z., Wang, Z., & Feng, Q. (2015).
> *Enhanced performance of brain tumor classification via tumor region augmentation and partition.*
> PLOS ONE, 10(10), e0140381.

**BRISC2025**
> Fateh, A., Rezvani, Y., Moayedi, S., Rezvani, S., Fateh, F., Fateh, M., & Abolghasemi, V. (2025).
> *BRISC: Annotated Dataset for Brain Tumor Segmentation and Classification.*
> arXiv preprint arXiv:2506.14318.

---

## Citation

The paper associated with this repository is currently **under review**:

> **A Hybrid AI-based System for Brain Tumor Segmentation and Explainable Classification from MRI Images**  
> Submitted to *IEEE Transactions on Artificial Intelligence (TAI)*  
> *(Citation details will be added upon publication)*
