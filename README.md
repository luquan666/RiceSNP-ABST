# RiceSNP-ABST 

## Introduction

```text
RiceSNP-ABST: A Deep Learning Approach to Identify Abiotic Stress-Associated Single Nucleotide Polymorphisms in Rice
```
In this paper, a model called RiceSNP-ABST is proposed for predicting ABST-SNPs in rice, utilizing a novel strat-egy for constructing negative samples. Firstly, six benchmark datasets were generated using three methods for con-structing negative samples across two lengths of DNA sequences. Secondly, four feature encoding methods were proposed based on DNA sequence fragments, followed by feature selection. Finally, Convolutional neural networks (CNNs) with residual connections were used to determine whether the sequences were ABST-SNPs in rice. 

## Data

#### Benchmark datasets
```shell
cd ./Feature/data/Benchmark datasets
```
“Random”, “Common”, and “Rearrange” represent three methods for constructing negative samples，“41_nt” and “101_nt” denote sequence lengths.
#### Independent dataset
```shell
cd ./Feature/data/Independent dataset
```

## Feature represention and selection

`Feature/Onehot.py`,`Feature/DNA2vec.py`,`Feature/DNABERT.py`,and `Feature/DNAshape.py`are four feature extraction methods. <br>
`Feature/Feature selection.py`is for feature selection.

## Model training and test

`Model/train.py`is for model training.<br>
`Model/test.py`is for model testing

## Requirement

The Feature code has been tested running under Python 3.8.<br>
The required packages are as follows:
* transformers==4.29.2 
* torch==2.4.0 
* biopython==1.83 
* einops==0.8.0
* git clone https://github.com/JinsenLi/deepDNAshape<br>
  cd deepDNAshape<br>
  pip install .<br>
* gensim==3.8.3  
* scipy==1.7.3 
* pandas 
* scikit-learn

The Model code has been tested running under Python 3.7.<br>
The required packages are as follows:
* tensorflow-gpu==1.15.0 
* keras==2.2.5
* scikit-learn==1.0.2
* numpy==1.18.5 
* h5py==2.10.0 
* matplotlib==3.5.3
* seaborn==0.10.0
* amber-automl==0.1.0
if you don't have CUDA-enabled GPU, or on MacOS, replace tensorflow-gpu=1.15.0 with tensorflow=1.15.0
## Contact

Please feel free to contact us if you need any help (E-mail: mengyaliu1003@foxmail.com).
