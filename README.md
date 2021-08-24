# scHiCStackL
## Introduction
scHiCStackL is a comprehensive python package for single-cell Hi-C data Classification. scHiCStackL contains a two-layer stacking ensemble model. The stacking ensemble model integrates Ridge Regression (RR) classifier and Logistic Regression (LR) classifier as the base-classifiers (i.e., first-level) and Gaussian Naive Bayes (GaussianNB) classifier as the meta-classifier (i.e., second-level).

### Installing scHiCStackL:
Download the zip file of the scHiCStackL project, and install the python package through the following two methods:

(1)Install the python package through setup.py

```python
python setup.py install
```

(2)Install the python package through the whl file

```python
pip install scHiCStackL-0.0.3-py3-none-any.whl
```

#### Import scHiCStackL

```python
import scHiCStackL.scHiCStackL as sc
```

We provide PCA files generated by ML1 and ML3, Ramani and Flyamer datasets (processed by KPCA) and stacking_model method.

(1)Evaluate the classification performance of scHiCStackL stacking model on ML1 and ML3 data sets (The range of recommended parameter ndim is [40, 50]):

```python
 ARI, Acc, MCC, F1, Precision, NMI = sc.stackling_model(cell_type="human", cell_num = 626, ndim = 40)
```

(2)Evaluate the classification performance of scHiCStackL stacking model on the whole Ramani data set (The range of recommended parameter ndim is [40, 50]):

```python
    ARI, Acc, MCC, F1, Precision, NMI = sc.stackling_model(cell_type="human", cell_num = 2655, ndim = 40)
```

(3)Evaluate the classification performance of scHiCStackL stacking model on the Flyamer dataset (The range of recommended parameter ndim is [40, 50]):

```python
         ARI, Acc, MCC, F1, Precision, NMI = sc.stackling_model(cell_type="mouse", cell_num = 178, ndim = 40)
```

Note：Files and parameters folders need to be placed in the project directory you created

## Contact us

If you have any questions, please contact us: haowu@sdu.edu.cn.