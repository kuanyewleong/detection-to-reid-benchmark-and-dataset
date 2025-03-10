# Bridging Detection and Re-identification

## Abstract
(to be updated soon)

## Introduction of Dataset
Our dataset was meticulously curated from publicly accessible YouTube videos featuring individual faces from diverse backgrounds worldwide, and currently comprises 100 sets of videos, primarily containing at least one individual, though some feature multiple individuals; half are categorized for indoor ambient, and the other half for outdoor environments. The generation process involved several key steps:
•	Video Selection: We identified and selected videos showcasing individuals from various ethnicities and cultures to ensure a comprehensive representation of global diversity.
•	Timestamping and Clip Extraction: Specific segments within these videos were marked based on their relevance, and frames were sampled from these segments for further analysis.
•	Annotation: A total of 1,500 instances were annotated, with each unique face marked with bounding boxes and assigned an identifier (ID). 
Recognizing the ethical considerations associated with sharing facial data, we have implemented anonymization techniques to protect individual identities while maintaining the dataset's utility for research purposes. Prior to distribution, the following measures are applied:
Attribute-Preserving Anonymization: Utilizing latent code optimization, we alter identity-specific features of each face. This process ensures that, while the unique identity is obfuscated, essential facial attributes necessary for detection and re-identification tasks are preserved.
Compliance with Ethical Standards: Our anonymization approach aligns with established privacy protection methods, including de-identification and pseudonymization, to mitigate the risk of re-identification.


## Technical Documentation of Dataset
