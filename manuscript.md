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
  <meta name="citation_author_institution" content="Department of Civil and Environmental Engineering, University of Illinois" />
  <meta name="citation_author" content="Yueh-Ti Lee" />
  <meta name="citation_author_institution" content="Department of Civil and Environmental Engineering, University of Illinois" />
  <meta name="citation_author" content="Minjiang Zhu" />
  <meta name="citation_author_institution" content="Department of Civil and Environmental Engineering, University of Illinois" />
  <meta name="citation_author" content="Chengyou Yue" />
  <meta name="citation_author_institution" content="Department of Civil and Environmental Engineering, University of Illinois" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/869f2b3a282d15963fed3c07babd7e13cb81f28e/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/869f2b3a282d15963fed3c07babd7e13cb81f28e/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/869f2b3a282d15963fed3c07babd7e13cb81f28e/manuscript.pdf" />
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
     Department of Civil and Environmental Engineering, University of Illinois
  </small>

+ **Yueh-Ti Lee**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Yueh-Ti](https://github.com/Yueh-Ti)<br>
  <small>
     Department of Civil and Environmental Engineering, University of Illinois
  </small>

+ **Minjiang Zhu**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Minjiang-Zhu](https://github.com/Minjiang-Zhu)<br>
  <small>
     Department of Civil and Environmental Engineering, University of Illinois
  </small>

+ **Chengyou Yue**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [TensorYue](https://github.com/TensorYue)<br>
  <small>
     Department of Civil and Environmental Engineering, University of Illinois
  </small>









## Introduction

The existence of cracks in concrete materials is of vital importance in Civil Engineering. An accurate and fast method to detect the existence of cracks in concrete images is always sought by engineers. Nowadays, even though a Convolutional neural network (CNN) based model can easily tell the existence of concrete cracks, the information of the exact locations of cracks is smeared in the network. We aim to firstly rebuild a CNN-based model for crack detection, and then find and apply another model to locate the exact positions of cracks. 

# please add more details about the potential applications of the second model or why this model is better

We first train a CNN with the Surface Crack Detection dataset [@{https://www.kaggle.com/datasets/arunrk7/surface-crack-detection}] to judge if any concrete crack exists. The dataset contains images (each has $227 \times 227$ pixels and RGB channels) of concrete surfaces with or without crack. Each class contains $20000$ images. Examples are shown in Figure @fig:Negative_and_Positive:

![**Negative and Positive Examples from the Surface Crack Detection Dataset**](https://user-images.githubusercontent.com/67733344/203328454-b16bba03-9eae-4936-83f6-8878ec4b2fa3.png "Tall image"){#fig:Negative_and_Positive height=2in}

# The dataset is splitted into a training set with ??? images and a testing set with ??? images. 

We then train a CNN-based network call U-Net [@doi:10.1007/978-3-319-24574-4_28] with the Concrete Crack Conglomerate Dataset [@doi:10.7294/16625056.v1] to segment the concrete from its cracks. The dataset contains over $20000$ crack images (each has $448 \times 448$ pixels and RGB channels). Each image data has an origin image and a mask image. Examples are shown in Figure @fig:Origin_and_Mask:

![**Origin and Mask Images from the Concrete Crack Conglomerate Dataset**](https://user-images.githubusercontent.com/67733344/203328939-52346bad-ea56-4424-bc9b-76f47f5a83dd.png "Tall image"){#fig:Origin_and_Mask height=2in}

The dataset is splitted into a training set with 19801 images and a testing set with 2195 images. 

## A Brief Introduction to CNN 

![**Basic Convolutional Neural Network for Classification.**
](./images/Basic_Convolutional_Neural_Network_for_Classification.png "Wide image"){#fig:Basic_Convolutional_Neural_Network_for_Classification}

CNN network is briefly introduced in this section. As shown in Figure @fig:Basic_Convolutional_Neural_Network_for_Classification, a typical CNN network involves several convolutional and pooling layers, and then several fully connected layers. Convolution is an operation that uses filter to extract information that we want to detect. 

# Hard to understand. Check your grammar below

The filter size determines how many filters will be applied to the input tensor to produce the same number of channels. Each filter can detect their specified geometries with colors in the given kernel size. 

# Hard to understand. Check your grammar above 

The kernel size determines the size of the area that the filters would apply to. Activation function is added to import nonlinearity into the model, considering the operation of filter is linear. MaxPooling is a down-sampling operation that allows our network to capture deeper information from its original dimensions. The pool size and strides determine the dimensions of the down-sample procedure. Notice that the sigmoid function rather than the softmax function shown in  Figure @fig:Basic_Convolutional_Neural_Network_for_Classificationwill be applied in our model, as as we only have two classes of results. 

## Network Design and Training Results
In the first convolutional block, we would specify 16 filters (consider 8 straight lines and 8 curves) with 3 by 3 kernels (consider the size of crack is relatively small), assign ReLu as the activation function in the Conv2D layer, and go deeper with a pool size of 2 by 2 in the MaxPool2D layer.

In the second convolutional block, we double the channels number to 32 with Conv2D and apply the same MaxPool2D.

Finally, we apply an GlobalAveragePooling2D layer, as we are focusing on the whole image rather than a part of it in segmentation. 

The result of our network would be a number in (0,1). We could treat it as the probability of the existence of crack in the image.

![**Model for Concrete Crack Classification using_Keras.**
](./images/Model_for_Concrete_Crack_Classification_using_Keras.png "Wide image"){#fig:Model_for_Concrete_Crack_Classification_using_Keras}

Notice that the original images have size of (227,227,3), we would resize it into (120,120,3) in preprocess procedure.

![**Model Summary and Hyperparameters.**
](./images/Model_Summary_and_Hyperparameters.png "Tall image"){#fig:Model_Summary_and_Hyperparameters height=4in}

| training   | validation | testing    | Optimizer | Loss Function | Metrics | Epochs |
|:-----------|:------|:------|:------|:------|:------|:------|
| 3360 | 840  | 1800 | Adam | Binary Crossentropy | Accuracy | 100 | 

Table: Hyperparameters.
{#tbl:CNNHyperparameters}

### Prediction and Analysis 

We can check our trained model by inputting the testing data, below is the confusion matrix our model generated:

![
**Confusion Matrix.**
](./images/Confusion_Matrix.png "Square image"){#fig:Confusion_Matrix height=3in}

![
**Loss Evolution.**
](./images/Loss_Evolution.png "Tall image"){#fig:Loss_Evolution height=3in}

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

| | Precision | Recall | Score | Support |
|:-----------|:------|:------|:------|:------|
| Negative	| 0.96|	0.99 | 0.98 | 917 | 
| Positive | 0.99 | 0.96 | 0.97 | 883 |	
| Macro Avg | 0.98 | 0.97 | 0.97 | 1800 |	
| Weighted Avg | 0.97 | 0.97 | 0.97 | 1000 |	


Table: Result Analysis
{#tbl:Result_Analysis}

It has overall good performance.

## Concrete Segmentation 

The original U-Net architecture is shown below:

![**U-net Architecture.**
](./images/U-net_Architecture.png "Wide image"){#fig:U-net_Architecture}

### Modeling and Training 

For achieving segmentation, we have built and trained two models, one based on our own architecture, and the other based on the paper. 
We perform a normalization before plug in the U-Net architecture based on the range of RGB number:

![**Input Normalization.**
](./images/Input_Normalization.png "Wide image"){#fig:Input_Normalization}

In the previous classification model, we have shown that the first convolutional block would only need 16 filters to perform well. We also add the random dropout in each convolution blocks to prevent the overfitting problem. Based on this experiment, we modified U-Net architecture as figure shown below. 

![**Modified U-Net Architecture.**
](./images/Modified_U-Net_Architecture.png "Wide image"){#fig:Modified_U-Net_Architecture}

Notice that the original images have size of (448,448,3), we would keep this size for this network, but there is still a resize procedure that allow this network to predict images with different size.

![**Model Summary**
](./images/Model_Summary.png "Wide image"){#fig:Model_Summary}

U-Net could learn from very few numbers of dataset, so we only need to have a small dataset.

![**U-Net Loss Evaluation.**](https://user-images.githubusercontent.com/67733344/203299831-e2a78d2b-2c6b-4945-b915-a073371f3380.png "Tall image"){#fig:U-Net_Loss height=3inch}

| training   | validation | testing    | Optimizer | Loss Function | Metrics | Epochs |
|:-----------|:------|:------|:------|:------|:------|:------|
| 105 | 2 | 17 | Adam | Binary Crossentropy | Accuracy | 50 |

Table: U-Net Hyperparameters.
{#tbl:U-NetHyperparameters}

We can see that this trained model has good performance on the testing data, it only takes 30 epochs because of our early stop condition.

## Prediction and Analysis 

![**Prediction Result**](https://user-images.githubusercontent.com/67733344/203314642-4d22a93d-8601-43ac-8747-9bf9cd1b1e0b.png){#fig:Prediction_Result}

Here are the prediction results of our testing images, it performs extremely well.

We could also notice that in the testing image 7, the network predict zone with dark color as crack. It is because the filter would not only capture geometries of the image in the kernel, but also the color of it (recall we have RGB channels as the input).

We are still working on the next U-Net model with Conv2D=>BatchNormalization=>ReLU  as conv_block!
We also trained a U-Net model with pretrained Inception as backbone, but we haven’t upload it yet!


Computer vision-based concrete crack detection using U-net fully convolutional networks
[@doi:10.1016/j.autcon.2019.04.005]

U-Net: Convolutional Networks for Biomedical Image Segmentation
[@doi:10.1007/978-3-319-24574-4_28]

Surface Crack Detection | Kaggle
[@{https://www.kaggle.com/datasets/arunrk7/surface-crack-detection}].

Concrete Crack Conglomerate Dataset | Virginia Tech
[@doi:10.7294/16625056.v1]

Performance Evaluation of Deep CNN-Based Crack Detection and Localization Techniques for Concrete Structures
[@doi:10.3390/s21051688]



