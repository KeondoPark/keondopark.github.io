---
title: "Unexplored Faces of Robustness and Out-of-Distribution: Covariate Shifts in Environment and Sensor Domains"
collection: publications
category: conferences
permalink: /publication/2024-imagenetes
excerpt: 'This paper is about covariate shift of AI models, caused by changes in environment or sensor parameters.'
date: 2024-02-07
venue: 'Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)'
slidesurl: 'http://keondopark.github.io/files/CVPR_ImageNet_ES_slide.pdf'
paperurl: 'http://keondopark.github.io/files/ImageNet_ES__CVPR__24_03_29___Camera_Ready_.pdf'
youtubeurl: 'https://youtu.be/rdfUkYSWpik?si=s4j2sZ-Cms-s9tOs'
citation: 'Baek, E., Park, K., Kim, J. and Kim, H.S., 2024. Unexplored faces of robustness and out-of-distribution: Covariate shifts in environment and sensor domains. In Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (pp. 22294-22303).'
---

Computer vision applications predict on digital images acquired by a camera from physical scenes through light. However conventional robustness benchmarks rely on perturbations in digitized images diverging from distribution shifts occurring in the image acquisition process. To bridge this gap we introduce a new distribution shift dataset ImageNet-ES comprising variations in environmental and camera sensor factors by directly capturing 202k images with a real camera in a controllable testbed. With the new dataset we evaluate out-of-distribution (OOD) detection and model robustness. We find that existing OOD detection methods do not cope with the covariate shifts in ImageNet-ES implying that the definition and detection of OOD should be revisited to embrace real-world distribution shifts. We also observe that the model becomes more robust in both ImageNet-C and -ES by learning environment and sensor variations in addition to existing digital augmentations. Lastly our results suggest that effective shift mitigation via camera sensor control can significantly improve performance without increasing model size. With these findings our benchmark may aid future research on robustness OOD and camera sensor control for computer vision. Our code and dataset are available at https://github.com/Edw2n/ImageNet-ES.