# Ascending_neuron_screen_analysis_pipeline
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Version](https://badge.fury.io/gh/tterb%2FHyde.svg)](https://badge.fury.io/gh/tterb%2FHyde)

This repository is for generating the figures published in the paper of **Ascending neurons convey high-level behavioral-state signals to multimodal sensory and action selection centersin the Drosophila brain**.
 
## Content
- [Installation](#installation)
- [Reproducing the figures](#reproducing-the-figures)
 

## Installation
**1. To be able to execute the codes and NeLy homemade packages, install the python environment** ```AN``` **as guided below:**
- Change directory to your ```/Ascending_neuron_screen_analysis_pipeline``` where ```AN_env_public.yml``` locates by:
```bash
$ cd ../../Ascending_neuron_screen_analysis_pipeline
```
- Install the python environment with specified package in AN_env_public.yml
```bash
$ conda env create -f AN_env_public.yml
```
 
**2. Install [NeLy](https://github.com/NeLy-EPFL)'s homemade packages of deepfly, df3dPostProcess, flydf, utils2p in** ```AN``` **environment as guided below:**

- Activate to the AN environemnt:
```bash
$ source activate AN
```
or if ```source``` doesn't work, try:
```bash
$ conda activate AN
```

- Dowload and install deepfly3d:
```bash
$ pip install git+https://github.com/NeLy-EPFL/DeepFly3D.git@974f839e224a41e7c5774e2effddf8ff763da88a#egg=deepfly
```

- Dowload and install df3dPostProcess:
```bash
$ pip install git+https://github.com/NeLy-EPFL/df3dPostProcessing.git@b6be9b0587db55023bb41858c6b49d4e11a98e9f#egg=df3dPostProcessing
```

- Dowload and install flydf:
```bash
$ pip install git+https://github.com/NeLy-EPFL/flydf.git@5d8dc3979b565c87809c75022208623310d4ca82#egg=flydf
```

- Dowload and install utils2p:
```bash
$ pip install git+https://github.com/NeLy-EPFL/utils2p.git@0f155bd3357d3fdf82e1e20605a6948d2a47fd75#egg=utils2p
```
- Leave the environment:
```bash
$ conda deactivate
```
 
**3. Install CPU version of DeepLabCut used in this paper in its own environment (make sure leave** ```AN``` **environment by** ```conda deactivate``` **before the following steps)**
- Downlaod and install DeepLabCut:
```bash
git clone git+https://github.com/DeepLabCut/DeepLabCut.git@413ae5e2c410fb9da3da26c333b6a9b87ab6c38f#egg=deeplabcut
```
- Change direcotry to ```/conda-environments``` where the ```DLC-CPU.yaml``` locates:
```bash
cd ../../DeepLabCut/conda-environments
```
- Create DLC-CPU environment and install CPU version of DeepLabCut:
```bash
conda env create -f DLC-CPU.yaml
```

Now, the dependencies of ```AN``` environment and DeepLabCut are installed.
If you need to use DeepLabCut independently, please activate the environment manually by:
```bash
source activate DLC-CPU
```

If you need to use AN independently, please activate ```AN``` environment manually by:
```bash
source activate AN
```
 
## Reproducing the figures

**Note:** before running the following scripts, please be sure to the python environment and R package are installed (see the installation guide)







