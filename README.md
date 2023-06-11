
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
    <a href=""><strong>Evaluation Server</strong></a>
    <br />
  </p>
</div>
<!--<h3><b>Visual-Abductive-Reasoning-Meets-Driving-Hazard-Prediction</b></h3>-->
<a href="https://github.com/DHPR-dataset/Visual-Abductive-Reasoning-Meets-Driving-Hazard-Prediction"><strong> DHPR dataset</strong> </a> <br>


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
      <a href="#Evaluation">Evaluation</a>
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
    Link
    ```
4. Obtain the performance results as shown in the example below.
    ```
    {
    }
    ```
<!-- LICESE -->
## License

The dataset used in this paper is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.





### Citation ###

If you find these models useful for your resesarch, please cite with this bibtex.

```

```


