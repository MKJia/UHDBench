
# Dataset Card for Dataset Name

<!-- Provide a quick summary of the dataset. -->
Ultra-high definition benchmark for zero-shot image reconstruction evaluation.


## Dataset Description

<!-- Provide a longer summary of what this dataset is. -->

- **Total images:** 2 293 at 2K resolution  
- **Source datasets:** HRSOD, LIU4k, UAVid, UHDM, UHRSD  
- **Resolution filter:** Only images ≥ 2560 × 1440 included  
- **Purpose:** Zero-shot image reconstruction benchmarking.
- **license**: cc-by-sa-4.0

### Dataset Sources

- **Repository:** [https://github.com/MKJia/MGVQ](https://github.com/MKJia/MGVQ)
- **Paper:** [https://arxiv.org/abs/2507.07997](https://arxiv.org/abs/2507.07997)
- **Dataset Repository:** [https://github.com/MKJia/UHDBench](https://github.com/MKJia/UHDBench)


## Dataset Leaderboard
**Call for Submissions!**
We're continuously expanding our public benchmark leaderboard and welcome contributions from the community.

Feel free to suggest other VQVAEs or VAEs. We're happy to assist with the evaluation. We also invite you to share your reconstruction results to be included in our leaderboard.
| Method | Type  | Ratio | rFID↓ | PSNR↑ |
|--------|:-----:|:-----:|:-----:|:-----:|
|  SD-VAE  | Continuous |  16  | **1.07**  | <ins>26.86</ins>  |
|  VQGAN  | Discrete |  16  | 5.95  | 22.91  |
|  LlamaGen  | Discrete |  16  | 5.59  | 23.90  |
|  OpenMagvit2  | Discrete |  16  | 4.18  | 23.91  |
|  VAR  | Discrete |  16  | 9.85  | 21.79  |
|  MGVQ-f16c32-g4  | Discrete |  16  | <ins>1.59</ins>  | **28.27**  |

<image src="./assets/recon_tab_3.jpg"/>
<image src="./assets/recon_qual.png"/>

## Dataset Structure

<!-- This section provides a description of the dataset fields, and additional information about the dataset structure such as criteria used to create the splits, relationships between data points, etc. -->

UHDBench/  
├── HRSOD_release/  
├── LIU4k/  
├── uavid_test/  
├── UHDM/  
├── HRSD_TE/  
└── UHDBench.json # json file for image sources and paths

## Dataset Creation

#### Source data producers

<!-- This section describes the people or systems who originally created the data. It should also include self-reported demographic or identity information for the source data creators if this information is available. -->
- **HRSOD & UHRSD:**
  By Xie et al. in “Pyramid Grafting Network for One-Stage High Resolution Saliency Detection” 
- **LIU4K:**
  By Liu et al. in “A Comprehensive Benchmark for Single Image Compression Artifact Reduction” 
- **UAVid:**
  By Lyuet al. in “UAVid: A semantic segmentation dataset for UAV imagery” 
- **UHDM:**
  By Yu et al. in “Towards efficient and scale-robust ultra-high-definition image demoireing”

### Source Data Licenses

- **HRSOD & UHRSD:** MIT
- **LIU4K:** CC0
- **UAVid:** CC-BY-SA-4.0
- **UHDM:** Apache 2.0


## Citation

<!-- If there is a paper or blog post introducing the dataset, the APA and Bibtex information for that should go in this section. -->
Please consider staring UHDBench&MGVQ and citing the following paper if you feel this dataset useful.  
```bibtex
@article{jia2025mgvq,
  title={MGVQ: Could VQ-VAE Beat VAE? A Generalizable Tokenizer with Multi-group Quantization},
  author={Jia, Mingkai and Yin, Wei and Hu, Xiaotao and Guo, Jiaxin and Guo, Xiaoyang and Zhang, Qian and Long, Xiao-Xiao and Tan, Ping},
  journal={arXiv preprint arXiv:2507.07997},
  year={2025}
}
```


