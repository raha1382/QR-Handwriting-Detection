# Handwritten Letter Recognition Using QR Decomposition

## Overview
This project implements a handwritten letter recognition system using the **least squares method** and **QR decomposition**. 

The project uses the **EMNIST Letters dataset** and explores two QR decomposition approaches:  
1. **Householder transformations**  
2. **Incremental QR updating using Givens rotations**  

# Language $ Tools
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) 
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white) 
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![EMNIST](https://img.shields.io/badge/EMNIST-FF6F61?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8Xw8AApAB0U3Me4AAAAASUVORK5CYII=)

---

## Objectives
- Implement QR decomposition with **Householder matrices** for each letter class.  
- Classify test samples using **least squares** reconstruction error.  
- Update QR decomposition **incrementally** with new samples using **Givens rotations**.  
- Compare performance before and after QR updates.

---

## Dataset
- **Dataset:** [EMNIST Letters](https://www.nist.gov/itl/products-and-services/emnist-dataset)  
- **Classes:** 26 (A-Z)  
- **Training samples per class:** 200  
- **Test samples per class:** 20  

---
## Steps

### Section 1: QR decomposition using Householder matrices
1. For each class, create a matrix `A` of training samples.
2. Perform QR decomposition using Householder matrices.
3. Predict test samples using the least squares solution.
4. Evaluate classification accuracy.

###Section 2: Incremental QR updating using Givens rotations

Add 20 new samples per class.
Update the QR decomposition incrementally using Givens rotations.
Predict test samples again and evaluate accuracy.

##Results

Accuracy using Householder QR (Section 1): 70.58%

Accuracy using Incremental QR with Givens rotations (Section 2): 70.19%

## How to Run

1. **Clone the repository**:
```bash
git clone https://github.com/raha1382/QR-Handwriting-Detection.git
cd QR-Handwriting-Detection
pip install -r requirements.txt

```



