
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="">
    <img src="images/preview_image.jpg" alt="Logo" width="720">
  </a>

  <h3 align="center">DHPR: Driving Hazard Prediction and Reasoning</h3>

  <p align="center">
    Visual Abductive Reasoning Meets Driving Hazard Prediction: Problem Formulation and  Dataset
    <br />
    <a href="https://trafficreasoningdatasetimage1.s3.ap-northeast-1.amazonaws.com/DHPR/image_folder.tar.gz"><strong>Download Assets</strong></a> <strong>|</strong>
    <a href="https://huggingface.co/spaces/DHPR/Demo"><strong>Dataset Demo</strong></a> <strong>|</strong>
    <a href="https://huggingface.co/spaces/DHPR/Evaluation_Server"><strong>Evaluation Server</strong>|</a>
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
* Visual entity descriptions

<!-- Demo -->
## Demo

Please find more details of the dataset in this <a href="https://huggingface.co/spaces/DHPR/Demo"><strong>Demo</strong></a>. 

<!-- DATA Tree -->
## Data Files

Given the following file tree:
```
annotation_files
├── anno_train.json
├── anno_val_direct.json
└── anno_val_indirect.json
```

<!-- Evaluation -->
## Evaluation

This is an evaluation section that guides you on how to evaluate benchmarking on our system with the test dataset. You will be using our prepared evaluation files to run the model. You can give us both image and text embedding tokens in the given format. Then, upload the file and you will be given the performance of your model.

1. Download the evaluation files in the annonation_files folder.
   ```
   annotation_files/eval_test_image.json
   annotation_files/eval_test_text.json
   ```
2. Run model and output the result image and text embedding in the following dictionary format. 
The evaluation script for baseline CLIP-based model is also provided in the evaluation folder.
    ```
    {'857729eb-3dcb8ec9:9b2a56310bf10f2032145bbf503d4543': 0.7750905,
     '857729eb-3dcb8ec9:f908aaf7cfb390e5ea938452e3916a65': 0.81745917,
     '857729eb-3dcb8ec9:89d9cb127c5a1fd8519554772366182a': 0.8823063,
     .....
    }
    ```
3. Upload the output embedding dictionary to our evaluation server at 
    ```
    https://huggingface.co/spaces/DHPR/Evaluation_Server
    ```
4. Obtain the performance results as shown in the example below.
    ```
    {
    "direct": {"i2t rank": 82.026, "t2i rank": 66.033, "ndcg score": 0.829821706142076}, 
    "indirect": {"i2t rank": 52.1475, "t2i rank": 68.077, "ndcg score": 0.8046468245315274}
    }
    ```
<!-- Leaderboard -->
    
## Leaderboard

To submit results, please upload the result file <a href="https://forms.gle/EfTiKoB1QWJRcGRh6"><strong>here</strong></a>. 

#### Comparison of average rank of GT texts and NDCG score on test split for both direct and indirect hazard type. Lower ranks indicate better performance, while higher NDCG scores indicate better. Noted that the ranking is compared with random sampled 1000 data samples within the same data split.

| Model | Visual Encoder |Direct <p>T2I</p>| Indirect <p>T2I</p>| Direct <p>I2T</p>| Indirect <p>I2T</p> | NDCG <p>Direct <br> I2T </p> | NDCG <p>Indirect<br> I2T </p> |
| :---:   | :---: | :---: | :---: | :---:  | :---: | :---:  | :---: |
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


