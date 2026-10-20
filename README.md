# Handwritten Letter Classification via Least Squares and QR Decomposition

## Overview
This project implements a handwritten letter classifier using the **least squares method** and **QR decomposition** on the **EMNIST Letters** dataset. Two QR approaches are explored:
1. **Householder transformations** for full QR decomposition
2. **Incremental QR updating** using **Givens rotations**
   
Course project for **Linear Algebra Applications in Data Mining**.

## Languages & Tools
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![EMNIST](https://img.shields.io/badge/EMNIST-FF6F61?style=for-the-badge&logoColor=white)

## Objectives
- Implement QR decomposition with **Householder matrices** for each letter class.
- Classify test samples using **least-squares reconstruction error**.
- Update QR decomposition **incrementally** with new samples using **Givens rotations**.
- Compare classification accuracy before and after incremental updates.

## Dataset
- **Dataset:** EMNIST Letters
- **Classes:** 26 (A–Z)
- **Training samples per class:** 200
- **Test samples per class:** 20

## Method

### Section 1: Householder QR
1. Build a matrix `A` of training samples for each class.
2. Compute QR decomposition using Householder reflections.
3. Classify test samples by least-squares reconstruction error.
4. Evaluate accuracy.

### Section 2: Incremental QR with Givens Rotations
1. Add 20 new samples per class.
2. Update the existing QR decomposition incrementally using Givens rotations.
3. Re-evaluate classification accuracy.

## Results

| Method | Accuracy |
|---|---|
| Householder QR | 70.58% |
| Incremental QR (Givens) | 70.19% |

Accuracy dropped slightly after incremental updates (70.58% → 70.19%), likely because the added samples introduced class overlap without re-orthogonalization.

## How to Run
```bash
git clone https://github.com/raha1382/QR-Handwriting-Detection.git
cd QR-Handwriting-Detection
pip install -r requirements.txt
python main.py
