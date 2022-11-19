---
title: Concrete Crack Detection
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-11-19'
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
  <meta name="dc.date" content="2022-11-19" />
  <meta name="citation_publication_date" content="2022-11-19" />
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
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3035dfc9a064bafd348cd1a1dbbc9aafa9bd386f/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3035dfc9a064bafd348cd1a1dbbc9aafa9bd386f/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3035dfc9a064bafd348cd1a1dbbc9aafa9bd386f/manuscript.pdf" />
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

![Figure 1](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig1_neg_1.png)
![Figure 2](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig2_pos_1.png)

Figure 1. Example of Images with and without Cracks


[Segmentation]

Source: Virginia Tech/ Concrete Crack Conglomerate Dataset

Data Format: Images with 448*448 pixels with RGB channels

Content: The dataset contains over 10,995 crack images. Each image data has its origin image and mask image for image segmentation.

![Figure 3](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig3_ori_1.png)
![Figure 4](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig4_segged_1.png)

Figure 2. Example of an Original Image and an Mask Image


## Proposal:

In our project, we plan to train two models to detect concrete crack. First, by using the classification dataset, we plan to detect concrete crack based on convolutional neural network (CNN) to find out whether the concrete is defective. Second, by using the segmentation dataset, we plan to conduct concrete crack segmentation based on U Net to illustrate the position of the crack on concrete crack images.


## Exploratory Data Analysis

In classification, the dataset consists of 20,000 images with cracks and 20,000 images without cracks. We are planning to use convolutional neural network to train a classification model.
![Figure 5](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig5_plot_cla.png)

Figure 3. Number of Images with and without Cracks

In segmentation, we use the dataset consists of 21,996 images, splitting it into train data with 19,801 images and train data with 2,195 images. Here, we’ll be applying U Net to train a model that is capable of pointing out the cracks in a concrete image.
![Figure 6](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig6_plot_seg.png)

Figure 4. Number of Train Images and Test Images


## Predictive Modeling

In our group project, we trained two models: 
1.	Concrete crack detection based on convolutional neural network (CNN)
2.	Concrete crack segmentation based on U Net.


[Crack detection]
Dataset: Surface Crack Detection | Kaggle Positive: 20000 Negative: 20000
Training, validating, testing: 3360, 840, 1800
Network: CNN

![Figure 7](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig7_sch_cla.png)

Figure 5. Schematic of CNN

![Figure 8](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig8_code_cla.png)

Figure 6. Code of CNN

Input: images with 120x120x3 [height, width, channel (RGB)] (resized from 227x227)

Output: some kind of probability (was proceed by sigmoid)

Solver: Adam

Loss: Binary Cross Entropy

Testing result: True Positive, False Positive, True Negative, False Negative.

Positive or negative was predicted by the network, and true or false is the result of prediction (right or wrong)

![Figure 14]()

Figure 7. Confusion Matrix of the Test Result


[Crack Segmentation]
Dataset: Concrete Crack Conglomerate Dataset (vt.edu)

Would only use a part of it (107 for training and validating, 11 for testing) as U-Net is an effective architecture.

Network: U-Net [1505.04597v1] U-Net: Convolutional Networks for Biomedical Image Segmentation (arxiv.org)

![Figure 9](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig9_sch_seg.png)

Figure 8. Schematic of a U Net

Here we would have input with 3 channel, and would become 16 channel after the first convolution.

![Figure 10](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig10_biowulf.png)

![Figure 11](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig11_result1.png) ![Figure 12](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig12_result2.png)

Figure 9. Example of U Net Applied in Biomedical Image

U net applied in crack detection Computer vision-based concrete crack detection using U-net fully convolutional networks - ScienceDirect (It has almost the same structure with original U-net, but we would use a different channel number, we would also use a different architecture with pretrained convolutional neural network as backbone (VGG, ResNet, Inception))

![Figure 13](https://raw.githubusercontent.com/uiceds/cee-492-term-project-fall-2022-cmyy/main/fig13_code_seg.png)

Input: images with 120x120x3 [height, width, channel (RGB)] (resized from 227x227)

Output: some kind of probability (was proceed by sigmoid)

Solver: Adam

Loss: Binary Cross Entropy



## References
Surface Crack Detection | Kaggle
Concrete Crack Conglomerate Dataset | Virginia Tech
Computer Vision-based Concrete Crack Detection using U-net Fully Convolutional Networks
Data for: Computer Vision-based Concrete Crack Detection using U-net Fully Convolutional Networks
Performance Evaluation of Deep CNN-Based Crack Detection and Localization Techniques for Concrete Structures
GitHub - agoor97/Cracks_Detection: This Repository provides a Cracks Detection Implementation using Deep Learning for a Kaggle Dataset.



## References

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
[Energy Efficiency of buildings in New York]([https://manubot.org](https://www.kaggle.com/datasets/mikhailma/energy-efficiency-of-buildings-in-new-york))
