<div align="center">

# Assignment  7- Model Explanability

### Output:
**GradCam**


![](images/output/_0/_dog-2.jpg_gradcam.png)

**GradCam++**


![](images/output/_0/_dog-2.jpg_gradcam_plus_plus.png)

**Gradient SHAP**


![](images/output/_0/_dog-2.jpg_gradient_shap.png)

**IG**


![](images/output/_0/_dog-2.jpg_ig.png)

**IG w/ Noise Tunnel**


![](images/output/_0/_dog-2.jpg_ig_with_noisetunnel.png)

**Robust Perturbation**

![](images/output/_0/_dog-2.jpg_min_robust_perturbation.png)

**Occlusion**


![](images/output/_0/_dog-2.jpg_occlusion.png)

**Captum Model Robustness**


![](images/output/_0/_dog-2.jpg_org_img.png)

**Perturbation**


![](images/output/_0/_dog-2.jpg_perturbed_image.png)

**Salinecy1**


![](images/output/_0/_dog-2.jpg_saliency1.png)

**Saliency2**


![](images/output/_0/_dog-2.jpg_saliency2.png)

**SHAP**


![](images/output/_0/_dog-2.jpg_shap.png)

**PGD**


![](images/output/_0/_dog-2.jpgperturbed_pgd.png)












<a href="https://pytorch.org/get-started/locally/"><img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-ee4c2c?logo=pytorch&logoColor=white"></a>
<a href="https://pytorchlightning.ai/"><img alt="Lightning" src="https://img.shields.io/badge/-Lightning-792ee5?logo=pytorchlightning&logoColor=white"></a>
<a href="https://hydra.cc/"><img alt="Config: Hydra" src="https://img.shields.io/badge/Config-Hydra-89b8cd"></a>
<a href="https://github.com/ashleve/lightning-hydra-template"><img alt="Template" src="https://img.shields.io/badge/-Lightning--Hydra--Template-017F2F?style=flat&logo=github&labelColor=gray"></a><br>
[![Paper](http://img.shields.io/badge/paper-arxiv.1001.2234-B31B1B.svg)](https://www.nature.com/articles/nature14539)
[![Conference](http://img.shields.io/badge/AnyConference-year-4b44ce.svg)](https://papers.nips.cc/paper/2020)

</div>

## Description

Experiment that explains how the model predicts.

## How to run

Install dependencies

```bash
# clone project
git clone https://github.com/sushant097/TSAI-Assignment4-Deployment-for-Demos
cd TSAI-Assignment4-Deployment-for-Demos

# [OPTIONAL] create conda environment
conda create -n myenv python=3.9
conda activate myenv

# install pytorch according to instructions
# https://pytorch.org/get-started/

# install requirements
pip install -r requirements.txt
```

Train model with default configuration

```bash
# train on CPU
python src/train.py trainer=cpu

# train on GPU
python src/train.py trainer=gpu
```

Train model with chosen experiment configuration from [configs/experiment/](configs/experiment/)

```bash
python src/train.py experiment=experiment_name.yaml
```

You can override any parameter from command line like this

```bash
python src/train.py trainer.max_epochs=20 datamodule.batch_size=64
```

### Assignment Related
See on `ModelExplanability/`