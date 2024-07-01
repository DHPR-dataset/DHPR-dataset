
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="">
    <img src="images/preview_image.jpg" alt="Logo" width="720">
  </a>

  <h3 align="center">Exploring the Potential of Multi-Modal AI for Driving Hazard Prediction</h3>

  <p align="center">
    DHPR: Driving Hazard Prediction and Reasoning
    <br />
    <a href="https://ieeexplore.ieee.org/document/10568360"><strong>Paper</strong></a> <strong>|</strong>
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
| CLIP | ViT-L/14 | 10.8 | 24.1% | 10.9 | 24.8% | - | - | - | - | - | - |
| BLIP | ViT-B/16 | 15.3 | 9.3% | 15.9 | 8.1% | BERT | 12.6 | 32.9| 34.9 | 30.3 | 39.3| 
| BLIP2 | ViT-g/14 | 11.5 | 19.1% | 12.1 | 19.8% | OPT-6.7B | 18.7 | 42.7| 38.9 | 35.4| 50.5| 
| LLaVA-1.5 | ViT-L/14 | - | - | - | - | LLaMA-2 7B | 14.9 | 36.9| 34.5 | 30.9 | 56.2|
| GPT-4V | - | - | - | - | - | GPT-4 | 0.3 | 19.0| 0.9 | 7.2 | 50.0|
| Ours | ViT-L/14 | 10.2 | 24.9% | 10.3 | 26.3% | LLaMA-2 7B | 16.9 | 39.5 | 49.1 | 39.6 | 58.5 |



<!-- LICESE -->
## License
The dataset used in this paper is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.





<!-- ### Citation ### -->
## Citation

```bibtex

@article{10568360,
  author={Charoenpitaks, Korawat and Nguyen, Van-Quang and Suganuma, Masanori and Takahashi, Masahiro and Niihara, Ryoma and Okatani, Takayuki},
  journal={IEEE Transactions on Intelligent Vehicles}, 
  title={Exploring the Potential of Multi-Modal AI for Driving Hazard Prediction}, 
  year={2024},
  volume={},
  number={},
  pages={1-11},
  keywords={Hazards;Cognition;Videos;Automobiles;Accidents;Task analysis;Natural languages;Vision;Language;Reasoning;Traffic Accident Anticipation},
  doi={10.1109/TIV.2024.3417353}
}



