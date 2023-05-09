<div align="center">
<!-- <h1>Predictive_Analysis_of_Parkinsons_Disease_from_Gait_Sensor_Data_and_Brain_MRI_Images: Predictive Analysis of Parkinsons Disease from Gait Sensor Data and Brain MRI Images</h1> -->
<h2><a href="https://arxiv.org/abs/2211.03295">Efficient Multi-order Gated Aggregation Network</a></h2>

[Arunava Chaudhuri](https://lupin1998.github.io/)<sup>\*,1,2</sup>, [Zedong Wang](https://zedongwang.netlify.app/)<sup>\*,1</sup>, [Zicheng Liu](https://pone7.github.io/)<sup>1,2</sup>, [Chen Tan](https://chengtan9907.github.io/)<sup>1,2</sup>, [Haitao Lin](https://bird-tao.github.io/)<sup>1,2</sup>, [Di Wu](https://scholar.google.com/citations?user=egz8bGQAAAAJ&hl=zh-CN)<sup>1,2</sup>, [Zhiyuan Chen](https://zyc.ai/)<sup>1</sup>, [Jiangbin Zheng](https://scholar.google.com/citations?user=egz8bGQAAAAJ&hl=zh-CN)<sup>1,2</sup>, [Stan Z. Li](https://scholar.google.com/citations?user=Y-nyLGIAAAAJ&hl=zh-CN)<sup>†,1</sup>

<sup>1</sup>[Westlake University](https://westlake.edu.cn/), <sup>2</sup>[Zhejiang University](https://www.zju.edu.cn/english/)
</div>

<p align="center">
<a href="https://arxiv.org/abs/2211.03295" alt="arXiv">
    <img src="https://img.shields.io/badge/arXiv-2211.03295-b31b1b.svg?style=flat" /></a>
<a href="https://github.com/Westlake-AI/MogaNet/blob/main/LICENSE" alt="license">
    <img src="https://img.shields.io/badge/license-Apache--2.0-%23B7A800" /></a>
<a href="https://colab.research.google.com/github/Westlake-AI/MogaNet/blob/main/demo.ipynb" alt="Colab">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" /></a>
<a href="https://huggingface.co/MogaNet" alt="Huggingface">
    <img src="https://img.shields.io/badge/huggingface-MogaNet-blueviolet" /></a>
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44519745/202308950-00708e25-9ac7-48f0-af12-224d927ac1ae.jpg" width=100% height=100% 
class="center">
</p>

Within the modern ConvNet framework, we tailor the two feature mixers with conceptually simple yet effective depthwise convolutions to facilitate middle-order information across spatial and channel spaces respectively. We propose **MogaNet**, a new family of efficient ConvNets, to pursue informative context mining with preferable complexity-performance trade-offs, which shows excellent scalability and attains competitive results among state-of-the-art models with more efficient use of parameters on ImageNet and multifarious typical vision benchmarks, including COCO object detection, ADE20K semantic segmentation, 2D\&3D human pose estimation, and video prediction.

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#catalog">Catalog</a></li>
    <li><a href="#image-classification">Image Classification</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgement">Acknowledgement</a></li>
    <li><a href="#citation">Citation</a></li>
  </ol>
</details>

## Catalog

We plan to release implementations of MogaNet in a few months. Please watch us for the latest release. Currently, this repo is reimplemented according to our official implementations in [OpenMixup](https://github.com/Westlake-AI/openmixup), and we are working on cleaning up experimental results and code implementations. Models are released in [GitHub](https://github.com/Westlake-AI/MogaNet/releases) / [Baidu Cloud](https://pan.baidu.com/s/1d5MTTC66gegehmfZvCQRUA?pwd=z8mf) / [Hugging Face](https://huggingface.co/MogaNet).

- [x] **ImageNet-1K** Training and Validation Code with [timm](https://github.com/rwightman/pytorch-image-models) [[code](#image-classification)] [[models](https://github.com/Westlake-AI/MogaNet/releases/tag/moganet-in1k-weights)] [[Hugging Face 🤗](https://huggingface.co/MogaNet)]
- [x] **ImageNet-1K** Training and Validation Code in [OpenMixup](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/moganet) / [MMPretrain (TODO)](https://github.com/open-mmlab/mmpretrain)
- [x] Downstream Transfer to **Object Detection and Instance Segmentation on COCO** [[code](detection/)] [[models](https://github.com/Westlake-AI/MogaNet/releases/tag/moganet-det-weights)]
- [x] Downstream Transfer to **Semantic Segmentation on ADE20K** [[code](segmentation/)] [[models](https://github.com/Westlake-AI/MogaNet/releases/tag/moganet-seg-weights)]
- [x] Downstream Transfer to **2D Human Pose Estimation on COCO** [[code](pose_estimation/)] (baseline models are supported)
 - [ ] Downstream Transfer to **3D Human Pose Estimation** (baseline models will be supported) <!--[[code](human_pose_3d/)] (baseline models will be supported) -->
- [x] Downstream Transfer to **Video Prediction on MMNIST** [[code](video_prediction/)] (baseline models are supported)
- [x] Image Classification on Google Colab and Notebook Demo [[here](demo.ipynb)]


## Image Classification

### 1. Installation

Please check [INSTALL.md](INSTALL.md) for installation instructions.

### 2. Training and Validation

See [TRAINING.md](TRAINING.md) for ImageNet-1K training and validation instructions, or refer to our [OpenMixup](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/moganet/) implementations. We released pre-trained models on [OpenMixup](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/moganet/) in [moganet-in1k-weights](https://github.com/Westlake-AI/openmixup/releases/tag/moganet-in1k-weights). We have also reproduced ImageNet results with this repo and released `args.yaml` / `summary.csv` / `model.pth.tar` in [moganet-in1k-weights](https://github.com/Westlake-AI/MogaNet/releases/tag/moganet-in1k-weights). The parameters in the trained model can be extracted by [code](extract_ckpt.py).

Here is a notebook [demo](demo.ipynb) of MogaNet which run the steps to perform inference with MogaNet for image classification.

### 3. ImageNet-1K Trained Models

| Model | Resolution | Params (M) | Flops (G) | Top-1 / top-5 (%) | Script | Download |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| MogaNet-XT | 224x224 | 2.97 | 0.80 | 76.5 \| 93.4 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz224_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz224_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz224_8xbs128_ep300_summary.csv) |
| MogaNet-XT | 256x256 | 2.97 | 1.04 | 77.2 \| 93.8 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz256_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz256_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xtiny_sz256_8xbs128_ep300_summary.csv) |
| MogaNet-T | 224x224 | 5.20 | 1.10 | 79.0 \| 94.6 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz224_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz224_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz224_8xbs128_ep300_summary.csv) |
| MogaNet-T | 256x256 | 5.20 | 1.44 | 79.6 \| 94.9 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz256_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz256_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_tiny_sz256_8xbs128_ep300_summary.csv) |
| MogaNet-T\* | 256x256 | 5.20 | 1.44 | 80.0 \| 95.0 | [config](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/moganet/moga_tiny_deit3_sz256_lr2e_3_8xb128_fp16_ep300.py) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/openmixup/releases/download/moganet-in1k-weights/moga_tiny_deit3_sz256_lr2e_3_8xb128_fp16_ep300.pth) \| [log](https://github.com/Westlake-AI/openmixup/releases/download/moganet-in1k-weights/moga_tiny_deit3_sz256_lr2e_3_8xb128_fp16_ep300.log.json) |
| MogaNet-S | 224x224 | 25.3 | 4.97 | 83.4 \| 96.9 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_small_sz224_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_small_sz224_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_small_sz224_8xbs128_ep300_summary.csv) |
| MogaNet-B | 224x224 | 43.9 | 9.93 | 84.3 \| 97.0 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_base_sz224_8xbs128_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_base_sz224_8xbs128_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_base_sz224_8xbs128_ep300_summary.csv) |
| MogaNet-L | 224x224 | 82.5 | 15.9 | 84.7 \| 97.1 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_large_sz224_8xbs64_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_large_sz224_8xbs64_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_large_sz224_8xbs64_ep300_summary.csv) |
| MogaNet-XL | 224x224 | 180.8 | 34.5 | 85.1 \| 97.4 | [args](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xlarge_sz224_8xbs64_ep300_args.yaml) \| [script](TRAINING.md) | [model](https://github.com/Westlake-AI/MogaNet/releases/download/moganet-in1k-weights/moganet_xlarge_sz224_8xbs64_ep300.pth.tar) \| [log](https://github.com/Westlake-AI/openmixup/releases/download/moganet-in1k-weights/moga_xlarge_ema_sz224_8xb32_accu2_ep300.log.json) |

### 4. Analysis Tools

(1) The [code](get_flops.py) to count MACs of MogaNet variants.

```
python get_flops.py --model moganet_tiny
```
<p align="center">
<img src="https://user-images.githubusercontent.com/44519745/212429257-f0b09d7a-7503-4945-9517-68ea36d10e00.png" width=100% height=100% 
class="center">
</p>

(2) The [code](cam_image.py) to visualize Grad-CAM activation maps (or variants of Grad-CAM) of MogaNet and other popular architectures.

```
python cam_image.py --use_cuda --image_path /path/to/image.JPEG --model moganet_tiny --method gradcam
```

<p align="right">(<a href="#top">back to top</a>)</p>

## License

This project is released under the [Apache 2.0 license](LICENSE).

## Acknowledgement

Our implementation is mainly based on the following codebases. We gratefully thank the authors for their wonderful works.

- [pytorch-image-models (timm)](https://github.com/rwightman/pytorch-image-models): PyTorch image models, scripts, pretrained weights.
- [PoolFormer](https://github.com/sail-sg/poolformer): Official PyTorch implementation of MetaFormer.
- [ConvNeXt](https://github.com/facebookresearch/ConvNeXt): Official PyTorch implementation of ConvNeXt.
- [OpenMixup](https://github.com/Westlake-AI/openmixup): Open-source toolbox for visual representation learning.
- [MMDetection](https://github.com/open-mmlab/mmdetection): OpenMMLab Detection Toolbox and Benchmark.
- [MMSegmentation](https://github.com/open-mmlab/mmsegmentation): OpenMMLab Semantic Segmentation Toolbox and Benchmark.
- [MMPose](https://github.com/open-mmlab/mmpose): OpenMMLab Pose Estimation Toolbox and Benchmark.
- [MMHuman3D](https://github.com/open-mmlab/mmhuman3d): OpenMMLab 3D Human Parametric Model Toolbox and Benchmark.

## Citation

If you find this repository helpful, please consider citing:
```
@article{Li2022MogaNet,
  title={Efficient Multi-order Gated Aggregation Network},
  author={Siyuan Li and Zedong Wang and Zicheng Liu and Cheng Tan and Haitao Lin and Di Wu and Zhiyuan Chen and Jiangbin Zheng and Stan Z. Li},
  journal={ArXiv},
  year={2022},
  volume={abs/2211.03295}
}
```

<p align="right">(<a href="#top">back to top</a>)</p>
