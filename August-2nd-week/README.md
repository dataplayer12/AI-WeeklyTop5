# Listen to the Clubhouse room here

# Paper 1

[Separate Anything You Describe](https://audio-agi.github.io/Separate-Anything-You-Describe/AudioSep_arXiv.pdf)

[Code](https://github.com/Audio-AGI/AudioSep)

[Project Page](https://audio-agi.github.io/Separate-Anything-You-Describe/)

Abstract

Language-queried audio source separation (LASS) is a new paradigm for computational auditory scene analysis (CASA). LASS aims to separate a target sound from an audio mixture given a natural language query, which provides a natural and scalable interface for digital audio applications. Recent works on LASS, despite attaining promising separation performance on specific sources (e.g., musical instruments, limited classes of audio events), are unable to separate audio concepts in the open domain. In this work, we introduce AudioSep, a foundation model for open-domain audio source separation with natural language queries. We train AudioSep on large-scale multimodal datasets and extensively evaluate its capabilities on numerous tasks including audio event separation, musical instrument separation, and speech enhancement. AudioSep demonstrates strong separation performance and impressive zero-shot generalization ability using audio captions or text labels as queries, substantially outperforming previous audio-queried and language-queried sound separation models. For the reproducibility of this work, we will release the source code, evaluation benchmark and pre-trained model.

# Paper 2

[FocalFormer3D : Focusing on Hard Instance for 3D Object Detection](https://arxiv.org/abs/2308.04556)

[Code](https://github.com/NVlabs/FocalFormer3D)

Abstract

False negatives (FN) in 3D object detection, {\em e.g.}, missing predictions of pedestrians, vehicles, or other obstacles, can lead to potentially dangerous situations in autonomous driving. While being fatal, this issue is understudied in many current 3D detection methods. In this work, we propose Hard Instance Probing (HIP), a general pipeline that identifies \textit{FN} in a multi-stage manner and guides the models to focus on excavating difficult instances. For 3D object detection, we instantiate this method as FocalFormer3D, a simple yet effective detector that excels at excavating difficult objects and improving prediction recall. FocalFormer3D features a multi-stage query generation to discover hard objects and a box-level transformer decoder to efficiently distinguish objects from massive object candidates. Experimental results on the nuScenes and Waymo datasets validate the superior performance of FocalFormer3D. The advantage leads to strong performance on both detection and tracking, in both LiDAR and multi-modal settings. Notably, FocalFormer3D achieves a 70.5 mAP and 73.9 NDS on nuScenes detection benchmark, while the nuScenes tracking benchmark shows 72.1 AMOTA, both ranking 1st place on the nuScenes LiDAR leaderboard. Our code is available.

# Paper 3

[FLIRT: Feedback Loop In-context Red Teaming](https://arxiv.org/pdf/2308.04265.pdf)

Abstract

As generative models become available for public use in various applications, testing and analyzing vulnerabilities of these models has become a priority. Here we propose an automatic red teaming framework that evaluates a given model and exposes its vulnerabilities against unsafe and inappropriate content generation. Our framework uses in-context learning in a feedback loop to red team models and trigger them into unsafe content generation. We propose different in-context attack strategies to automatically learn effective and diverse adversarial prompts for text-to-image models. Our experiments demonstrate that compared to baseline approaches, our proposed strategy is significantly more effective in exposing vulnerabilities in Stable Diffusion (SD) model, even when the latter is enhanced with safety features. Furthermore, we demonstrate that the proposed framework is effective for red teaming text-to-text models, resulting in significantly higher toxic response generation rate compared to previously reported numbers.

# Paper 4

[Pre-Trained Large Language Models for Industrial Control](https://arxiv.org/pdf/2308.03028)


Abstract

For industrial control, developing high-performance controllers with few samples and low technical debt is appealing. Foundation models, possessing rich prior knowledge obtained from pre-training with Internet-scale corpus, have the potential to be a good controller with proper prompts. In this paper, we take HVAC (Heating, Ventilation, and Air Conditioning) building control as an example to examine the ability of GPT-4 (one of the first-tier foundation models) as the controller. To control HVAC, we wrap the task as a language game by providing text including a short description for the task, several selected demonstrations, and the current observation to GPT-4 on each step and execute the actions responded by GPT-4. We conduct series of experiments to answer the following questions: 1)~How well can GPT-4 control HVAC? 2)~How well can GPT-4 generalize to different scenarios for HVAC control? 3) How different parts of the text context affect the performance? In general, we found GPT-4 achieves the performance comparable to RL methods with few samples and low technical debt, indicating the potential of directly applying foundation models to industrial control tasks.

# Paper 5

[Convolutions Die Hard: Open-Vocabulary Segmentation with Single Frozen Convolutional CLIP](https://arxiv.org/pdf/2308.02487)

[Code](https://github.com/bytedance/fc-clip)

Abstract

Open-vocabulary segmentation is a challenging task requiring segmenting and recognizing objects from an open set of categories. One way to address this challenge is to leverage multi-modal models, such as CLIP, to provide image and text features in a shared embedding space, which bridges the gap between closed-vocabulary and open-vocabulary recognition. Hence, existing methods often adopt a two-stage framework to tackle the problem, where the inputs first go through a mask generator and then through the CLIP model along with the predicted masks. This process involves extracting features from images multiple times, which can be ineffective and inefficient. By contrast, we propose to build everything into a single-stage framework using a shared Frozen Convolutional CLIP backbone, which not only significantly simplifies the current two-stage pipeline, but also remarkably yields a better accuracy-cost trade-off. The proposed FC-CLIP, benefits from the following observations: the frozen CLIP backbone maintains the ability of open-vocabulary classification and can also serve as a strong mask generator, and the convolutional CLIP generalizes well to a larger input resolution than the one used during contrastive image-text pretraining. When training on COCO panoptic data only and testing in a zero-shot manner, FC-CLIP achieve 26.8 PQ, 16.8 AP, and 34.1 mIoU on ADE20K, 18.2 PQ, 27.9 mIoU on Mapillary Vistas, 44.0 PQ, 26.8 AP, 56.2 mIoU on Cityscapes, outperforming the prior art by +4.2 PQ, +2.4 AP, +4.2 mIoU on ADE20K, +4.0 PQ on Mapillary Vistas and +20.1 PQ on Cityscapes, respectively. Additionally, the training and testing time of FC-CLIP is 7.5x and 6.6x significantly faster than the same prior art, while using 5.9x fewer parameters. FC-CLIP also sets a new state-of-the-art performance across various open-vocabulary semantic segmentation datasets. 
