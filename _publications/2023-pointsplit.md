---
title: "PointSplit: Towards on-device 3D object detection with heterogeneous low-power accelerators"
collection: publications
category: conferences
permalink: /publication/2023-pointsplit
excerpt: 'This paper is about optimizing on-device 3D object detection on mobile devices equipped with CPU-GPU-NPU.'
date: 2023-05-09
venue: 'International Conference on Information Processing in Sensor Networks'
slidesurl: 'http://keondopark.github.io/files/PointSplit_vf.pdf'
paperurl: 'http://keondopark.github.io/files/PointSplit_ACM_Published.pdf'
citation: 'Park, K., Choi, Y.R., Lee, I. and Kim, H.S., 2023, May. PointSplit: Towards on-device 3D object detection with heterogeneous low-power accelerators. In Proceedings of the 22nd International Conference on Information Processing in Sensor Networks (pp. 67-81).'
---

 Running deep learning models on resource-constrained edge devices has drawn significant attention due to its fast response,privacy preservation, and robust operation regardless of Internet connectivity. While these devices already cope with various intelligent tasks, the latest edge devices that are equipped with multiple types of low-power accelerators (i.e., both mobile GPU and NPU) can bring another opportunity; a task that used to be too heavy for an edge device in the single-accelerator world might become viable in the upcoming heterogeneous-accelerator world. To realize the potential in the context of 3D object detection, we identify several technical challenges and propose PointSplit, a novel 3D object detection framework for multi-accelerator edge devices that addresses the problems. Specifically, our PointSplit design includes (1) 2D semantics-aware biased point sampling, (2) parallelized 3D feature extraction, and (3) role-based group-wise quantization. We implement PointSplit on TensorFlow Lite and evaluate it on a customized hardware platform comprising both mobile GPU and EdgeTPU.Experimental results on representative RGB-D datasets, SUN RGB-D and Scannet V2, demonstrate that PointSplit on a multi-accelerator device is 24.7× faster with similar accuracy compared to the full precision, 2D-3D fusion-based 3D detector on a GPU-only device.
