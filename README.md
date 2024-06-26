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
This project tackles the challenge of accurately retrieving 3D objects using Sino-nom characters as image input. Sino-nom characters, a unique feature of East Asian cultures, combine Chinese characters and Vietnamese Nom script. Accurate retrieval of these characters is essential for various applications such as historical document analysis, cultural heritage preservation, and language research.

I decided to tackle this problem with a deep learning approach, which is expected to outperform traditional methods (SIFT and SURF).

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
1. Install open3d and learning3d
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
My final approach using multi-stream model aresulted in an MRR@5 score of 0.0867.

## Contributors
- Nguyen Khoa Dang - 21021478

## Report

Link to the [pdf:](https://github.com/Dan-the-dunk/3D-Object-Retrieval/blob/main/full_report.pdf)

Link to the [overleaf project:](https://www.overleaf.com/read/cdvwmpwcwzps#b30c51).
