# 医学人工智能项目《多模态视觉预训练用于医学图像分析》
the project of medical ai

### Pre-training
你可以自行下载1.6万mpMRI预训练数据，或是从原项目的 [huggingface repo](https://huggingface.co/datasets/shaohao011/BrainMVP-16k) 中下载。
### Downstream
数据集可在原项目的huggingface中访问 <a href='https://huggingface.co/datasets/shaohao011/BrainMVP-ds/tree/main'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue'></a>

所有下游数据集都是开源的。
## 环境配置

**安装**
```bash
conda create -n brainmvp python=3.9
conda activate brainmvp
pip install -r requirements.txt
```

**下载模型**

我们准备了两种预训练模型 [Uniformer (recommend)](https://drive.google.com/file/d/1DTmz5WACESD0wfkZ2r0x-zjTwOgd9ov3/view?usp=drive_link)和 [Unet](https://drive.google.com/file/d/16DvqjYBfenNEdggLu2fXuMJ6FjxBxQsS/view?usp=drive_link).


**预训练**
因为此项目核心为预训练项目，所以这里专门写了一个脚本来运行预训练代码，详情请参考项目文件中的do_pretrain.sh文件
```bash 
CUDA_VISIBLE_DEVICES=0,1,2,3 bash do_pretrain.sh
```
**微调**

提供了 BraTS-PED 数据集的微调示例代码，您可以根据自己的任务进行修改。
```bash 
# train
cd Downstream
bash do_train.sh
# test
bash do_test.sh
```
