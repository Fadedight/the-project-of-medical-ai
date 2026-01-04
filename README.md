# the-project-of-medical-ai
the project of medical ai

### Pre-training
You can download 16k mpMRI pre-training data on your own or download from the [huggingface repo](https://huggingface.co/datasets/shaohao011/BrainMVP-16k) of the original projiect.
### Downstream
Dataset available at <a href='https://huggingface.co/datasets/shaohao011/BrainMVP-ds/tree/main'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue'></a>

All downstream datasets are open-source.
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

