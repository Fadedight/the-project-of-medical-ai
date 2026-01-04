# the-project-of-medical-ai
the project of medical ai
# BrainMVP 
<a href="https://arxiv.org/abs/2410.10604"><img src='https://img.shields.io/badge/arXiv-BrainMVP-red' alt='Paper PDF'></a>
<a href='https://huggingface.co/datasets/shaohao011/BrainMVP-16k'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue'></a>

Code for our CVPR 2025 paper[Highlight] [Multi-modal Vision Pre-training for Medical Image Analysis](https://arxiv.org/abs/2410.10604)

> ⚠️ **For complete setup instructions and to explore issues raised by other users, please visit our official GitHub repository: [shaohao011/BrainMVP](https://github.com/shaohao011/BrainMVP).**

[openmedlab](https://github.com/openmedlab/BrainMVP)
TL;DR

This work introduces BrainMVP, the first pre-training framework designed for large-scale missing modality medical imaging. We have made available the pre-training 16k mpMRI images and corresponding pretrained models.

We achieve state-of-the-art performance on 10 open-source segmentation and classification tasks. Feel free to use it to adapt to your own tasks!


## Datasets
![dataset](assets/dataset.png)
### Pre-training
You can download our 16k mpMRI pre-training data on your own or download from our [huggingface repo](https://huggingface.co/datasets/shaohao011/BrainMVP-16k).
### Downstream
Dataset available at <a href='https://huggingface.co/datasets/shaohao011/BrainMVP-ds/tree/main'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue'></a>

All downstream datasets are open-source. If you encounter any difficulties downloading them, please feel free to email ruishaohao@sjtu.edu.cn to request access.
## Get Started

**Installation**
```bash
conda create -n brainmvp python=3.9
conda activate brainmvp
pip install -r requirements.txt
```

**Download Model**

We prepare two varients of our pre-trained models [Uniformer (recommend)](https://drive.google.com/file/d/1DTmz5WACESD0wfkZ2r0x-zjTwOgd9ov3/view?usp=drive_link) and [Unet](https://drive.google.com/file/d/16DvqjYBfenNEdggLu2fXuMJ6FjxBxQsS/view?usp=drive_link).


**Pre-train**
```bash 
CUDA_VISIBLE_DEVICES=0,1,2,3 bash do_pretrain.sh
```
**Finetune**

We provide example code for fine-tuning on the BraTS-PED dataset, which you can modify to suit your own task.
```bash 
# train
cd Downstream
bash do_train.sh
# test
bash do_test.sh
```

## 🙏 Acknowledgement

A lot of code is modified from [MONAI](https://github.com/Project-MONAI/MONAI).

## 📝 Citation
