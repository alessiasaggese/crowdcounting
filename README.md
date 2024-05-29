# CrowdCounting-CL

This repository contains the code for the Curriculum Learning (CL) based algorithm for crowd counting, as described in our paper "Optimizing Crowd Counting in Dense Environments through Curriculum Learning Training Strategy".

If you use it, please cite it:

```bibtext
@article{,
  title={Optimizing Crowd Counting in Dense Environments through Curriculum Learning Training Strategy},
  author={Fotia, Lidia and Percannella, Gennaro and Saggese, Alessia and Vento, Mario},
  journal={SN Computer Science},
  pages={},
  year={2024},
  organization={SpringerNature}
}

```

## Proposed methodologies

An overview of the proposed CL based framework is depicted in the following figure: for each sample in the dataset, a scoring function is used so as to assign a complexity indicator to each image of the dataset. As the training evolves, epochs by epochs, a pacing function determines the composition of the training at each step.

![alt text](https://github.com/MiviaLab/.../CL.png)

The baseline we used in our approach is P2P network. [Paper Link](https://openaccess.thecvf.com/content/ICCV2021/papers/Song_Rethinking_Counting_and_Localization_in_Crowds_A_Purely_Point-Based_Framework_ICCV_2021_paper.pdf)

## An example 


![alt text](https://github.com/MiviaLab/.../example.png)

First Row [(a) Ground Truth: 88 persons; (b) P2P output: 98; (c) CLN D output: 94] 
Second Row [(d) Ground Truth: 130 persons; (e) P2P output: 215; (f) CLN D output: 137] 
Third Row [(g) Ground Truth: 1659 persons; (h) P2P output: 1379; (i) CLN D output: 1746]

## Installation

- Clone this repo into a directory named CL_Framework
- Organize your datasets as required
- Install Python dependencies. 

```bash
pip install -r requirements.txt
```



## Usage
The proposed model is available at "./ckpt_index". 
The network can be tested on image or video using `run_test.py` script. For the mode of evaluation (--mode), use image for images and video for videos.  
Note that you must update the path of image or video. To evaluate the model, run the following command:

```bash
CUDA_VISIBLE_DEVICES=0 python run_test.py --mode ‘insert image or video’ 
```
