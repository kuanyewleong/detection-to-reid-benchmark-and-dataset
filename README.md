## Bridging Detection and Re-identification: Evaluating Trustworthiness and Error Propagation in Face Recognition Pipelines

<p style="text-align: center;">
Kuan Yew Leong and Jaeseung Han<br>
A.I. System Research Co. Ltd.<br>
Kyoto, 606-8302 Japan<br>
{kyleong, han}@aisystemresearch.com
</p>

## Abstract
Face recognition systems typically rely on a two-stage pipeline – face detection and re-identification (ReID) – yet existing evaluations often overlook how detection errors propagate to affect recognition accuracy. This work empirically analyzes the interplay between detection and ReID, proposing a holistic framework to quantify synergy and error propagation. Grounded in information entropy, we introduce the Detection-Recognition Synergy (DRS) Score, a composite metric integrating Mutual Information (MI), Jensen-Shannon Divergence (JSD), and Wasserstein Distance (WD) to assess detection’s impact on recognition. We construct a novel benchmark dataset, annotated for both detection and ReID, featuring temporal sequences of the same individuals, diverse backgrounds, and natural settings across both indoor and outdoor environments. Experiments with diverse detection models, including YOLOX, Faster R-CNN, SSD, MTCNN and several others reveal substantial performance shifts due to detection variations. Our findings advocate for integrated evaluation strategies to enhance trustworthiness in face recognition pipelines. By bridging detection and ReID assessments, this study sets a foundation for more robust, explainable, and trusted face recognition pipelines.

![Figure 1](/page_media/figure1.png)
> **Figure 1**: A face was identified and localized from the same image frame by several different detection models. From left: ATSS-r50-fpn, FCOS-MobileNetV2, SSD-MobileNetV2, YOLOX-L, YOLOX-tiny. As shown in the figure, each model positioned its bounding box slightly differently, highlighting variations in detection. These discrepancies can ultimately affect ReID performance, as demonstrated in our experiments. The face is anonymized using attribute-preserving technique due to ethical concerns.

## Introduction of Dataset
Our dataset was meticulously curated from publicly accessible YouTube videos featuring individual faces from diverse backgrounds worldwide, and currently comprises 100 sets of videos, primarily containing at least one individual, though some feature multiple individuals; half are categorized for indoor ambient, and the other half for outdoor environments. The generation process involved several key steps:

Step 1:
Video Selection: We identified and selected videos showcasing individuals from various ethnicities and cultures to ensure a comprehensive representation of global diversity.

Step 2:
Timestamping and Clip Extraction: Specific segments within these videos were marked based on their relevance, and frames were sampled from these segments for further analysis.

Step 3
Annotation: A total of 1,500 instances were annotated, with each unique face marked with bounding boxes and assigned an identifier (ID). 

Recognizing the ethical considerations associated with sharing facial data, we have implemented anonymization techniques to protect individual identities while maintaining the dataset's utility for research purposes. Prior to distribution, the following measures are applied:

Attribute-Preserving Anonymization: Utilizing latent code optimization, we alter identity-specific features of each face. This process ensures that, while the unique identity is obfuscated, essential facial attributes necessary for detection and re-identification tasks are preserved.

Compliance with Ethical Standards: Our anonymization approach aligns with established privacy protection methods, including de-identification and pseudonymization, to mitigate the risk of re-identification.


## Technical Documentation of Dataset

