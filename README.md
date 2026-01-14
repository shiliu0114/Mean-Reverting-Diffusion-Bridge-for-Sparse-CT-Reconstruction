# PMRDB: Mean-Reverting Diffusion Bridge with Projection Prior for Sparse CT Reconstruction
[![Journal](https://img.shields.io/badge/CT_Theory_&_Apps.-10.15953%2Fj.ctta.2025.356-blue.svg)](https://doi.org/10.15953/j.ctta.2025.356)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
This repository contains the PyTorch implementation of the paper **"Mean-Reverting Diffusion Bridge with Projection Prior for Sparse CT Reconstruction"** (面向稀疏角CT重建的投影先验引导均值回归扩散桥模型).


## Abstract
<p align="left">
In sparse-view computed tomography (CT), incomplete projection data often lead to artifacts, edge blurring, and structural distortions  in  the  reconstructed  images.  To  address  this  challenge,  this  study  proposes a diffusion  bridge  model  based  on  the     Ornstein–Uhlenbeck  (OU)   process  for  the   conditional   completion  of  missing   projection-domain   data   to   enable     high-quality  sparse  view reconstruction. The proposed method leverages the mean-reverting property of the OU process to   establish a  physically  consistent  stochastic  diffusion  mechanism. The  diffusion  bridge constraint anchors the sampling trajectory  between  the  reconstruction  prior  and  sparse  projections,   thereby   achieving   high fidelity restoration of the missing data. Furthermore, a multiscale feature fusion module in the wavelet domain is incorporated into the network architecture to effectively integrate low-frequency structural information with high frequency  texture  details,  thereby enhancing  the  capability  of  the  model  to  recover  fine  image  features.  Experimental  results demonstrate that under the same sparse-view conditions, the proposed method outperforms existing state-of-the-art approaches in terms of both visual quality and quantitative metrics, confirming its effectiveness for sparse-view CT reconstruction tasks.
</p>

Keywords: computed tomography; diffusion bridge model; sinogram prior; discrete wavelet transform

## Key Features
* **Mean-Reverting Diffusion Bridge:** Utilizes the Generalized Ornstein-Uhlenbeck (OU) process to model the transition between clean data and prior data, rather than traversing to pure noise.
* **Projection Prior Guidance:** Leverages the rough reconstruction (e.g., FBP of sparse views) as the terminal distribution of the forward process, preserving low-frequency structural information.
* **Manifold Constraint:** Incorporates a data-consistency step during sampling to project the intermediate results back onto the measurement subspace, reducing hallucinations.
* **High Fidelity:** Outperforms traditional methods (FBP, TV) and standard deep learning models (RED-CNN, DDPM) in preserving texture and suppressing streak artifacts.

## Method Overview
<p align="center">
  <img src="images/1.png" alt="Visual Comparison" width="800">
  <br>
</p>

<p align="center">
  <img src="images/2.png" alt="Visual Comparison" width="800">
  <br>
</p>

<p align="center">
  <img src="images/3.png" alt="Visual Comparison" width="800">
  <br>
</p>

## Results
<p align="center">
  <img src="images/4.png" alt="Visual Comparison" width="800">
  <br>
</p>

<p align="center">
  <img src="images/5.png" alt="Visual Comparison" width="800">
  <br>
</p>

<p align="center">
  <img src="images/6.png" alt="Visual Comparison" width="800">
  <br>
</p>

<p align="center">
  <img src="images/7.png" alt="Visual Comparison" width="800">
  <br>
</p>




## Citation
If you use this code or find our work useful, please cite:
@article{li2025,
  title={Mean-Reverting Diffusion Bridge with Projection Prior for Sparse CT Reconstruction},
  author={Li, Yan and Shi, Liu and Liu, Qiegen},
  journal={Computerized Tomography Theory and Applications},
  volume={34},
  number={3},
  pages={356},
  year={2025},
  doi={10.15953/j.ctta.2025.356}
}
