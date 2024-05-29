# 3D Sino-nom Character Retrieval
INT3404E 20 - Image Processing: 3D Object Retrieval


![image](https://github.com/Dan-the-dunk/3D-Object-Retrieval/assets/92426318/ccb8b837-6e28-4b13-83b2-cf43dcdac2f1)


## Introduction
This repo contains the code for an image retrieval pipeline designed to retrieve Sino-nom characters. The dataset includes 3D items in the database folder and 2D items in the query folder.

## Table of Contents
- [Goal](#goal)
- [Repo Tree](#repo-tree)
- [Installation](#installation)
- [Result](#result)
- [Contributors](#contributors)
- [Report](#report)

## Goal
The goal of this project is to develop an accurate image retrieval system specifically tailored for Sino-nom characters. Sino-nom characters are a unique aspect of East Asian cultures, blending Chinese characters (Sino) with Vietnamese Nom script (nom). Retrieving similar characters accurately is crucial for various applications, including historical document analysis, cultural preservation, and language research. 

Although many local feature matching algorithms like SIFT, SURF, or ORB exist, these are designed to achieve speed and efficiency in the retrieval process. We decided to tackle this problem with a deep learning approach, which is expected to outperform traditional methods.

**This repo implements:**
- Point Cloud sampling from 3D mesh.
- Features extractions model using PyTorch Image Models and learning3d. 
- Multi-stream pipeline with Triplet loss.



## Repo Tree
```
│---evaluation_notebook.ipynb # Notebook for evaluation
│---requirements.txt
│---train_notebook.ipynb # Train an retrieval model with open3d and learning3d library
│   
├───model
│   |---retrival_net_(pntnet).ckpt
│       
└───wb_2D3Dretrieval_dataset
    |---database
    |---pairs
    │   |---print
    │   |---stl
    |---queries

```

## Installation
To reproduce the results, follow the installation steps:
1. Install open-metric-learning
```
pip install open3d
pip install learning3d
```
2. Install pip requirements
```
pip install -r requirements.txt
```

After the installation, you can start by running the training scripts provided and evaluate on your own data.


## Result
Our final approach using multi-stream model aresulted in an MRR@5 score of 0.0867.

## Contributors
- Nguyen Khoa Dang - 21021478

## Report

Link to pdf: [link](https://github.com/Dan-the-dunk/3D-Object-Retrieval/blob/main/full_report.pdf)

Link to the overleaf project: [link](https://www.overleaf.com/read/cdvwmpwcwzps#b30c51).
