---
layout: post
title: "AAAI'18 transfer-based papers"
date: 2018-05-16
---


﻿Summary of transfer-based papers in AAAI'18

May. 16. 2018, by Hangwei

-----------------------------------------------------

### Tips
1. many of the accepted papers do not choose keywords 'transfer learning'
2. the category of the paper does not all match the keywords chosen during submission.

### Summary
In total, there are 20 papers that contain 'transfer' in title in accepted papers of AAAI'18. There does not exist papers on transfer-based Human Activity Recognition, therefore it's possible and promise to conduct such a paper for AAAI'19.

### Summary Table

|keywords  |paper contents      | datasets  | baseline methods                |
|--------|------------|----------------|-----|
|Artificial Intelligence and the Web| unbalanced domain adaptation (existing work assume that importance of source and target domain data is the same)  pure DL structure            | NUS-WIDE (web image data), Amazon Reviews (cross-language data) | non-transfer methods (SVM, DNN, Semi-supervised DAE); transfer methods (5 DL methods)
|Cognitive systems       | style transfer: paper-news title transfer, positive-negative review transfer      |propose a new dataset        | NLP tasks |
|Computational Sustainability and AI    |energy breakdown method, transfer two cities having distinct weather|city data| -|
|Knowledge Representation and Reasoning    |resource-poor languages translation, suffer in the presence of translation and language gaps between different cultural area |translation|  multilingual translation  |
|Machine Learning Methods |object detection with few shot transfer detector|object detection|-|
|Machine Learning Methods | bring the 'learning to rank' proposed by Hinton into deep metric learning formulation |metric learning tasks (pedestrian re-identification, image retrieval and image clustering)||
|Machine Learning Methods | transferable contextual bandit for cross-domain recommendation, reinforcement learning | - | exploit-explore methods |
| Machine Learning Methods | transfer info for a tam of agents in decentralized data fusion algorithms. propose a new information sharing mechanism | - |  -|
| Machine Learning Methods  | transfer learning based segmentation method; transferable subspace clustering method by exploring useful info from relevant source data to enhance clustering performance in target temporal data | temporal datasets (multi-modal ation detection data in videos) | subspace clustering |
| NLP and Machine Learning | a transfer reinforcement learning framework based on POMDP, to construct a personalized dialogue system | personalized dialogue systems | different transfer and reinforcement learning methods |
| NLP and Machine Learning | a parameter transfer learning strategy for word similarity | NLP datasets | - |
| NLP and Machine Learning | neural machine translation problem. transfer the knowledge contained in the dual model (target-to-source translation) to boost the training of the primal model (source-to-target translation). | language translation | dual methods (reinforcement learning) |
| NLP and Text Mining | cross-domain sentiment classification | reviews | DL-based |
| Vision | transfer adversarial hashing, extend deep harshing into transfer setting | image-text pairs | DL |
| Vision | multi-task framework, spectral transfer network between day and night images | vision | baseline methods |
| Vision | use unrelated data to transfer in attribute learning | datasets | attention |
| Vision | transferable semi-supervised semantic segmentation model to transfer the learned segmentation knowledge from a few strong categories with pixel-level annotations to unseen weak categories with only image-level annotations | image data | DL |
| Vision | people re-identification | imgae | DL |
| student abstract | enhance RNN based OCR by transductive transfer learning from text to images | - | - |
| student abstract | use web-distance to align the data of different domains | HAR in smart homes | SVM, transfer-based methods |


