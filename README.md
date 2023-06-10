
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
    <a href="https://trafficreasoningdatasetimage1.s3.ap-northeast-1.amazonaws.com/DHPR/image_folder.tar.gz"><strong>Download Assets »</strong></a>
    <br />
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
      <a href="#Evaluation">Evaluation</a>
    </li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

<!-- INTRODUCTION -->
## Introduction

This repository contains details about the DHPR (Driving Hazard Prediction and Reasoning) dataset. 
The DHPR dataset was introducted to solve the problem of predicting hazards that drivers may encounter while driving a car. We formulate it as visual abductive reasoning using a single input image captured by car dashcams. 

The dataset consists of:
* 14,975 street scenes 
* Car speeds 
* Hazard descriptions
* Visual entity descriptions

<!-- Evaluation -->
## Evaluation

This is an evaluation section which guide you how to evaluate with our test dataset. You will be using our prepared evaluation files to run the model. You can give us both image and text embedding token in the given format. Then, upload the file and you will be given the performance of your model.

1. Download the evaluation files in the annonation_files folder.
   ```
   eval_test_image.json
   eval_test_text.json
   ```
2. Run model to obtain image and text embedding in the following format.
    ```
    
    ```




3. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```




<!-- LICESE -->
## License

The dataset used in this paper is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.





### Citation ###

If you find these models useful for your resesarch, please cite with this bibtex.

```

```


