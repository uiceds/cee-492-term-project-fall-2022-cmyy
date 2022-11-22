---
title: Concrete Crack Detection
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-11-22'
author-meta:
- Yu-Sian Lin
- Yueh-Ti Lee
- Minjiang Zhu
- Chengyou Yue
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Concrete Crack Detection" />
  <meta name="citation_title" content="Concrete Crack Detection" />
  <meta property="og:title" content="Concrete Crack Detection" />
  <meta property="twitter:title" content="Concrete Crack Detection" />
  <meta name="dc.date" content="2022-11-22" />
  <meta name="citation_publication_date" content="2022-11-22" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Yu-Sian Lin" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <meta name="citation_author" content="Yueh-Ti Lee" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <meta name="citation_author" content="Minjiang Zhu" />
  <meta name="citation_author_institution" content="Department of Something, University of Illinois" />
  <meta name="citation_author" content="Chengyou Yue" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/cc834f230f3dfd8b456057542d72999a2ce35455/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/cc834f230f3dfd8b456057542d72999a2ce35455/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/cc834f230f3dfd8b456057542d72999a2ce35455/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...

## Authors



+ **Yu-Sian Lin**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [yslin0114](https://github.com/yslin0114)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>

+ **Yueh-Ti Lee**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Yueh-Ti](https://github.com/Yueh-Ti)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>

+ **Minjiang Zhu**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Minjiang-Zhu](https://github.com/Minjiang-Zhu)<br>
  <small>
     Department of Something, University of Illinois
  </small>

+ **Chengyou Yue**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [TensorYue](https://github.com/TensorYue)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>









## Description

In this project, we plan to use two main datasets to detect concrete crack. First, we use a dataset from Kaggle, titled “Surface Crack Detection” to make the classification of the concrete crack. Second, we use a dataset from Virginia Tech, titled “Concrete Crack Conglomerate Dataset” to make the segmentation of the concrete crack.

[Classification]

Source: Kaggle/ Surface Crack Detection.

Data Format: Images with 227*227 pixels with RGB channels.

Content: The dataset contains images of various concrete surfaces with and without crack. The image data are divided into two as negative (without crack) and positive (with crack) for image classification. Each class has 20000 images with a total of 40000 images.

![Figure 1](../fig1_neg_1.png)
![Figure 2](../fig2_pos_1.png)

Figure 1. Example of Images with and without Cracks



[Segmentation]

Source: Virginia Tech/ Concrete Crack Conglomerate Dataset

Data Format: Images with 448*448 pixels with RGB channels

Content: The dataset contains over 10,995 crack images. Each image data has its origin image and mask image for image segmentation.

![Figure 3](../fig3_ori_1.png)
![Figure 4](../fig4_segged_1.png)

Figure 2. Example of an Original Image and an Mask Image


## Proposal:

In our project, we plan to train two models to detect concrete crack. First, by using the classification dataset, we plan to detect concrete crack based on convolutional neural network (CNN) to find out whether the concrete is defective. Second, by using the segmentation dataset, we plan to conduct concrete crack segmentation based on U Net to illustrate the position of the crack on concrete crack images.


## Exploratory Data Analysis

In classification, the dataset consists of 20,000 images with cracks and 20,000 images without cracks. We are planning to use convolutional neural network to train a classification model.
![Figure 5](../fig5_plot_cla.png)

Figure 3. Number of Images with and without Cracks

In segmentation, we use the dataset consists of 21,996 images, splitting it into train data with 19,801 images and train data with 2,195 images. Here, we’ll be applying U Net to train a model that is capable of pointing out the cracks in a concrete image.
![Figure 6](../fig6_plot_seg.png)

Figure 4. Number of Train Images and Test Images


## Preliminary Predictive Modeling

Dataset: 
- Concrete images with attached label 'Positive' or 'Negative'
- Concrete images and their masks

Goal:
- Concrete crack detection
- Concrete crack segmentation

Architecture:
- Concrete crack detection based on convolutional neural network (CNN)
- Concrete crack segmentation based on U-Net and improved U-Net using Inception as backbone

## Concrete Crack Detection 

![
**Basic Convolutional Neural Network for Classification.**
](./images/Basic_Convolutional_Neural_Network_for_Classification.png "Wide image"){#fig:Basic_Convolutional_Neural_Network_for_Classification}

### Model and training 
Here we need to specify the hyperparameters of our layers:
  1. Convolutional layer. Convolution is an operation that use filter to extract information that we want to detect. 
      a. Filter size determines how many filters that would apply on the input tensor to produce the same number of channels, each filter could detect their specified geometries with colors in the given kernel size. 
      b. Kernel size determines the size of the area the filters would apply. 
      c. Activation function is added to achieve nonlinearity of the model, as the operation of filter is linear.
  3. MaxPooling layer. MaxPooling is a down-sampling operation that allows our network to capture deeper information from original dimensions. 
      a. Pool size and strides determine the dimensions of down-sample procedure. 
     
In the first convolutional block, we would specify 16 filters (consider 8 straight lines and 8 curves) with 3 by 3 kernel (consider the size of crack is relatively small) and ReLu as activation function in the Conv2D layer and go deeper with pool size of 2 by 2 in the MaxPool2D layer.

And in the second convolutional block, we double the channels number to 32 with Conv2D, apply the same MaxPool2D.

Finally, we process our data input an GlobalAveragePooling2D layer (because we are focusing on the whole image, not a part of it in segmentation) and dense the tensor to 1 with Sigmoid function (As we only have 1 class of result, for multiclass classification, use SoftMax).

The result of our network would be a number in (0,1), we could treat this as a probability of crack in the image.

![
**Model_for_Concrete_Crack_Classification_using_Keras.**
](./images/Model_for_Concrete_Crack_Classification_using_Keras.png "Wide image"){#fig:Model_for_Concrete_Crack_Classification_using_Keras}

Notice that the original images have size of (227,227,3), we would resize it into (120,120,3) in preprocess procedure.

![
**Model_Summary_and_Hyperparameters.**
](./images/Model_Summary_and_Hyperparameters.png "Wide image"){#fig:Model_Summary_and_Hyperparameters}

| Properties | Value |
|:-----------|:------|
| training   | 3360 |
| validation | 840  |
| testing    | 1800 |
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Metrics | Accuracy |
| Epochs | 100 | 

Table: Hyperparameters.
{#tbl:CNNHyperparameters}

### Prediction and Analysis 

We can check our trained model by inputting the testing data, below is the confusion matrix our model generated:

![
**Confusion Matrix.**
](./images/Confusion_Matrix.png "Square image"){#fig:Confusion_Matrix}

![
**Loss Evolution.**
](./images/Loss_Evolution.png "Tall image"){#fig:Loss_Evolution height=5in}

We can see that this trained model has good performance on the testing data, it only takes 25 epochs because of our early stop condition.
We can further calculate the following parameters:

$$
\mathrm{Precision}=\frac{TP}{TP+FP}
\\
\mathrm{Recall}=\frac{TP}{TP+FN}
\\
\mathrm{Score}=2\times \frac{\mathrm{Precision}\times \mathrm{Recall}}{\mathrm{Precision}+\mathrm{Recall}}
\\
\mathrm{Macro} \mathrm{Avg}=\frac{1}{n}\sum_{i=1}^n{\mathrm{Score}_i}
\\
\mathrm{Weighted} \mathrm{Avg}=\frac{1}{n}\sum_{i=1}^n{\mathrm{Support}_i\times \mathrm{Score}_i}
$${#eq:regular-equation}

















## References

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

[Surface Crack Detection | Kaggle](https://www.kaggle.com/datasets/arunrk7/surface-crack-detection) 

[Concrete Crack Conglomerate Dataset | Virginia Tech](https://data.lib.vt.edu/articles/dataset/Concrete_Crack_Conglomerate_Dataset/16625056)

[Computer Vision-based Concrete Crack Detection using U-net Fully Convolutional Networks](https://doi.org/10.1016/j.autcon.2019.04.005) 

[Network: U-Net](https://arxiv.org/abs/1505.04597v1) 

[Performance Evaluation of Deep CNN-Based Crack Detection and Localization Techniques for Concrete Structures](https://doi.org/10.3390/s21051688) 
