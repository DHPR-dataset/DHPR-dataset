
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="">
    <img src="images/preview_image.jpg" alt="Logo" width="720">
  </a>

  <h3 align="center">DHPR: Driving Hazard Prediction and Reasoning</h3>

  <p align="center">
    Visual Abductive Reasoning Meets Driving Hazard Prediction
    <br />
    <a href="https://trafficreasoningdatasetimage1.s3.ap-northeast-1.amazonaws.com/DHPR/image_folder.tar.gz"><strong>Download Assets</strong></a> <strong>|</strong>
    <a href="https://huggingface.co/spaces/DHPR/Demo"><strong>Dataset Demo</strong></a> <strong>|</strong>
    <a href="https://huggingface.co/spaces/DHPR/Evaluation_Server"><strong>Evaluation Server</strong></a> <strong>|</strong>
    <a href="https://huggingface.co/spaces/DHPR/inference_demo"><strong>Inference Demo</strong></a>
    <br />
  </p>
</div>
<!--<h3><b>Visual-Abductive-Reasoning-Meets-Driving-Hazard-Prediction</b></h3>-->

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#introduction">Introduction</a>
    </li>
     <li>
      <a href="#Demo">Demo</a>
    </li>
    <li>
      <a href="#DataFiles">Data Files</a>
    </li>
    <li>
      <a href="#Evaluation">Evaluation</a>
    </li>
     <li>
      <a href="#Leaderboard">Leaderboard</a>
    </li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

<!-- INTRODUCTION -->
## Introduction

This repository contains details about the DHPR (Driving Hazard Prediction and Reasoning) dataset. 
The DHPR dataset was introduced to solve the problem of predicting hazards that drivers may encounter while driving a car. We formulate it as visual abductive reasoning using a single input image captured by car dashcams.  

The dataset consists of:
* 14,975 street scenes 
* Car speeds 
* Hazard descriptions
* Visual entity descriptions (Oracle Scenario Only)

<!-- Demo -->
## Demo

Please find more details of the dataset in this <a href="https://huggingface.co/spaces/DHPR/Demo"><strong>Demo</strong></a>. 

<!-- DATA Tree -->
## Data Files

Given the following file tree:
```
annotation_files
├── anno_train.json
└── anno_val.json
```

<!-- Evaluation -->
## Evaluation

To be updated.

<!-- Leaderboard -->
    
## Leaderboard

To submit results, please upload the result file (To be updated).

#### Leaderboard of Results for the image retrieval (IR) and text retrieval (TR) tasks and the generation task on the DHPR test split. The retrieval tasks are evaluated by the average rank and Recall@1. The generation task is evaluated using BLEU (B4), ROUGE (R), CIDEr (C), SPIDER (S), and the GPT-4 score. For all metrics except the rank metric, higher values indicate better performance. For GPT-4V, we perform a zero-shot evaluation on the test split. 

| Model | Visual Encoder | IR Rank | IR R@1| TR Rank | TR R@1 | Text Decoder | B4 | R | C | S | GPT-4 |
| :---: | :---: | :---: | :---: | :---:  | :---: | :---:  | :---: | :---: | :---: | :---: | :---: |
| Random | - | 500 | 500 | 500| 500 | - | - |
| UNITER | Faster R-CNN | 172.3 | 186.5 | 173.8| 181.2 | 74.2 | 71.9|
| BLIP | ViT-B/16 | 153.4 | 172.1 | 151.9 | 176.1 | 78.6 | 72.3|
| Baseline | ViT-B/16 | 77.2 | 75.3 | 78.4 | 73.3 | 81.8 | 79.2|
| Baseline <p>w/ Text Encoders</p> | ViT-B/16 | 75.9 | 73.5 | 73.2 | 68.1 | 82.2 | 80.3|
| Baseline <p>w/ Image Encoders</p> | ViT-B/16 | 74.5 | 72.2 | 79.1 | 69.7 | 81.4 | 80.3|
| Baseline <p>w/ Dual Encoders</p> | ViT-B/16 | 74.8 | 70.2 | 69.2 | 64.3 | 82.9 | 80.4|
| Baseline <p>w/ Dual Encoders</p> | ViT-L/14 | 65.9 | 55.8 | 66.5 | 53.8 | 84.4 | 80.7|


<!-- LICESE -->
## License

The dataset used in this paper is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.





<!-- ### Citation ###

If you find these models useful for your resesarch, please cite with this bibtex.

```

``` -->


